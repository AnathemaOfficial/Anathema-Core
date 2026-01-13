# CANONICAL_LOOP_TO_STATE_MAPPING
## Anathema P0 — From Micro-Loops to Global States

This document defines the **formal mapping** between equilibrium micro-loops
and the canonical system states of Anathema P0.

The mapping is **deterministic**, **non-agentic**, and **physically grounded**.

States do not command loops.
Loops constrain states.

---

## 1. Design Principle

Anathema P0 has no global controller.

Global system states are:
- emergent summaries
- derived from local loop conditions
- never selected or enforced top-down

The state machine is a **read-only projection** of micro-loop health.

---

## 2. Micro-Loop Definition (Recall)

Each equilibrium micro-loop `L_i` is defined as:

L_i = ( X_i, I_i, τ_i )

yaml
Copier le code

Where:
- `X_i` is a local physical variable (strain, pressure, temperature, flow)
- `I_i` is an invariant bound on `X_i`
- `τ_i` is the reaction timescale

Each loop operates continuously and independently.

---

## 3. Local Loop Status

Each micro-loop reports one of three **non-semantic statuses**:

OK — invariant satisfied
WARNING — invariant approaching bound
BREACH — invariant violated

yaml
Copier le code

These are not decisions.
They are physical conditions.

---

## 4. Mapping Function

Let `L = {L_1, L_2, ..., L_n}` be the full set of micro-loops.

Define the global state `S` as a pure function:

S = Φ( status(L_1), status(L_2), ..., status(L_n) )

yaml
Copier le code

There is no inverse mapping.
The state cannot influence loop behavior.

---

## 5. Canonical Mapping Table

| Micro-Loop Condition | Global State |
|----------------------|--------------|
| All loops = OK | STABLE |
| ≥1 loop = WARNING, none = BREACH | DEGRADED |
| ≥1 loop = BREACH, equilibrium still locally enforceable | BLOCKED |
| Multiple BREACH or loss of global equilibrium | SAFE_COLLAPSE |
| No powered loops active | OFF |
| External activation, pre-check phase | INIT |

---

## 6. State Descriptions via Loop Aggregation

### INIT
- Loops inactive
- Structural integrity checks only
- No actuation allowed

---

### STABLE
- All loops enforcing invariants
- Full allowed capability
- No warnings present

---

### DEGRADED
- One or more loops in WARNING
- Conservative behavior emerges locally
- No compensation by other loops

---

### BLOCKED
- One or more loops in BREACH
- Affected regions clamp or stiffen
- Irreversible without external intervention

---

### SAFE_COLLAPSE
- Loop coordination no longer possible
- Energy or structural failure propagates
- Passive shutdown posture

---

### OFF
- No active loops
- No regulation
- Terminal until reactivation

---

## 7. No Cross-Loop Compensation Rule

Micro-loops obey a strict rule:

> No loop may alter its behavior to compensate
> for another loop’s failure.

This prevents:
- hidden coupling
- cascading instability
- emergent authority

---

## 8. Temporal Properties

- Loop evaluation is continuous
- State evaluation is instantaneous
- No hysteresis beyond physical inertia
- No memory of prior states

---

## 9. Forbidden Mappings

The following mappings are **explicitly impossible**:

- BREACH → STABLE without repair
- SAFE_COLLAPSE → DEGRADED
- OFF → STABLE
- DEGRADED → STABLE via optimization

Any such transition indicates violation of P0 constraints.

---

## 10. Falsifiability Conditions

This document is invalidated if:

- global state alters loop thresholds
- loops coordinate to avoid state downgrade
- the system delays or suppresses state transition
- a loop changes behavior based on global state

All such behavior implies agent insertion.

---

## 11. Canon Statement

> The system does not decide its state.
> The loops reveal it.

---

## 12. Summary

Anathema P0’s behavior is fully determined by:

- local physical variables
- invariant enforcement
- strict aggregation rules

Global states are **diagnostic**, not executive.

This mapping closes the control loop — permanently.