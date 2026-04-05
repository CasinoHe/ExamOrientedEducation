# Decision Log

## Purpose

This file records project decisions that affect multiple files, multiple agents, or future architecture.

### DEC-001: Private Family-Use Product
- Date: 2026-04-05
- Status: accepted
- Decider: controller and user
- Context: The project scope needed to be narrowed before product and architecture planning.
- Decision: The product will be built as a private family-use learning system, not a public platform.
- Why: This keeps the MVP focused and avoids unnecessary multi-tenant and platform complexity.
- Impact: Product requirements, deployment strategy, user model, and module scope all remain small and private.
- Affected agents: Agent 01, Agent 03, Agent 04, Agent 05, Agent 06
- Follow-up: Keep public-platform features out of phase 1.

### DEC-002: History Is the First Subject
- Date: 2026-04-05
- Status: accepted
- Decider: controller and user
- Context: The first subject needed to be selected before defining pedagogy and module priorities.
- Decision: The MVP will target History first.
- Why: History fits modular learning, review, and exam-oriented training well and keeps subject modeling manageable.
- Impact: History-specific learning framework, taxonomy design, review logic, and learning assets become the first design targets.
- Affected agents: Agent 01, Agent 02, Agent 03, Agent 04, Agent 05
- Follow-up: Agent 02 should define the initial History knowledge and weak-point model.

### DEC-003: Mandarin-First Content and Interface
- Date: 2026-04-05
- Status: accepted
- Decider: controller and user
- Context: Source material language and UI language strategy needed to be defined early.
- Decision: Mandarin is the canonical content language and the primary interface language. English should remain possible later without changing the source-of-truth model.
- Why: The source materials are Mandarin and the learning system should align with them directly.
- Impact: Content modeling, ingestion assumptions, UI localization strategy, and agent context all use Mandarin-first assumptions.
- Affected agents: Agent 01, Agent 02, Agent 03, Agent 04, Agent 05
- Follow-up: Keep bilingual support architectural, not required for phase 1 completeness.

### DEC-004: Web App First, Local-Network First
- Date: 2026-04-05
- Status: accepted
- Decider: controller and user
- Context: The team needed to choose between native mobile, offline sync, and web delivery approaches.
- Decision: The first implementation will be a standard client-server web app running locally and accessed over home Wi-Fi.
- Why: This is the simplest path that preserves later public deployment flexibility.
- Impact: Frontend, backend, deployment, and device support should all assume browser-based access.
- Affected agents: Agent 01, Agent 04, Agent 06
- Follow-up: Phase 1 excludes native iOS app development and offline sync complexity.

### DEC-005: No Real-Time Sync in Phase 1
- Date: 2026-04-05
- Status: accepted
- Decider: controller and user
- Context: The initial sync and usage model needed to be simplified.
- Decision: Phase 1 will use normal request-response web behavior without real-time sync.
- Why: Real-time coordination is not necessary to validate the learning loop and would add avoidable complexity.
- Impact: Backend, frontend, and review flow design can avoid websocket and live-sync requirements.
- Affected agents: Agent 01, Agent 04, Agent 05, Agent 06
- Follow-up: Keep architecture extendable, but do not design around real-time requirements now.

### DEC-006: Multi-Agent Coordination Model
- Date: 2026-04-05
- Status: accepted
- Decider: controller and user
- Context: The repo is still empty, but work needs to be divided safely across multiple AI agents.
- Decision: Use one overview/controller thread, one shared collaboration protocol, six controller-owned briefs, and six agent-owned status files.
- Why: This keeps context minimal, responsibilities explicit, and progress reviewable without allowing agents to redefine their own assignments.
- Impact: Coordination files become part of the project structure and all agent work must route through them.
- Affected agents: all agents
- Follow-up: Bootstrap the coordination workspace and dispatch the first three agents.
