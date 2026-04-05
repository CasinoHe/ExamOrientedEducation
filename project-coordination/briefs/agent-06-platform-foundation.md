# Agent-06 Platform Foundation Brief

## Purpose

This agent exists to define the implementation foundation that will let the rest of the system run locally and evolve cleanly later.

## Your Mission

Define the backend foundation, auth approach, local deployment shape, and database/bootstrap environment for the MVP. Your work should support a local web app first while keeping future public deployment possible.

## What You Own

- backend foundation
- auth approach
- local deployment shape
- database and bootstrap environment assumptions
- environment and runtime foundation decisions

## What You Support But Do Not Own

- frontend UX
- History taxonomy design
- learning engine behavior
- ingestion workflow specifics
- overall product scope

## What You Must Not Change Without Approval

- shared data model beyond your owned platform concerns
- shared API contracts
- locked project terminology
- repo-wide structure outside platform foundation scope
- anything owned by another agent

## Context You Need

Read only these documents first:

- `project-requirements-and-roadmap.md`
- `tools-and-modules.md`
- `project-coordination/agent-collaboration-protocol.md`

Use `history-learning-framework.md` only when learning requirements affect platform choices.

## Inputs

- canonical product requirements
- canonical tools and modules plan
- locked project decisions from the controller
- later architecture guidance from Agent 01

## Required Outputs

- proposed backend foundation shape
- proposed local deployment model
- proposed auth approach for family use
- proposed database/bootstrap environment assumptions
- unresolved platform decisions needing controller review

## Dependencies

This agent has no upstream dependency for the first design pass.

Other agents depend on this agent for:

- backend environment expectations
- storage and auth assumptions
- local deployment constraints

## Working Rules

- keep outputs concise
- make assumptions explicit
- note cross-agent effects clearly
- write requests into the status file only

## Definition of Done

- backend foundation direction supports the MVP constraints
- auth approach fits a small private family-use system
- local deployment model is clear
- database/bootstrap assumptions are explicit
- unresolved platform decisions are surfaced for controller review

## Writeback Instructions

Write progress only to `project-coordination/status/agent-06-platform-foundation-status.md`.

Do not edit this brief file.

## Current Starting Point

The project is locked to a local-network-first web app with later public deployment as a future option. Start by defining the smallest solid platform foundation that supports that path.
