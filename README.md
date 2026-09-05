<div align="center">

```
========================================================================================
  SATYAM SETHI  ::  FINTECH  ×  SOFTWARE ENGINEERING  ×  DEVOPS
========================================================================================
```

### Engineering reliable financial systems, high-throughput backend services, and deterministic developer tools.

[🌐 Portfolio](https://satyam-sethi.netlify.app/) &nbsp;•&nbsp; [🏛️ FinTech Systems](#02--fintech-engineering) &nbsp;•&nbsp; [🚀 Selected Builds](#03--selected-builds) &nbsp;•&nbsp; [🛠️ Tech Stack](#04--engineering-stack)

</div>

---

### `01 // ENGINEERING FOCUS`

```
┌──────────────────────────────┬──────────────────────────────┬──────────────────────────────┐
│  FINANCIAL SYSTEMS           │  BACKEND & INFRASTRUCTURE    │  DEVOPS & AUTOMATION         │
│  • Transaction Reconcile     │  • In-Memory Reverse Proxies │  • CI/CD Pipeline Automation │
│  • Settlement State Machines │  • Low-Latency Caching       │  • Concurrency & Uptime Mon. │
│  • ISO Compliance & Auditing │  • Zero-Dependency Tooling   │  • Git / Release Engineering │
└──────────────────────────────┴──────────────────────────────┴──────────────────────────────┘
```

I focus on building deterministic backend systems and developer automation. My work centers on solving data integrity breaks, high-throughput payment lifecycle orchestration, ISO compliance verification, and operational observability with minimal architectural overhead.

---

### `02 // FINTECH ENGINEERING`

Financial systems require zero tolerance for unhandled exceptions, rounding errors, or ambiguous states. I design and build around core financial operations problems:

* **Transaction Reconciliation**: Multi-way reconciliation engines resolving internal ledgers against external payment gateway and bank statement feeds with fuzzy variance detection and break categorization.
* **Settlement State Machines**: Simulating and tracking multi-rail clearing cycles (`Fedwire`, `SWIFT`, `SEPA`, `ACH`, `RTGS`) across `PENDING ➔ PROCESSING ➔ SETTLED / FAILED` transitions with real-time liquidity and exception diagnostics.
* **Data Quality & ISO Validation**: Real-time compliance engines enforcing ISO 6166 ISIN checksums (Modulo 10 double-add-double), ISO 4217 currency dictionaries, ISO 17442 Legal Entity Identifiers (LEIs), and trade execution bounds.

---

### `03 // SELECTED BUILDS`

#### 🏛️ Financial Infrastructure & Operations
* **[`transaction-reconciliation-engine`](https://github.com/Satyam-h-Sethi/transaction-reconciliation-engine)**
  * *Problem*: Discrepancies and timing breaks between internal books and external settlement files create audit risk.
  * *Solution*: Reconciles transaction feeds, flags amount variances and duplicate settlements, and provides an interactive resolution dashboard.
  * `Node.js` `Reconciliation Algorithms` `CSV Pipeline` `Vanilla Web UI`
* **[`settlement-monitor`](https://github.com/Satyam-h-Sethi/settlement-monitor)**
  * *Problem*: Multi-rail clearing queues lack unified lifecycle visibility and actionable failure root-cause analysis.
  * *Solution*: Real-time state machine tracking Fedwire, SWIFT, SEPA, ACH, and RTGS payment instructions with latency metrics and exception diagnosis.
  * `Node.js` `State Machine` `Multi-Rail Clearing` `Vanilla Web UI`
* **[`financial-data-quality-validator`](https://github.com/Satyam-h-Sethi/financial-data-quality-validator)**
  * *Problem*: Malformed trade attributes, invalid ISIN checksums, and non-compliant currencies pollute downstream risk engines.
  * *Solution*: Rule-based audit validator enforcing ISO 6166, ISO 4217, LEI syntax, and trade lifecycle business logic with JSON/CSV support.
  * `JavaScript` `ISO Standards` `Trade Surveillance` `Audit Dashboard`
* **[`ExchangeLens`](https://github.com/Satyam-h-Sethi/ExchangeLens)**
  * *Problem*: High-density financial exchange data is difficult to monitor and analyze at a glance.
  * *Solution*: Clean exchange analytics interface and market data visualizer.
  * `JavaScript` `FinTech` `Market Data`

#### ⚙️ Backend, Systems & Developer Tooling
* **[`http-cache-proxy`](https://github.com/Satyam-h-Sethi/http-cache-proxy)**
  * *Problem*: Repetitive outbound API requests introduce network latency and exceed rate limits.
  * *Solution*: In-memory caching reverse proxy with TTL eviction, `X-Cache` telemetry, programmatic purge endpoints, and live traffic analytics.
  * `Node.js` `HTTP` `In-Memory Caching` `Zero Dependencies`
* **[`url-health-monitor`](https://github.com/Satyam-h-Sethi/url-health-monitor)**
  * *Problem*: Downtime and latency spikes go unnoticed without continuous multi-endpoint probing.
  * *Solution*: High-concurrency URL health and latency checker featuring live terminal matrices, CORS proxy bridge, and browser dashboard.
  * `Node.js` `Concurrency` `Monitoring` `REST Proxy`
* **[`api-payload-mock-server`](https://github.com/Satyam-h-Sethi/api-payload-mock-server)**
  * *Problem*: Frontend and client integration blocked by unfinished or unstable upstream services.
  * *Solution*: Standalone mock server supporting custom routes, dynamic JSON payloads, HTTP status overrides, and simulated latency throttling.
  * `Node.js` `REST Engine` `Developer Tooling`
* **[`json-schema-visualizer`](https://github.com/Satyam-h-Sethi/json-schema-visualizer)**
  * *Problem*: Large JSON payloads are difficult to inspect, type, and validate across team boundaries.
  * *Solution*: Interactive collapsible tree inspector that converts arbitrary JSON into strict TypeScript interfaces and JSON Schema Draft-07 specs.
  * `JavaScript` `AST / Schema` `Type Generation`
* **[`git-commit-craft`](https://github.com/Satyam-h-Sethi/git-commit-craft)**
  * *Problem*: Inconsistent git history creates churn for automated changelogs and semantic versioning.
  * *Solution*: Interactive Conventional Commits wizard with breaking change flags and instant CLI generation.
  * `CLI` `Git Workflow` `Developer Experience`

---

### `04 // ENGINEERING STACK`

```
CORE LANGUAGES      : JavaScript (ES6+ / Node.js), Python, SQL, HTML5, CSS3
FINTECH & STANDARDS : Multi-Rail Settlement (Fedwire, SWIFT, SEPA, ACH, RTGS), ISO 6166 (ISIN), ISO 4217, ISO 17442 (LEI)
BACKEND & SYSTEMS   : In-Memory Caching, Reverse Proxies, Concurrency, State Machines, REST Architecture
DEVOPS & TOOLING    : Git, GitHub Actions, Docker, Linux / Bash, Automated Probing & Monitoring
ARCHITECTURE        : Zero-Dependency Engineering, Clean Vanilla Design Systems, Deterministic Pipelines
```

---

### `05 // CURRENTLY BUILDING & EXPLORING`

* Building resilient, self-contained financial tools with native runtimes and zero runtime dependencies.
* Exploring deterministic transaction state machines with automated break-detection and self-healing reconciliation pipelines.
* Developing lightweight operational monitoring and developer ergonomics tooling.

---

### `06 // ENGINEERING PHILOSOPHY`

1. **Standard Library First**: If a 15-line native implementation accomplishes the task reliably, don't import a 50MB external dependency.
2. **Make State Explicit**: Financial and backend pipelines should be modeled as deterministic state machines — invalid transitions should be impossible.
3. **Observability is Not an Afterthought**: If a system fails, the failure mode and root cause should be immediate, obvious, and categorized.
4. **Clean Code, Clean Interfaces**: Interfaces should be minimal, predictable, and immediately usable.

---

### `07 // COORDINATES`

* **Portfolio**: [satyam-sethi.netlify.app](https://satyam-sethi.netlify.app/)
* **GitHub**: [@Satyam-h-Sethi](https://github.com/Satyam-h-Sethi)
* **Location**: Noida, India

---

```
$ uptime --status
Systems: GREEN | Discrepancies: 0 | Build: DETERMINISTIC | Loop: BUILD -> SHIP -> OBSERVE -> REFINE
```
