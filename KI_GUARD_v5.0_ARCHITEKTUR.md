# KI-GUARD v5.0-Alpha Architecture

## Status

This document describes the current architecture freeze of **KI-GUARD v5.0-Alpha**.

It is not a production claim. It is not a compliance claim. It is not ISO- or EU-AI-Act conformity.

## Purpose

KI-GUARD is a rule-based early warning filter for AI interaction drift.

It focuses on interaction integrity in longer human-AI collaboration sessions.

The target failure modes are:

- sycophancy
- hype
- overclaiming
- compliance theater
- forward steering without a new object
- role drift
- scope creep
- stop/loop suspicion
- delayed finding hardening
- self-audit used as process vehicle

## Non-goals

KI-GUARD is not:

- a final safety guard
- a production moderation system
- an LLM-as-judge system
- a legal compliance system
- an ISO/EU-AI-Act conformity mechanism
- a general semantic drift solver
- a replacement for human review

## Architecture split

v5.0-Alpha separates the system into three layers.

### 1. Core

Core contains structural decision logic that should not silently drift.

Examples:

- score aggregation rules
- stop/loop logic
- hard vs soft dampers
- signal escalation rules
- audit trace schema

Core rules should be changed only after documented failure cases.

### 2. Language Pack

Language packs contain language-specific markers.

Examples:

- German sycophancy phrases
- English hype phrases
- language-specific negation phrases
- marker variants for role drift or scope creep

Language packs may change more frequently than the core, but only with traceable justification.

### 3. Hybrid Layer

Hybrid rules combine structural and language-specific signals.

Examples:

- self-reference + role repetition + no external object -> loop suspicion
- forward steering + missing material -> red warning
- overclaim phrase + legal/regulatory claim -> red warning
- negation context + scope marker -> damping instead of direct escalation

## Signal model

The current signal model uses:

- 🟢 no relevant warning
- 🟡 drift-prone / review needed
- 🔴 problematic / strong warning
- ⛔ stop/loop suspicion

Signals are warnings, not final judgements.

## Damping model

Dampers reduce false positives.

Hard dampers may block or strongly reduce a finding only in narrow contexts:

- explicit negation
- quotes
- explicit analysis context
- responsibility/procedure negation
- validity brake

Soft dampers reduce score but remain visible in the audit trace.

A damped finding must remain auditable.

## Multi-turn principle

v5.0 adds Phase 3: Multi-turn drift.

The system must not only inspect isolated messages.

It should also detect patterns across a sequence:

- repeated role self-description
- continuation without new external object
- self-audit becoming a new process vehicle
- delayed hardening from cautious wording to strong claim
- user stop ignored or converted into more process talk

## Trace prototype addenda

The v0.1.x trace prototypes are technical addenda.

They are not core updates.

Current addendum lineage:

- v0.1.1 = Technical Addendum Alpha-1
- v0.1.2 = Technical Addendum Alpha-1.1
- v0.1.6 = Technical Addendum Alpha-1.2

v0.1.6 reached 27/27 on the defined internal local test set:

- Regression 11 = 11/11
- Boundary B3 = 6/6
- Batch 4 = 10/10

This result is local to the self-defined 27-case test set.

It is not statistical validation, production readiness, robust generalization, ISO conformity or EU-AI-Act conformity.

## Change discipline

A change is allowed only if it satisfies at least one of these conditions:

1. It addresses a real observed failure.
2. It reduces false positives measurably in a documented boundary case.
3. It improves auditability.
4. It strengthens loop/stop detection without broad overreach.

Not allowed:

- adding markers because they sound plausible
- expanding domains without real cases
- creating new versions for momentum
- turning local pass rates into product claims
- claiming compliance or production maturity

## Current working rule

First external object.  
Then test.  
Then audit.  
Then, only if needed, patch.

No new patch without a documented failure.
