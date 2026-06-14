# HealthTM — Scoping Document

<!-- Scoping Document Establishes the context for all later analysis in HealthTM -->
<!-- Discover Pillar has as an output the Scoping Document -->
<!-- This template is an example, you can adapt it and create your own artefacts -->

| General Information | `<Your healthcare context>` |
|-------|-------|
| Artifact | Scoping Document |
| Version | `<e.g., 1.0>` |
| Date | `<YYYY-MM-DD>` |
| Owner | `<e.g., Cybersecurity Analyst>` |
| System / Service/ Component | `<e.g. system / organization>` |
| Status | `<e.g. draft / under review / approved>` |

## Scoping Document Inputs

<!-- List known documentations and sources -->

| Documentation name | Source | Observations |
|-------|--------|-------|
| `<e.g. Architecture diagrams, contracts>` | `<e.g. documentation URLs>` | `<Additional notes>` |

## Discover Pillar Activities

### Cybersecurity scope | Owner: *Cybersecurity Analyst*

<!-- Define the organizational and technical perimeter in scope. -->

- In-scope systems and networks: `<e.g. EHR>`
- Out of scope (and why): `<e.g. Medical images systems>`

### Regulatory mapping | Owner: *Cybersecurity Analyst* / *Healthcare Domain Expert*

<!-- List the legal and normative instruments that apply, as fields to map. Do not
assert compliance here. -->

| Instrument | Applies? | Obligation to track | Reference |
|------------|----------|------------------------------|-----------|
| `<e.g. LGPD (Lei 13.709/2018)` | `<yes/no>` | `<fill in>` | `<art./section>` |
| `<e.g. HIPAA>` | `<yes/no>` | `<fill in>` | `<art./section>` |
| `<e.g. GDPR>` | `<yes/no>` | `<fill in>` | `<art./section>` |
| `<e.g. ISO 14971>` | `<yes/no>` | `<fill in>` | `<art./section>` |
| `<e.g. IEC 62304>` | `<yes/no>` | `<fill in>` | `<art./section>` |
| `<e.g. IEC 81001-5-1>` | `<yes/no>` | `<fill in>` | `<art./section>` |
| `<e.g. ANVISA RDC 657/2022>` | `<yes/no>` | `<fill in>` | `<art./section>` |

### Healthcare system definition | Owner: *Healthcare Domain Expert*
 
<!-- Care workflows, medical specialties, and patient-facing processes in scope. -->

- Care workflows: `<fill in>`
- Medical specialties: `<fill in>`
- Patient-facing processes: `<fill in>`
- Time-critical workflows: `<fill in>`

### 4. Actor & trust mapping | Owner: *Cybersecurity Analyst*

<!-- Register human and system actors with access levels and trust tiers. -->

| Actor | Internal/External | Access level | Trust tier | Observation |
|-------|-------------------|--------------|-----------|-------|
| `<e.g., Radiologist>` | `<e.g. Internal>` | `<e.g. admin access> ` | `<e.g. trusted>` | `<fill in>` |
| `<e.g., Imaging vendor>` | `<e.g. External>` | `<e.g. view access> ` | `<e.g. untrusted>` | `<fill in>` |

### 5. Dependency inventory / SBOM | Owner: *Development Team*

<!-- Catalogue third-party components and vendor relationships with risk tiers. -->

| Component / dependency | Vendor | Risk tier | Patch path (autonomous / vendor) | Open issues |
|------------------------|--------|-----------|----------------------------------|-------------|
| `<fill in>` | `<fill in>` | `<fill in>` | `<fill in>` | `<fill in>` |

## Output

**Scoping Document** consolidating: system boundary, regulatory applicability map,
actor and trust model, dependency inventory. 

Confirm before exit:

- [ ] System boundary defined
- [ ] Regulatory applicability mapped
- [ ] Actor and trust model complete
- [ ] Dependency inventory complete, open items flagged
- [ ] Reviewed by security leadership
- [ ] Reviewed by clinical governance

## Iteration triggers

Revisit this artifact on system change, new threat, regulatory update, new IoMT device or AI model or/and new medical sector in scope.

## Version control

| Version | Date | Author | Change summary |
|---------|------|--------|----------------|
| `<e.g. 1.0.0> ` | `<2026-10-04>` | `<e.g. Juliana Severo>` | `<e.g. added new component>` |

| Role | Name | Decision | Date |
|------|------|----------|------|
| Security leadership | `<e.g. John Doe>` | `<approve / reject>` | `<fill in>` |
| Clinical governance | `<e.g. João Silva>` | `<approve / reject>` | `<fill in>` |
