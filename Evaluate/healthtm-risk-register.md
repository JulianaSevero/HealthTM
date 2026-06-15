# HealthTM — Risk Register

<!-- Output of the **Evaluate** pillar. Translates the Threat Catalogue into a -->
<!-- prioritized register and maps mitigation feasibility. Inherits ATT&CK identifiers -->
<!-- and PSI/Likelihood values from the Threat Catalogue.-->

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
| Threat Catalogue | Analyze pillar |
| Organizational scoring method (if any) | `<fill in: DREAD / CVSS / ISO 31000 / other>` |

## Scoring approach

HealthTM supports two paths. Record which one is used.

- [ ] Path A — apply the organization's existing risk method (e.g., DREAD, CVSS,
  ISO 31000) using its native dimensions.
- [ ] Path B — use PSI alongside Likelihood so patient-safety impact stays a
  traceable dimension, independent of the organizational scale.

Method in use: `<fill in>`

## Activities

### Risk prioritization — *Cybersecurity Analyst*
List risks with their priority score. Carry PSI and L from the Threat Catalogue.

### Mitigation mapping — *Cybersecurity Analyst + Development Team*
Assign each threat a control and classify how it can be executed: **autonomous**
(the organization can deploy it unilaterally), **vendor-dependent** (requires the
manufacturer/vendor), or **clinically constrained** (limited by clinical operation).

## Risk register table

| Risk ID | Asset / threat | ATT&CK | PSI | L | Priority | Mitigation | Feasibility | Residual risk |
|---------|----------------|--------|-----|---|----------|------------|-------------|---------------|
| `<id>` | `<fill in>` | `<Txxxx>` | `<0–4>` | `<1–3>` | `<fill in>` | `<fill in>` | `<autonomous / vendor-dependent / clinically constrained>` | `<fill in>` |

Risk model reference (asset → threat → vulnerability → likelihood → impact →
treatment → residual risk). Use this chain when describing each entry.

## Residual-risk decisions (ADR style)

Record one block per residual risk that cannot be fully closed, especially
vendor-dependent or clinically constrained items.

### Decision: `<short title>`
- **Context:** `<fill in: why the risk cannot be fully mitigated now>`
- **Decision:** `<fill in: accept / defer / compensating control>`
- **Consequences:** `<fill in: what remains exposed, monitoring in place>`
- **PSI / Likelihood:** `<fill in>`
- **Status:** `<proposed / accepted / superseded>`
- **Sign-off required from:** `<role named in Scoping Document>`

## Output

**Risk Register** consolidating priority scores, feasibility classifications,
mitigation assignments, and inherited ATT&CK identifiers. Confirm before exit:

- [ ] Every catalogued threat carried into the register
- [ ] Priority assigned via the chosen path
- [ ] Mitigation feasibility classified for each
- [ ] Residual risks documented with ADR blocks
- [ ] PSI ≥ 3 items routed to clinical governance escalation

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
