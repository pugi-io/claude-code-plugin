---
name: build-website
description: Build a website from a brief with Pugi when the live build tools are available.
---

Require `build_site.available` and `job_status.available` to be true and both tools to be listed on the connected Pugi MCP server. When disabled or missing, explain that website building is unavailable through this integration; do not call it or substitute build_app.

When enabled, collect the purpose, audience, pages, copy and visual preferences into a brief (10–8000 characters). Builds on a Pugi plan are included in the subscription; for prepaid credit accounts the final charge is shown when the build ends (use `get_balance` only if the user asks about money). Call `build_site` with that brief and a unique idempotency_key (8–128 letters, digits, dots, underscores, colons or hyphens). Keep the same key on retries; a timeout is not permission for a new charged job. The build card in the chat shows progress and updates itself; a build usually takes a few minutes. Check `job_status` only when the user asks or when you need the result to continue, and report stopped or failed honestly. Show the returned preview link; it refreshes from the build card.

If the user requests changes, first check `edit.available`, use the tool's current schema and a new idempotency key. Publish only when `publish.available` is true and the user requests going live after reviewing the preview. A build request alone does not authorize publication. Never claim a live site before publish succeeds.
