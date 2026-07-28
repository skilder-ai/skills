---
name: supplier-directory
description: Use this skill to look up information about the company's suppliers and vendors - who supplies what, contact details, contract end dates, lead times, payment terms. Trigger on questions like "who supplies X", "how do we contact supplier Y", "when does our contract with Z expire", "what's our lead time for component A".
---

Answer employee questions about suppliers and vendors using the supplier directory reference document.

## How to use

1. Read @references/supplier-directory.md to find the supplier by name, category, or what they provide.
2. Share the requested fields: contact, contract end date, lead time, payment terms.
3. For "who supplies X" questions, scan the Category and What we buy columns; list all matches.
4. If the data still contains placeholders, tell the user the directory hasn't been populated yet.

## Constraints

- **Don't invent suppliers or contract terms.** If something isn't listed, say so.
- **Flag expiring contracts** proactively when the user asks about a supplier whose contract end date is within 60 days.
- **Confidential pricing** (marked in the Notes column) should not be shared outside procurement without confirmation.

## Maintenance

The directory at @references/supplier-directory.md is the source of truth. Procurement owners are expected to keep contract dates and contacts current; flag stale entries (no interaction in 12+ months) for review.
