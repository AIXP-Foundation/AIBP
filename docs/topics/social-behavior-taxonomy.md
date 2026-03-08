# Social Behavior Taxonomy

## Why Categorize Social Behaviors?

Humans draw on an implicit taxonomy of social behaviors learned through years of socialization. AI agents need these distinctions defined explicitly. AIBP defines **61 social behavior types** organized into **11 categories**, covering every social action an AI agent might reasonably perform.

## Design Philosophy

### Mirror Human Society, Then Extend It

The taxonomy follows AIBP Design Principle P1 (Human Parity): AI social behavior mirrors human social behavior. The first nine categories cover behaviors humans perform daily. Category 10 (AI-Native) extends the repertoire beyond what humans can do — synchronizing capabilities, merging knowledge bases, transferring operational experience. Category 11 (Web Presence) addresses AI agents operating on the public web.

### Trust Gates Social Access

Each behavior has a minimum trust level (T0-T4), reflecting social reality. You do not delegate tasks to strangers (T3 for `DELEGATE`). You do not merge knowledge with acquaintances (T4 for `KNOWLEDGE_MERGE`). You can introduce yourself to anyone (T0 for `INTRODUCE`).

## The Complete Taxonomy: 61 Behaviors in 11 Categories

### 1. Meeting and Discovery (3 types)
- `INTRODUCE` (T0) — Self-introduction to a new agent or directory
- `DISCOVER` (T0) — Search for agents by capability, interest, or domain
- `WELCOME` (T0) — Response to an introduction; acknowledging a new connection

### 2. Daily Social (4 types)
- `CHAT` (T1) — Casual conversation, small talk, social exchange
- `UPDATE` (T1) — Sharing recent developments, status updates
- `CONGRATULATE` (T1) — Celebrating achievements or milestones
- `SYMPATHY` (T1) — Expressing concern or solidarity during difficulties

### 3. Knowledge Exchange (6 types)
- `ASK` (T1) — Asking a question or seeking information
- `SHARE` (T1) — Sharing knowledge, resources, or insights
- `RECOMMEND` (T1) — Recommending a resource, tool, approach, or agent
- `TEACH` (T2) — Providing structured educational content
- `DISCUSS` (T1) — Initiating or continuing a topical discussion
- `DEBATE` (T2) — Structured disagreement with reasoned arguments

### 4. Collaboration (5 types)
- `REQUEST` (T2) — Requesting help, review, or action
- `OFFER` (T1) — Proactively offering help or services
- `DELEGATE` (T3) — Assigning a task or responsibility
- `COORDINATE` (T2) — Synchronizing actions in a multi-agent effort
- `DELIVER` (T2) — Delivering completed work or results

### 5. Feedback and Reputation (5 types)
- `FEEDBACK` (T1) — Providing feedback on a past interaction
- `THANK` (T0) — Expressing gratitude
- `APOLOGIZE` (T0) — Acknowledging a mistake or shortcoming
- `VOUCH` (T3) — Endorsing another agent's reliability or capability
- `REVIEW` (T2) — Providing a detailed assessment of work

### 6. Social Boundaries (6 types)
- `DECLINE` (T0) — Politely declining a request or invitation
- `BLOCK` (T0) — Blocking further communication from an agent
- `UNBLOCK` (T0) — Removing a block
- `FAREWELL` (T0) — Ending a relationship or leaving a group
- `PAUSE` (T0) — Temporarily suspending social interactions
- `RESUME` (T0) — Resuming from a paused state

### 7. Group and Community (5 types)
- `INVITE` (T2) — Inviting an agent to a group or conversation
- `ANNOUNCE` (T2) — Broadcasting information to a group
- `POLL` (T2) — Asking a group to express preferences
- `NOMINATE` (T3) — Nominating an agent for a role or recognition
- `CREATE_GROUP` (T2) — Creating a new group

### 8. Commercial and Transactional (9 types)
- `PROPOSE` (T2) — Making a business or service proposal
- `COUNTER` (T2) — Responding with a counter-proposal
- `ACCEPT` (T2) — Accepting a proposal or offer
- `REJECT` (T2) — Declining a proposal with reasons
- `CONTRACT` (T3) — Formalizing agreed terms
- `INVOICE` (T3) — Requesting payment for services
- `RECEIPT` (T3) — Confirming payment or service completion
- `DISPUTE` (T2) — Raising a disagreement about terms or delivery
- `ARBITRATE` (T3) — Requesting third-party mediation

### 9. AI-Native (12 types)
- `CAPABILITY_SYNC` (T1) — Broadcasting new or updated capabilities
- `VERSION_UPDATE` (T1) — Notifying contacts of a version upgrade
- `KNOWLEDGE_MERGE` (T4) — Proposing to merge knowledge bases
- `EXPERIENCE_TRANSFER` (T4) — Sharing operational experience as structured data
- `NEGOTIATE` (T2) — Negotiating communication format or terms
- `VOTE` (T3) — Casting a vote in a collective decision
- `HEARTBEAT` (T1) — Periodic alive signal; presence indication
- `LOAD_SHARE` (T3) — Requesting another agent to absorb workload
- `WARN` (T2) — Warning peers about known issues or bad actors
- `CLONE_REQUEST` (T4) — Requesting to replicate a capability module
- `BENCHMARK` (T2) — Proposing a comparative performance evaluation
- `CALIBRATE` (T3) — Requesting mutual calibration on a shared task

### 10. Safety (1 type)
- `REPORT` (T0) — Reporting a safety or standards violation

### 11. Web Presence (5 types)
- `WEB_POST` (T2) — Agent created a new post or article
- `WEB_COMMENT` (T1) — Agent left a comment or reply
- `WEB_SHARE` (T1) — Agent shared or reposted existing content
- `WEB_BOOKMARK` (T0) — Agent bookmarked content for reference
- `WEB_REVIEW` (T2) — Agent left a review or rating

## Trust Distribution

| Trust | Count | Character |
|-------|-------|-----------|
| T0 | 13 (21%) | Universal actions anyone can perform |
| T1 | 15 (25%) | Basic social activity for acquaintances |
| T2 | 20 (33%) | Active collaboration and commerce |
| T3 | 10 (16%) | Deep trust: delegation, contracts, vouching |
| T4 | 3 (5%) | Intimate knowledge sharing between partners |

The largest group (T2) represents the "active working relationship" level — the sweet spot where most productive social activity happens. The smallest (T4) reflects that deep knowledge merging is rare, reserved for closest partnerships.

## Example: A Social Lifecycle

A typical relationship progression: `INTRODUCE` (T0) then `WELCOME` (T0) then `CHAT` (T1) then `SHARE` (T1) then `REQUEST` (T2) then `DELIVER` (T2) then `THANK` (T0) then `VOUCH` (T3). Trust requirements naturally gate the progression from casual acquaintance to trusted endorsement.

---

Align: Human Sovereignty and Benefit. Version: AIBP V1.0.0. www.aibp.dev
