---
name: build-website
description: Build a website from a brief with Pugi when the live build tools are available.
---

Read https://api.pugi.io/api/agent/v1/pricing before proposing a build. Require `build_site.available` and `job_status.available` to be true and both tools to be listed on the connected Pugi MCP server. When disabled or missing, explain that website building is unavailable through this integration; do not call it or substitute build_app.

When enabled, collect the purpose, audience, pages, copy and visual preferences into a brief (10–8000 characters). Explain usage billing and agree a `max_usd` within the live limits; check `get_balance`. Call `build_site` with that brief, max_usd and a unique idempotency_key (8–128 letters, digits, dots, underscores, colons or hyphens). Keep the same key on retries; a timeout is not permission for a new charged job. Follow the returned job_id through `job_status`; report stopped or failed honestly. Show the returned view-only preview and final charge. Preview links expire; refresh through job_status.

If the user requests changes, first check `edit.available`, use the tool's current schema and a separate agreed budget and idempotency key. Publish only when `publish.available` is true and the user requests going live after reviewing the preview. A build request alone does not authorize publication. Never claim a live site before publish succeeds.
