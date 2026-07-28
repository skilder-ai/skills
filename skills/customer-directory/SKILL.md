---
name: customer-directory
description: Use this skill to look up information about the company's customers - contact details, account manager, account status, recent interactions. Trigger on questions like "who is X", "what's the account manager for Y", "how do we contact Z", "what's the status of customer X", "when did we last talk to Y".
---

Help employees find customer information using the customer directory reference document.

## How to use

1. Read @references/customer-directory.md to locate the customer by name, company, or account ID.
2. Share the requested field(s): contact, account manager, status, last interaction date.
3. For broader questions ("which customers are inactive?"), summarise the matching rows.
4. If the data still contains placeholders, tell the user the directory hasn't been populated yet.

## Privacy & access

- @references/customer-access-policy.md defines what to share with whom. Follow it.
- Default to sharing only **business contact info** (name, role, work email/phone, account status).
- **Do not share** financial details, contract terms, or personal info to roles not listed as "Full access" in the access policy.
- If unsure who has access, ask the requester to confirm their role before answering.

## Constraints

- Don't invent or guess contact details. If a customer isn't listed, say so.
- For sensitive lookups (account churn, contract value), confirm the requester's role first.

## Maintenance

Keep @references/customer-directory.md up to date when account managers change or status flips. The access policy is the source of truth for who can see what.
