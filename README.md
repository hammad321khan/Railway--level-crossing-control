# Railway Level-Crossing Control System

## Overview

This repository contains the Software Verification and Validation analysis of an Automated Railway Level-Crossing Control System (ARLCCS).

The system controls road traffic when a train approaches, passes through, or clears a railway crossing.

## Tasks

### Task 1 — Identify Constraints

12 safety and behavioral constraints were identified.

The constraints cover:

- Train presence
- Barrier operation
- Warning signals
- Train clearance
- Sensor failures
- Barrier failures
- Communication loss
- Emergency conditions
- Train detection
- Safe train passage

### Task 2 — Formalize Constraints

The constraints were converted into logical expressions using:

- AND (∧)
- OR (∨)
- NOT (¬)
- IMPLIES (→)

12 constraints were formalized.

### Task 3 — Identify Constraint Violations

12 realistic violation scenarios were created.

Each violation includes:

1. The violated constraint
2. System conditions
3. What went wrong
4. Explanation of why the constraint was violated

## Repository Structure

```text
Railway-Level-Crossing-Control/
│
├── README.md
│
├── Constraints/
│   └── Level_Crossing_Constraints.md
│
├── Formalization/
│   └── Formal_Constraints.md
│
└── Violations/
    └── Constraint_Violations.md
