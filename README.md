# Pugi for Claude Code

This folder is a standalone marketplace root and the `pugi` plugin root. Copy its **contents**, including dotfiles, to the approved public distribution repository; do not publish this private monorepo. The marketplace entry `source: "./"` resolves within this folder. No public repository URL is asserted here.

Local validation and installation from the monorepo root:

```sh
claude plugin validate ./integrations/claude-code
claude plugin marketplace add ./integrations/claude-code
claude plugin install pugi@pugi
```

Restart Claude Code if needed, then open `/mcp` and authenticate Pugi through OAuth. No token belongs in the manifests. The remote transport is Streamable HTTP. Use `/pugi:security-check`, `/pugi:make-logo`, or `/pugi:build-website`.

The three skills use the connected Pugi tools and live availability; the website skill currently reports unavailable rather than starting a build. See [live evidence](../evidence/README.md). Paid calls use existing account credit; confirm the budget before spending. Publishing requires a separate user request after preview review. This plugin does not promise a pentest, private repository scanning, or a brand kit.

Before release: validate with the current Claude CLI, test OAuth and each available tool in Claude, and publish only the isolated folder. Adding a marketplace locally does not submit it to Anthropic. Official formats: [manifest](https://code.claude.com/docs/en/plugins-reference), [marketplace](https://code.claude.com/docs/en/plugin-marketplaces), [directory submission](https://claude.com/docs/plugins/submit).
