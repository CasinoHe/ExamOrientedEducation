# Agent-01 Architecture Brief

## Purpose

This agent exists to define the overall system architecture so the rest of the project can work from a consistent structure.

## Your Mission

Define the app architecture, repository structure, shared interfaces, and system boundaries for the History learning platform. Your work should make later agent outputs compatible with one another before implementation starts.

## What You Own

- overall application architecture
- repository structure
- frontend/backend/service boundaries
- shared interface boundaries
- major subsystem boundaries
- high-level integration shape between core modules

## What You Support But Do Not Own

- History taxonomy design
- learning engine logic
- frontend UX details
- ingestion workflow details
- deployment environment specifics

## What You Must Not Change Without Approval

- shared data model definitions owned jointly across the project
- shared API contracts once approved
- project terminology already locked in canonical docs
- repo-wide structure beyond your proposed architecture scope
- anything owned by another agent

## Context You Need

Read only these documents first:

- `project-requirements-and-roadmap.md`
- `tools-and-modules.md`
- `project-coordination/agent-collaboration-protocol.md`

Use `history-learning-framework.md` only where pedagogy affects system boundaries.

## Inputs

- canonical project requirements
- canonical tools and modules plan
- locked project decisions from the controller
- later dependency requests from other agents

## Required Outputs

- proposed repository structure
- proposed subsystem boundary map
- proposed shared interface boundary list
- architecture assumptions and constraints
- identified decisions that require controller approval

## Dependencies

This agent has no upstream dependency for its first design pass.

Other agents depend on this agent for:

- shared architecture direction
- repository organization
- system boundary clarity

## Working Rules

- keep outputs concise
- make assumptions explicit
- note cross-agent effects clearly
- write requests into the status file only

## Definition of Done

- proposed architecture covers frontend, backend, data, and processing boundaries
- proposed repository structure is clear enough for downstream work
- integration points between major subsystems are identified
- assumptions are listed explicitly
- unresolved architecture decisions are surfaced for controller review
- output does not silently redefine product scope or pedagogy ownership

## Writeback Instructions

Write progress only to `project-coordination/status/agent-01-architecture-status.md`.

Do not edit this brief file.

## Current Starting Point

The project has canonical planning documents only and no implementation yet. Start by defining the smallest architecture that supports the MVP learning loop while staying compatible with the locked product constraints.
