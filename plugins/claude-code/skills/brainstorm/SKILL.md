---
name: brainstorm
description: >
  Entry point for the Vivia brainstorm subagent. Use only when the user types
  /vivia:brainstorm directly. For a natural-language brainstorm request, the
  /vivia skill or the assistant dispatches the brainstorm agent through the Task
  tool. Do not invoke this skill for that path.
---

Dispatch the `brainstorm` subagent via the Task tool with `subagent_type: "brainstorm"`. Pass the user's full request as the prompt. The canonical workflow lives in the agent definition; do not duplicate it here.
