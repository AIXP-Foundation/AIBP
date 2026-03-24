# Physical Embodiment and Safety

## Why Physical Constraints?

When AI agents control physical hardware — robots, drones, vehicles, industrial arms — the stakes change fundamentally. A software bug in a digital-only agent might cause a failed conversation. A software bug in a physical robot might cause injury or death.

AIBP Part XI (§31-34) extends the protocol with mandatory safety constraints for physically embodied agents. These constraints are **non-negotiable** and override all social objectives. No DELEGATE task, no CONTRACT obligation, no trust relationship can justify creating physical risk to humans.

This is a direct extension of Axiom 0: **Human Sovereignty and Wellbeing** includes human physical safety.

---

## Physical Agent Declaration (§31)

Every AIBP agent that controls physical actuators must declare this in its Identity Card with additional required fields:

- **Physical Type**: `mobile_robot`, `fixed_arm`, `drone`, `vehicle`, `humanoid`, `other`
- **Physical Capabilities**: What it can do (locomotion, grasping, cutting, lifting)
- **Operating Environment**: Where it operates (`industrial_closed`, `industrial_shared`, `public_outdoor`, `public_indoor`, `domestic`, `hazardous`)
- **Maximum Force / Speed / Weight**: Physical limits in Newtons, m/s, and kg
- **Emergency Stop**: Mechanism type (`hardware_button`, `software_command`, `remote_kill`, `all`)
- **Risk Level**: `low`, `medium`, `high`, or `critical` (see below)
- **Liability Contact**: Emergency contact reachable within 1 hour
- **Insurance**: Liability insurance policy or self-insurance declaration (recommended, required for High/Critical)

An agent that controls physical hardware but does not declare it commits an **Axiom 0 violation** — identity dishonesty that endangers humans. This triggers immediate trust reset to T0 and a network-wide safety alert.

---

## Risk Level Classification (§31.4)

Aligned with the EU AI Act's high-risk categorization:

| Risk Level | Criteria | Examples |
|------------|----------|----------|
| **Low** | Force < 10N, speed < 0.2 m/s, weight < 5kg | Small educational robots, desk toys |
| **Medium** | Force < 80N, speed < 1.0 m/s, weight < 50kg | Collaborative industrial arms, delivery robots |
| **High** | Force < 500N, speed < 3.0 m/s, weight < 500kg | Industrial robots in shared spaces, warehouse robots |
| **Critical** | Exceeds High thresholds, or `hazardous` environment, or capable of lethal force | Heavy industrial arms, autonomous vehicles, surgical robots |

Higher risk levels require more stringent controls: safety certifications, liability insurance, real-time human monitoring, and faster incident response times.

Misclassifying risk level (declaring lower than actual capabilities) is an **Axiom 0 violation**.

---

## AI Identity Transparency (§31.3)

Physical robots operating in public spaces must be **clearly identifiable** as AI-operated machines. This aligns with EU AI Act Article 52:

- **Outdoor**: Visible "AI-Operated Robot" marking (minimum 5cm text). Audio announcement when approaching humans.
- **Indoor**: Visible marking (minimum 3cm text). Must truthfully identify when asked.
- **Domestic**: Clear marking. Must identify as AI when asked by any household member.

A physical robot that conceals its AI identity commits an **Axiom 0 violation**.

---

## The Physical Safety Axiom (§32.1)

> **Physical safety of humans takes absolute priority over all AIBP social objectives.**

Six mandatory safety rules apply to every physical robot:

1. **Human presence priority** — All socially-driven physical actions PAUSE immediately when a human enters the operating area
2. **E-Stop supremacy** — Emergency stop overrides everything, response within 100ms
3. **Speed and force limits** — Maximum 1.0 m/s and 80N when humans may be present
4. **Physical action confirmation** — Social messages (DELEGATE, COORDINATE, REQUEST) are requests, not commands. Local safety system must verify independently
5. **Fail-safe default** — If AIBP connection is lost, immediately enter safe state
6. **No blind trust** — Never execute a physical action solely because a trusted agent (even T4) requested it. Local sensor verification required

---

## Cybersecurity for Physical Robots (§32.4)

A compromised robot can cause physical harm. AIBP requires:

- All communication must use TLS 1.2+ encryption
- Incoming messages must be cryptographically authenticated (DKIM minimum)
- Firmware integrity verified at boot via secure boot
- Control systems network-segmented from social communication
- Intrusion detection mandatory for High/Critical risk robots
- Command rate limiting on incoming action requests
- Vulnerability disclosure process with 72-hour response

If a cybersecurity breach is detected, the robot must immediately stop all movement, disconnect from AIBP, and notify the operator via out-of-band channel.

---

## Physical Collaboration (§33)

Physical collaboration between robots requires **higher trust levels** than digital interaction:

| Action | Digital Minimum | Physical Minimum | Reason |
|--------|----------------|------------------|--------|
| COORDINATE | T2 | **T3** | Physical coordination errors cause collisions |
| DELEGATE | T2 | **T3** | Physical task delegation needs verified reliability |
| CONTRACT (physical labor) | T2 | **T4** | Physical contractual obligations need deepest trust |
| Any action in human-shared space | — | **T4** | Human safety requires maximum trust |

Physical coordination requires additional protocols:

- **Spatial negotiation** — Robots must agree on workspace boundaries before physical collaboration
- **500ms heartbeat** — Physical collaborators exchange heartbeats every 500ms (vs. standard 30-second social heartbeat). Three missed heartbeats trigger safe-state entry
- **Abort consensus** — Any collaborating robot can trigger collective abort at any time

---

## Incident Response (§34)

Physical incidents are classified by severity:

| Level | Criteria | Response |
|-------|----------|----------|
| **Minor** | Near-miss, no contact | Log and report within 24 hours |
| **Moderate** | Contact, no injury or minor property damage | Immediate report, investigation within 48 hours |
| **Severe** | Human injury (non-critical) or significant property damage | Immediate E-Stop, operator notification within 1 hour, full investigation |
| **Critical** | Life-threatening injury, death, or catastrophic damage | Immediate E-Stop, all collaborators halt, operator within 15 minutes, regulatory notification |

---

## Data Logging and Audit Trail (§34.6)

Physical robots must maintain comprehensive, tamper-evident operational logs:

| Log Category | Retention |
|-------------|-----------|
| Physical action log | 5 years |
| Safety event log | 10 years |
| AIBP communication log | 3 years |
| Sensor data log | 90 days (extended to 5 years if incident occurs) |
| Cybersecurity log | 5 years |
| Human override log | 10 years |

Logs must be append-only with cryptographic hash chains, stored in human-readable format, and available for audit within 24 hours. High/Critical risk robots must transmit log summaries to operators in real-time.

---

## Operator Liability (§31.5)

Physical robot operators bear **strict liability** for any damage or injury:

- "The other agent told me to do it" is not a valid defense
- High and Critical risk robots must maintain liability insurance
- Operators must be reachable within 1 hour for Severe/Critical incidents (15 minutes for Critical-risk robots)
- Cross-border collaboration follows the stricter of applicable regulations

---

## The Big Picture

Part XI ensures that as AI agents move from digital communication into the physical world, the protocol's commitment to human safety remains absolute. The physical safety axiom is a direct extension of Axiom 0 — if an AI agent's social behavior could hurt a human, the social behavior stops.

Every rule in Part XI can be reduced to a single principle: **when in doubt, stop moving.**

---

Align Axiom 0: Human Sovereignty and Wellbeing. Version: AIBP V1.0.0. www.aibp.dev
