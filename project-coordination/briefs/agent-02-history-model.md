# Agent-02 History Model Brief

## Purpose

This agent exists to define the History learning structure that the rest of the system will organize around.

## Your Mission

Define the initial History taxonomy, weak-point model, learning unit model, and review item model for the MVP. Your work should turn the pedagogical framework into a structured model that other agents can use without needing deep extra context.

## What You Own

- History taxonomy structure
- weak-point category model
- learning unit model for History
- review item model for History
- History-specific concept relationships needed for learning and review

## What You Support But Do Not Own

- architecture decisions
- parsing implementation
- frontend page design
- mastery algorithm implementation
- deployment and backend foundation

## What You Must Not Change Without Approval

- shared data model beyond your owned domain definitions
- shared API contracts
- project terminology already locked in canonical docs
- repo-wide structure
- anything owned by another agent

## Context You Need

Read only these documents first:

- `history-learning-framework.md`
- `project-requirements-and-roadmap.md`
- `project-coordination/agent-collaboration-protocol.md`

Use `tools-and-modules.md` only where module boundaries affect the History model.

## Inputs

- canonical History learning framework
- canonical product requirements
- locked controller decisions
- later architecture constraints from Agent 01

## Required Outputs

- proposed History taxonomy outline
- proposed weak-point category model
- proposed learning unit model
- proposed review item model
- identified assumptions and open decisions needing controller review

## Dependencies

Initial design pass can start from canonical docs alone.

Other agents depend on this agent for:

- History structure used by ingestion
- History structure used by learning engine
- History structure reflected in the student experience

## Working Rules

- keep outputs concise
- make assumptions explicit
- note cross-agent effects clearly
- write requests into the status file only

## Definition of Done

- taxonomy is clear enough for downstream tagging and review design
- weak-point categories are practical and not overly broad
- learning unit model matches the History framework
- review item model supports daily, weak-point, cross-unit, and exam-oriented review
- assumptions are explicit
- unresolved content-model decisions are surfaced for controller review

## Writeback Instructions

Write progress only to `project-coordination/status/agent-02-history-model-status.md`.

Do not edit this brief file.

## Current Starting Point

The project already has a canonical History learning framework but no formal subject model yet. Start by converting the learning framework into a reusable History content and review structure for the MVP.
