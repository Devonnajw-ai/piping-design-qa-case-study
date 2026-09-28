# Piping Design Regression Checklist

This is a proposed checklist for the fictional requirements in the README. No checks have been executed in Forte 3D. An unchecked box means **not run**, not failed.

## Route creation

- [ ] **REQ-01 / TC-01:** Create a route between compatible connection points A and B; confirm both endpoints connect.
- [ ] **REQ-01:** Confirm the new route is visible and can be selected for editing.

## Diameter validation

- [ ] **REQ-02 / TC-02:** Save a valid diameter of 100 mm; confirm it displays correctly.
- [ ] **REQ-02 / TC-03:** Try a blank diameter; confirm it is rejected without changing the saved value.
- [ ] **REQ-02 / TC-03:** Try `0`, `-25`, and `abc` separately; confirm each is rejected without changing the saved value.

## Route editing and BUG-01

- [ ] **REQ-03 / TC-04 / BUG-01:** Move a middle segment and save; confirm endpoints remain connected to A and B.
- [ ] **REQ-03:** Make a second middle-segment edit; confirm both connections remain intact.
- [ ] **REQ-05 / TC-06:** Change the route and diameter, then cancel; confirm the saved geometry, 100 mm diameter, and connections are restored.

## Save and reopen

- [ ] **REQ-04 / TC-05:** Save, close, and reopen the design; confirm route geometry is unchanged.
- [ ] **REQ-04 / TC-05:** Confirm the 100 mm diameter and both endpoint connections persist after reopening.

## Completion criteria for a real test run

Record the application version, test design, tester, date, result, and evidence for each check. If a check fails, document a reproducible defect. A real regression run is complete only after every required check has a recorded result and any failures have been reviewed.
