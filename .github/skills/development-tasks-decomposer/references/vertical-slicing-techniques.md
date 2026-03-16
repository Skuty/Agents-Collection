# Vertical Slicing Techniques (Development Phase)

Never split tasks by technical layers (e.g., UI vs. Database). Instead, find a single, complete action that a user can perform from start to finish. Use the following techniques to split synthesized requirements:

## 1. Vertical Slicing (Single User Action)
Slice by distinct actions a user can take.
- *Example:* Instead of "Build the shopping cart", split it into:
  - Subtask A: User can add a single item to the cart.
  - Subtask B: User can remove an item from the cart.

## 2. Splitting by Workflow Steps (Chronological)
If a process has multiple stages, make each stage its own task.
- *Example:* Instead of "Build the checkout", split it into: Subtask A (Summary screen), Subtask B (Address form), Subtask C (Payment integration).

## 3. Splitting by Happy Path and Edge Cases
Always build the simplest success scenario first. Leave exceptions for later.
- *Example:* Subtask A (Successful login), Subtask B (Wrong password error), Subtask C (Forgot password reset).

## 4. Splitting by Basic vs. Complex Rules
Start with a bare-bones implementation. Add complex business logic as separate, subsequent tasks.
- *Example:* Subtask A (Sum base price), Subtask B (Apply flat-rate shipping), Subtask C (Apply percentage discounts).
