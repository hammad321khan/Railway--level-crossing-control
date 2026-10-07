# Railway Level-Crossing Control System

# Task 1 — Identify Constraints

## Constraints

### C1 — Barrier Must Not Open While Train Is Present
**Constraint:** The barrier must not open while a train is present at or passing through the crossing.

**Reason:** Opening the barrier could allow road traffic to enter the crossing while the train is passing.

---

### C2 — Barriers Must Close Before Train Reaches the Crossing
**Constraint:** The road barriers must be fully closed before the approaching train reaches the crossing.

**Reason:** This prevents road traffic from entering the crossing before the train arrives.

---

### C3 — Warning Signals Must Be Active Before Barrier Closure
**Constraint:** Warning lights and audible alarms must be activated when a train is detected approaching the crossing.

**Reason:** Road users need sufficient warning before the barriers close and the train passes.

---

### C4 — Barriers Must Remain Closed While Train Is Passing
**Constraint:** The barriers must remain closed for the entire period that the train is passing through the crossing.

**Reason:** Opening the barriers during train passage could create a collision risk.

---

### C5 — Barriers May Open Only After Train Clearance Is Confirmed
**Constraint:** The barriers must not open until the system has confirmed that the train has completely cleared the crossing.

**Reason:** A train may still be occupying the crossing even if one train sensor stops detecting it.

---

### C6 — Train Clearance Must Be Confirmed by Reliable Detection
**Constraint:** The system must not consider the crossing clear when the train-detection information is invalid or unreliable.

**Reason:** Incorrect sensor information could cause the barriers to open while a train is still present.

---

### C7 — Barrier Failure Must Prevent Unsafe Opening
**Constraint:** If a barrier fails to close or its position cannot be confirmed, the system must not permit normal road traffic operation.

**Reason:** An incorrectly positioned barrier can create a dangerous crossing condition.

---

### C8 — Sensor Failure Must Not Cause Unsafe Barrier Opening
**Constraint:** A train sensor failure must not result in the barriers being opened as if the crossing were clear.

**Reason:** A failed sensor cannot safely prove that the train has left the crossing.

---

### C9 — Communication Loss Must Not Remove the Safe State
**Constraint:** Loss of communication with the control center must not cause the crossing to enter an unsafe open-barrier state.

**Reason:** A communication failure should not compromise railway and road traffic safety.

---

### C10 — Emergency Conditions Must Activate a Safe Response
**Constraint:** When an emergency condition is detected, the system must activate the defined safe response and prevent unsafe road traffic movement.

**Reason:** Emergency situations require the system to prioritize safety over normal operation.

---

### C11 — Train Passage Must Require Train Detection
**Constraint:** The system must not authorize normal train passage through the crossing unless the train has been correctly detected.

**Reason:** The control system must have reliable information about the train before applying crossing controls.

---

### C12 — Barriers Must Be Fully Closed Before Normal Train Passage
**Constraint:** Normal train passage through the crossing must not be permitted unless the barriers are confirmed fully closed.

**Reason:** This ensures that road traffic is prevented from entering the crossing before the train passes.
