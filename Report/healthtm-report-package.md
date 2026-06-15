# HealthTM — Report Package

<!-- Output of the **Report** pillar. Closes the cycle: verifies mitigation -->
<!-- effectiveness, validates clinical compatibility, and produces governance outputs. -->
<!-- Consumes the Risk Register. -->

| General Information | `<Your healthcare context>` |
|-------|-------|
| Artifact | Scoping Document |
| Version | `<e.g., 1.0>` |
| Date | `<YYYY-MM-DD>` |
| Owner | `<e.g., Cybersecurity Analyst>` |
| System / Service/ Component | `<e.g. system / organization>` |
| Status | `<e.g. draft / under review / approved>` |

## Inputs

| Input | Source |
|-------|--------|
| Risk Register | Evaluate pillar |
| Threat Catalogue (for ATT&CK-derived test cases) | Analyze pillar |

## Activities

### Control verification — *Cybersecurity Analyst + Development Team*
Derive test cases from the ATT&CK-mapped scenarios in the Threat Catalogue. Plan
penetration testing, SAST, and DAST against the catalogued vectors.

| Test ID | Threat / ATT&CK | Test type | Expected result | Outcome |
|---------|------------------|-----------|-----------------|---------|
| `<id>` | `<Txxxx>` | `<pentest / SAST / DAST>` | `<fill in>` | `<pass / fail / pending>` |

### Healthcare workflow test — *Healthcare Domain Expert + Cybersecurity Analyst*
Validate controls against care-delivery requirements with representative clinical
users. Define latency thresholds by workflow urgency; controls exceeding a
threshold return to redesign.

| Workflow | Control under test | Latency threshold | Measured | Within threshold? |
|----------|--------------------|-------------------|----------|-------------------|
| `<fill in>` | `<fill in>` | `<fill in>` | `<fill in>` | `<yes/no>` |

> Note: a control that degrades a PSI 3 workflow below its operational requirement
> is itself a patient-safety issue and must be redesigned before deployment.

### Residual-risk acceptance — *Clinical governance + named stakeholders*
Require sign-off for all high-priority threats and clinically constrained
mitigations. Carry forward any unresolved open items from the Scoping Document.

| Open item | Origin | PSI | Decision | Signed off by | Date |
|-----------|--------|-----|----------|---------------|------|
| `<fill in>` | `<e.g., Scoping Document alert>` | `<0–4>` | `<accept / remediate / defer>` | `<role/name>` | `<date>` |

### Decision record (ADR style)
One block per accepted residual risk.

#### Decision: `<short title>`
- **Context:** `<fill in>`
- **Decision:** `<fill in>`
- **Consequences:** `<fill in>`
- **Status:** `<accepted / superseded>`

## Output

**Report Package** containing the threat report, workflow test report, control
verification results, and any regulatory instruments the scope requires. Confirm
before exit:

- [ ] Control verification complete, results recorded
- [ ] Workflow tests complete; failing controls returned to redesign
- [ ] All high-priority and clinically constrained items signed off
- [ ] Unresolved Scoping Document items surfaced and addressed
- [ ] Audience-specific outputs produced (technical, governance, regulatory)

## Audience outputs

| Audience | Output | Produced? |
|----------|--------|-----------|
| Technical team | `<e.g., threat report, test results>` | `- [ ]` |
| Clinical governance | `<e.g., escalation summary, sign-offs>` | `- [ ]` |
| Regulatory / audit | `<e.g., mapped evidence per instrument>` | `- [ ]` |

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
