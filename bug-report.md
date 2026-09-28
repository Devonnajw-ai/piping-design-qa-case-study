# Simulated Bug Report: Route endpoint disconnects after editing a middle segment

> Portfolio scenario only. This defect was invented to demonstrate bug reporting. I have not tested Forte 3D or observed this behavior in Octave software.

**Bug ID:** BUG-01  
**Related requirement:** REQ-03  
**Related test case:** TC-04  
**Suggested severity:** Major — a route may no longer connect to its intended equipment.  
**Suggested priority:** High  
**Execution status:** Hypothetical; not reproduced in a real application.

## Scenario setup

A saved pipe route connects compatible equipment points A and B. Both endpoints are connected before the edit.

## Steps to reproduce in the fictional scenario

1. Open the saved design.
2. Select the route and enter edit mode.
3. Move a middle segment without selecting either endpoint.
4. Save the edit.
5. Inspect the connections at A and B.

## Expected result

The middle segment moves, and the route remains connected to both A and B, as specified by REQ-03.

## Simulated actual result

The route's B endpoint appears disconnected after saving, even though the user did not disconnect it.

## Impact

A user could mistake the edited route for a complete connection. The disconnected endpoint could also affect later design review or downstream work.

## Evidence and limitations

No screenshot, log, application build, or reproduction rate is available because this is a simulated defect. In a real test, I would record the software version, design file, before-and-after screenshots, and whether the issue reproduces consistently.

## Suggested regression checks

- Repeat TC-04 to confirm both endpoints stay connected after editing.
- Run TC-05 to verify the connections remain intact after saving and reopening.
- Run TC-06 to verify canceling an edit restores the original route.
