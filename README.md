<div align="center">
  <img src="./assets/avatar.jpg" width="120" height="120" style="border-radius: 50%; object-fit: cover; border: 1px solid rgba(255, 255, 255, 0.15);" alt="Priyanshu" />
  <br/><br/>
  <h1>Priyanshu</h1>
  <p><strong>Product Engineer • AI Systems & Autonomous Runtimes • Cloud Infrastructure</strong></p>
  
  <p>
    <a href="https://www.linkedin.com/in/priyanshu-s4nvi/">LinkedIn</a> &nbsp;•&nbsp;
    <a href="https://x.com/w3fparthh">X (Twitter)</a> &nbsp;•&nbsp;
    <a href="mailto:priyanshupk2022@gmail.com">Email</a> &nbsp;•&nbsp;
    <a href="https://github.com/priyanshupk2022-arch?tab=repositories">Repositories</a> &nbsp;•&nbsp;
    <code>Discord: w3f.parthh</code>
  </p>
</div>

---

### Overview

I am a software engineer and product builder focused on autonomous AI systems, full-stack applications, and resilient backend infrastructure. I specialize in taking products from initial architecture through implementation, testing, and production deployment.

My work spans compiler-level AST code transformations, isolated sandbox execution, mathematical drift detection in automated data pipelines, and deterministic financial governance engines.

```
Core Focus: Autonomous AI Agents • SaaS Product Engineering • Distributed Concurrency • Deterministic Systems
```

---

### Flagship Systems

#### 1. [ZeroShield](https://github.com/priyanshupk2022-arch/zeroshield) — Autonomous Cyber Red-Team & Exploit Immunizer
*Autonomous vulnerability hunter, ephemeral sandbox exploit arena, and AST codemod synthesizer.*

- **Problem:** Static analysis flags vulnerabilities with high false-positive rates, and automated LLM patch generators often produce hallucinated, non-compiling, or regression-inducing code.
- **Architecture & Implementation:**
  - **AST Traversal:** Scans JavaScript/TypeScript ASTs (`ts.createSourceFile`) for tainted source-to-sink injection vectors (CWE-78 Command Injection, CWE-1321 Prototype Pollution, CWE-287 Broken Auth).
  - **Ephemeral Sandboxes:** Provisions isolated execution containers (Daytona SDK & Docker) to run live attack payloads, proving exploitability with zero false positives.
  - **NVIDIA AVO Codemod Synthesizer:** Rewrites vulnerable sinks into type-safe parameterized implementations validated by `Zod` schemas.
  - **Triple-Lock Verification:** Enforces a three-tier gate before PR creation—asserting exploit payload is blocked, golden application inputs pass (HTTP 200), and test suite passes (Exit 0).
  - **TrueForge MCP Server:** Implements JSON-RPC 2.0 Model Context Protocol tools backed by SQLite WAL session persistence.
- **Verification:** **27/27 passing adversarial & sandbox tests** (`node --test packages/core/dist/**/*.test.js`).
- **Stack:** `TypeScript 5.7`, `Node.js 22`, `React 19`, `Daytona SDK`, `TrueForge MCP`, `Express 5.2`, `SQLite WAL`.

---

#### 2. [SENTINEL-CHAIN](https://github.com/priyanshupk2022-arch/SENTINEL-CHAIN) — Autonomous CTI Harvester & Self-Healing Web Substrate
*Continuous Cyber Threat Intelligence ingestion platform with closed-loop selector self-healing upon DOM mutations.*

- **Problem:** Web intelligence and security advisory harvesters break silently when target portals update their HTML structure, causing data pipeline downtime.
- **Architecture & Implementation:**
  - **Mathematical Drift Model:** Evaluates feed health via deterministic quality and drift equations:
    $$\text{Quality: } Q_s = 0.50 C_f + 0.30 V_t + 0.20 A_c \qquad \text{Drift: } D_t = 1.0 - Q_s$$
  - **Quarantine Isolation:** Isolates degraded feeds when $D_t > 0.35$ to protect the downstream Threat Knowledge Graph from corrupted entities.
  - **Bright Data AI Flow Loop:** Automatically dispatches DOM deltas to `/refactor_template`, verifies updated CSS selectors against clean data ($Q_s = 1.00$), and resumes collection without human intervention.
  - **Deterministic Testing:** In-process mock target server simulating V1 and V2 DOM layouts for 100% offline, reproducible E2E tests.
- **Verification:** **13/13 passing async Pytest tests** (`pytest backend/tests/ -v`).
- **Stack:** `Python 3.11`, `FastAPI`, `Next.js 14`, `SQLAlchemy 2.0 Async`, `Bright Data API`, `SQLite / PostgreSQL`.

---

#### 3. [V4P0R](https://github.com/priyanshupk2022-arch/V4P0R) — Agentic Corporate Card & Spend Governance Engine
*Two-speed financial execution engine combining sub-100ms atomic Redis Lua authorizations with immutable PostgreSQL double-entry ledgers.*

- **Problem:** Concurrent AI agents spending against shared budgets suffer from double-spend race conditions, and JavaScript float math introduces rounding exploits.
- **Architecture & Implementation:**
  - **Zero-Float Precision:** Custom integer minor units engine with `BigInt` splitting (`centsMath.ts`) preventing IEEE 754 precision errors.
  - **Atomic Concurrency (Speed 1):** Sub-100ms authorization decisions executed in a single atomic Redis Lua script (`process_authorization.lua`) with instant budget reservation.
  - **Immutable Double-Entry Ledger (Speed 2):** Append-only PostgreSQL schema enforcing database-level balance constraints (`DEBIT == CREDIT`) and tenant Row-Level Security (RLS).
  - **Replay Protection:** Constant-time HMAC-SHA256 signature verification with 300-second timestamp drift tolerance.
- **Verification:** **66/66 passing Vitest tests** across unit math, state machines, and Prava card adapters (`npm test`).
- **Stack:** `TypeScript`, `Next.js 15 App Router`, `Upstash Redis (Lua)`, `Supabase (PostgreSQL 15 RLS)`, `Vitest`.

---

#### 4. [ANOTAI.PRO](https://github.com/priyanshupk2022-arch/ANOTAI.PRO) — Shopify Embedded Multi-Agent Revenue Team
*Shopify-embedded Remix application delivering an autonomous 5-agent operations squad with hard COGS margin protections.*

- **Problem:** Unbounded e-commerce sales AI agents often hallucinate excessive discounts that destroy merchant profitability.
- **Architecture & Implementation:**
  - **Hierarchical Agent Squad:** Coordinates Personal Shopper, Cart Sniper, Retention Engine, and Department Managers with CEO executive escalation for high-value carts.
  - **Margin Guardian Guardrail:** Hard financial verification layer that computes Cost of Goods Sold (COGS) in real time and automatically vetoes or forces merchant sign-off on unprofitable discounts.
  - **Durable Action Queue:** Decouples agent recommendations from Shopify GraphQL execution, enforcing merchant risk tolerances (`suggest_only`, `draft_action`, `auto_execute`).
  - **Token Cost Accounting:** Records token consumption and exact dollar API costs per workflow execution in Supabase audit logs.
- **Stack:** `TypeScript`, `Remix Vite`, `Shopify Polaris`, `Shopify App Bridge`, `Prisma ORM`, `Supabase PostgreSQL`, `Google Gemini 1.5 Pro`.

---

#### 5. [BRAHMA](https://github.com/priyanshupk2022-arch/BRAHMA) — Cognitive Operating System (CogOS) in Pure Rust
*Autonomous programming runtime with Monte Carlo Tree Search (MCTS) AST delta synthesis and cryptographic enclaves.*

- **Problem:** AI code generation in compiled languages frequently produces non-compiling syntax errors and type mismatches.
- **Architecture & Implementation:**
  - **Compiler-Coincident State Synthesis (SQCS):** Salsa-like query database that tests incremental AST mutations and automatically rolls back type mismatches in memory.
  - **MCTS Type-Solver:** Simulates candidate code transformations and prunes type-invalid AST branches before compilation.
  - **Memory Safety & Security:** Strict `#![forbid(unsafe_code)]` with zero unhandled panics, Argon2 password hashing, and AES-GCM encrypted episodic memory journals.
- **Stack:** `Rust 2024 Edition`, `Tokio Async`, `Syn`, `Quote`, `Rusqlite (WAL)`, `Ratatui TUI`.

---

### Technical Capabilities

```
┌─────────────────────────┬────────────────────────────────────────────────────────────────────────┐
│ Domain                  │ Core Technologies & Competencies                                       │
├─────────────────────────┼────────────────────────────────────────────────────────────────────────┤
│ Languages               │ TypeScript, Python 3.11+, Rust 2024, JavaScript (ESNext), SQL, Bash     │
│ Full-Stack & UI         │ React 19, Next.js (App Router), Remix Vite, Shopify Polaris, Tailwind  │
│ Backend & Runtimes      │ Node.js 22, FastAPI, Tokio (Async Rust), Express, Prisma ORM           │
│ Databases & Storage     │ PostgreSQL (Supabase RLS), Upstash Redis (Lua), SQLite (WAL Mode)      │
│ AI & Autonomous Systems │ Model Context Protocol (MCP), AST Codemods, Sandboxing, Multi-Agent   │
│ Security & Invariants   │ HMAC-SHA256, Zero-Float Cents Math, Triple-Lock Gates, Cryptography    │
│ DevOps & Testing        │ Docker, Daytona SDK, Vitest, Pytest, Node Test Runner, Cargo Test, CI  │
└─────────────────────────┴────────────────────────────────────────────────────────────────────────┘
```

---

### Engineering Principles

1. **Deterministic Invariants Over Probabilistic Outputs:** Business logic, financial arithmetic, and security perimeters must be enforced by deterministic code (Zod schemas, BigInt cents math, SQLite WAL, Redis Lua scripts).
2. **Triple-Lock Verification:** Systems must prove negative defense (exploit blocked), positive functionality (golden inputs pass HTTP 200), and non-regression (full test suite passes Exit 0) before shipping.
3. **Fail-Closed Security:** Webhook replays, path traversals, unverified cryptographic tokens, and type mismatches reject immediately by default.
4. **Code As The Source Of Truth:** Documentation and architecture specifications reflect verified, reproducible code rather than aspirational claims.

---

<div align="center">
  <sub>Priyanshu • Autonomous AI Systems & Product Engineering</sub>
</div>
