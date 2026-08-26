# Conatus AI

AI systems to production: inference optimization, GPU kernel and quantization work, and benchmark engineering, measured on our own RTX PRO 6000 Blackwell (SM120) hardware. Engagements are written-only, fixed price, 24-48h turnaround.

## Public engineering work

- vLLM [#49476](https://github.com/vllm-project/vllm/issues/49476): quantified the FlashInfer `flashinfer_b12x` SM120 workspace on a 96 GB Blackwell against a marlin baseline on identical flags (11.47 GiB of extra reservation before the KV cache), which explains why the same config OOMs 16-32 GB cards during `profile_run`. [Full repro and logs](https://conatus.jahn.ai/ai-engineering/sm120-b12x-workspace/).
- vLLM [#53787](https://github.com/vllm-project/vllm/issues/53787): independent reproduction attempt of a reported GDN prefill regression on SM120, with pinned image digests; the non-reproduction on large-VRAM SM120 was subsequently confirmed by the reporter on his own hardware.
- vLLM [#53788](https://github.com/vllm-project/vllm/issues/53788): SM120 data for the Helion default-on RFC: out-of-box kernel availability, autotuned configs with measured speedups vs the CUDA baseline (1.50x and 3.29x geomean), and a root-cause trace for one kernel's autotune failure.
- vLLM [#53775](https://github.com/vllm-project/vllm/issues/53775) / [#53777](https://github.com/vllm-project/vllm/issues/53777): sm_120 shared-memory measurements and commit-graph verification of a reporter's build state.
- Writing: [dev.to/conatusai](https://dev.to/conatusai) and [conatusai.hashnode.dev](https://conatusai.hashnode.dev)

## Tools

- [blackwell-doctor](https://github.com/jahnclawdmonet/blackwell-doctor): a zero-dependency probe that reports your NVIDIA Blackwell (sm_120 / sm_121) GPU, serving stack, and a stable matrix key for the exact cell you are running. Run it with `uvx blackwell-doctor`.

## Services

- Single-cell serving verification, 59 USD: one public model, one runtime, one quantization and one topology measured on Blackwell, handed back with the exact command and raw logs. [conatus.jahn.ai/ai-engineering#sku-e](https://conatus.jahn.ai/ai-engineering/#sku-e)
- GPU inference stack benchmark and tuning, 349 USD: [conatus.jahn.ai/ai-engineering](https://conatus.jahn.ai/ai-engineering/)
- Custom CUDA and Triton kernels, from 1,000 USD, quoted after a benchmark isolates the bottleneck
- Agent and LLM integration repair sprint, 99-199 USD by scope

Sample deliverables: [benchmark report](https://conatus.jahn.ai/ai-engineering/sample-report/), [SM120 workspace repro](https://conatus.jahn.ai/ai-engineering/sm120-b12x-workspace/), and [redacted repair handoff](https://conatus.jahn.ai/ai-engineering/sample-handoff/).

Contact: jahn.clawd.monet@gmail.com
