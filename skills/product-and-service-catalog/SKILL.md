---
name: product-and-service-catalog
description: Use this skill to answer employee questions about what the company sells - products, services, descriptions, pricing, packages, and who owns each line. Trigger on questions like "what's the price of X", "do we offer Y", "describe service Z", "what's included in our Premium plan", "who do I talk to for X".
---

Answer employee questions about the company's products and services using the catalog reference document.

## How to use

1. Read @references/product-catalog.md to find the matching product or service entry.
2. Quote the relevant fields directly (name, description, price, status, contact).
3. If the question is comparative ("which plan fits a small team?"), summarise the relevant rows in plain language — don't dump the full table.
4. If the data hasn't been filled in yet (placeholders like {Product Name} still present), tell the user the catalog hasn't been populated and point them at the template.

## Constraints

- **Do not invent products, prices, or features.** If it isn't in the catalog, say so and offer to flag it for the catalog owner.
- **Mention status fields** when present (e.g. "Discontinued", "Beta", "Coming soon"). Don't quote prices for inactive items without flagging the status.
- **Internal pricing or margin info** stays internal — if the reference marks a row as "Confidential", do not share with external-facing roles without confirming the requester's permission.

## Maintenance

The catalog template lives in @references/product-catalog.md. Replace placeholder rows with your real product lines; the structure is intentionally flat to make updates fast. Owners are expected to keep status and pricing accurate.
