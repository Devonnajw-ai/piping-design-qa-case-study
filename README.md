# Piping Design QA Case Study

An independent QA portfolio project inspired by piping workflows in 3D engineering software, created for my preparation for Octave’s Software Consultant, QA role (req 3046).

## Project Context

I do not have access to Forte 3D. This case study uses fictional requirements and simulated scenarios; it does not document verified Forte 3D features or defects and is not affiliated with Octave.

## Objective

Demonstrate how I translate requirements into test cases, document a defect, and select regression checks for a piping design workflow.

## Workflow Under Test

A user creates a pipe route between two equipment connection points, assigns a pipe diameter, edits the route, and saves the design.

## Proposed Requirements

These requirements are defined for this exercise:

- REQ-01: A user can connect two compatible equipment connection points with a pipe route.
- REQ-02: Pipe diameter must be a positive numeric value in millimeters. Blank, zero, negative, and nonnumeric values are rejected.
- REQ-03: Editing a route preserves its endpoint connections unless the user explicitly disconnects them.
- REQ-04: Saving and reopening a design preserves the route geometry, diameter, and connections.
- REQ-05: Canceling an edit restores the route to its state before the edit began.

## Planned QA Deliverables

- Test cases linked to the proposed requirements
- A simulated bug report with reproduction steps and expected versus actual behavior
- A regression checklist covering the affected workflow

## Testing Approach

Use positive, negative, boundary-value, and state-transition scenarios. Prioritize connection integrity, input validation, and saved-data accuracy.

Test cases will remain marked “Not Run” unless executed against a working test application. Any illustrative defect will be clearly labeled as simulated.

## Author

Devonna Williams
