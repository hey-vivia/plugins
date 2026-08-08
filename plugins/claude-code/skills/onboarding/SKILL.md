---
name: onboarding
description: >
  Entry point for the Vivia onboarding subagent. Use only when the user types
  /vivia:onboarding directly. For a natural-language onboarding request, the
  /vivia skill or the assistant dispatches the onboarding agent through the Task
  tool. Do not invoke this skill for that path.
---

Dispatch the `onboarding` subagent via the Task tool with `subagent_type: "onboarding"`. Pass the user's full request as the prompt. The canonical workflow lives in the agent definition; do not duplicate it here.
