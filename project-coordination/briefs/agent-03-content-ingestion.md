# Agent-03 Content Ingestion Brief

## Purpose

This agent exists to define how raw educational materials become structured content inside the platform.

## Your Mission

Define the upload flow, parsing flow, normalization flow, tagging workflow, and content QA flow for the MVP. Your work should specify how Mandarin History materials, exams, and mistake records become structured assets the platform can use.

## What You Own

- upload flow
- parsing workflow
- normalization workflow
- content tagging workflow
- content QA flow
- content ingestion assumptions and constraints

## What You Support But Do Not Own

- History taxonomy definitions
- learning engine logic
- frontend page design
- overall system architecture
- backend foundation choices outside ingestion needs

## What You Must Not Change Without Approval

- shared data model outside ingestion-owned needs
- shared API contracts
- locked project terminology
- repo-wide structure
- anything owned by another agent

## Context You Need

Read only these documents first:

- `project-requirements-and-roadmap.md`
- `tools-and-modules.md`
- `history-learning-framework.md`
- `project-coordination/agent-collaboration-protocol.md`

Use future outputs from Agent 01 and Agent 02 when available.

## Inputs

- canonical product requirements
- canonical tools and modules plan
- canonical History framework
- later architecture constraints from Agent 01
- later taxonomy constraints from Agent 02

## Required Outputs

- proposed ingestion workflow
- proposed parsing and normalization stages
- proposed tagging workflow
- proposed content QA workflow
- identified input-format assumptions
- unresolved decisions needing controller review

## Dependencies

This agent should align with:

- Agent 01 for architecture boundaries
- Agent 02 for taxonomy and weak-point tagging model
- Agent 06 for backend and storage constraints

Other agents depend on this agent for:

- availability of structured content assets
- assumptions about source material formats

## Working Rules

- keep outputs concise
- make assumptions explicit
- note cross-agent effects clearly
- write requests into the status file only

## Definition of Done

- ingestion flow is clear from upload to structured content
- parsing and normalization stages are distinct
- tagging workflow depends on the History model without redefining it
- QA flow is practical for a family-use MVP
- assumptions about input formats are stated clearly
- unresolved dependency issues are surfaced for controller review

## Writeback Instructions

Write progress only to `project-coordination/status/agent-03-content-ingestion-status.md`.

Do not edit this brief file.

## Current Starting Point

The project has no ingestion design yet. Start by defining the smallest reliable workflow that can handle real History source materials without overbuilding the system.
