# Railway Level-Crossing Control System

# Task 3 — Constraint Violations

## V1 — Barrier Opens While Train Is Present

### Constraint
C1: Train_Present → ¬Barrier_Open

### Violation
Train_Present = TRUE  
Barrier_Open = TRUE

### What Went Wrong?
The barrier is open even though a train is present at the crossing.

### Why Is the Constraint Violated?
C1 requires the barrier to remain closed whenever a train is present.

---

## V2 — Train Approaching but Barrier Is Open

### Constraint
C2: Train_Approaching → Barrier_Closed

### Violation
Train_Approaching = TRUE  
Barrier_Closed = FALSE

### What Went Wrong?
A train is approaching, but the barriers are not closed.

### Why Is the Constraint Violated?
C2 requires the barriers to be closed when a train is approaching.

---

## V3 — Train Approaching but Warning Is Inactive

### Constraint
C3: Train_Approaching → Warning_Active

### Violation
Train_Approaching = TRUE  
Warning_Active = FALSE

### What Went Wrong?
The train is approaching but warning lights and audible alarms are not active.

### Why Is the Constraint Violated?
C3 requires warning signals to be active whenever a train is approaching.

---

## V4 — Barrier Opens During Train Passage

### Constraint
C4: Train_Present → Barrier_Closed

### Violation
Train_Present = TRUE  
Barrier_Closed = FALSE

### What Went Wrong?
The barrier has opened while the train is still passing through the crossing.

### Why Is the Constraint Violated?
C4 requires barriers to remain closed while a train is present.

---

## V5 — Barrier Opens Before Train Clearance

### Constraint
C5: Barrier_Open → Train_Clear

### Violation
Barrier_Open = TRUE  
Train_Clear = FALSE
