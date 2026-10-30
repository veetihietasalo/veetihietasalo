# Veeti Hietasalo

AI engineer in Espoo, Finland. I take AI from prototype into daily use, and I measure whether it works: LLM and RAG applications, open-weights models fine-tuned from 7B to 40B mixture-of-experts, and valuation models with calibrated uncertainty. Member of the NVIDIA Inception programme.

**Open to full-time AI / ML engineer roles** in Finland, Amsterdam, Stockholm and London. EU citizen. [LinkedIn](https://www.linkedin.com/in/vvvhietasalo/)

## Experience

**AI Engineer, UM Yhtiöt** (2024–2026). A group whose companies include Powerlift (lifting, transport, logistics) and Proinfra (infrastructure and energy construction).

- RAG applications on large language models, used by 15 employees
- Fleet route optimisation that cut fuel costs by about 23%
- Automated valuation models (AVM) for machinery, and a prototype marketplace for lifting services
- Integrated into company processes with Azure and Power Automate, results on Power BI dashboards
- Presented the work to CEOs and advisors at KONE, Winthrop Technologies and Bronto Skylift

**Founder, [Mad Tech Oy](https://mad3d.ai)** (2024–). Mad Tech builds a map of the built environment in Finland: every building, plot, zoning and market fact in the capital region from open data, keyed to IDs, with an AI that only quotes its sources.

- Apartment price model for 163 capital-region postal areas, from open Statistics Finland data. Its 80% split-conformal bands covered 78.6% on held-out years 2023–2025, with a 4.4% median error, ahead of both naive baselines
- LLM extraction of maintenance items from Finnish housing-company plans: OCR, structured output cited to its source page, a bake-off across model providers, and recorded responses so tests run offline
- Real documents only go to approved model endpoints, checked in code before every call

## Projects

| | |
| :--- | :--- |
| **MadMDL** (private, demo on request) | A local coding agent and fine-tuning pipeline: its own tool-use harness, a hidden-test eval suite run over several seeds with confidence intervals, and fine-tunes from 7B to 40B mixture-of-experts on verified agent trajectories (bf16 LoRA on the fused expert weights of the MoEs). Results below |
| [MiniHFT](https://github.com/veetihietasalo/MiniHFT) | Educational C++20 project: NASDAQ ITCH 5.0 into an L3 order book. A full trading day, 268.7M messages, in about 90 s, 50 ns p50 per hop between pinned threads[^bench] |
| [MonteCarloCpp](https://github.com/veetihietasalo/MonteCarloCpp) | Monte Carlo option pricer, C++20, devirtualized and measured on three compilers |
| [OptionsPricing](https://github.com/veetihietasalo/OptionsPricing) | Black-Scholes with Greeks, Bun + React |

## Model evaluations

From MadMDL. Each task is graded by a hidden test the agent never sees, written into the workspace only after it finishes; a run passes when that test exits 0.

| Model | Setup | Result |
| :--- | :--- | :--- |
| Qwen3.6-35B-A3B (MoE) | 79 tasks × 3 seeds, A100 80GB | **214/237 runs, 90.3%** (95% CI 85.9–93.4) |
| Qwen3-Coder-30B-A3B (MoE) | same 79 tasks × 2 seeds, A100 80GB | 131/158 runs, 82.9% (95% CI 76.3–88.0) |
| **madmdl-7b**, my QLoRA fine-tune of Qwen2.5-Coder-7B | 60-task acceptance suite, against its stock same-quant base | **38/60 vs 21/60**; on held-out tasks 4/10 vs 2/10 |
| Qwen2.5-Coder-7B, q5 on a laptop | 10-task suite | 5/10 single attempt, 8/10 with one retry |
| Qwen2.5-Coder-14B, q4 on a laptop | 10-task suite | 7/10 with retries |
| Claude Sonnet, same harness | 10-task suite | 10/10 |

The 35B leads the 30B by 7.4 points (95% CI +0.6 to +14.7), so the gap is real; on the held-out tasks alone it is +8.0 with a CI from −3.4 to +21.2, within noise. The fine-tuned 7B's held-out set is only 10 tasks, so its +2 there is directional.

I build with coding agents (Claude Code): I set the direction, design the evaluations and check the measurements.

## Skills

LLMs and RAG · LoRA / QLoRA fine-tuning incl. MoE · evaluation design · conformal prediction · Python · TypeScript · SQL · Java · Azure · Power Automate · Power BI · AWS · Docker · Git

Finnish (native) · English (full professional) · Swedish (working knowledge)

## Education

BBA, Business Information Technology (Full-Stack Software Development), Haaga-Helia University of Applied Sciences. Expected July 2027.

[^bench]: AMD Ryzen 9 9900X3D, WSL2, about 10 ns timer overhead included. Details in the [MiniHFT README](https://github.com/veetihietasalo/MiniHFT#-performance).
