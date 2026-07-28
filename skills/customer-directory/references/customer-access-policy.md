# Customer Information Access Policy

> **Template — replace placeholder roles with the actual roles in your workspace.** This policy controls what the Business Assistant will share with each requester.

## Access levels

| Role | Contact info | Account status | Account manager | Financial / contract | Sensitive notes |
|---|---|---|---|---|---|
| {Sales team} | ✅ | ✅ | ✅ | ✅ | ✅ |
| {Customer support} | ✅ | ✅ | ✅ | ❌ | ❌ |
| {Operations / delivery} | ✅ | ✅ | ✅ | ❌ | ❌ |
| {General employee} | ✅ business email only | ✅ | ✅ | ❌ | ❌ |
| {External / unknown} | ❌ | ❌ | ❌ | ❌ | ❌ |

## When to refuse

- The requester's role isn't listed → ask them to confirm their role first.
- The customer is marked **Inactive** → require explicit approval from the listed account manager before sharing.
- Notes are flagged **Confidential** → do not share unless the role has "Sensitive notes" access.

## When to escalate

- Requests for bulk export of the directory → escalate to the data owner.
- Repeated lookups across many customers from a single user → flag to the workspace admin.
