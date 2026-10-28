# Wizzist for Claude Code

Personalized study plans and a lasting learning record for a Wizzist student
account, inside Claude Code. This repository is the published marketplace for
the Wizzist plugin; it is built from the Wizzist source repository and is not
edited by hand.

## Install

```
/plugin install wizzist --marketplace wizzist/claude-plugin
```

Then open `/plugin`, choose Wizzist, then Configure options, and enter a
planner key created in Wizzist Settings under AI assistants. Claude Code
stores the key; it is never typed in chat.

## Update

Marketplace plugins do not update themselves:

```
claude plugin update wizzist@wizzist
```

## Contents

- `plugins/wizzist`: the plugin, version 0.2.1. Its README explains what
  it can and cannot do.
- `.claude-plugin/marketplace.json`: the marketplace manifest.
- `SHA256SUMS`: SHA-256 digests of every published file.

Privacy: https://wizzist.com/privacy. Status and documentation:
https://wizzist.com/claude.

## License

MIT. See `LICENSE`.
