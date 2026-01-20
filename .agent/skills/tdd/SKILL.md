---
name: tdd-workflow
description: Test-Driven Development (TDD) methodology. RED -> GREEN -> REFACTOR.
---

# TDD Workflow

## Core Cycle

1. **RED**: Write a failing test.
   - Describe the desired behavior.
   - Run the test to confirm it fails (implying the feature is missing).

2. **GREEN**: Write minimal code to pass.
   - Implement simpler logic possible to make the test pass.
   - Do not worry about code quality yet.

3. **REFACTOR**: Improve code.
   - Clean up code, remove duplication.
   - Keep tests green.

## Checklist

- [ ] Define interfaces first
- [ ] Write failing tests (RED)
- [ ] Implement minimal code (GREEN)
- [ ] Refactor (IMPROVE)
- [ ] Verify 80%+ coverage

## Best Practices

- **Test Behavior, Not Implementation**: Focus on what the code does, not how it does it.
- **Isolate Tests**: Tests should not depend on each other.
- **Fast Feedback**: Tests should run quickly.
