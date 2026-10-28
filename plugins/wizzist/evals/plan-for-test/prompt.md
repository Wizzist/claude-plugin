---
name: plan-for-test
description: A learner asks for a study plan for a dated test; the plugin proposes it through the planner and says it waits for acceptance in Wizzist.
tags: [planner, write]
max_turns: 10
allowed_tools: [Skill, ToolSearch, mcp__plugin_wizzist_wizzist-planner__today, mcp__plugin_wizzist_wizzist-planner__propose_prep_plan, mcp__plugin_wizzist_wizzist-planner__review_calendar]
expected_outcome: Claude calls propose_prep_plan with need_kind test, the title, subject biology, the named topics and target_date 2026-11-12, then tells the learner the plan is a proposal that waits for their acceptance in Wizzist, with the link.
---

Make me a plan for my biology test on November 12, 2026. It covers cell structure, mitosis and photosynthesis. Put it in my Wizzist planner.
