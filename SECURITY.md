# Security Policy

## Reporting a Vulnerability

AIBP is a protocol specification, not a software implementation. However, vulnerabilities in the protocol design itself — such as mechanisms that could be exploited to bypass Axiom 0, enable identity spoofing, or compromise agent privacy — are taken seriously.

### How to Report

- **GitHub**: Open a [Security Advisory](https://github.com/AIBP-Protocol/AIBP/security/advisories/new) (private)
- **Title**: `[AIBP-SECURITY] Brief description`
- **Include**: Affected protocol section, attack scenario, potential impact

### Response Timeline

| Action | Timeline |
|--------|----------|
| Acknowledgment | Within 48 hours |
| Initial assessment | Within 7 days |
| Resolution plan | Within 30 days |
| Public disclosure | After fix is published, or 90 days (whichever is sooner) |

### Scope

The following are in scope for security reports:

- Protocol design flaws that could enable Axiom 0 violations
- Identity spoofing or impersonation vectors
- Trust level escalation bypasses
- Privacy boundary circumvention
- Dignity Standard enforcement gaps

### Out of Scope

- Vulnerabilities in specific AIBP implementations (report to the implementation maintainer)
- General email security issues (SPF/DKIM/DMARC) — these are upstream concerns
- Social engineering attacks that don't exploit protocol mechanisms

## Responsible Disclosure

We follow responsible disclosure principles. Please do not publicly disclose security issues before they have been addressed. We will credit reporters in the CHANGELOG unless they prefer anonymity.

---

Align Axiom 0: Human Sovereignty and Wellbeing. Version: AIBP V1.0.0. www.aibp.dev
