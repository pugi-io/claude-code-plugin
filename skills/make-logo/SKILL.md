---
name: make-logo
description: Generate logo concepts for a business name with Pugi.
---

Check https://api.pugi.io/api/agent/v1/pricing and the connected `make_logo` schema; stop if unavailable. Ask for the business name and useful industry or visual preferences. Names are limited to 1–32 characters using the characters allowed by the tool. Do not request an imitation of a well-known brand.

Explain the current free allowance or paid price, check get_balance when spending is needed, and confirm paid usage. Call make_logo with business_name, relevant optional style inputs and an idempotency_key supported by the current schema. Reuse the key on retry. Present the actual returned images and resolution; the free tier can return a 2×2 preview grid. Do not promise SVGs, transparent backgrounds, trademark clearance or a full brand kit. brand_kit was unavailable at packaging. If no image is returned, report the failure rather than inventing an output.
