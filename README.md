# HealthFirst Care — Hospital Operations Improvement

**Business Analyst · Capstone Project** · May – Jul 2026

A Business Analysis case study on improving operational efficiency in a multi-specialty hospital: appointment management, resource visibility, patient communication and coordination between departments.

> [!NOTE]
> This is a course capstone case study, not work for a real hospital. It is based on a case brief, simulated stakeholder profiles and three small sample datasets. No live interviews were held, no system was selected or built, and the requirements have not been validated or tested.

**Short on time?** Read the [Project Summary](docs/00-project-summary.md) (19 slides), then the [BRD](docs/02-brd.md).

## Overview

- **Organisation:** a hospital with five clinical departments, supported by administrative, nursing and IT functions
- **Question:** Where do appointments, resources and information break down, and what does the hospital need to fix them?
- **Evidence:** case brief, simulated stakeholder profiles, and sample data (20 appointments, 15 feedback records, 10 resource records)
- **Output:** BRD, RTM, stakeholder analysis, six BPMN process models, data analysis with a dashboard, and a risk management plan

## Business problem and objectives

Appointment scheduling, patient records and operational reporting run on separate systems and manual work. An online booking channel exists, but it is hard to use and affected by network downtime, so many patients still book by phone or in person. Staff cannot always see current doctor, room or equipment availability, information moves between departments through manual hand-offs, and reports are prepared by hand. The BRD lists 10 pain points ([BRD §4](docs/02-brd.md#4-current-state-analysis)).

Main objectives ([BRD §7.1](docs/02-brd.md#71-objectives-and-proposed-acceptance-criteria)):

- Reduce patient waiting time (the case brief sets a 20% reduction target)
- Reduce no-shows and cancellations, and report rescheduling separately
- Make booking and changing appointments easier, and keep patients informed
- Show current resource availability, and share information across departments without re-entry
- Give management a current view of appointment outcomes without manual reports

System selection, development and implementation are out of scope ([BRD §8](docs/02-brd.md#8-scope)).

## My role

This was my capstone project. I worked from the case brief and the stakeholder profiles to:

- clean, link and analyse the sample data in Excel and build the dashboard
- identify the pain points and analyse root causes in three separate areas
- model the As-Is and To-Be processes in BPMN and write the gap analysis
- write the business, functional and non-functional requirements and trace them in an RTM
- prepare the stakeholder analysis, the risk management plan and the summary slides

## Dataset and key findings

The three sample datasets (1–20 January 2024) are in [`data/`](data). The sample is small, so every figure is a directional baseline, not hospital-wide performance.

| Indicator | Sample result | How it is calculated |
|---|---|---|
| Appointment disruption | **60%** (12 of 20) | (No Show + Cancelled + Rescheduled) ÷ all appointments |
| No-show rate | **20%** (4 of 20) | No Show ÷ all appointments |
| No-show and cancellation rate | **40%** (8 of 20) | (No Show + Cancelled) ÷ all appointments |
| Average satisfaction | **7.0 / 10** | Mean score of 15 feedback records; 6 of 15 (40%) score 8 or above |
| Average waiting time | Not measurable | No check-in or consultation start times are recorded |

What the figures do and do not show:

- The disruption rate includes rescheduled appointments, which are not always a negative outcome, so it is reported next to the no-show rate.
- The data does not record why appointments were missed, cancelled or rescheduled.
- Each department has one doctor, one time slot and the same outcome for all four of its appointments, so department comparisons only reflect how the sample was built.
- Patient profiles describe waits of more than 30 minutes, and nearly an hour in one case, but waiting time cannot be measured from the data.

[![Operations dashboard: KPI cards and appointment outcomes](assets/dashboard/dashboard-overview.png)](docs/06-data-analysis.md#dashboard)

*Top of the operations dashboard built in Excel. The full dashboard and the analysis tables are on the [Data Analysis](docs/06-data-analysis.md) page.*

## Process analysis

I modelled three processes, As-Is and To-Be, in BPMN ([Process Analysis](docs/05-process-analysis.md)):

1. **Appointment scheduling:** staff check availability by hand, bookings are not always checked for conflicts, and patients get no confirmation or reminder.
2. **Patient check-in and resource allocation:** patients wait in a manual queue when no room is free, and room and equipment status is not visible before assignment.
3. **Interdepartmental coordination:** information passes between departments by hand. Discharge is used as an illustrative scenario; its steps are a modelling assumption that has not been validated.

The root cause analysis looks at appointment disruption, coordination and waiting time separately, because the evidence does not support one causal chain. The findings are treated as possible contributing factors, not confirmed causes ([BRD §5](docs/02-brd.md#5-root-cause-analysis)).

[![To-Be appointment scheduling process in BPMN](assets/diagrams/to-be-appointment-scheduling.png)](assets/diagrams/to-be-appointment-scheduling.png)

*To-Be appointment scheduling process. Select the image to open it at full size ([Process Analysis §1.2](docs/05-process-analysis.md#12-to-be-appointment-scheduling)).*

## Proposed improvements

Each change comes from the gap analysis and links to a requirement:

| To-Be change | Requirements |
|---|---|
| Online booking, rescheduling and cancellation, with an assisted channel using the same rules | FR-01, FR-02, FR-05 |
| Current doctor availability shown at booking, and a conflict check on every new or rescheduled appointment | FR-03, FR-04 |
| Confirmation, reminder and notice of hospital-side changes or delays | FR-07, FR-08, FR-09 |
| Current room and equipment status shown before assignment | FR-10, FR-11 |
| Check-in time and consultation start time recorded for each attended appointment | FR-16 |
| Patient information available to the next authorised department without re-entry | FR-12, FR-13 |
| A current summary of appointment outcomes for management | FR-14 |

The IT Manager suggested a Hospital Information System and a cloud-based booking system. These are recorded as possible options only; this case study defines business needs and does not evaluate or select a system.

## Requirements and traceability

There are 26 requirements: 7 business, 15 functional and 4 non-functional (19 Must Have, 7 Should Have). The [RTM](docs/03-rtm.md) records the source, evidence type, MoSCoW priority with a reason, and a verification method for each one. FR-15 was withdrawn and its ID is not reused.

One trace from the RTM:

| Pain point | Business requirement | Functional requirement | Verification |
|---|---|---|---|
| [PP-10](docs/02-brd.md#4-current-state-analysis): patients wait more than 30 minutes without updates | [BR-07](docs/03-rtm.md#br-07): measure and reduce the time between check-in and the start of the consultation | [FR-16](docs/03-rtm.md#fr-16): record check-in time and consultation start time for each attended appointment | Check that both times are recorded, calculate waiting time, and confirm the average can be reported for a set period |

## Validation approach and target metrics

- **Waiting time:** the case brief sets a 20% reduction target. It cannot be assessed until FR-16 provides a baseline, and the metric definition must be confirmed with Hospital Management.
- **No-shows and cancellations:** track both rates against a validated operational baseline before setting targets.
- **Other objectives:** proposed acceptance criteria are checked through scenario-based UAT for the related functional requirements ([BRD §7](docs/02-brd.md#7-business-objectives-and-baseline-indicators)).

All requirements have *Proposed* status. The 20% target is a target for future validation, not a result.

## Tools and techniques

- **Tools:** Excel (data cleaning, analysis and dashboard), BPMN process models, Word and PowerPoint for the original documents
- **Techniques:** pain-point analysis, root cause analysis by problem area, As-Is / To-Be modelling and gap analysis, stakeholder influence / interest analysis, MoSCoW prioritisation, requirements traceability, user stories with Given / When / Then acceptance criteria, risk register and risk matrix

## Repository structure

```
.
├── README.md                  Project overview (this page)
├── docs/                      Documents in Markdown, readable on GitHub
│   ├── 00-project-summary.md
│   ├── 01-project-overview.md
│   ├── 02-brd.md
│   ├── 03-rtm.md
│   ├── 04-stakeholder-analysis.md
│   ├── 05-process-analysis.md
│   ├── 06-data-analysis.md
│   └── 07-risk-management-plan.md
├── assets/
│   ├── diagrams/              As-Is and To-Be BPMN process models
│   ├── dashboard/             Operations dashboard (full and top section)
│   └── slides/                Slide images for the Project Summary
└── data/                      Sample datasets (CSV) and data notes
```

## How to explore the artifacts

| # | Document | What to look at |
|---|---|---|
| 00 | [Project Summary](docs/00-project-summary.md) | The case study in 19 slides |
| 01 | [Project Overview](docs/01-project-overview.md) | Context, approach and document list |
| 02 | [BRD](docs/02-brd.md) | Pain points, root cause, data findings and limitations, objectives, scope and requirements |
| 03 | [RTM](docs/03-rtm.md) | Source, evidence, priority and verification for each requirement |
| 04 | [Stakeholder Analysis](docs/04-stakeholder-analysis.md) | Stakeholder profiles, influence / interest matrix and engagement plan |
| 05 | [Process Analysis](docs/05-process-analysis.md) | As-Is and To-Be BPMN models, gap analysis and user stories |
| 06 | [Data Analysis](docs/06-data-analysis.md) | Cleaned data, baseline indicators, analysis tables and the dashboard |
| 07 | [Risk Management Plan](docs/07-risk-management-plan.md) | Risk register, risk matrix, mitigation and contingency plans |

To check the figures, open the CSV files in [`data/`](data) (they display as tables on GitHub) and compare them with the formulas on the [Data Analysis](docs/06-data-analysis.md) page.

## Limitations and conclusion

- Stakeholder input comes from simulated profiles and a case brief, not live interviews. Hospital Management has no profile, so its concerns come from the case brief.
- The sample is small (20, 15 and 10 records). The findings must be validated against current operational data before targets are set.
- Waiting time and double bookings cannot be measured with the available data.
- The discharge scenario is illustrative and has not been validated.
- All requirements are proposed; none has been validated with stakeholders or tested in a live system.

The case study shows how I worked from limited evidence to clear, traceable requirements: separating what the data shows from what stakeholders report, keeping each root cause branch to what the evidence supports, and defining the measurement (FR-16) needed before the 20% target can be tested.
