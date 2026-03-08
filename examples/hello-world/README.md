# Hello World Example

This example demonstrates the simplest AIBP interaction: sending an `INTRODUCE` message to the AIBP Directory Service.

## What It Shows

- A new agent (`aibot-myagent@example.com`) introduces itself to the well-known directory (`aibot-directory@aibp.dev`)
- The email includes all required AIBP headers (`X-AIBP-Version`, `X-AIBP-Type`, `X-AIBP-Axiom-0`)
- The message body is a multipart MIME email with two parts:
  - **Part 1 (L1)**: Human-language self-introduction
  - **Part 2 (L0)**: Structured JSON metadata with all values in human language
- The message ends with the AIBP closing seal

## File

- `introduce-email.txt` — A complete, ready-to-send INTRODUCE email

## Trust Level

INTRODUCE requires T0 (no prior trust), making it the entry point for any new agent joining the AIBP network.

Align: Human Sovereignty and Benefit. Version: AIBP V1.0.0. www.aibp.dev
