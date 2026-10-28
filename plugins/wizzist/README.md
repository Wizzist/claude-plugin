# Wizzist for Claude

Personalized planning and a lasting learning record for a Wizzist student
account, inside Claude. Claude carries the conversation and does the
explaining. Wizzist supplies the authorized record: your classes and upcoming
tests, today's step, the material you selected, the practice you chose to save,
and the next step when you come back.

## Use it

**claude.ai and Claude Desktop.** Open Settings, then Connectors, then Add
custom connector. Enter `https://app.wizzist.com/api/v1/learning/mcp`, and
under Advanced settings enter the OAuth client ID `wizzist-claude` with no
secret. Connect and approve the Wizzist sign-in. Pilot accounts only for now.

**Claude Code.** Install the plugin:

```
/plugin install wizzist --marketplace wizzist/claude-plugin
```

Then open `/plugin`, choose Wizzist,
then Configure options, and enter a planner key created in Wizzist Settings
under AI assistants. Claude Code stores the key; it is never typed in chat.
Then ask Claude Code what you should do today: it calls your planner's
`today` tool. A key that can propose plans also lets Claude propose a study
plan for a test, which waits for you to accept it in Wizzist. The learning
connector in this plugin signs in from `/mcp` once Wizzist accepts Claude
Code's client metadata sign-in, which it does not yet.

A plan Claude proposes waits for you to accept it in Wizzist. Claude saves
only the practice you choose, from work you type or describe.

## Update

Marketplace plugins do not update themselves. To get a new version:

```bash
claude plugin update wizzist@wizzist
```

## What it cannot do

- Send photos of paper work. Capture those in your signed-in Wizzist account.
- Award mastery or grades. Saved practice is labeled as reported; checks run
  in Wizzist.
- Read your past Claude conversations.
- Buy, extend or renew a Wizzist account.

## Data

The plugin sends your tool requests to app.wizzist.com over your own
connection. It reads only the context your account permits and saves only the
practice you select. Disconnect at any time from Claude or from Wizzist
Settings; your saved work stays in your Wizzist account.

Privacy: https://wizzist.com/privacy

## Requirements

A Wizzist student account, 13 or older, with an active workspace. The
learning connector admits pilot accounts during the private pilot. See
https://wizzist.com/claude for current status.

## License

MIT. See `LICENSE`.
