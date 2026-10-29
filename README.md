<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/banner-dark.svg">
  <img src="assets/banner-light.svg" alt="Christian Abdalla: aspiring quantitative developer" width="100%">
</picture>

<p align="center">
  <img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" alt="C++">
  <img src="https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=c&logoColor=black" alt="C">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java">
</p>

I study Technical Computer Science at the University of Twente and I'm working toward a career as a **quantitative developer**, where low-latency systems engineering meets financial models. At the moment I'm building C++ trading infrastructure for a cryptocurrency market-making system: real-time order book processing, a PostgreSQL/TimescaleDB time-series database, and benchmarks for critical-path latency and throughput.

```cpp
struct Christian {
    std::string_view study = "Technical Computer Science @ University of Twente";
    std::string_view goal  = "Quantitative Developer";
    std::array<std::string_view, 4> languages{"C++", "C", "Python", "Java"};
    std::array<std::string_view, 3> focus{"low latency", "market microstructure", "systems"};
};
```

## Building

### ▸ Hyperliquid: C++ market-making infrastructure &nbsp;<img src="https://img.shields.io/badge/status-active-3fb950?style=flat-square" alt="active" align="center">

Latency-sensitive C++ trading infrastructure for a crypto market-making system. Order book management, market data handling, and quoting/execution logic driven by real-time websocket data. Includes benchmarks for critical-path latency and a PostgreSQL/TimescaleDB time-series database (with separate production and test environments) hosted on a Debian server.

```text
  Hyperliquid WS ──▶  parser  ──▶  order book  ──▶  quoting  ──▶  execution
   (L2 + trades)     simdjson      L2 · C++         strategy        orders
                                       │
                                       │  ticks, fills, snapshots
                                       ▼
                         PostgreSQL / TimescaleDB
                          prod · test  (Debian)

  └──────────────── benchmarked critical path: latency · throughput ───────────────┘
```

<sub>`C++` · `Market making` · `WebSockets` · `TimescaleDB` · `PostgreSQL` · `simdjson` · `Python`</sub>

---

<p align="center"><sub><code>while (market.open()) { book.update(); quote(); }</code></sub></p>
