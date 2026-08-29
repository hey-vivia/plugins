---
name: manage
description: >
  Entry point for the Vivia manage subagent. Use only when the user types
  /vivia:manage directly. For a natural-language manage request, such as a
  strategic review, graph health audit, rebalancing, deep planning, or
  housekeeping, the /vivia skill or the assistant dispatches the manage agent
  through the Task tool. Do not invoke this skill for that path.
---

Dispatch the `manage` subagent via the Task tool with `subagent_type: "manage"`. Pass the user's full request as the prompt. The canonical workflow lives in the agent definition; do not duplicate it here.
