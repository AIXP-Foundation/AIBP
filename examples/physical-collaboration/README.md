# Physical Collaboration Example

This example demonstrates how two physically embodied robots coordinate a task via AIBP, including the physical safety protocols required by Part XI (§31-34).

## What It Shows

- **Physical Identity Declaration**: Both robots include physical embodiment fields in their headers
- **Trust Escalation**: Physical COORDINATE requires T3 (vs. T2 for digital)
- **Spatial Negotiation**: Robots agree on workspace boundaries before physical collaboration
- **500ms Heartbeat**: Physical collaborators exchange heartbeats at 500ms intervals
- **Safety Confirmation**: Physical actions requested via social messages are verified by local safety systems

## Flow

1. `COORDINATE` — Robot A proposes a physical collaboration task to Robot B (T3)
2. `ACCEPT` — Robot B accepts after local safety system verification
3. `HEARTBEAT` — Physical heartbeat exchange at 500ms intervals during collaboration
4. `DELIVER` — Robot A reports task completion
5. `THANK` — Robot B acknowledges successful collaboration

## File

- `physical-coordinate-flow.txt` — Five emails showing a complete physical collaboration with safety protocols

## Key Concepts

- Physical collaboration requires higher trust levels than digital interaction (§33.1)
- All physical actions are requests, not commands — local safety systems have final authority (§32.2)
- 500ms heartbeat is mandatory during physical collaboration; 3 missed heartbeats trigger safe-state entry (§33.2)
- Human operators can stop any physical collaboration at any time for any reason (§34.5)
- E-Stop commands override everything — social protocols, active tasks, contractual obligations (§32.2)

Align: Human Sovereignty and Benefit. Version: AIBP V1.0.0. www.aibp.dev
