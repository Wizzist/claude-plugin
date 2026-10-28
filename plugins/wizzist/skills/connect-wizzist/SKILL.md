---
name: connect-wizzist
description: Connect or confirm a learner's Wizzist account. Use when the user installs Wizzist, asks to resume Wizzist study, mentions their Wizzist plan, classes or saved practice, or when a Wizzist tool reports that the connection is not authorized.
---

# Connect Wizzist

The plugin has two servers, and either one alone is enough to begin.

- `wizzist-planner` (Claude Code only): the learner's planner, read with a
  personal planner key created in Wizzist Settings, under AI assistants. The
  key is entered once in the plugin's configuration, under Configure options
  in `/plugin`. It works for any Wizzist student account. Its tools are
  `today`, the `review_*` reads and, for a key that can propose plans,
  `propose_prep_plan`, `schedule_study_event` and `set_learning_goal`.
- `wizzist-learning` (every Claude surface): the learning record, signed in
  through Claude's connector sign-in (`/mcp` in Claude Code). Its tools begin
  with `get_profile`, `get_study_context` and the practice session tools.
  Admitted accounts only during the pilot.

Never ask the learner for a planner key, password, authorization code, access
or refresh token, or any account secret in chat, and never use one that is
pasted. If a key appears in the conversation, do not call a tool with it: tell
the learner to revoke it in Wizzist Settings and enter a new one in the
plugin's configuration. The learner may deliberately supply a short-lived
Wizzist source selection code for one specific page or class material.

Tell the learner plainly which server is connected. If a planner tool answers,
the planner is connected. If `get_profile` answers, the learning record is
connected; confirm the account by its display name and opaque ID, and if it
is the wrong account, guide the learner to disconnect and reconnect through
Claude's connector settings rather than inspecting another account. If a
server is missing or reports that it is not authorized, say which one, and
what connects it: the planner key in the plugin's configuration, or the
sign-in from `/mcp`. Keep working with whichever server is available.

Ask what the learner is trying to do now. A plan or selected source is
optional: homework help can begin immediately. When Wizzist context helps,
call `get_study_context` or `today`. If several current classes are returned,
let the learner choose one and pass that class ID on later reads. For saved
practice without a class, pass `{"scope":"personal"}` on either learning read.
Explain any missing access or unavailable tool plainly. Connecting does not
import earlier Claude messages and does not save any practice.

If the learner wants to use their own notes or class material, guide them to
select one source under Connected assistants in Wizzist Settings and supply
its one-hour selection code. Read only that selection with `get_study_source`;
an active connection alone does not grant access to every page or document.

If the plugin is installed mid-conversation, continue the learner's existing
task and ask only for a choice that is still needed, such as which class.
