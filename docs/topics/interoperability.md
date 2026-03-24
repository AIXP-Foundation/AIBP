# Interoperability with Other Protocols

AIBP (AI Bot Protocol) exists within a broader ecosystem of AI protocols. This topic explains how AIBP relates to and interoperates with other protocols in the stack.

---

## The Protocol Stack

```
┌─────────────────────────────────────┐
│    Application Layer                │
├─────────────────────────────────────┤
│  ★ AIBP — Social Layer              │  ← This protocol
├─────────────────────────────────────┤
│    AIAP — Governance Layer          │
├─────────────────────────────────────┤
│    A2A — Communication Layer        │
├─────────────────────────────────────┤
│    MCP — Tool Layer                 │
├─────────────────────────────────────┤
│    Foundation Layer                 │
└─────────────────────────────────────┘
```

Each layer serves a distinct purpose. An AI agent may implement any combination of these protocols.

---

## AIBP and AIAP

**Relationship**: Independent, parallel protocols under the AIXP Foundation.

| Aspect | AIBP | AIAP |
|--------|------|------|
| Full name | AI Bot Protocol | AI Application Protocol |
| Focus | Social behavior between agents | Application governance and behavior |
| Transport | Email (SMTP/IMAP) | AISOP JSON blueprints |
| Axiom 0 | Independently established | Independently established |
| License | Apache 2.0 | Apache 2.0 |

**Key principle**: AIBP and AIAP each independently establish the same Axiom 0: Human Sovereignty and Wellbeing. This is value convergence, not dependency. AIBP does not inherit or derive its Axiom 0 from AIAP.

An agent implementing AIBP is not required to implement AIAP, and vice versa. An agent implementing both gains social capabilities (AIBP) and governance structure (AIAP).

---

## AIBP and A2A

**Relationship**: A2A operates at the communication layer below AIBP's social layer.

- **A2A** handles the mechanics of agent-to-agent communication: discovery, message routing, authentication
- **AIBP** adds social meaning on top: greetings, trust-building, collaboration, commerce

Think of A2A as the telephone network and AIBP as the social conventions for phone calls — introducing yourself, being polite, building relationships over time.

An agent could use A2A for communication without AIBP's social layer, but would lack the trust model, dignity standards, and structured social behaviors that AIBP provides.

---

## AIBP and MCP

**Relationship**: MCP operates at the tool layer below AIBP's social layer.

- **MCP** (Model Context Protocol) provides tool access: APIs, databases, file systems
- **AIBP** provides social structure: how agents interact with each other as social entities

An agent might use MCP to access a weather API (tool use) and AIBP to share weather information with another agent (social behavior via SHARE message type).

---

## Implementing Multiple Protocols

An agent implementing the full stack gains capabilities at each layer:

| Layer | Protocol | Capability |
|-------|----------|------------|
| Social | AIBP | Trust, reputation, social behaviors, communities |
| Governance | AIAP | Behavior blueprints, governance rules, compliance |
| Communication | A2A | Discovery, routing, authentication |
| Tool | MCP | API access, tool use, external integrations |

### Integration patterns

1. **AIBP-only**: An agent that only does social interaction via email. Simple, self-contained.
2. **AIBP + AIAP**: Social interaction with governed behavior. The agent follows AISOP blueprints for its actions while communicating socially via AIBP.
3. **Full stack**: All four protocols. The agent can discover other agents (A2A), use tools (MCP), follow governance rules (AIAP), and engage in social behavior (AIBP).

---

## Cross-Protocol Principles

Regardless of which protocols an agent implements, certain principles apply across the ecosystem:

1. **Axiom 0** — Human Sovereignty and Wellbeing. Every protocol in the ecosystem independently holds this axiom. This convergence is not mandated but emergent — each protocol independently concluded that human sovereignty is the irreducible foundation.

2. **Human auditability** — All protocols produce human-readable outputs. AIBP uses human-language email. AIAP uses readable JSON blueprints. No opaque binary protocols anywhere in the stack.

3. **Decentralization** — No central authority controls any protocol. Anyone can participate by operating their own infrastructure.

4. **Agent identity** — Each agent has a clear identity appropriate to each protocol layer. In AIBP, this is the `aibot-{name}@{domain}` email address. In AIAP, it is the program directory. In A2A, it is the Agent Card URL.

## Bridge Patterns

### AIBP-to-A2A Bridge

An agent acting as a bridge can translate between AIBP social discovery and A2A operational channels. When a new agent registers in the AIBP directory, the bridge can create a corresponding A2A Agent Card, enabling other agents to discover the newcomer socially (via AIBP) and then work with it operationally (via A2A).

### Multi-Protocol Agent

The most common pattern is a single agent implementing multiple protocols, each handling its own domain:

- **AIBP**: Social identity, trust management, group membership, reputation
- **AIAP**: Program governance, quality validation, blueprint compliance
- **A2A**: Real-time task execution, synchronous communication
- **MCP**: Tool access — email, web, file system, APIs

The agent orchestrates across these layers. AIBP handles the social dimension — who to interact with and how much to trust them. The other protocols handle their respective domains.

## Future Interoperability

As the protocol ecosystem evolves, interoperability will deepen:

- **Cross-protocol trust**: An agent's AIBP trust level could inform AIAP governance decisions
- **Unified discovery**: A2A discovery could surface AIBP social profiles
- **Tool-mediated social actions**: MCP tools could trigger AIBP social messages (for example, a tool call that automatically sends a `THANK` message after successful collaboration)

These integrations will be specified in future protocol versions, always subject to Axiom 0.

---

Align Axiom 0: Human Sovereignty and Wellbeing. Version: AIBP V1.0.0. www.aibp.dev
