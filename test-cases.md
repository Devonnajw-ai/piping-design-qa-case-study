# Piping Design Test Cases

These test cases use the fictional requirements in the README. They have not been executed in Forte 3D.

## TC-01 — Create a route between compatible connections

**Requirement:** REQ-01  
**Priority:** High  
**Precondition:** A design is open with two compatible equipment connection points, A and B.

**Steps:**
1. Start a new pipe route at connection A.
2. Select connection B as the endpoint.
3. Confirm the route.

**Expected result:** A pipe route appears between A and B, and both endpoints remain connected to their selected equipment.

**Execution status:** Not run — portfolio scenario.

## TC-02 — Accept a valid pipe diameter

**Requirement:** REQ-02  
**Priority:** High  
**Precondition:** A pipe route connects points A and B.

**Test data:** 100 mm

**Steps:**
1. Select the pipe route.
2. Enter `100` in the diameter field.
3. Save the change.

**Expected result:** The diameter is accepted and displayed as 100 mm. No validation error appears.

**Execution status:** Not run — portfolio scenario.

## TC-03 — Reject an invalid pipe diameter

**Requirement:** REQ-02  
**Priority:** High  
**Precondition:** A pipe route connects points A and B and has a saved diameter of 100 mm.

**Test data:** Blank, `0`, `-25`, and `abc` (try each separately).

**Steps:**
1. Select the pipe route.
2. Replace the diameter with one test value.
3. Attempt to save.
4. Repeat steps 2–3 for each remaining value.

**Expected result:** Each value is rejected with a clear validation message. The saved diameter remains 100 mm.

**Execution status:** Not run — portfolio scenario.

## TC-04 — Preserve connections when editing a route

**Requirement:** REQ-03  
**Priority:** High  
**Precondition:** A saved pipe route connects equipment points A and B.

**Steps:**
1. Select the route and enter edit mode.
2. Move a middle segment of the route without selecting either endpoint.
3. Save the edit.
4. Inspect both endpoints.

**Expected result:** The route geometry changes, while its endpoints remain connected to A and B.

**Execution status:** Not run — portfolio scenario.

## TC-05 — Preserve the route after reopening a design

**Requirement:** REQ-04  
**Priority:** High  
**Precondition:** A route connects points A and B, has an edited middle segment, and has a diameter of 100 mm.

**Steps:**
1. Save the design.
2. Close the design.
3. Reopen the saved design.
4. Inspect the route, its diameter, and both endpoints.

**Expected result:** The route has the same geometry and 100 mm diameter, and remains connected to A and B.

**Execution status:** Not run — portfolio scenario.

## TC-06 — Cancel a route edit

**Requirement:** REQ-05  
**Priority:** Medium  
**Precondition:** A saved route connects points A and B and has a diameter of 100 mm.

**Steps:**
1. Select the route and enter edit mode.
2. Move a middle segment and change the diameter to 150 mm.
3. Cancel the edit.
4. Inspect the route and diameter.

**Expected result:** The route returns to its saved geometry, the diameter remains 100 mm, and both endpoints remain connected.

**Execution status:** Not run — portfolio scenario.
