---
layout: default
title: "llm-d Benchmarks"
permalink: /llm-d-bench/Llama-3.1-8B-Instruct-4xL40S/
---

[//]: # (# llm-d Benchmarks)

### Created May 26, 2025

<details>
<summary>Results JSON</summary>
{% highlight json %}
{
  "date": "20250526-040420",
  "backend": "vllm",
  "model_id": "meta-llama/Llama-3.1-8B-Instruct",
  "tokenizer_id": "meta-llama/Llama-3.1-8B-Instruct",
  "num_prompts": 150,
  "deployment": "no-features",
  "gpu": "4xNVIDIA_L40S",
  "model": "meta-llama/Llama-3.1-8B-Instruct",
  "gateway": "kgateway",
  "prefill_replicas": "0",
  "decode_replicas": "4",
  "request_rate": 5.0,
  "burstiness": 1.0,
  "max_concurrency": null,
  "duration": 103.50128086900077,
  "completed": 150,
  "total_input_tokens": 149850,
  "total_output_tokens": 250280,
  "request_throughput": 1.4492574269670306,
  "request_goodput:": null,
  "output_throughput": 2418.1343254753897,
  "total_token_throughput": 3865.942495015453,
  "mean_ttft_ms": 113.90907388660708,
  "median_ttft_ms": 108.93868600032874,
  "std_ttft_ms": 22.834136006816504,
  "p99_ttft_ms": 183.9973396716959,
  "mean_tpot_ms": 34.140149674642394,
  "median_tpot_ms": 34.52975710980377,
  "std_tpot_ms": 2.6358126316454142,
  "p99_tpot_ms": 37.29995607045018,
  "mean_itl_ms": 34.894649786954695,
  "median_itl_ms": 35.296155998366885,
  "std_itl_ms": 6.582189789290744,
  "p99_itl_ms": 42.828577700784074
}{
  "date": "20250526-040738",
  "backend": "vllm",
  "model_id": "meta-llama/Llama-3.1-8B-Instruct",
  "tokenizer_id": "meta-llama/Llama-3.1-8B-Instruct",
  "num_prompts": 300,
  "deployment": "no-features",
  "gpu": "4xNVIDIA_L40S",
  "model": "meta-llama/Llama-3.1-8B-Instruct",
  "gateway": "kgateway",
  "prefill_replicas": "0",
  "decode_replicas": "4",
  "request_rate": 10.0,
  "burstiness": 1.0,
  "max_concurrency": null,
  "duration": 129.965749125,
  "completed": 300,
  "total_input_tokens": 299700,
  "total_output_tokens": 508391,
  "request_throughput": 2.3083004716224305,
  "request_goodput:": null,
  "output_throughput": 3911.7306168953305,
  "total_token_throughput": 6217.722788046139,
  "mean_ttft_ms": 129.61986193688062,
  "median_ttft_ms": 126.20357649939251,
  "std_ttft_ms": 46.468853722224615,
  "p99_ttft_ms": 283.6090160591628,
  "mean_tpot_ms": 46.37729875331297,
  "median_tpot_ms": 47.726302522010755,
  "std_tpot_ms": 5.672097744233126,
  "p99_tpot_ms": 52.29845130658762,
  "mean_itl_ms": 47.87537876805538,
  "median_itl_ms": 47.757329000887694,
  "std_itl_ms": 11.050990245258982,
  "p99_itl_ms": 101.30114200001111
}{
  "date": "20250526-041235",
  "backend": "vllm",
  "model_id": "meta-llama/Llama-3.1-8B-Instruct",
  "tokenizer_id": "meta-llama/Llama-3.1-8B-Instruct",
  "num_prompts": 600,
  "deployment": "no-features",
  "gpu": "4xNVIDIA_L40S",
  "model": "meta-llama/Llama-3.1-8B-Instruct",
  "gateway": "kgateway",
  "prefill_replicas": "0",
  "decode_replicas": "4",
  "request_rate": 20.0,
  "burstiness": 1.0,
  "max_concurrency": null,
  "duration": 227.94775883699913,
  "completed": 600,
  "total_input_tokens": 599400,
  "total_output_tokens": 1019311,
  "request_throughput": 2.6321820537356015,
  "request_goodput:": null,
  "output_throughput": 4471.686868958816,
  "total_token_throughput": 7101.236740640682,
  "mean_ttft_ms": 199.0707764850049,
  "median_ttft_ms": 175.68682850105688,
  "std_ttft_ms": 102.13288551973744,
  "p99_ttft_ms": 557.1080786814855,
  "mean_tpot_ms": 74.85396973822814,
  "median_tpot_ms": 69.54485496798374,
  "std_tpot_ms": 23.42558142766361,
  "p99_tpot_ms": 98.67802757238474,
  "mean_itl_ms": 75.57563861233167,
  "median_itl_ms": 62.015204999624984,
  "std_itl_ms": 1006.1340729948624,
  "p99_itl_ms": 209.77048090062465
}{
  "date": "20250526-041722",
  "backend": "vllm",
  "model_id": "meta-llama/Llama-3.1-8B-Instruct",
  "tokenizer_id": "meta-llama/Llama-3.1-8B-Instruct",
  "num_prompts": 600,
  "deployment": "no-features",
  "gpu": "4xNVIDIA_L40S",
  "model": "meta-llama/Llama-3.1-8B-Instruct",
  "gateway": "kgateway",
  "prefill_replicas": "0",
  "decode_replicas": "4",
  "request_rate": "inf",
  "burstiness": 1.0,
  "max_concurrency": null,
  "duration": 218.40525616300147,
  "completed": 600,
  "total_input_tokens": 599400,
  "total_output_tokens": 1007756,
  "request_throughput": 2.747186631590059,
  "request_goodput:": null,
  "output_throughput": 4614.156351841119,
  "total_token_throughput": 7358.595796799588,
  "mean_ttft_ms": 6453.811295348399,
  "median_ttft_ms": 6275.929862000339,
  "std_ttft_ms": 3637.1270723002754,
  "p99_ttft_ms": 13583.897760610344,
  "mean_tpot_ms": 81.84168011979374,
  "median_tpot_ms": 72.73693835943006,
  "std_tpot_ms": 23.39811030770798,
  "p99_tpot_ms": 187.58318112021695,
  "mean_itl_ms": 77.33718025899174,
  "median_itl_ms": 61.89066399929288,
  "std_itl_ms": 1065.7034788623446,
  "p99_itl_ms": 193.9360334485171
}{
  "date": "20250526-043639",
  "backend": "vllm",
  "model_id": "meta-llama/Llama-3.1-8B-Instruct",
  "tokenizer_id": "meta-llama/Llama-3.1-8B-Instruct",
  "num_prompts": 150,
  "deployment": "base",
  "gpu": "4xNVIDIA_L40S",
  "model": "meta-llama/Llama-3.1-8B-Instruct",
  "gateway": "kgateway",
  "prefill_replicas": "0",
  "decode_replicas": "4",
  "request_rate": 5.0,
  "burstiness": 1.0,
  "max_concurrency": null,
  "duration": 107.8759891180016,
  "completed": 150,
  "total_input_tokens": 149850,
  "total_output_tokens": 248459,
  "request_throughput": 1.3904855123592006,
  "request_goodput:": null,
  "output_throughput": 2303.1909327683643,
  "total_token_throughput": 3692.2859596152057,
  "mean_ttft_ms": 117.74122390655975,
  "median_ttft_ms": 108.96949149901047,
  "std_ttft_ms": 28.248830656805737,
  "p99_ttft_ms": 203.74891979990906,
  "mean_tpot_ms": 34.946552008198516,
  "median_tpot_ms": 36.46396865632801,
  "std_tpot_ms": 4.110573497060544,
  "p99_tpot_ms": 39.5032601762733,
  "mean_itl_ms": 35.54707718159643,
  "median_itl_ms": 35.084262999589555,
  "std_itl_ms": 7.491283663760972,
  "p99_itl_ms": 46.48240300215548
}{
  "date": "20250526-043954",
  "backend": "vllm",
  "model_id": "meta-llama/Llama-3.1-8B-Instruct",
  "tokenizer_id": "meta-llama/Llama-3.1-8B-Instruct",
  "num_prompts": 300,
  "deployment": "base",
  "gpu": "4xNVIDIA_L40S",
  "model": "meta-llama/Llama-3.1-8B-Instruct",
  "gateway": "kgateway",
  "prefill_replicas": "0",
  "decode_replicas": "4",
  "request_rate": 10.0,
  "burstiness": 1.0,
  "max_concurrency": null,
  "duration": 128.18271712200294,
  "completed": 300,
  "total_input_tokens": 299700,
  "total_output_tokens": 512054,
  "request_throughput": 2.340409118605773,
  "request_goodput:": null,
  "output_throughput": 3994.7195027285347,
  "total_token_throughput": 6332.788212215702,
  "mean_ttft_ms": 106.76067082670973,
  "median_ttft_ms": 94.73688549951476,
  "std_ttft_ms": 60.30702334896684,
  "p99_ttft_ms": 301.8533356611442,
  "mean_tpot_ms": 46.094781816298244,
  "median_tpot_ms": 47.1882647293644,
  "std_tpot_ms": 6.316757533996857,
  "p99_tpot_ms": 51.45072459278227,
  "mean_itl_ms": 47.50753773145105,
  "median_itl_ms": 47.869449999780045,
  "std_itl_ms": 10.604668519864411,
  "p99_itl_ms": 101.32459413092873
}{
  "date": "20250526-044446",
  "backend": "vllm",
  "model_id": "meta-llama/Llama-3.1-8B-Instruct",
  "tokenizer_id": "meta-llama/Llama-3.1-8B-Instruct",
  "num_prompts": 600,
  "deployment": "base",
  "gpu": "4xNVIDIA_L40S",
  "model": "meta-llama/Llama-3.1-8B-Instruct",
  "gateway": "kgateway",
  "prefill_replicas": "0",
  "decode_replicas": "4",
  "request_rate": 20.0,
  "burstiness": 1.0,
  "max_concurrency": null,
  "duration": 222.8934304209979,
  "completed": 600,
  "total_input_tokens": 599400,
  "total_output_tokens": 1009845,
  "request_throughput": 2.691869378414288,
  "request_goodput:": null,
  "output_throughput": 4530.618054074628,
  "total_token_throughput": 7219.7955631105015,
  "mean_ttft_ms": 164.31253460329876,
  "median_ttft_ms": 142.53808600005868,
  "std_ttft_ms": 114.24278546901645,
  "p99_ttft_ms": 510.2548310522615,
  "mean_tpot_ms": 71.77195483126623,
  "median_tpot_ms": 68.00384016483288,
  "std_tpot_ms": 20.517574080437086,
  "p99_tpot_ms": 96.43081588793252,
  "mean_itl_ms": 73.72781094509163,
  "median_itl_ms": 61.85768900104449,
  "std_itl_ms": 944.5543014365774,
  "p99_itl_ms": 211.45989799973898
}{
  "date": "20250526-044927",
  "backend": "vllm",
  "model_id": "meta-llama/Llama-3.1-8B-Instruct",
  "tokenizer_id": "meta-llama/Llama-3.1-8B-Instruct",
  "num_prompts": 600,
  "deployment": "base",
  "gpu": "4xNVIDIA_L40S",
  "model": "meta-llama/Llama-3.1-8B-Instruct",
  "gateway": "kgateway",
  "prefill_replicas": "0",
  "decode_replicas": "4",
  "request_rate": "inf",
  "burstiness": 1.0,
  "max_concurrency": null,
  "duration": 212.7082737669989,
  "completed": 600,
  "total_input_tokens": 599400,
  "total_output_tokens": 1006568,
  "request_throughput": 2.8207647468252284,
  "request_goodput:": null,
  "output_throughput": 4732.1525494706275,
  "total_token_throughput": 7550.09653154903,
  "mean_ttft_ms": 5673.821735669929,
  "median_ttft_ms": 5821.99754550129,
  "std_ttft_ms": 2920.091745724143,
  "p99_ttft_ms": 11120.799167320873,
  "mean_tpot_ms": 79.87534744510529,
  "median_tpot_ms": 70.64062360005009,
  "std_tpot_ms": 21.460663277854362,
  "p99_tpot_ms": 173.41601675689162,
  "mean_itl_ms": 76.4411274797708,
  "median_itl_ms": 61.78928799818095,
  "std_itl_ms": 1054.1400670947783,
  "p99_itl_ms": 187.4729780307825
}
{% endhighlight %}
</details>

{% include_relative summary_mean_ttft_ms_meta-llama_Llama-3.1-8B-Instruct.html %}
{% include_relative summary_mean_tpot_ms_meta-llama_Llama-3.1-8B-Instruct.html %}
{% include_relative summary_mean_itl_ms_meta-llama_Llama-3.1-8B-Instruct.html %}
{% include_relative summary_request_throughput_meta-llama_Llama-3.1-8B-Instruct.html %}
