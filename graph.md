### Example Graph with Plotly

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

### Total Distribution Resources

The first comparison was to measure the total resources consumed by the 
basic single node installation. 

The pod count of running pods after installation was complete are as follows:

- MicroShift: 6
- OpenShift SNO: 80
- K3s: 5

The installation versions are as follows:

- MicroShift: (v1.21.0)
- OpenShift SNO: (v1.22.3+2cb6068, OCP 4.9.19)
- K3s: (v1.22.7+k3s1)

The following numbers are collected from these deployments without any 
workloads being run and only the base minimum objects required to run 
the distribution.

{% include resource-totals.html %}

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
around 175 pods. This was due to there only being 16GB of memory on the VM. 
If the node had more memory it would handily scale beyond 250 pods as 
described in [OpenShift scalability and performance](https://docs.openshift.com/container-platform/4.6/scalability_and_performance/planning-your-environment-according-to-object-maximums.html).

The following is percent of compute available on the node. Each node is identical
and resourced as listed above:

{% include cpu-comps.html %}

Lastly, is the percent of memory consumed on each node. Again, OpenShift SNO hits
the wall around 175 workload pods:

{% include memory-comps.html %}