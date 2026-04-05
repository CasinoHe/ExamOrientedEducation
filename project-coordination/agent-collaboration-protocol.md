# Agent Collaboration Protocol

## Purpose

This file defines how all project agents must collaborate.

## Project Context

This project is a family-use History learning system. It is Mandarin-first, web-app-first, and local-network-first for the initial implementation. The repository is still early-stage and coordination-heavy, so agents must work with clear ownership and minimal context drift.

## Roles in the System

### Controller

The controller maintains the overall plan, dispatches work, reviews outputs, resolves conflicts, and keeps the project coherent.

### Execution Agents

Execution agents work within a specific assigned scope defined by their brief files and write structured progress back through their status files.

### Optional Future Review Agents

Additional review agents may be introduced later if independent design or implementation review becomes necessary.

## Source of Truth

- product decisions come from `project-requirements-and-roadmap.md`
- History pedagogy comes from `history-learning-framework.md`
- module and tooling decisions come from `tools-and-modules.md`
- coordination rules come from this protocol
- assignment comes from the agent's brief
- progress and requests go into the agent's status file

## What Agents May Do

- work inside assigned scope
- propose designs
- note blockers
- request changes from the controller
- reference dependencies explicitly

## What Agents Must Not Do Without Controller Approval

- redefine shared data model
- redefine shared API contracts
- rename cross-agent concepts
- change overall folder structure
- claim ownership outside their brief
- edit other agents' brief files
- edit other agents' status files

## Required Working Style

- keep outputs concise and structured
- make assumptions explicit
- prefer minimal context
- note cross-agent impacts
- do not solve problems by silently expanding scope

## Required Status File Format

Every status file update must include:

- current mission
- completed work
- decisions made
- blockers
- requests for controller
- cross-agent requests
- next step

## Dependency Request Rules

If an agent needs something from another agent, it should write that request in its own status file first.

The controller decides whether to redirect another agent, revise a brief, or log a project-wide decision. Agents should not directly rewrite each other's assignments.

## Review and Handoff Rules

An agent signals readiness through its status file.

The controller reviews the output and then:

- approves it
- asks for revision
- logs a project-wide decision if necessary

## File Ownership Rules

### Controller-Owned Files

- `project-coordination/controller-state.md`
- `project-coordination/decision-log.md`
- `project-coordination/agent-collaboration-protocol.md`

### Brief-Owned Files

- all files under `project-coordination/briefs/`

These files are controller-owned assignments and should not be edited by execution agents.

### Status-Owned Files

- all files under `project-coordination/status/`

These files are the only writeback channel for execution agents.

## Naming and Update Rules

- use stable filenames
- do not rename files casually
- keep dates on meaningful updates
- keep updates brief and scannable
- append to change logs in newest-first order
- update current-state sections consistently rather than mixing multiple contradictory states

## Escalation Rules

The following must be escalated immediately:

- conflicts with locked decisions
- shared interface changes
- architecture changes
- blocked dependencies
- scope mismatch

## Summary

Briefs assign work, status files report progress, and the controller integrates and resolves cross-agent issues.
