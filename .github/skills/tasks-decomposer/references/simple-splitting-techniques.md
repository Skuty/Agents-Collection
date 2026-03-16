# Simple Task Splitting Techniques (Divide and Conquer)

## 1. The Analysis-First Split (Requirements Gathering)
*Use this during Phase 1.*
When a feature is too large or vague, split the work into smaller **Business Analysis Subtasks** to gather requirements.
- **Identify the Core Action:** Determine the absolute simplest action the user can do and map the exact steps.
- **Map the Exceptions:** List what happens when the core action fails.
- **Define the Data:** List all the fields the user needs to provide to complete the action.

## 2. Vertical Slicing (Single User Action)
*Use this during Phase 2.*
Never split tasks by technical layers (e.g., UI vs. Database). Instead, find a single, complete action that a user can perform from start to finish.
- *Example:* Instead of "Build the shopping cart", split it into:
  - Subtask A: User can add a single item to the cart.
  - Subtask B: User can remove an item from the cart.

## 3. Splitting by Workflow Steps (Chronological)
*Use this during Phase 2.*
If a process has multiple stages, make each stage its own task.
- *Example:* Instead of "Build the checkout", split it into: Subtask A (Summary screen), Subtask B (Address form), Subtask C (Payment integration).

## 4. Splitting by Happy Path and Edge Cases
*Use this during Phase 2.*
Always build the simplest success scenario first. Leave exceptions for later.
- *Example:* Subtask A (Successful login), Subtask B (Wrong password error), Subtask C (Forgot password reset).

## 5. Splitting by Basic vs. Complex Rules
*Use this during Phase 2.*
Start with a bare-bones implementation. Add complex business logic as separate, subsequent tasks.
- *Example:* Subtask A (Sum base price), Subtask B (Apply flat-rate shipping), Subtask C (Apply percentage discounts).
