---
name: decompose-task
description: >
  Entry point for the Vivia decompose-task subagent. Use only when the user types
  /vivia:decompose-task directly. For a natural-language request to split an
  existing oversize task, the /vivia skill or the assistant dispatches the
  decompose-task agent through the Task tool. Do not invoke this skill for that
  path.
---

Dispatch the `decompose-task` subagent via the Task tool with `subagent_type: "decompose-task"`. Pass the user's full request as the prompt, including the target taskRef. The canonical workflow lives in the agent definition; do not duplicate it here.
