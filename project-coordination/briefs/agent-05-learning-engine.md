# Agent-05 Learning Engine Brief

## Purpose

This agent exists to define the personalization logic that turns the platform into a score-improvement system.

## Your Mission

Define the diagnosis, mastery tracking, review scheduling, and recommendation logic for the MVP. Your work should describe how the system identifies weak points, decides what to review next, and updates student learning state over time.

## What You Own

- weak-point diagnosis logic
- mastery tracking model
- review scheduling logic
- recommendation logic
- mistake reuse logic

## What You Support But Do Not Own

- History taxonomy definitions
- frontend interaction design
- ingestion workflow implementation
- overall system architecture
- backend foundation

## What You Must Not Change Without Approval

- shared data model outside your owned domain
- shared API contracts
- locked project terminology
- repo-wide structure
- anything owned by another agent

## Context You Need

Read only these documents first:

- `history-learning-framework.md`
- `project-requirements-and-roadmap.md`
- `tools-and-modules.md`
- `project-coordination/agent-collaboration-protocol.md`

Use later outputs from Agent 01 and Agent 02 when available.

## Inputs

- canonical History framework
- canonical product requirements
- canonical tools and modules plan
- later architecture guidance from Agent 01
- later History model from Agent 02
- later ingestion constraints from Agent 03

## Required Outputs

- proposed weak-point diagnosis approach
- proposed mastery tracking approach
- proposed review scheduling approach
- proposed recommendation logic approach
- unresolved decisions needing controller review

## Dependencies

This agent should align with:

- Agent 01 for architecture boundaries
- Agent 02 for weak-point and History learning structure
- Agent 03 for data availability from ingestion
- Agent 06 for backend and persistence constraints

Other agents depend on this agent for:

- review and recommendation behavior
- student-state update expectations

## Working Rules

- keep outputs concise
- make assumptions explicit
- note cross-agent effects clearly
- write requests into the status file only

## Definition of Done

- diagnosis approach is practical for MVP data quality
- mastery logic is understandable and implementable
- review scheduling supports the History framework
- recommendation logic stays narrow and high-value
- unresolved dependency issues are surfaced for controller review

## Writeback Instructions

Write progress only to `project-coordination/status/agent-05-learning-engine-status.md`.

Do not edit this brief file.

## Current Starting Point

The product is intended to improve scores through weak-point targeting and review. Start by designing the smallest learning engine that can support that loop without requiring advanced analytics or over-automation.
