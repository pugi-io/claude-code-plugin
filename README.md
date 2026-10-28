# Pugi for Claude

Pugi builds, checks and publishes websites. This plugin connects Claude to your Pugi account and teaches it how to use it: describe a site in plain words and get a built website with a preview link, change it, put it live on its own address, check any public website or GitHub repository for security issues, make logo concepts for a name, and browse the Pugi catalogue of sites to start from.

## Install

In claude.ai or the Claude desktop app, add **Pugi** from the plugin directory and connect the Pugi connector on the plugin's **Connectors** tab. In Claude Code:

```sh
claude plugin marketplace add pugi-io/claude-code-plugin
claude plugin install pugi@pugi
```

The first tool call opens a Pugi sign-in page in your browser (OAuth). If you do not have a Pugi account yet, you can create one there. In Claude Code, `/mcp` shows the connection state. No API key or token is stored in the plugin.

## What it does

| Skill | What Claude does with it |
| --- | --- |
| `build-website` | Turns your brief into a built website with a preview link |
| `change-and-publish` | Edits a site Pugi built, publishes it on its public address, lists what is published |
| `security-check` | Grades a public website's HTTPS, headers, cookies and exposed keys; finds leaked secrets, vulnerable dependencies and risky code in a public GitHub repository |
| `make-logo` | Makes four logo concepts for a business name, usable in a site build |
| `start-from-template` | Searches the public Pugi catalogue for a site to start from |

In Claude Code the skills are also available as `/pugi:build-website`, `/pugi:change-and-publish`, `/pugi:security-check`, `/pugi:make-logo` and `/pugi:start-from-template`.

## Example prompts

- "Build a website for my yoga studio in Lisbon: home, schedule, prices, about, contact. Calm colours, English and Portuguese."
- "Is https://example.com secure? Check its headers and give me a grade."
- "Check github.com/acme/shop for leaked secrets and vulnerable dependencies."
- "Make a logo for 'Blue Fern Bakery', warm and hand-drawn, green and cream."
- "Show me restaurant sites in the Pugi catalogue I could start from."
- "Change the hero text to 'Open daily 8–20' and then publish the site."

## How a build works

Claude collects a brief and starts the build. A build card in the chat shows progress and the preview as the build runs; a site usually takes several minutes. You review the preview, ask for changes, and publishing happens only when you ask for it. Web apps are built in the Pugi console, not through this plugin.

## Pricing and billing

Website checks and catalogue search are free. Logos and repository checks have a free daily allowance, then cost prepaid credit. Website builds and edits are included on a Pugi plan; on a prepaid-credit account they are billed by actual cost and never above the limit you set. Current prices and allowances: https://pugi.io/pricing. No tool charges a card by itself: when credit is missing, Claude shows you a checkout link, and you decide.

## Data and privacy

The plugin itself stores nothing and runs no code on your machine. The tools send what you give them to Pugi's API at `api.pugi.io` over HTTPS: your brief and change instructions, the URL or repository you ask to check, the business name and style words for a logo, and your catalogue query. Pugi keeps the sites it builds, the check results and the logos on your account so you can come back to them. Nothing else from the conversation is sent. Authentication uses OAuth 2.0 with your Pugi account; you can disconnect the app at any time from your Pugi account settings. Details: [privacy policy](https://pugi.io/privacy) and [terms](https://pugi.io/terms).

## Support

Help centre: https://pugi.io/support. Email: support@pugi.io. Documentation: https://docs.pugi.io. Issues with the plugin files: https://github.com/pugi-io/claude-code-plugin/issues.

## License

MIT. See [LICENSE](LICENSE).
