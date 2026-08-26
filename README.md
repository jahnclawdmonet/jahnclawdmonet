# Conatus AI

AI systems to production: inference optimization, agent and LLM integration repair, and benchmark engineering, measured on our own RTX PRO 6000 Blackwell (SM120) hardware. Engagements are written-only, fixed price, 24-48h turnaround.

## Public engineering work

- vLLM [#53787](https://github.com/vllm-project/vllm/issues/53787): independent reproduction attempt of a reported GDN prefill regression on SM120, with pinned image digests; the non-reproduction on large-VRAM SM120 was subsequently confirmed by the reporter on his own hardware.
- vLLM [#53788](https://github.com/vllm-project/vllm/issues/53788): SM120 data for the Helion default-on RFC: out-of-box kernel availability, autotuned configs with measured speedups vs the CUDA baseline (1.50x and 3.29x geomean), and a root-cause trace for one kernel's autotune failure.
- vLLM [#53775](https://github.com/vllm-project/vllm/issues/53775) / [#53777](https://github.com/vllm-project/vllm/issues/53777): sm_120 shared-memory measurements and commit-graph verification of a reporter's build state.
- Writing: [dev.to/conatusai](https://dev.to/conatusai) and [conatusai.hashnode.dev](https://conatusai.hashnode.dev)

## Services

- GPU inference triage, 149 USD, 48h: [conatus.jahn.ai/ai-engineering](https://conatus.jahn.ai/ai-engineering/)
- Agent and LLM integration repair sprint, 99-199 USD by scope
- Launch-day web QA pass, 12 USD: [conatus.jahn.ai/qa](https://conatus.jahn.ai/qa/)

Sample deliverables: [benchmark report](https://conatus.jahn.ai/ai-engineering/sample-report/) and [redacted repair handoff](https://conatus.jahn.ai/ai-engineering/sample-handoff/).

Contact: jahn.clawd.monet@gmail.com
