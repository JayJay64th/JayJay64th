## Methodology

**Manual, invariant-driven security auditing.**

**1. Scope & Threat Model**  
Establish the impact boundaries, identify trust assumptions and privileged actors, and define the invariants that must hold.

**2. Architecture & State Mapping**  
Trace entry points, authorization paths, cross-contract calls, and state transitions. Map who can change what, and under which conditions.

**3. Systematic Code Review**  
Review the codebase through three lenses:
- **Accounting:** Asset/share consistency, debt tracking, fee flows, and rounding.
- **Authorization:** Caller permissions, lifecycle checks, and inconsistencies across equivalent paths.
- **Trust boundaries:** External calls, oracles, user-controlled inputs, and transaction-level manipulation.

**4. Attack Enumeration**  
Challenge each relevant path with adversarial inputs, call sequences, transaction ordering, reentrancy, and boundary conditions. Trace the path from violated invariant to economic impact.

**5. Impact Validation**  
Require concrete evidence: a failing test, fork-based verification, or quantified execution analysis. Establish the attacker's cost, the victim's loss, and the conditions required for exploitation.

**6. Falsification & Variant Hunting**  
Reject hypotheses only when a specific safeguard or economic constraint explains why they fail. For confirmed issues, search equivalent functions and related code paths for variants before reporting.
