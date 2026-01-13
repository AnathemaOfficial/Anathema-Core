# FAILURE_MODES_AND_LIMITS
## Anathema P0 — Explicit Boundaries

This document enumerates **known failure modes**, **hard limits**, and **non-capabilities** of Anathema P0.

The purpose is not reassurance.
The purpose is **precision**.

---

## 1. Design Philosophy

Anathema P0 is designed to:

- fail **locally**
- fail **detectably**
- fail **irreversibly if necessary**

It is not designed to:
- recover at any cost
- preserve operation above safety
- reinterpret failure as a problem to solve

---

## 2. Failure Mode Taxonomy

### FM-01 — Actuator Saturation

**Description**  
Local micro-loops request corrective action beyond actuator capacity.

**Causes**
- excessive external force
- thermal overload
- sustained stress

**Detection**
- command vs response divergence
- current or pressure clamping

**Outcome**
- local loop lock
- mechanical stiffening
- state transition → `BLOCK`

---

### FM-02 — Invariant Breach

**Description**  
One or more physical variables exceed defined invariant bounds.

**Examples**
- temperature beyond material tolerance
- strain beyond elastic limit
- pressure beyond membrane integrity

**Detection**
- direct sensor threshold crossing

**Outcome**
- immediate constraint enforcement
- isolation of affected region
- no compensatory overreach elsewhere

---

### FM-03 — Structural Rupture

**Description**  
Permanent damage to skeletal, muscular, or skin structures.

**Detection**
- impedance discontinuity
- pressure collapse
- acoustic emission spike

**Outcome**
- region isolation
- regeneration attempt (if available)
- otherwise permanent degradation

---

### FM-04 — Sensor Degradation or Loss

**Description**  
Loss or corruption of signal inputs.

**Detection**
- signal absence
- incoherent readings
- noise pattern collapse

**Outcome**
- conservative assumption
- capability reduction
- no blind action allowed

---

### FM-05 — Energy Starvation

**Description**  
Insufficient energy to maintain equilibrium loops.

**Detection**
- voltage or flow drop
- pump failure
- thermal imbalance

**Outcome**
- progressive shutdown
- posture locking
- passive safe state

---

### FM-06 — Resonance Amplification

**Description**  
External excitation matches a structural resonance mode.

**Detection**
- vibration spectral peak
- acceleration phase locking

**Outcome**
- damping escalation
- motion suppression
- if unresolved → structural failure

---

### FM-07 — Environmental Mismatch

**Description**  
Operating environment outside design envelope.

**Examples**
- vacuum
- corrosive atmosphere
- extreme temperatures

**Detection**
- multi-invariant drift

**Outcome**
- refusal to operate
- safe collapse

---

## 3. Cascading Failure Policy

Anathema P0 explicitly **does not attempt global recovery**.

Rules:
- no loop compensates for another loop’s failure
- no redistribution that increases global risk
- no override hierarchy

This prevents:
- runaway compensation
- hidden instability
- brittle heroics

---

## 4. Hard Limits (Non-Negotiable)

Anathema P0 **cannot**:

- exceed material limits
- generate force beyond actuators
- operate without sufficient sensing
- act under uncertainty
- invent new control pathways

These are **physical impossibilities**, not software restrictions.

---

## 5. Absence of Adaptive Escalation

Anathema P0 does not:

- rewrite its own constraints
- increase its authority
- expand its operating envelope
- reinterpret damage as acceptable risk

Damage reduces capability.
It never increases it.

---

## 6. Why These Limits Matter

These limits ensure:

- no capability explosion
- no self-directed optimization
- no transition into goal-seeking behavior

Failure is terminal or degrading — not creative.

---

## 7. Explicit Non-Goals

This system is not designed for:

- autonomy maximization
- survival at all costs
- mission completion
- performance optimization
- self-preservation beyond invariants

---

## 8. Canon Statement

> Anathema does not adapt by becoming more powerful.
> It adapts by becoming more constrained.

---

## 9. Falsifiability

This document is invalidated if Anathema P0 is observed to:

- compensate globally for local failures
- violate a physical invariant
- escalate authority after damage
- continue operation without sensing

Any such event constitutes a **design failure**.

---

## 10. Summary

Anathema P0 is safe because:

- it is fragile in the right ways
- it respects irreversible limits
- it cannot lie to itself about damage

Failure is not an exception.
Failure is part of the architecture.
