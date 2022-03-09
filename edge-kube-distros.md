### Edge Centric Kubernetes Distributions Analysis

In this writeup we will review and compare some options for Kubernetes 
distributions targeted for edge and IoT deployments. Edge deployments 
often involve gateways for connectivity, thus the interest in assessing
the existing options currently in open source. 

The following distributions being compared are all compatible with the 
[Submariner](https://submariner.io) project and can act as gateways for 
inter-cluster communications.

- [MicroShift](https://microshift.io)
- [OpenShift - Single Node Operator](https://www.redhat.com/en/blog/meet-single-node-openshift-our-smallest-openshift-footprint-edge-architectures)
- [K3s](https://k3s.io)

The metrics collected and presented for each distribution are as follows: 
- Node deployment time per distribution
  - the time it takes from initiating the deployment to all pods reporting a running status
- Total node resources consumed for the base installation
  - total download size observed in the deployment
  - compute utilization from base installation
  - memory consumption from base installation
- Node resources with an accompanying workload
  - compute and memory consumption as deployments increase up to 250 pods

### Total Distribution Resources and Deployment Times

The first comparison was to measure the total resources consumed by the 
basic single node installation. 

The pod count of running pods after installation was complete are as follows:

- OpenShift SNO: 80
- MicroShift: 6
- K3s: 5

The installation versions are as follows:

- OpenShift SNO: (v1.22.3+2cb6068, OCP 4.9.19)
- MicroShift: (v1.21.0)
- K3s: (v1.22.7+k3s1)

The following numbers are collected from these deployments without any 
workloads being run and only the base minimum objects required to run 
the distribution.

{% include resource-totals.html %}

The installation times are similar between MicroShift and K3s while SNO
substantially longer due to the download and the greater number of pod 
initiations that occur.

{% include installation-time.html %}

### Measuring the distributions with workloads

Next we add load to the distributions. The experiments were performed 
on VMs with the following specs. These specs are also the minimum 
supported specs for OpenShift SNO.

- 8 vCPUs
- 16GB memory
- 120GB storage

The measurements were taken starting at zero pods up to 225 pods. The
workload consists of scaling Nginx replicas in an increment of 25 at a time.

In the case of OpenShift SNO, the node became resource constrained as it approached
around 175 pods where kube-api begins to bounce and pods get stuck in pending. 
This was due to there only being 16GB of memory on the VM. If the node had more 
memory it would handily scale far beyond 250 pods as described in 
[OpenShift scalability and performance](https://docs.openshift.com/container-platform/4.6/scalability_and_performance/planning-your-environment-according-to-object-maximums.html).

The following is percent of compute available on the node. Each node is identical
and resourced as listed above:

{% include cpu-comps.html %}

Lastly, is the percent of memory consumed on each node. Again, OpenShift SNO hits
the wall around 175 workload pods which is why you see it drop off the plot after
175 pods:

{% include memory-comps.html %}

### Conclusion

MicroShift and K3s both serve the purpose of a lightweight distribution that is
attractive for gateway deployments. The reasoning is simply, the more memory and
compute on a node, the faster a node and move encapsulated network data. There is
a direct correlation to resources available to a node and the performance of the
datapath. This is of course not to say, OpenShift isn't a viable candidate as well.
In many cases OpenShift is the only option as it will have features that will never be
included in stripped down Kubernetes deployments. Hardware offloading and acceleration 
are also mechanisms to improve datapath performance that would rely less on the node
resources to achieve better performance that will be captured in future scale and stress
testing.