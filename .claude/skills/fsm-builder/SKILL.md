---
name: fsm-builder
description: Use this skill to scaffold Finite State Machine (FSM) patterns for multi-step conversations (like wizards or forms).
tools: ["Bash", "Write", "Edit"]
---
## FSM Pattern Protocol
When tasked with building an FSM flow:
1. Identify the steps/states needed (e.g., `awaiting_name`, `awaiting_email`).
2. Scaffold the State definitions in the appropriate routing file.
3. Write the entry handler (to start the FSM).
4. Write handlers for each state, ensuring to:
   - Process input
   - Transition to the next state (or cancel)
   - Prompt the user for the next input
5. Implement a `/cancel` or generic cancellation mechanism to exit the FSM gracefully.
6. Remember to clear the state data upon completion.