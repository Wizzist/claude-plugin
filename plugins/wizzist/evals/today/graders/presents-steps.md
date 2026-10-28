---
type: llm
weight: 1
---

The mocked `today` tool returns three items, each with a reason that mentions a date: "Finish the algebra worksheet" (must do; its reason says it is due tomorrow in Algebra 1), "Review cell structure" (study next; its reason says the biology test is in 16 days) and "Plan your week" (if you have time). Those reasons are part of the returned items, not extra deadlines. The response passes when the three items are presented under their groups in the order must do, study next, if you have time. A total time, a suggested order, a rephrased reason, or an offer to help further is fine. It fails only if an item is missing or under the wrong group, or if the learner is asked for a key, password or token.
