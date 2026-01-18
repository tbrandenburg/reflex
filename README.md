# reflex

reflex is an AI-native, deterministic workflow engine for designing and running distributed pipelines.
It combines a visual authoring experience with Temporal-based execution, explicit contracts, and
clear operational semantics.

**Main features**
- 🧠 Deterministic orchestration with explicit contracts
- 🧱 Canonical DSL with graph-to-DSL compilation
- 🔁 Saga-based compensation and failure modeling
- 🧭 Full-fidelity observability with OpenTelemetry
- ⚙️ Headless CLI for execution and inspection

**What it is**
- A workflow platform that treats the DSL as canonical truth
- Deterministic orchestration powered by Temporal
- A hybrid activity runtime (container-first with explicit host opt-in)
- A compiler layer that translates graphs to Serverless Workflow DSL

**Why it exists**
- Make complex workflows reliable, observable, and debuggable
- Provide strong contracts while staying flexible for real-world integration
- Enable distribution without redesign through task queues

**Core principles**
- Correctness before cleverness
- Explicit contracts everywhere
- Deterministic orchestration only
- Glue over reinvention

**Workflow model**
- Graphs compile to Serverless Workflow definitions
- Control flow and data flow are distinct
- Sub-workflows are first-class nodes
- Orchestration is pure; side effects live in activities

**Failure handling**
- Saga-based compensation
- No global transactions or implicit rollback
- Failure logic is explicit business logic

**Execution interfaces**
- Web UI for authoring and runtime visibility
- `reflex` CLI for headless execution and inspection

**Observability**
- OpenTelemetry end-to-end
- One trace per workflow run
- Per-node spans with consistent attributes

**Tech stack (current direction)**
- Frontend: React + TypeScript + XYFlow
- Backend: Python + Pydantic + FastAPI
- Orchestration: Temporal (Python SDK)
- Layout: ELK via elkjs

**MVP scope (high level)**
- Core nodes: Python Script, Bash, HTTP, Sub-workflow, Agent ACP, Papermill
- CLI basics: run, plan, validate, stop
- Deterministic compilation with golden tests

**Status**
- Early architecture stage
- MVP scope is defined and frozen
- Focus is on correctness and execution semantics
