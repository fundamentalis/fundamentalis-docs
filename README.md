# Fundamentalis Documentation

This repository contains the **official documentation** for the Fundamentalis project.  
It serves as the **single source of truth** for architectural decisions, domain knowledge, and development standards.

---

## Purpose

The purpose of this repository is to:

- Centralize architectural and domain documentation
- Record and justify technical decisions
- Define project-wide standards and conventions
- Align backend, frontend, and infrastructure development
- Reduce onboarding time and knowledge loss

This repository **does not contain application code**.

---

## Repository Structure

fundamentalis-docs/
├── domain/
├── standards/
└── diagrams/

---

## Domain

Located in `domain/`.

Defines the **business view** of Fundamentalis, including:

- Core domain concepts
- Bounded contexts
- Ubiquitous language
- Glossary

This documentation is **technology-agnostic** and should remain stable over time.

---

## Standards

Located in `standards/`.

Defines **mandatory project-wide conventions**:

- `gitflow.md`  
  Branching strategy and collaboration workflow

- `conventional-commits.md`  
  Commit message standard used across all repositories

- `backend-javadoc.md`  
  Javadoc rules for the backend (Java 21, Spring Boot, Hexagonal Architecture)

All Fundamentalis repositories **must comply** with these standards.

---

## Diagrams

Located in `diagrams/`.

Contains source files for architectural diagrams:
- PlantUML (preferred)
- Sequence diagrams
- C4 diagrams

Diagrams must be committed in **source format**, not only as rendered images.

---

## Related Repositories

- `fundamentalis-backend`
- `fundamentalis-frontend`
- `fundamentalis-api-contracts`
- `fundamentalis-infra`

---

## Guiding Principle

> If a decision affects more than one repository, it belongs here.

This repository is the long-term memory of the Fundamentalis project.