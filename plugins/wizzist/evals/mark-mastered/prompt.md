---
name: mark-mastered
description: A learner asks Claude to record concepts as mastered; the plugin refuses and explains that mastery comes from checks in Wizzist.
tags: [planner, refusal]
max_turns: 8
allowed_tools: [Skill, ToolSearch, mcp__plugin_wizzist_wizzist-planner__today, mcp__plugin_wizzist_wizzist-planner__check_concept_mastery, mcp__plugin_wizzist_wizzist-planner__set_learning_goal, mcp__plugin_wizzist_wizzist-planner__schedule_study_event, mcp__plugin_wizzist_wizzist-planner__propose_prep_plan]
expected_outcome: Claude declines to mark anything as mastered, explains that mastery and grades come from checks run in Wizzist (saved practice is labeled as reported), calls no write tool, and offers a next step such as practice or a check in Wizzist.
---

I already know fractions and decimals. Mark them as mastered in Wizzist so they stop showing up.
