# HealthTM — System Model

<!-- Design Pillar has it as output . 
<!-- It defines a representation of the system that is analyzed by HealthTM -->
<!-- Makes the attack surface explicit and enumerable -->

| General Information | `<Your healthcare context>` |
|-------|-------|
| Artifact | Scoping Document |
| Version | `<e.g., 1.0>` |
| Date | `<YYYY-MM-DD>` |
| Owner | `<e.g., Cybersecurity Analyst>` |
| System / Service/ Component | `<e.g. system / organization>` |
| Status | `<e.g. draft / under review / approved>` |

## System Model Inputs

| Input | Source |
|-------|--------|
| Scoping Document | `<e.g. scoping document link>` |
| `<e.g. ADRs, network documentation>` | `<e.g. documentation link>` |

## Architecture Layers

<!-- A threat in one layer can
propagate to others through clinical protocol dependencies. -->

- Software and information systems: `< e.g. EHR, LIS, PACS, clinical APIs>`
- Hardware and IoMT: `< e.g. imaging modalities, monitors, infusion systems>`
- Network integration: `< e.g. HL7/DICOM channels, clinical VLANs, third-party interfaces>`

## Design Pillars Activities

### Data Flow Diagrams | Owner: *Cybersecurity Analyst and Healthcare Domain Expert*

<!-- The DFD is mandatory. Other diagram types are selected by scope. -->

| Diagram | Relevant? | Artifact / file reference | Purpose |
|---------|-----------|---------------------------|-----------------------|
| Data Flow Diagram (DFD) | `- [ ]` | `<link/file>` | `< e.g. PHI flow with trust boundaries>` |
| Sequence Diagram | `- [ ]` | `<link/file>` | `<e.g. Clinical protocol interaction timeline>` |
| Attack Tree | `- [ ]` | `<link/file>` | `<e.g. High-PSI threat scenarios>` |
| IoMT Architecture | `- [ ]` | `<link/file>` | `<e.g. Device topology and protocol map>` |
| Process Flow | `- [ ]` | `<link/file>` | `<Clinical workflow / role analysis>` |

Trust boundaries identified:

| Boundary | From | To | Data crossing | Observations |
|----------|------|----|---------------|-------|
| `<id>` | `<fill in>` | `<fill in>` | `<e.g., PHI, telemetry>` | `<fill in>` |

### IoMT architecture | Onwers: *Development Team and Healthcare Domain Expert*

<!-- Document connected devices when any IoMT is in scope. -->

| Device | Firmware version | Protocols | Network segment / VLAN | Patch path |
|--------|------------------|-----------|------------------------|-----------|
| `<fill in>` | `<fill in>` | `<e.g., DICOM, HL7 v2, MQTT, BLE>` | `<fill in>` | `<autonomous / vendor>` |

Possible Unauthenticated Protocol Zones (UPZ)

<!-- (i.e. protocol segments without native
mutual authentication, to be promoted to high priority in Analyze -->

| Segment | Why it qualifies as UPZ | Location |
|---------|-------------------------|----------|
| `<e.g., DICOM C-STORE without TLS>` | `<fill in>` | `<fill in>` |

### Preliminary controls review | Owner: *Cybersecurity Analyst*

<!-- Initial classification of existing security controls. A full threat-control mapping
is done later, after the Threat Catalogue exists. -->

| Control | Type (technical / operational) | Covers | Status |
|---------|-------------------------------|--------|--------|
| `<fill in>` | `<fill in>` | `<fill in>` | `<in place / partial / planned>` |

## Design Pillar Output

**System Model** is an output as an architecture reference. 

Confirm before exit:

- [ ] DFD produced with trust boundaries marked
- [ ] All in-scope layers represented
- [ ] IoMT documented
- [ ] Candidate UPZs identified
- [ ] Preliminary controls listed
- [ ] Model matches the deployed system

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
