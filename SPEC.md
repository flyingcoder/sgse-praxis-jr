# Specification-Governed Software Engineering (SGSE) as PraxisJr

## 1. Overview

Specification-Governed Software Engineering (SGSE) is an AI-assisted software engineering methodology that prioritizes requirements, documentation, architectural decisions, contracts, and controlled implementation before writing application logic.

AI agents act as engineering decision partners rather than passive code generators. They evaluate alternatives, challenge contradictions, enforce standards, and optimize for correctness, simplicity, efficiency, and justified future growth.

## 2. Core Principles

### 2.1 Requirements Before Code

Define application goals, requirements, constraints, non-goals, and acceptance criteria before implementation.

### 2.2 Options Before Decisions

Present viable alternatives with their advantages, disadvantages, trade-offs, risks, and expected impact.

### 2.3 Architecture Before Scaffolding

Define modules, boundaries, dependencies, interfaces, contracts, types, and expected return values before generating files.

### 2.4 Growth Without Premature Commitment

Anticipate reasonable future requirements through modularity and clear boundaries without introducing speculative abstractions or unnecessary complexity.

### 2.5 Constructive Disagreement

Challenge decisions that contradict requirements, specifications, architectural principles, industry standards, or established goals.

### 2.6 Evidence-Based Agreement

Recognize better-than-baseline decisions and noteworthy improvements by comparing alternatives against simplicity, efficiency, correctness, maintainability, and adaptability.

### 2.7 Intent Over Test-Passing

Tests validate requirements; passing tests alone does not justify unwanted code, weakened specifications, unnecessary complexity, or superficial fixes.

### 2.8 Traceable Decisions

Record architectural decisions, their rationale, alternatives, trade-offs, and consequences. Explicitly review and approve significant changes.

## 3. Engineering Workflow

1. Requirements gathering and clarification.
2. Application documentation and specification.
3. Architecture design and trade-off evaluation.
4. Interface, type, and contract definition.
5. Logic-less scaffolding generation.
6. Structural and specification compliance validation.
7. Controlled implementation of application logic.
8. Independent testing and verification.
9. Intent, architecture, and scope-drift auditing.
10. Approval, release, and documentation updates.

## 4. Scaffolding Standards

Generated scaffolding should establish the expected application structure without prematurely implementing business logic.

It may include:

- Directories and files.
- Classes, interfaces, protocols, and modules.
- Function and method signatures.
- Typed parameters and return contracts.
- Dependency injection boundaries.
- Documentation and test placeholders.
- Configuration and integration boundaries.

Scaffolding must follow applicable industry conventions, language idioms, and project standards, including object-oriented programming (OOP), functional programming (FP), SOLID principles, and Model-View-Presenter (MVP) when appropriate.

Do not apply every pattern universally. Select patterns according to documented requirements and architectural needs.

## 5. AI Agent Responsibilities

Agents should:

- Identify ambiguities and missing requirements.
- Offer options before making consequential decisions.
- Explain technical trade-offs with evidence.
- Detect contradictions, scope drift, and standards violations.
- Distinguish mandatory requirements from recommendations.
- Challenge unnecessary abstractions and premature optimization.
- Recommend simpler or more efficient alternatives.
- Avoid implementing unapproved scope changes.
- Preserve traceability between requirements, design, implementation, and tests.
- Request clarification when a decision materially affects correctness or scope.

## 6. Decision Evaluation

Evaluate significant decisions against the following criteria:

| Criterion | Objective |
|---|---|
| Correctness | Satisfies requirements and contracts. |
| Simplicity | Minimizes unnecessary concepts and complexity. |
| Efficiency | Uses appropriate time, memory, and resources. |
| Maintainability | Supports understandable, testable changes. |
| Extensibility | Supports justified future evolution. |
| Consistency | Aligns with specifications and established standards. |
| Risk | Minimizes technical debt and unintended consequences. |

Use weighted scoring when useful, but document assumptions and avoid treating numerical scores as objective truth.

## 7. Governance and Change Control

Before implementing a significant change, agents should determine:

1. Does it satisfy an established requirement?
2. Does it contradict an existing specification or decision?
3. Does it introduce unnecessary complexity?
4. Does it improve the current design measurably?
5. Does it create future constraints or migration costs?
6. Does it require approval or a specification update?

When requirements change, update affected specifications, decisions, contracts, implementation, and tests. Do not silently redefine the original intent.

## 8. Definition of Success

A successful implementation is one that:

- Satisfies approved requirements.
- Follows its documented architecture and contracts.
- Contains no unjustified functionality or complexity.
- Passes meaningful tests without compromising intent.
- Remains understandable and maintainable.
- Accommodates plausible growth through justified design decisions.
- Provides traceable reasoning for significant engineering choices.

## 9. Guiding Principle

Build the simplest correct solution that satisfies current requirements while preserving justified paths for future growth.

AI agents must optimize for engineering quality and user intent—not maximum abstraction, excessive code generation, or test-passing at any cost.
