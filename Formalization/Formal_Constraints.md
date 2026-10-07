# Railway Level-Crossing Control System

# Task 2 — Formalize Constraints

## Logical Variables

The following variables are used:

- Train_Present = TRUE when a train is present at the crossing.
- Barrier_Open = TRUE when the barrier is open.
- Barrier_Closed = TRUE when the barrier is fully closed.
- Train_Approaching = TRUE when a train is approaching.
- Warning_Active = TRUE when warning lights and alarms are active.
- Train_Clear = TRUE when complete train clearance has been confirmed.
- Sensor_Valid = TRUE when train-detection sensors provide reliable information.
- Barrier_Fault = TRUE when a barrier failure is detected.
- Sensor_Fault = TRUE when a sensor failure is detected.
- Communication_Lost = TRUE when communication with the control center is lost.
- Emergency = TRUE when an emergency condition is detected.
- Safe_Response = TRUE when the defined emergency safe response is active.
- Train_Detected = TRUE when the train has been correctly detected.
- Normal_Train_Passage = TRUE when normal train passage is authorized.

---

## Formal Constraints

### C1 — Barrier Must Not Open While Train Is Present

**Formal Expression:**

Train_Present → ¬Barrier_Open

**Meaning:** If a train is present, the barrier must not be open.

---

### C2 — Barriers Must Close Before Train Reaches Crossing

**Formal Expression:**

Train_Approaching → Barrier_Closed

**Meaning:** When a train is approaching, the barriers must be closed before the train reaches the crossing.

---

### C3 — Warning Signals Must Be Active

**Formal Expression:**

Train_Approaching → Warning_Active

**Meaning:** If a train is approaching, warning signals must be active.

---

### C4 — Barriers Must Remain Closed While Train Is Passing

**Formal Expression:**

Train_Present → Barrier_Closed

**Meaning:** A train being present requires the barriers to remain closed.

---

### C5 — Barriers Open Only After Train Clearance

**Formal Expression:**

Barrier_Open → Train_Clear

**Meaning:** If the barrier is open, complete train clearance must already have been confirmed.

---

### C6 — Invalid Sensor Data Must Not Prove Clearance

**Formal Expression:**

¬Sensor_Valid → ¬Train_Clear

**Meaning:** If sensor information is invalid, the system cannot confirm that the train has cleared the crossing.

---

### C7 — Barrier Failure Must Prevent Normal Opening

**Formal Expression:**

Barrier_Fault → ¬Barrier_Open

**Meaning:** If a barrier fault exists, the system must not permit the barrier to be considered safely open for normal operation.

---

### C8 — Sensor Failure Must Not Allow Safe Opening

**Formal Expression:**

Sensor_Fault → ¬Barrier_Open

**Meaning:** If a train-detection sensor fails, the barrier must not be opened as part of normal safe operation.

---

### C9 — Communication Loss Must Not Cause Unsafe Opening

**Formal Expression:**

Communication_Lost → ¬Barrier_Open

**Meaning:** Loss of communication must not result in the barrier being opened.

---

### C10 — Emergency Must Activate Safe Response

**Formal Expression:**

Emergency → Safe_Response

**Meaning:** When an emergency is detected, the defined safe response must be activated.

---

### C11 — Train Passage Requires Detection

**Formal Expression:**

Normal_Train_Passage → Train_Detected

**Meaning:** Normal train passage can only be authorized when the train has been correctly detected.

---

### C12 — Train Passage Requires Closed Barriers

**Formal Expression:**

Normal_Train_Passage → Barrier_Closed

**Meaning:** Normal train passage can only be authorized when the barriers are confirmed fully closed.
