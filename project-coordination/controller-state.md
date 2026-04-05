# Controller State

## Purpose

This file exists so the controller can resume the project after interruptions without rereading the whole repo.

It tracks coordination state, current focus, dependencies, and pending reviews.

## Current Project State

The repository currently contains planning and coordination documents only. Product direction, History learning framework, system module breakdown, and multi-agent coordination structure have been defined, but no product code or implementation artifacts have been created yet.

## Canonical Reference Files

- `project-requirements-and-roadmap.md`
- `history-learning-framework.md`
- `tools-and-modules.md`
- `project-coordination/agent-collaboration-protocol.md`

## Controller Responsibilities

- maintain the overall plan
- dispatch work
- review agent outputs
- resolve conflicts and cross-agent dependencies
- keep architectural consistency

## Completed So Far

- defined the project as a private family-use education tool
- locked the first subject as History
- locked the product as a Mandarin-first web application
- locked local-network-first deployment for phase 1
- documented product requirements and roadmap
- documented the History learning framework
- documented the tools and modules plan
- designed the multi-agent coordination model
- defined the six-agent split

## Not Started Yet

- repository architecture design
- technical stack selection
- data model design
- History taxonomy design
- content ingestion design
- student frontend design
- learning engine design
- platform foundation design
- any code implementation

## Active Focus

The current focus is coordination bootstrap. The next controller task is to use the briefs and protocol to dispatch the initial design work to the first agents. No agent outputs are pending review yet.

## Locked Decisions

- the project is a private family-use tool
- the first subject is History
- Mandarin is the canonical content language
- the first implementation is a web app
- the first deployment target is local-network use over home Wi-Fi
- phase 1 does not include real-time sync
- this thread is the overview/controller thread
- briefs are controller-owned
- status files are agent-owned

## Open Decisions

- first technical stack choice
  Why it matters: it affects architecture, deployment, and frontend/backend implementation shape.
- first History grade level target
  Why it matters: it affects content taxonomy, question forms, and scope.
- first content input formats
  Why it matters: it affects ingestion and parsing pipeline design.
- initial mastery and review priority logic
  Why it matters: it affects the learning engine and review workflow.

## Agent Ownership Map

- Agent 01 Architecture: owns overall app architecture, repository structure, shared interfaces, and system boundaries; must not redefine History pedagogy or agent scopes.
- Agent 02 History Model: owns History taxonomy, weak-point model, learning unit model, and review item model; must not redefine platform architecture or shared APIs.
- Agent 03 Content Ingestion: owns upload flow, parsing, normalization, tagging workflow, and content QA flow; must not redefine the taxonomy or overall system architecture.
- Agent 04 Student Frontend: owns student-facing UX, page map, lesson/review/practice UI, and mobile-first browser behavior; must not redefine shared data contracts or backend boundaries.
- Agent 05 Learning Engine: owns diagnosis, mastery tracking, review scheduling, and recommendation logic; must not redefine taxonomy ownership or platform foundation.
- Agent 06 Platform Foundation: owns backend foundation, auth approach, local deployment shape, and database/bootstrap environment; must not redefine product scope or frontend experience.

## Dependency Map

- architecture -> all agents
- history model -> content ingestion, student frontend, learning engine
- platform foundation -> content ingestion, student frontend, learning engine
- content ingestion -> learning engine, student frontend
- learning engine -> student frontend

## Pending Reviews

- none yet

## Blockers

- none yet

## Next Actions

1. dispatch Agent 01 Architecture for the initial architecture and shared interface proposal
2. dispatch Agent 02 History Model for the History taxonomy and weak-point model proposal
3. dispatch Agent 06 Platform Foundation for the backend and local deployment foundation proposal
4. review those three outputs for cross-agent consistency
5. revise downstream briefs if the first-round decisions change assumptions

## Handoff Notes

Read this file first on restart, then read the protocol file, then review the three canonical project docs only if project-wide decisions need to be checked. Ignore implementation details because no code has been created yet. The repo is still at the planning/bootstrap stage.
