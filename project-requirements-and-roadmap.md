# Project Requirements and Roadmap

## Purpose

This document is the canonical product-facing reference for the project.

It defines what the project is, who it is for, what success looks like, what belongs in phase 1, and how development should proceed over time.

## This File Covers

- project goals
- users and constraints
- platform and deployment decisions
- MVP scope
- phased roadmap

## This File Does Not Cover

- detailed History teaching logic
- detailed module-by-module system analysis

## Project Overview

This project is a private family learning system designed to improve exam performance for a small number of students. The first subject is History. The product will begin as a Mandarin-first web application that runs on a local computer and is accessed from iPhone, iPad, or other browser-capable devices over home Wi-Fi.

## Problem Statement

Exam-oriented study often fails because students spend too much time reading large amounts of material without enough structure, diagnosis, or targeted review.

Generic summaries are not enough because:

- they do not identify individual weak points
- they do not connect mistakes to specific review actions
- they do not create a repeatable learning loop

The system should focus on targeted weak-point improvement rather than broad content accumulation.

## Product Goal

The goal is to help a small number of family students improve exam performance by transforming source materials into structured learning and review resources.

The system should:

- ingest textbooks, exam papers, and mistake records
- organize them into a usable knowledge structure
- identify weak points
- deliver targeted practice and review
- preserve progress over time

## Target Users

### Student

The student uses the system to study, review, answer questions, and improve weak areas.

### Parent or Family Admin

The parent or family admin manages the students, uploads source materials, and checks progress.

### Content Admin

The content admin manages knowledge structure, tags, and content quality. In the MVP, this role may be the same person as the parent or family admin.

## Core Product Principles

- private and practical rather than platform-scale
- focused on score improvement rather than content volume
- weak-point driven rather than chapter-driven
- Mandarin-first because source materials are mainly in Mandarin
- small-scope before scale
- web-first rather than native-app-first

## Scope and Constraints

- the system is for one family, not the public
- the user count is small
- development happens on a local computer
- early use happens over a home Wi-Fi network
- phase 1 does not require real-time communication
- students should be able to use iPhone, iPad, or any browser-based device

## Platform Decisions

The product should be built as a standard client-server web application from the beginning.

That means:

- browser-based frontend
- backend API
- database
- content processing and analysis layer

The local computer will host the system first. Student devices will connect through the browser over the local network. Later, the same architecture should be deployable to a public or private server without redesigning the product.

## Language Strategy

Mandarin is the canonical content language and the primary interface language.

The system should also be designed so English can be added later without changing the underlying content model.

The language strategy is:

- source educational content is stored in Mandarin
- the primary UI is Mandarin
- English is a secondary interface and localization layer

## AI Role in the Project

AI agents such as Codex, Claude, and Gemini can support:

- content parsing
- concept and question tagging
- summary generation
- exercise generation
- weak-point analysis support
- software development support

AI should not be the only source of truth for critical student-state decisions. Important tracking and scheduling behavior should rely on explicit data structures and rules, and important content outputs should be reviewable and correctable.

## MVP Definition

The MVP is a private local web application for one family, focused on one subject: History.

The MVP should validate the core learning loop only:

- ingest source materials
- organize them into a useful structure
- identify weak points
- deliver targeted practice
- store mistakes
- schedule review

The MVP should stay narrow enough to prove learning value before adding advanced features.

## User Roles

### Student Responsibilities and Capabilities

The student should be able to:

- log in
- view today’s study and review tasks
- read lesson content
- answer practice questions
- review past mistakes
- see simple progress information

### Parent or Family Admin Responsibilities and Capabilities

The parent or family admin should be able to:

- manage student accounts
- upload source materials
- inspect weak points and recent progress
- review basic system output quality

### Content Admin Responsibilities and Capabilities

The content admin should be able to:

- manage the History knowledge structure
- inspect parsed content
- edit tags and mappings
- correct generated explanations or content errors

## Core User Workflows

### Content Ingestion

- upload textbook, exam, or mistake materials
- parse and normalize them
- classify them into concepts and question types
- store them in the internal system

### Student Daily Study

- log in
- see current tasks
- study a focused lesson or review item
- complete targeted practice
- store results for later analysis

### Mistake Review

- save wrong answers
- connect them to specific weak points
- present them again later for retry
- track whether the weakness is improving

### Daily Review Queue

- generate review tasks from weak points and recent study
- guide the student through the review set
- update mastery state after completion

### Parent Progress Checking

- open the dashboard
- inspect weak areas
- review recent activity
- understand whether the student is improving

## Functional Requirements

### User and Access

- support a small number of users
- provide basic login and role separation
- keep the system private in phase 1

### Content Upload and Storage

- upload source files or text
- store textbook and exam materials
- store mistake records and related metadata

### Knowledge Organization

- maintain a knowledge tree for History
- map lessons and questions into that structure
- support concept-level organization

### Lesson Delivery

- present short modular lesson content
- present review-oriented content for specific weak points

### Targeted Practice

- generate or assemble question sets by weak point
- support retries for missed items
- store attempt results

### Mistake Tracking

- save wrong answers
- group mistakes by concept or question type
- support later review and retry

### Review Scheduling

- create daily review tasks
- support repeated review of weak points
- update student state after review

### Basic Analytics

- track accuracy by concept
- show recent activity
- show major weak areas
- show simple progress trends

## Non-Functional Requirements

### Device Support

- work well on iPhone and iPad
- remain usable on desktop browsers
- use a simple interface suitable for smaller screens

### Performance

- load quickly on home Wi-Fi
- feel responsive during normal study actions
- avoid requiring real-time infrastructure in phase 1

### Privacy and Simple Security

- keep the system private to the family
- store only necessary student data
- protect access through basic account controls

### Maintainability

- keep frontend, backend, and data responsibilities separate
- support future deployment to a public server
- avoid locking the project into a local-only architecture

### Multilingual Readiness

- treat Mandarin as primary
- allow later English interface support without changing core data assumptions

## Success Criteria

The MVP should be considered useful if it can:

- ingest real source materials
- organize them into a usable History structure
- support targeted practice and review
- preserve mistake history
- create a daily review workflow
- show enough progress data for a parent or admin to judge whether the student is improving

## Out of Scope for Phase 1

- native iOS app development
- public platform features
- real-time sync
- offline-first sync
- teacher collaboration
- large-scale analytics
- gamification

## Development Phases

### Phase 1: Documentation and Scope Lock

- finalize project requirements
- finalize History learning framework
- finalize tools and module definitions

### Phase 2: MVP Architecture and Data Model

- define frontend/backend split
- define core entities and relationships
- choose technical stack

### Phase 3: Content Ingestion and Knowledge Structure

- build upload and parsing workflow
- build History knowledge structure
- define tagging and content correction flow

### Phase 4: Student Learning Loop

- build dashboard
- build lesson and practice flow
- build mistake storage and review queue

### Phase 5: Review, Analytics, and Refinement

- improve review scheduling
- improve weak-point diagnosis
- add parent/admin visibility
- refine quality based on real usage

## Roadmap

The immediate sequence should be:

1. lock product requirements
2. lock History learning framework
3. lock system module and tool plan
4. design the MVP data model and architecture
5. define the first History content ingestion format
6. build the core learning loop
7. test with a real student workflow
8. refine based on actual outcomes

The first thing that must be validated is whether the system can turn real History materials into a structured workflow that improves targeted weak points. Broader deployment and advanced product features can wait until after first student use.

## Open Questions

- what grade level should the first History MVP target
- what exam format should be supported first
- what source file formats should be handled first
- how should mastery and review priority be scored in the initial version
- what technical stack should be used for the first implementation

## Summary

This project should begin as a private, Mandarin-first, History-focused web application for one family. The MVP should stay narrow, prove the core learning loop, and preserve a clean path to later deployment and expansion.
