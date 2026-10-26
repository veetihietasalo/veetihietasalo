# Veeti Hietasalo

Founder and CEO of [Mad Tech Oy](https://mad3d.ai), Espoo. Engineer first: low-latency C++, Rust and data systems.

**Mad Tech** builds a map of the built environment in Finland: every building, plot, zoning and market fact in the capital region from open data, keyed to IDs, with an AI that only quotes its sources.

**Systems work**

| | |
| :--- | :--- |
| [MiniHFT](https://github.com/veetihietasalo/MiniHFT) | NASDAQ ITCH 5.0 into an L3 order book, C++20. A full trading day, 268.7M messages, in about 90 s, 50 ns p50 per hop between pinned threads[^bench] |
| [MonteCarloCpp](https://github.com/veetihietasalo/MonteCarloCpp) | Monte Carlo option pricer, C++20, devirtualized and measured on three compilers |
| [OptionsPricing](https://github.com/veetihietasalo/OptionsPricing) | Black-Scholes with Greeks, Bun + React |

Also an OS in Rust and a coding agent tuned to run on a laptop, both private, happy to walk through them.

C++20 · Rust · Python · TypeScript · perf · bpftrace · ThreadSanitizer · Linux

[LinkedIn](https://www.linkedin.com/in/vvvhietasalo/) · [mad3d.ai](https://mad3d.ai)

[^bench]: AMD Ryzen 9 9900X3D, WSL2, about 10 ns timer overhead included. Details in the [MiniHFT README](https://github.com/veetihietasalo/MiniHFT#-performance).
