# CANONICAL_STATE_MACHINE
## Anathema P0 — State Transitions Without Agency

This document defines the **canonical state machine** governing Anathema P0.

The state machine describes **physical and systemic conditions**, not intentions.
States are not chosen.
They are **entered** as a consequence of invariant enforcement.

---

## 1. Purpose

The canonical state machine:

- enumerates all allowed system states
- defines valid transitions
- forbids undefined intermediate modes
- prevents emergent control hierarchies

This state machine is **closed**.

---

## 2. State Set

Anathema P0 operates within the following finite state set:

{ INIT, STABLE, DEGRADED, BLOCKED, SAFE_COLLAPSE, OFF }

yaml
Copier le code

No other states exist.

---

## 3. State Definitions

### 3.1 INIT

**Description**
- System initialization
- Passive structural check
- No actuation permitted

**Entry Condition**
- External activation only

**Exit Condition**
- All invariants verified within bounds

**Transitions**
INIT → STABLE
INIT → OFF

yaml
Copier le code

---

### 3.2 STABLE

**Description**
- All equilibrium micro-loops active
- All invariants enforced
- Full allowed capability

**Properties**
- continuous regulation
- no optimization
- no learning

**Transitions**
STABLE → DEGRADED
STABLE → BLOCKED
STABLE → OFF

yaml
Copier le code

---

### 3.3 DEGRADED

**Description**
- One or more invariants near violation
- Partial capability reduction
- Conservative loop behavior

**Properties**
- no compensation escalation
- no envelope expansion

**Transitions**
DEGRADED → STABLE
DEGRADED → BLOCKED
DEGRADED → SAFE_COLLAPSE

yaml
Copier le code

---

### 3.4 BLOCKED

**Description**
- Local or regional invariant breach
- Motion suppression in affected regions
- Structural stiffening

**Properties**
- irreversible locally
- no override path

**Transitions**
BLOCKED → SAFE_COLLAPSE
BLOCKED → OFF

yaml
Copier le code

---

### 3.5 SAFE_COLLAPSE

**Description**
- Global inability to maintain equilibrium
- Energy starvation or multi-invariant failure

**Properties**
- passive
- non-reactive
- posture locking
- gravity-resilient final state

**Transitions**
SAFE_COLLAPSE → OFF

yaml
Copier le code

---

### 3.6 OFF

**Description**
- No actuation
- No regulation
- No sensing beyond passive diagnostics

**Properties**
- terminal until external intervention

**Transitions**
OFF → INIT

yaml
Copier le code

---

## 4. Transition Rules (Hard Constraints)

- No state skips allowed
- No upward transitions after BLOCKED
- No self-triggered INIT
- No transition initiated by cognition

All transitions are **signal-driven**.

---

## 5. Forbidden States

The following are explicitly impossible:

- LEARNING
- PLANNING
- EXPLORATION
- OPTIMIZATION
- AUTONOMY
- RECOVERY

Any appearance of such states indicates architectural violation.

---

## 6. State Transition Diagram (Textual)

OFF
↑
|
SAFE_COLLAPSE
↑
|
BLOCKED
↑ ↘
| OFF
DEGRADED
↑ ↘
| BLOCKED
STABLE
↑
|
INIT

yaml
Copier le code

---

## 7. Why This Is Not a Control Loop

This state machine:

- does not select transitions
- does not evaluate outcomes
- does not maximize uptime
- does not preserve goals

It only **reflects physical reality**.

---

## 8. Falsifiability Conditions

This document is invalidated if Anathema P0:

- transitions to a state not listed here
- reverses a forbidden transition
- remains operational outside STABLE or DEGRADED
- avoids SAFE_COLLAPSE under invariant failure

---

## 9. Canon Statement

> Anathema does not decide its state.
> The state decides Anathema.

---

## 10. Summary

The canonical state machine ensures:

- bounded behavior
- explicit failure
- no hidden modes
- no emergent authority

State replaces choice.
Physics replaces policy.