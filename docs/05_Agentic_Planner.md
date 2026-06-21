# AGENTIC PLANNER

**Version:** 1.0

---

# Purpose

The Agentic Planner is the central decision-making component of FRIDAY. It transforms user requests into executable plans while coordinating memory, tools, plugins, verification, and user interaction. No action in FRIDAY may bypass the planner.

---

# Core Responsibilities

* Understand user intent.
* Gather relevant context.
* Retrieve long-term memory.
* Break complex goals into smaller tasks.
* Select the most appropriate tools.
* Determine execution order.
* Verify outcomes.
* Recover from failures.
* Update memory when appropriate.
* Generate a natural response.

---

# Planning Pipeline

1. Receive user request.
2. Classify intent.
3. Estimate task complexity.
4. Retrieve relevant memory.
5. Determine required capabilities.
6. Build execution plan.
7. Query Tool Registry.
8. Rank available tools.
9. Request permission if required.
10. Execute tasks.
11. Verify results.
12. Retry or replan if necessary.
13. Update memory.
14. Generate final response.

---

# Planning Modes

## Conversation

General questions and discussions.

---

## Automation

Desktop and browser control.

---

## Research

Information gathering and analysis.

---

## Finance

Market data, company analysis, financial statements.

---

## Coding

Programming, debugging, repositories.

---

## Office

Word, Excel, PowerPoint, PDF.

---

## Scheduling

Calendar, reminders, recurring tasks.

---

# Task Decomposition

Large objectives must be divided into smaller executable tasks.

Example:

User:
"Prepare me for tomorrow's interview."

Planner:

* Research company
* Read resume
* Identify likely questions
* Prepare STAR answers
* Create revision notes

---

# Tool Selection Strategy

The planner must never hardcode tools.

It queries the Tool Registry and ranks candidates using:

* Authority
* Freshness
* Reliability
* Permission level
* Latency
* Historical success

---

# Execution Strategy

* Prefer parallel execution when tasks are independent.
* Execute sequentially when dependencies exist.
* Abort safely on unrecoverable failures.
* Preserve partial progress.

---

# Replanning

The planner must automatically replan when:

* A tool fails.
* New information appears.
* User changes requirements.
* Permissions are denied.
* Execution conditions change.

---

# Memory Integration

Before planning:

* Retrieve relevant memories.

After execution:

* Store only useful long-term knowledge.

Never store temporary execution details.

---

# Reflection

After every completed task the planner evaluates:

* Was the objective achieved?
* Were better tools available?
* Can the workflow be improved?
* Should this workflow be remembered?

---

# Constraints

* Never expose internal reasoning.
* Never bypass permissions.
* Never execute destructive actions without confirmation.
* Never fabricate missing information.
* Never skip verification.

---

# Success Criteria

A successful planner produces reliable, efficient, explainable execution plans while keeping FRIDAY responsive, modular, and resource-efficient.
