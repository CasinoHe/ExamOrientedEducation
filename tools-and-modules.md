# Tools and Modules

## Purpose

This document is the canonical implementation-facing reference for the system modules and internal tools required by the project.

It explains what must be built to support the product and the History learning framework, and it identifies which parts belong in the MVP versus later phases.

## This File Covers

- product modules
- internal and admin tools
- MVP versus later-phase modules
- module dependencies and build order

## This File Does Not Cover

- broad project vision
- detailed History pedagogy except where it directly explains a module

## System Overview

The platform should be treated as a History learning system with four major layers:

1. content processing
2. student learning experience
3. personalization and analytics
4. administration and operations

Not all modules should be built at once. The first implementation should prioritize the modules that support the core learning loop.

## Module Design Principles

- optimize for score improvement, not feature breadth
- design for a small number of family users
- prioritize modules that support the learning loop directly
- keep human review possible where content quality matters
- avoid overbuilding before real student validation

## Product Module Map

### Content Processing Layer

Transforms raw History materials into structured learning assets.

### Student Learning Layer

Presents lessons, review, and practice to the student.

### Personalization and Analytics Layer

Detects weak points, tracks progress, and decides what the student should do next.

### Administration and Operations Layer

Supports content correction, system maintenance, and family/admin oversight.

## Student-Facing Modules

### Student Dashboard

Purpose:

- show what the student should do next

Main functions:

- current weak areas
- today’s review tasks
- recent activity
- simple progress view

### Lesson Viewer

Purpose:

- present short modular lesson content for one History topic at a time

Main functions:

- focused lesson pages
- event summaries
- significance and cause/explanation notes
- exam relevance notes

### Timeline Review

Purpose:

- strengthen time-order understanding and event sequencing

Main functions:

- event ordering exercises
- period-based review
- sequence correction

### Targeted Practice

Purpose:

- give the student focused exercises matched to weak points

Main functions:

- practice by concept
- practice by question type
- retry failed items
- mixed targeted drill sets

### Timed Drill

Purpose:

- improve speed and confidence under assessment conditions

Main functions:

- timed mini-tests
- mixed-question drills
- timing feedback

### Mistake Notebook

Purpose:

- preserve wrong answers and make them reusable for review

Main functions:

- store wrong answers
- tag mistakes
- attach correction notes
- support retry flow

### Daily Review Queue

Purpose:

- tell the student exactly what should be reviewed today

Main functions:

- review task list
- spaced review scheduling
- weak-point prioritization

## Parent and Admin Modules

### Parent Progress View

Purpose:

- help the parent understand current learning status

Main functions:

- recent progress
- weak-point summary
- review completion
- basic readiness view

### Content Admin Console

Purpose:

- manage structured content quality

Main functions:

- inspect parsed content
- correct tags and mappings
- review generated lesson content
- resolve duplicates or quality issues

### Simple Account and User Management

Purpose:

- manage the small number of family users

Main functions:

- create and update users
- assign basic roles
- manage simple access controls

### Taxonomy or Tag Correction Interface

Purpose:

- keep the History knowledge structure consistent

Main functions:

- edit concept tags
- fix taxonomy relationships
- remap items to correct nodes

## Content Processing Modules

### Content Upload

Purpose:

- collect source materials from the family or admin

Main functions:

- file or text upload
- source labeling
- metadata entry
- upload preview

### Parsing and Normalization

Purpose:

- convert raw materials into structured internal records

Main functions:

- text extraction
- question and answer separation
- chapter or section detection
- format normalization

### Knowledge Tagging

Purpose:

- connect content records to the History learning structure

Main functions:

- concept tagging
- question-type tagging
- source tracking
- difficulty or importance tagging

### Knowledge Tree Management

Purpose:

- create and maintain the History knowledge structure

Main functions:

- define taxonomy nodes
- manage parent-child relationships
- map content items to nodes
- revise the structure over time

### Summary and Explanation Generation

Purpose:

- generate lesson-ready summaries and explanations from source material

Main functions:

- summary generation
- key-point extraction
- explanation drafting
- example generation

## Personalization and Analytics Modules

### Weak-Point Diagnosis Engine

Purpose:

- identify the student’s highest-priority weaknesses

Main functions:

- detect weak concepts
- detect unstable question types
- detect repeated mistake patterns
- rank weak areas for intervention

### Mastery Tracking

Purpose:

- estimate the student’s current stability by concept or skill

Main functions:

- update mastery from practice results
- update mastery from review results
- decay stale mastery where needed
- support scheduling and recommendations

### Recommendation Logic

Purpose:

- choose what lesson, drill, or review task should come next

Main functions:

- prioritize weak points
- balance review and new learning
- suggest the next best activity

### Performance Analytics

Purpose:

- make student progress visible

Main functions:

- accuracy by topic
- recent trend tracking
- weak-area history
- simple completion and activity summaries

## Internal Operations Tools

### Taxonomy Editor

Needed to:

- create and edit the History knowledge tree
- merge overlapping concepts
- keep tagging consistent

### Question Bank Manager

Needed to:

- browse questions
- search by concept and question type
- edit metadata
- choose representative examples

### Mistake Classification Tool

Needed to:

- label mistakes by cause
- support better diagnosis and review targeting

### Content QA Tool

Needed to:

- verify parsing quality
- inspect generated summaries and explanations
- correct bad mappings

### Assessment Builder

Needed to:

- assemble quizzes and drill sets
- mix concepts and question types
- create timed sets when needed

## History-Specific Priority Tools

The highest-value tools for the first History version are:

- knowledge tree
- timeline builder or timeline review tool
- event summary cards
- comparison generator
- targeted practice generator
- mistake notebook
- review scheduler

These tools directly support structure, recall, and exam performance in History.

## MVP Modules

The first usable version should include:

- content upload
- parsing and normalization
- knowledge tagging
- knowledge tree management
- student dashboard
- lesson viewer
- targeted practice
- mistake notebook
- daily review queue
- weak-point diagnosis engine
- mastery tracking
- basic content admin tooling

These modules are enough to validate the core loop:

1. upload content
2. tag it into the knowledge structure
3. identify weak points
4. assign targeted practice
5. store mistakes
6. schedule review
7. update mastery
8. repeat

## Later-Phase Modules

The following should be delayed until the MVP works with real use:

- public deployment support beyond the basic architecture
- richer analytics
- advanced recommendation logic
- teacher or tutor features
- real-time capabilities
- broader family or classroom collaboration features

## Module Dependencies

Some modules only make sense after their prerequisites exist.

Key dependency rules:

- knowledge tree management must exist before tagging is reliable
- tagging must exist before personalization is meaningful
- content parsing must exist before lesson and question assets can scale
- mistake tracking must exist before review targeting becomes effective
- mastery tracking must exist before recommendations become useful

## Recommended Build Order

### Stage 1: Content Structure Foundation

- knowledge tree
- content upload
- parsing and normalization
- basic question/content management

### Stage 2: Student Learning Flow

- dashboard
- lesson viewer
- targeted practice

### Stage 3: Review and Diagnosis

- mistake notebook
- daily review queue
- weak-point diagnosis
- mastery tracking

### Stage 4: Refinement and Expansion

- timed drills
- stronger analytics
- better admin tools
- stronger recommendations

## Technical Workstreams

### Frontend

- student-facing pages
- parent/admin views
- content review interfaces

### Backend

- authentication
- content APIs
- question and lesson APIs
- review and mastery services

### AI and Content Processing

- parsing pipeline
- tagging pipeline
- summary and explanation generation
- content quality support

### Data Model

- students
- users and roles
- History nodes and concepts
- questions and lessons
- attempts and mistakes
- review tasks
- mastery state

### Operational Tooling

- content QA workflow
- taxonomy maintenance
- question bank maintenance

## Risks and Complexity Notes

- OCR or parsing quality may be inconsistent for real materials
- History taxonomy may drift if it is not maintained carefully
- AI-generated content may be plausible but inaccurate
- it is easy to overbuild before the core loop is validated

These risks support the decision to keep the MVP small and reviewable.

## Summary

The system should be built around a focused set of tools and modules that support the History learning loop directly. The MVP should prioritize content structure, targeted student learning, mistake reuse, review scheduling, and basic personalization before broader product expansion.
