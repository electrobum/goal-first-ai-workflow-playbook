# Example: Regression Bugfix

This example shows the playbook applied to a software bugfix cycle:

- one primary worker owns the regression investigation;
- a start gate defines the scope and invalid shortcuts;
- the hard gate checks failing and passing tests, not just patch creation;
- the handoff note leaves an exact next reproduction step.

Use this example when the work is code-heavy and correctness depends on source-level validation.
