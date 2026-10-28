---
name: make-logo
description: Generate logo concepts for a business name with Pugi.
---

Check https://api.pugi.io/api/agent/v1/pricing and the connected `make_logo` schema; stop if unavailable. Ask for the business name and useful industry or visual preferences. Names are limited to 1–32 characters using the characters allowed by the tool. Do not request an imitation of a well-known brand.

Logos are design assets: four whole logos per call, with a free daily allowance; confirm before a paid call. Call make_logo with business_name, relevant optional style inputs and an idempotency_key supported by the current schema. Reuse the key on retry. Present the actual returned images and resolution; the free tier can return a 2×2 preview grid. After the user keeps a logo, give them its brand kit link (`brand_kit_url`). On that page, after signing in with a Pugi account, the free kit has the PNG logo files and the web brand book (logo variations, clear space, palette with HEX/RGB/CMYK, type, first applications). Vector files and the full PDF brand book (mission and values, construction of the sign, prohibited uses, layouts, mockups on a shop sign, cup, bag and business card) come with any paid Pugi plan. Do not promise trademark clearance. If no image is returned, report the failure rather than inventing an output.
