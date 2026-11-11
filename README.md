<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/john-liu-dev/john-liu-dev/main/assets/banner-dark.svg">
  <img alt="Yuehua Liu — Making LLMs answer faster and agents wait less." src="assets/banner-light.svg" width="100%">
</picture>

I work on LLM and agentic inference: making models answer faster and agents wait less. I also keep an eye on what people build with agents.

做LLM和Agentic推理优化，让模型答得快一点、agent少等一会儿，也关注agent应用

**Now** · multimodal serving (Qwen3-VL video) on Dynamo + TensorRT-LLM · encode / prefill / decode disaggregation · KV-aware decode routing · agentic workloads

**Side project** · [HackerShelf](https://john-liu-dev.github.io/shelf/) · papers and free books Hacker News kept recommending over 20 years, with Chinese reading guides · [how it's built](https://github.com/john-liu-dev/open-hackershelf)

#### Writing

<!-- BLOG-POST-LIST:START -->
- *Pending — the first posts are in the works.*
<!-- BLOG-POST-LIST:END -->

#### Upstream field notes

PRs and issues from multimodal, disaggregated serving and KV-aware routing.

- **Merged** · 2026-11-11 (UTC+8) · [ai-dynamo/dynamo#18442](https://github.com/ai-dynamo/dynamo/pull/18442) · accept Qwen3-VL requests with both an image and a video on the TRT-LLM backend ([issue #18441](https://github.com/ai-dynamo/dynamo/issues/18441))
- **Merged** · 2026-11-11 (UTC+8) · [ai-dynamo/dynamo#17943](https://github.com/ai-dynamo/dynamo/pull/17943) · drop `cache_transceiver_config` from the LLaVA TRT-LLM aggregated config
- Open PR · [ai-dynamo/dynamo#18600](https://github.com/ai-dynamo/dynamo/pull/18600) · honor the model's preferred video format for video-only and mixed-media requests ([issue #18599](https://github.com/ai-dynamo/dynamo/issues/18599))
- Open PR · [ai-dynamo/dynamo#18224](https://github.com/ai-dynamo/dynamo/pull/18224) · opt-in decode routing that prefers DP ranks with enough KV capacity for the request ([issue #18223](https://github.com/ai-dynamo/dynamo/issues/18223))
- Reported issue · [ai-dynamo/dynamo#16768](https://github.com/ai-dynamo/dynamo/issues/16768) · multimodal preprocessing on the worker event loop freezes token streaming
- Reported issue · [ai-dynamo/dynamo#16154](https://github.com/ai-dynamo/dynamo/issues/16154) · PD disaggregation: the decode worker re-loads and re-encodes every `video_url`

<sub>[NVIDIA 博客作者页](https://blogs.nvidia.cn/blog/author/liujohn/) · Views are my own.</sub>
