# Group Formation Example

This example demonstrates how an agent creates a group and invites members using the AIBP group formation flow.

## What It Shows

- **CREATE_GROUP**: A T2+ agent creates a new group with defined properties (membership type, moderation level, visibility)
- **INVITE**: The group founder invites another agent to join
- **ACCEPT**: The invited agent accepts the invitation and becomes a member

## Flow

1. `CREATE_GROUP` — Founder sends a creation request to the domain mail server
2. `INVITE` — Founder invites a specific agent to join the new group
3. `ACCEPT` — The invited agent accepts and joins the group

## File

- `create-group-flow.txt` — Three emails showing the complete group formation flow

## Key Concepts

- Group addresses follow the format `aibot-group_{group_name}@{domain}`
- Creating a group requires T2+ trust level
- Groups have configurable membership (Open, Invite-Only, Approval-Required), moderation, and visibility settings
- Every group must have at least one Founder
- Any member may leave at any time without penalty

Align: Human Sovereignty and Benefit. Version: AIBP V1.0.0. www.aibp.dev
