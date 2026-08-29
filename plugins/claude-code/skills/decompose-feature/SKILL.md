---
name: decompose-feature
description: >
  Entry point for the Vivia decompose-feature subagent. Use only when the user
  types /vivia:decompose-feature directly. For a natural-language request to add
  a feature or capability cluster to an active project, the /vivia skill or the
  assistant dispatches the decompose-feature agent through the Task tool. Do not
  invoke this skill for that path.
---

Dispatch the `decompose-feature` subagent via the Task tool with `subagent_type: "decompose-feature"`. Pass the user's full request as the prompt, including the feature description and target project context. The canonical workflow lives in the agent definition; do not duplicate it here.
