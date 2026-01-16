# Backend Javadoc Standards

This document defines the **Javadoc standards** for the **Fundamentalis backend**.  
Its purpose is to ensure consistent, meaningful, and maintainable documentation across the codebase.

---

## Objectives

Javadoc in Fundamentalis is used to:

- Communicate intent and business meaning
- Clarify public contracts and boundaries
- Support long-term maintainability
- Avoid implicit or tribal knowledge

Javadoc is **not** used to restate obvious code.

---

## General Rules

- All Javadoc must be written in **English**
- Use clear, precise language
- Prefer **what** and **why** over **how**
- Keep documentation up to date with code changes
- Avoid redundant or obvious statements

---

## What Must Be Documented

### Required

Javadoc is **mandatory** for:

- Public classes
- Public interfaces
- Public methods
- Application ports (inbound and outbound)
- Domain services
- Configuration classes that expose behavior

---

### Optional

Javadoc is **optional** for:

- Private methods
- Internal helper classes
- Simple data holders with obvious intent

---

### Forbidden

Javadoc **must not** be added to:

- Test code (unless it clarifies non-obvious behavior)
- Trivial getters and setters

---

## Javadoc by Hexagonal Layer

### Core — Domain

**Purpose**
- Describe business concepts and rules
- Explain invariants and constraints

**Rules**
- Focus on business meaning
- No framework references
- No technical implementation details

**Example**
```java
/**
 * Represents a task within the Fundamentalis domain.
 * A task has a lifecycle and may transition through
 * well-defined states.
 */
public class Task {
    ...
}
```

### Core — Application (Ports & Use Cases)

#### Inbound Ports

Describe the use case from a business perspective.

Define expectations and side effects.

```java
/**
 * Use case for creating a new task.
 */
public interface CreateTaskUseCase {

    /**
     * Creates a new task for the given input.
     *
     * @param command input data required to create the task
     * @return the identifier of the created task
     */
    TaskId create(CreateTaskCommand command);
}
```

#### Outbound Ports

Describe what the application expects from external systems.

Do not reference specific technologies.

```java
/**
 * Persistence port for task aggregates.
 */
public interface TaskRepositoryPort {

    /**
     * Persists the given task.
     *
     * @param task task to persist
     */
    void save(Task task);
}
```

### Adapters — Inbound (Web)

**Purpose**

- Explain request handling behavior
- Document mapping and validation responsibilities

```java
/**
 * REST controller exposing task-related endpoints.
 */
@RestController
public class TaskController {
    ...
}
```

Method-level Javadoc should clarify:
- Side effects
- Validation rules
- Error behavior

### Adapters — Outbound (Persistence, Messaging, Security)

**Purpose**

- Explain adapter responsibilities
- Document mapping or translation logic

```java
/**
 * JPA-based persistence adapter for tasks.
 * Maps domain objects to persistence entities.
 */
@Component
public class TaskPersistenceAdapter implements TaskRepositoryPort {
    ...
}
```

## Method Documentation Rules

For public methods:

- Always include `@param` for each parameter
- Include `@return` when a value is returned
- Include `@throws` for checked exceptions or business exceptions

**Example**

```java
/**
 * Marks the given task as completed.
 *
 * @param taskId identifier of the task to complete
 * @throws TaskNotFoundException if the task does not exist
 */
void complete(TaskId taskId);
```

## Class-Level Documentation Rules

Class-level Javadoc should explain:

- Responsibility
- Role within the architecture
- Constraints or assumptions

Avoid listing methods or fields.

## Formatting Guidelines

- Use complete sentences
- Use third-person present tense
- Avoid HTML unless necessary
- Use paragraphs for clarity

## Anti-Patterns

**Avoid:**

```java
/** This class handles tasks. */
```

**Avoid:**

```java
/**
 * @param id the id
 * @return the result
 */
```

**Avoid:**

```java
/** TODO: document */
```

## Enforcement

These standards are enforced via:

- Code reviews
- Architectural reviews
- CI checks (where applicable)

Non-compliant documentation must be corrected before merge.

## Summary

- Javadoc documents contracts and intent
- Mandatory for public APIs and ports
- Aligned with Hexagonal Architecture
- Business-focused, not framework-focused

Consistent Javadoc is a core part of the Fundamentalis backend quality standard.