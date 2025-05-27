---
layout: default
title: llm-d Project Benchmarks
permalink: /llm-d-bench/
---

## PoC for Automating [llm-d](https://github.com/llm-d) Benchmark Smoke Testing. 

- Benchmarks are performed on EC2 instances g6e.12xlarge or g6e.2xlarge in Minikube for automating via GitHub Actions CI/CD. The benchmarks are 
generated using the [vLLM benchmarking](https://github.com/vllm-project/vllm/blob/main/benchmarks/benchmark_serving.py)
script. It is containerized and automated from provisioning the cluster to running and generating the benchmark results.
- The current comparisons, are the `no-features` and `base` deployments found in [llm-d-deployer/quickstart/examples/](https://github.com/llm-d/llm-d-deployer/tree/main/quickstart/examples).

## Available Benchmarks:

#### [Llama-3.1 8B Instruct (on 4x NVIDIA L40S)](./Llama-3.1-8B-Instruct-4xL40S/)
Benchmark results for meta-llama/Llama-3.1-8B-Instruct running on a 4xNVIDIA-L40S.

#### [Llama-3.2 3B Instruct (on 4x NVIDIA L40S)](./Llama-3.2-3B-Instruct-4xL40S/)
Benchmark results for meta-llama/Llama-3.2-3B-Instruct running on a 4xNVIDIA-L40S.

#### [Qwen3 0.6B (on 1x NVIDIA L4)](./Qwen3-0.6B-1xL4/)
Benchmark results for Qwen/Qwen3-0.6B running on a 1xNVIDIA-L4.

---

*Page last generated: {{ "now" | date: "%B %d, %Y" }}*
