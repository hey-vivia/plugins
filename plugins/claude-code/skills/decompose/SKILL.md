---
name: decompose
description: >
  Entry point for the Vivia decompose subagent. Use only when the user types
  /vivia:decompose directly. For a natural-language decompose request, the
  /vivia skill or the assistant dispatches the decompose agent through the Task
  tool. Do not invoke this skill for that path.
---

Dispatch the `decompose` subagent via the Task tool with `subagent_type: "decompose"`. Pass the user's full request as the prompt. The canonical workflow lives in the agent definition; do not duplicate it here.
