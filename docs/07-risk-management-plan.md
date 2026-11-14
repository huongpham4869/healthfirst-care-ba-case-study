# Risk Management Plan

*HealthFirst Care - Risk Register, Risk Assessment Matrix, Mitigation and Contingency Plans*

[← Data Analysis](06-data-analysis.md) · [README](../README.md)

---

## 1. Purpose

This plan identifies and assesses risks related to the HealthFirst Care case study and defines mitigation and contingency actions. Risks are based on the case brief, simulated stakeholder profiles, BRD constraints, and data limitations. Known limitations, such as the missing waiting-time baseline, are documented in the BRD rather than treated as risks. Risks affecting the analysis are managed within this case study. Risks associated with future implementation are documented for handover because implementation is outside scope.

## 2. Risk Categories and Rating Scale

| Category | Definition |
|---|---|
| Technical | System, integration, data security or infrastructure risks |
| Operational | Day-to-day hospital operations and resource capacity risks |
| Stakeholder | Stakeholder expectations, engagement or adoption risks |
| Analysis | Risks arising from limitations in the evidence used to define requirements |

| Rating | Likelihood | Impact |
|---|---|---|
| High | Expected to occur during the relevant phase (over 50%). | Material threat to project objectives, budget, timeline or patient safety |
| Medium | May occur during the relevant phase (20–50%). | Significant but recoverable delay or cost impact |
| Low | Unlikely to occur during the relevant phase (below 20%). | Minor impact, manageable within normal contingency |

*Severity = Likelihood × Impact, read from the matrix in Section 4.*

## 3. Risk Register

The register lists each risk with its category, phase, rating, trigger, mitigation, owner and residual rating. *Likelihood / Impact / Severity / Residual columns: H = High, M = Medium, L = Low.*

| ID | Risk description | Category | Phase | L | I | Sev. | Res. |
|---|---|---|---|---|---|---|---|
| [R01](#r01) | Patient data is exposed when systems or processes change | Technical | Implementation | M | H | H | M |
| [R02](#r02) | Staff do not adopt the new workflows or maintain accurate room and equipment status | Stakeholder | Implementation | H | M | H | M |
| [R03](#r03) | Staff, room and equipment shortages limit the benefit of better visibility | Operational | Post-implementation | M | H | H | H |
| [R04](#r04) | Network or system downtime interrupts online booking | Technical | Post-implementation | M | M | M | L |
| [R05](#r05) | Requirements are not validated in time, or stakeholders disagree on scope | Stakeholder | Analysis | M | M | M | L |
| [R06](#r06) | Requirements based on the small, simulated sample do not reflect actual operations | Analysis | Analysis | M | H | H | M |

### Risk details

#### R01

**Patient data is exposed when systems or processes change**

- **Trigger:** A security review identifies unprotected data or unresolved vulnerabilities.
- **Mitigation strategy:** Protect data in transit and at rest, restrict access by role, and address identified legacy vulnerabilities.
- **Owner:** IT Manager

#### R02

**Staff do not adopt the new workflows or maintain accurate room and equipment status**

- **Trigger:** Low training attendance, negative feedback, or mismatches between recorded and actual resource status.
- **Mitigation strategy:** Provide role-based training, involve staff in process reviews, and appoint departmental change champions.
- **Owner:** Hospital Management

#### R03

**Staff, room and equipment shortages limit the benefit of better visibility**

- **Trigger:** Resource status shows sustained unavailability
- **Mitigation strategy:** Monitor resource status and escalate persistent capacity gaps to Hospital Management. Staffing and facilities decisions remain outside scope.
- **Owner:** Hospital Management

#### R04

**Network or system downtime interrupts online booking**

- **Trigger:** Availability falls below the agreed target.
- **Mitigation strategy:** Agree an availability target with the IT Team and maintain an assisted booking channel where the scheduling system remains available. Define a separate fallback for full system outages.
- **Owner:** IT Manager

#### R05

**Requirements are not validated in time, or stakeholders disagree on scope**

- **Trigger:** Requirements remain Proposed at a review point, or a request conflicts with the agreed scope
- **Mitigation strategy:** Plan reviews around stakeholder availability, keep scope exclusions visible, and escalate scope decisions to Hospital Management.
- **Owner:** Business Analyst

#### R06

**Requirements based on the small, simulated sample do not reflect actual operations**

- **Trigger:** Operational data shows materially different patterns
- **Mitigation strategy:** Treat findings as directional and validate affected requirements against operational data before relying on them. Update the RTM as needed
- **Owner:** Business Analyst

## 4. Risk Assessment Matrix

The matrix combines likelihood and impact to give severity. Red = High (immediate attention), yellow = Medium (monitor and manage), green = Low (regular review).

|  | Low Impact | Medium Impact | High Impact |
|---|---|---|---|
| **High Likelihood** | - | R02 | - |
| **Medium Likelihood** | - | R04, R05 | R01, R03, R06 |
| **Low Likelihood** | - | - | - |

| Severity | Response |
|---|---|
| **High** | Active mitigation |
| **Medium** | Monitor; mitigation in place |
| **Low** | Accept |

## 5. Contingency Plans

Contingency actions define the response if a risk materialises despite mitigation.

| ID | Contingency action |
|---|---|
| **R01** | Restrict access to affected systems, notify the IT Manager and Hospital Management, investigate the incident, and apply corrective measures. |
| **R02** | Provide additional hands-on support and training. Escalate persistent adoption issues to department heads. |
| **R03** | Escalate sustained resource shortages to Hospital Management. Staffing and facilities decisions remain outside scope. |
| **R04** | If only the online channel is unavailable, direct patients to the assisted channel, provided staff can access current availability and conflict checks. If the scheduling system itself is unavailable, follow an approved downtime procedure; this procedure must be defined before implementation |
| **R05** | Hold a review with affected stakeholders, escalate scope decisions to Hospital Management, and record unresolved requirements as open items. |
| **R06** | Reanalyse the operational data, revise affected findings and requirements, and update the RTM. |

## 6. Risk Monitoring and Review

- Reassess R06 when operational data becomes available.

- Record new risks using the categories and rating scale in Section 2.

- Review the Risk Register alongside the RTM. Material changes to requirements or scope trigger a risk review.

---

[← Data Analysis](06-data-analysis.md) · [README](../README.md)
