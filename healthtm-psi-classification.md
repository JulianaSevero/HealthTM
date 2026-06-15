# HealthTM — Patient Safety Impact (PSI) Classification

| General Information | `<Your healthcare context>` |
|-------|-------|
| Artifact | Scoping Document |
| Version | `<e.g., 1.0>` |
| Date | `<YYYY-MM-DD>` |
| Owner | `<e.g., Cybersecurity Analyst>` |
| System / Service/ Component | `<e.g. system / organization>` |
| Status | `<e.g. draft / under review / approved>` |

This sheet is a shared reference used across the Analyze, Evaluate, and Report
pillars. PSI measures harm to the patient as an individual, which is independent
from organizational impact (financial, reputational, data loss). Record PSI as a
mandatory field for every threat so that patient harm stays visible and traceable
to clinical governance.

## PSI levels

| Level | Track | Clinical definition | Example |
|-------|-------|---------------------|---------|
| PSI 4 | Direct harm | Compromise of device actuation causing immediate physical harm | Infusion pump rate change; ventilator parameter alteration |
| PSI 3 | Indirect harm | Interruption of a time-critical diagnostic workflow with measurable mortality risk | PACS unavailable during stroke or major-trauma assessment |
| PSI 2 | Indirect harm | Delay in an urgent but non-time-critical workflow | LIS unavailable, delaying urgent lab results |
| PSI 1 | Indirect harm | Delay in an elective workflow with no acute clinical consequence | Scheduling outage affecting non-urgent appointments |
| PSI 0 | No impact | No clinical workflow affected | Administrative or billing system compromise |

Threats at PSI 3 or above trigger mandatory escalation to the clinical governance
body named in the Scoping Document.

## Decision rule

Apply in order and stop at the first match:

1. Does any patient-facing clinical workflow depend on the asset? If no, assign **PSI 0**.
2. Could a compromise cause direct device-actuation harm (e.g., incorrect drug delivery, harmful stimulation)? If yes, assign **PSI 4**.
3. Is the affected workflow time-critical with measurable mortality risk (e.g., emergency imaging for stroke or major trauma)?
   - Yes, and no maintained manual fallback exists → **PSI 3**.
   - Yes, but a documented and operationally tested manual fallback exists → **PSI 2**.
4. Is the workflow urgent but not time-critical for mortality? Assign **PSI 2**.
5. Is the workflow elective with no acute consequence? Assign **PSI 1**.

Discuss with your team if the questions are aligned to your context.

## Likelihood (L)

A 1–3 ordinal measure of exploitability in the healthcare environment, used
alongside PSI.

| L | Level | Definition |
|---|-------|------------|
| 1 | Low | Requires privileged access or physical presence |
| 2 | Medium | Remotely exploitable with moderate effort (valid credentials, or a known vulnerability without a trivially available exploit) |
| 3 | High | Remotely exploitable without authentication |

## Scoring sheet

| Threat ID | Asset | Dependent clinical workflow | Manual fallback? | PSI | L | Escalation required? |
|-----------|-------|------------------------------|------------------|-----|---|----------------------|
| `<id>` | `<fill in>` | `<fill in>` | `<yes/no>` | `<0–4>` | `<1–3>` | `<yes if PSI ≥ 3>` |

## Iteration triggers

Revisit this artifact on system change, new device or integration, topology change or/and new data flow in scope

## Version control & sign-off

| Version | Date | Author | Change summary |
|---------|------|--------|----------------|
| `<e.g. 1.0.0> ` | `<2026-10-04>` | `<e.g. Juliana Severo>` | `<e.g. added new component>` |

| Role | Name | Decision | Date |
|------|------|----------|------|
| Security leadership | `<e.g. John Doe>` | `<approve / reject>` | `<fill in>` |
| Clinical governance | `<e.g. João Silva>` | `<approve / reject>` | `<fill in>` |
