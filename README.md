<h1 align="center">Amlendu Pandey</h1>
<p align="center">
  Backend Engineer — Fintech Infrastructure & Distributed Systems<br>
  <a href="https://linkedin.com/in/amlendupandey16">LinkedIn</a> •
  <a href="mailto:amlendu2525@gmail.com">Email</a> •
  <a href="https://twitter.com/_infinimus">Twitter</a>
</p>

---

### About

Backend engineer specializing in **fintech infrastructure** and **distributed payment systems**.

I build production-grade backend systems focused on reliability, low latency, and financial correctness — idempotency, circuit breakers, reconciliation, and fraud detection. Currently working on high-frequency trading infrastructure and open-source payment tooling.

---

### PayCore — Distributed Payment Infrastructure

[**→ View Project**](https://github.com/Infinimus01/distributed-payment-system-)

A production-grade distributed payment system built to solve real fintech reliability problems:

- **Circuit Breaker** (CLOSED → OPEN → HALF-OPEN) — prevents cascading failures when downstream services degrade. Tested full lifecycle under real service outage.
- **Smart Retry with Error Classification** — non-retryable errors (insufficient funds, card expired) abort immediately. Retryable errors use exponential backoff with jitter — eliminates thundering herd on recovery.
- **End-to-End Idempotency** — dual-layer: Redis fast-path + PostgreSQL unique constraints as truth-path fallback. Guarantees exactly-once processing under concurrent duplicate requests.
- **Reconciliation Engine** — cross-checks payment records against append-only wallet ledger. Detects 4 mismatch types including completed payments with no wallet debit and failed payments with unexpected charges. Processes records in **17ms**.
- **Redis-backed Anomaly Detection** — 4 real-time fraud rules (velocity, large amount, failed streak, duplicate amount). Non-blocking by design — flags attacks without rejecting legitimate payments.
- **Load tested with k6** — 50 concurrent users, **51 req/sec**, p50=9ms, p95=32ms.

Stack: `Node.js` `TypeScript` `PostgreSQL` `Redis` `Docker`


### Real-Time Contract Address Monitoring & Alerting

[**→ View Project**](https://github.com/Infinimus01/ca-sentinel.bot)

Built a real-time monitoring system that detects newly published blockchain contract addresses and delivers validated 
alerts within seconds.

- Built a site-agnostic **real-time monitoring system** that detects newly published EVM and Solana contract addresses from public web pages and delivers validated alerts to Telegram within seconds.
- Implemented **async HTTP/2 polling** with **ETag/Last-Modified** conditional requests, **SHA-256** change verification, EIP-55/base58 validation, confidence scoring, and intelligent deduplication for reliable detection.
- Designed a **pluggable parser architecture** with SQLite WAL persistence, transactional outbox-based delivery, retry/backoff handling, automated route discovery, and Docker/systemd deployment, using Python 3.11+, asyncio, httpx, selectolax, SQLite, PyCryptodome, and Telegram Bot API.

Stack: `Python 3.11+` `httpx` `SQLite` ` PyCryptodome` `Telegram Bot API`

---

### Skills

| Area | Technologies |
|------|-------------|
| Backend | Golang, Node.js, TypeScript, Express, REST APIs |
| Fintech | Payment Systems, Idempotency, Circuit Breaker, Distributed Locking, ACID Compliance |
| Databases | PostgreSQL, Redis, MongoDB, MySQL |
| Infrastructure | Docker, AWS (ECS, ECR, CloudWatch), GCP, CI/CD |
| Observability | Prometheus, Grafana, Signoz |
| Languages | TypeScript, JavaScript, Python, C++ |

---

### Other Projects

- **[token-management-api](https://github.com/Infinimus01/token-management-api)** — Distributed token system with Redis + Docker for short-lived secure access control
- **[Incident_tracker](https://github.com/Infinimus01/Incident_tracker)** — Incident management and tracking prototype
- **[MCP-Gemini-Tool-Agent](https://github.com/Infinimus01/MCP-Gemini-Tool-Agent)** — AI command agent using Google Gemini and Model Context Protocol for real-world task execution

---

### Open Source

- [NexusTimer #475](https://github.com/bryanlundberg/NexusTimer/pull/475) — Merged PR
- [NexusTimer #469](https://github.com/Infinimus01/NexusTimer/pull/469) — Merged PR
- [DebugFest/snake-game #14](https://github.com/debugfest/snake-game/pull/14) — Merged PR

---

### Achievements

- LeetCode **1850+** (Top 5%) — Codeforces **1400+** — GFG Institute Rank **#3**
- Written technical articles on distributed systems and fintech engineering

---

*Open to backend engineering roles in fintech, infrastructure, and distributed systems.*
