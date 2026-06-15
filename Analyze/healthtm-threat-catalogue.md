# HealthTM — Threat Catalogue

<!-- Output of the **Analyze** pillar. Consumes the System Model and the Scoping -->
<!-- Document's actor register. Consolidates the attack surface, role-based scenarios, -->
<!-- STRIDE and LINDDUN findings, ATT&CK mappings, and PSI/Likelihood classification. -->

| General Information | `<Your healthcare context>` |
|-------|-------|
| Artifact | Scoping Document |
| Version | `<e.g., 1.0>` |
| Date | `<YYYY-MM-DD>` |
| Owner | `<e.g., Cybersecurity Analyst>` |
| System / Service/ Component | `<e.g. system / organization>` |
| Status | `<e.g. draft / under review / approved>` |

## Threat Catalogue Inputs

| Input | Source |
|-------|--------|
| System Model (DFDs, IoMT, controls) | Design pillar |
| Actor & trust register | Scoping Document (Discover) |
| PSI classification sheet | `e.g. You can use thehealthtm-psi-classification.md` |

## Analyze Pillar Activities

### Attack surface identification — *Cybersecurity Analyst*

<!-- Enumerate entry points, exposed interfaces, and trust-boundary crossings from the
DFDs. Mark UPZ entries as high priority by default. -->

| Surface element | Type | Trust boundary | UPZ? | Notes |
|-----------------|------|----------------|------|-------|
| `<fill in>` | `<e.g., API, protocol channel>` | `<id>` | `<yes/no>` | `<fill in>` |

### Role-based scenarios — *Healthcare Domain Expert + Cybersecurity Analyst*

<!-- Translate the actor register into threat narratives grounded in clinical workflow. -->

| Scenario ID | Actor | Workflow context | Threat narrative |
|-------------|-------|------------------|------------------|
| `<id>` | `<fill in>` | `<fill in>` | `<fill in>` |

### Threat modeling — *Cybersecurity Analyst*

- Apply STRIDE per DFD element. Apply LINDDUN to every PHI and IoMT telemetry flow.
- Assign a MITRE ATT&CK technique identifier to each entry where applicable. 

### Impact classification — *Cybersecurity Analyst + Healthcare Domain Expert*

- Apply PSI (Table in the PSI sheet) and a Likelihood score (1–3) to each threat.

## Threat catalogue table

| ID | Asset / element | STRIDE | LINDDUN | ATT&CK | Threat description | UPZ | PSI | L | Privacy/PHI flow? |
|----|-----------------|--------|---------|--------|--------------------|-----|-----|---|-------------------|
| `<id>` | `<fill in>` | `<S/T/R/I/D/E>` | `<L/I/N/D/D/U/N>` | `<Txxxx>` | `<fill in>` | `<yes/no>` | `<0–4>` | `<1–3>` | `<yes/no>` |

## Regulatory relevance mapping

- For threats touching PHI or device risk, note the regulatory priority to track downstream.

| Threat ID | Regulatory to map | Why relevant |
|-----------|-------------------|--------------|
| `<id>` | `<e.g., LGPD art. 11 / HIPAA / ISO 14971>` | `<fill in>` |

## Analyze Pillar Output

**Threat Catalogue** consolidating the items above. Confirm before exit:

- [ ] Attack surface enumerated from DFDs
- [ ] UPZ entries promoted to high priority
- [ ] STRIDE applied per element
- [ ] LINDDUN applied to PHI/telemetry flows
- [ ] ATT&CK identifiers assigned where applicable
- [ ] PSI and Likelihood assigned to every threat

## Iteration triggers

Revisit this artifact on system change, new device or integration, new threat intelligence, new Att&CK technique relevant to scope and/or regulatory update

## Version control & sign-off

| Version | Date | Author | Change summary |
|---------|------|--------|----------------|
| `<e.g. 1.0.0> ` | `<2026-10-04>` | `<e.g. Juliana Severo>` | `<e.g. added new component>` |

| Role | Name | Decision | Date |
|------|------|----------|------|
| Security leadership | `<e.g. John Doe>` | `<approve / reject>` | `<fill in>` |
| Clinical governance | `<e.g. João Silva>` | `<approve / reject>` | `<fill in>` |
