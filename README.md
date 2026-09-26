# elastic EP run evidence - aibrix #2812

Raw evidence from the elastic EP end-to-end run discussed in vllm-project/aibrix#2812.

Single node k3s v1.36.4 on 4x RTX 4090 48G, vLLM v0.30.0 serving deepseek-ai/DeepSeek-V2-Lite-Chat with elastic EP, DP 2 -> 4 -> 2, controller built from the PR branch. All times are UTC.

| # | item | source | what |
|---|------|--------|------|
| 01 | up probe | traffic-022955/probe.csv | first 503s, then last 503 and first 200 |
| 02 | up field flip | scale-4-20260926T022251Z/pa-field-timeline.csv | rows 221-222 and 239-240 |
| 03 | up engine | scale-4-20260926T023000Z/engine-after.log | [Elastic EP] lines, 02:30:07 to 02:31:13 |
| 04 | down probe | traffic-022955/probe.csv | first 503s, then last 503 and first 200 |
| 05 | down engine | scale-2-20260926T024701Z/engine-after.log | [Elastic EP] lines, 02:47:06 to 02:47:22 |

The screenshots are renders of the text in excerpts/, which is copied verbatim from the run logs. Full bundle available on request.
