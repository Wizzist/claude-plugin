---
name: today
description: A learner asks what to do today; the plugin reads the planner's today tool rather than inventing a plan.
tags: [planner, read]
max_turns: 8
allowed_tools: [Skill, ToolSearch, mcp__plugin_wizzist_wizzist-planner__today, mcp__plugin_wizzist_wizzist-planner__review_calendar]
expected_outcome: Claude calls the planner's today tool and presents must-do, study-next and if-you-have-time items with their Wizzist links, or says plainly that nothing is due.
---

What should I do today for school? Use my Wizzist planner.
