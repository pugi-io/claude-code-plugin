---
name: change-and-publish
description: Change a site Pugi built and put it live on its own address.
---

To change a built site, call `edit` with the job or project the user means and a plain description of the change, with a new idempotency_key. The build card shows progress; check `job_status` only when the user asks. Show the updated preview when it is ready.

Publish only after the user has looked at the preview and asks to go live. Call `publish` for that build; then show the live address it returns. Use `publish_status` to list the user's published sites and their status. Never say a site is live before `publish` succeeds. If the user wants their own domain, explain that it is set up in the Pugi console.
