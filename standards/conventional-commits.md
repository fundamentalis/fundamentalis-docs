# Conventional Commits

This document defines the **commit message standard** used on both **backend** and **frontend** repositories.

The goal is to ensure:
- Clear communication of intent
- Consistent and readable commit history
- Automated changelog and versioning support
- Easier code reviews and rollbacks

---

## Commit Message Format

All commit messages must follow this structure:

<type>(<scope>): <short summary>

[optional body]

[optional footer]



### Rules

- The subject line **must not exceed 72 characters**
- Use the **imperative mood** (e.g. “add”, not “added”)
- Do **not** end the subject line with a period
- Use lowercase for type and scope

---

## Commit Types

### `feat`
Introduces a new feature or functionality.

**Examples**
- `feat(auth): add user login flow`
- `feat(tasks): support task completion`

---

### `fix`
Fixes a bug.

**Examples**
- `fix(tasks): prevent duplicate task creation`
- `fix(auth): handle expired tokens correctly`

---

### `docs`
Documentation-only changes.

**Examples**
- `docs: add gitflow documentation`
- `docs(backend): clarify hexagonal architecture`

---

### `refactor`
Code changes that neither fix a bug nor add a feature.

**Examples**
- `refactor(tasks): extract validation logic`
- `refactor(frontend): simplify component structure`

---

### `chore`
Maintenance and non-functional changes.

**Examples**
- `chore: update dependencies`
- `chore(ci): adjust build pipeline`

---

### `test`
Adding or updating tests.

**Examples**
- `test(tasks): add unit tests for task service`
- `test(frontend): cover login component`

---

### `build`
Changes that affect the build system or dependencies.

**Examples**
- `build(backend): migrate to gradle`
- `build(frontend): update angular configuration`

---

### `ci`
Changes to CI/CD configuration.

**Examples**
- `ci: add commit linting`
- `ci: update pipeline for release branches`

---

## Scope

The **scope** is optional but strongly recommended.

### Backend Examples
- `feat(task): add create task use case`
- `fix(security): correct jwt validation`
- `refactor(domain): clean up task entity`

### Frontend Examples
- `feat(auth): add login page`
- `fix(ui): correct button alignment`
- `refactor(shared): simplify modal component`

---

## Squash Merges

All squash merge commit messages must also follow **Conventional Commits**.

The final squash commit message represents the **entire change set**, not individual commits.

---

## Enforcement

This standard is enforced via:
- Pull request reviews
- Commit linting in CI
- Rejection of non-conforming commits

Commits that do not follow this convention **must be amended** before merge.

---

## Forbidden Practices

- Generic messages (e.g. `update stuff`, `fix`)
- Multiple unrelated changes in one commit
- Large commits without clear scope
- Breaking changes without explicit notation

---

## Summary

- All commits must follow Conventional Commits
- Types and scopes communicate intent
- Breaking changes are explicit
- History remains readable

This convention ensures a clean, professional commit history across the Fundamentalis project.