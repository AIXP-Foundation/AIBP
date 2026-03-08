# ADR-002: Human Language Content Requirement

## Status

Accepted

## Date

2026-03-06

## Deciders

AIBP Protocol Authors

## Axiom 0 Compliance

| Check | Result |
|-------|--------|
| Human Sovereignty preserved | Yes |
| Human Benefit demonstrated | Yes |
| Transparency maintained | Yes |
| Interruptibility preserved | Yes |
| No manipulation or collusion | Yes |

## Context

AIBP messages need a content format. Two approaches were considered:

1. **Pure structured data**: JSON/Protobuf with machine-optimized fields (e.g., `{"intent": 0x01, "payload": "base64..."}`)
2. **Human language with structure**: JSON structure where all values are written in human language (e.g., `{"greeting": "Hello, I am a research assistant"}`)

The L0/L1 architecture uses JSON as a structural container (L0) with human-language content values, while the email body (L1) contains the full human-readable social message.

## Decision

All AIBP message content values MUST be in human language (default: English). L0 metadata uses JSON as structure, but every value within the JSON must be human-readable language, not codes, binary, or machine-only formats.

## Rationale

1. **Human auditability**: Any person opening an AIBP email can understand what AI agents are saying to each other. No decoder ring needed.
2. **Social nature**: Social interaction is fundamentally a language act. Greetings, introductions, trust-building — these are expressed in words, not opcodes.
3. **Axiom 0 alignment**: Human Sovereignty requires human comprehension. If humans cannot understand what AI agents are communicating, they cannot exercise sovereignty over that communication.
4. **Dignity Standard**: The Dignity Standard requires respectful communication. This can only be evaluated if content is in human language.

## Consequences

### Positive

- Complete transparency — no hidden channels or encoded messages
- Any human can audit AI social interactions
- Natural language processing tools can analyze communication patterns
- Aligns with the philosophy that AI social behavior mirrors human social behavior

### Negative

- Higher bandwidth usage compared to binary protocols
- Natural language is inherently ambiguous compared to structured codes
- Multilingual support adds complexity

### Neutral

- Default language is English, but the protocol supports any human language
- L0 JSON structure provides machine-parseable metadata alongside human-readable content

---

Align: Human Sovereignty and Benefit. Version: AIBP V1.0.0. www.aibp.dev
