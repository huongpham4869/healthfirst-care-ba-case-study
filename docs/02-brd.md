# Business Requirements Document

*HealthFirst Care - Business Analysis Case Study*

[← Project Overview](01-project-overview.md) · [README](../README.md) · [RTM →](03-rtm.md)

---

## 1. Project Overview

HealthFirst Care is a multi-specialty hospital seeking to improve operational efficiency and patient experience. This Business Requirements Document (BRD) defines the business problems, objectives, scope, and requirements for improving appointment management and coordination across departments. It describes the business capabilities and future-state processes required without selecting a system or vendor.

**Key Findings**

- Appointment outcomes: In the 20-record sample, 12 appointments (60%) did not go ahead as originally scheduled. Eight (40%) were recorded as No Show or Cancelled, including a 20% no-show rate, and four (20%) were rescheduled.

- Patient satisfaction: The average score was 7.0/10 across 15 feedback records, with 6 records (40%) scoring 8 or above.

- Waiting time: Patient profiles describe waits of more than 30 minutes past the appointment time, and nearly an hour in one case. No dataset records check-in or consultation start times, so a waiting-time baseline cannot be calculated.

- Operational challenges: Case materials and simulated stakeholder profiles indicate limited resource visibility, manual information hand-offs, and limited operational reporting.

These findings are directional. The small samples and missing data limit conclusions about hospital-wide performance and the causes of operational problems. Detailed pain points and supporting evidence are presented in Section 4, with data findings and limitations discussed in Section 6.

## 2. Business Background and Problem Statement

HealthFirst Care has five clinical departments supported by administrative, nursing, and IT functions. Appointment scheduling, patient information management, and operational reporting rely on separate systems and manual processes. Although an online appointment channel exists, the current operating model still depends heavily on staff assistance and manual coordination.

These conditions limit visibility across departments and make it difficult to coordinate appointments, communicate changes promptly, and allocate available resources effectively. They also increase administrative effort and limit management's ability to monitor operational performance.

The business problem is therefore how to improve appointment management, resource visibility, patient communication, and information sharing across departments while establishing reliable measures of operational performance. The specific pain points, their evidence, and their underlying process gaps are analysed in Sections 4 and 5.

## 3. Stakeholders

The analysis considers six stakeholder groups: Patients, Doctors, Nurses, Administrative Staff, the IT Team, and Hospital Management. Their needs, influence, interest, and proposed engagement approach are documented in the Stakeholder Analysis & Engagement Plan. This case study uses simulated stakeholder profiles and a case brief rather than live stakeholder interviews. Hospital Management has no separate stakeholder profile; its concerns are derived from the case brief.

## 4. Current State Analysis

The following pain points describe the current operating process and its limitations. Evidence is based on the case brief, simulated stakeholder profiles, process analysis, and available sample data.

| Ref | Current-state pain point | Process affected | Evidence type |
|---|---|---|---|
| **PP-01** | The online booking channel is difficult to use and affected by network downtime. Patients often rely on phone or in-person booking. | Appointment scheduling | Patient and IT profiles; case brief |
| **PP-02** | Bookings are not consistently checked for conflicts, resulting in double bookings. A doctor also reports overbooked schedules; whether this means double booking or more appointments than a session can hold is not yet confirmed. | Appointment scheduling | Administrative staff profile (double bookings); Cardiology doctor profile (overbooked schedules) |
| **PP-03** | Patients may not receive timely confirmation, reminders, or notice of appointment changes and cancellations. | Appointment scheduling | Patient profile; case brief |
| **PP-04** | Administrative staff cannot consistently see current doctor availability when booking appointments. | Appointment scheduling | Administrative staff profile |
| **PP-05** | Patients may wait in a manual queue when no examination room is available. | Patient check-in | Current-state process described in the case brief |
| **PP-06** | Examination rooms and equipment may be unavailable at peak times, and their status is not consistently visible before assignment. | Check-in / resource allocation | Cardiology doctor profile (diagnostic equipment at peak hours); As-Is check-in process; limited resource data |
| **PP-07** | Information is transferred through manual hand-offs between departments, causing delays. | Interdepartmental coordination | Doctor and nurse profiles (test results, referrals, patient transfers) |
| **PP-08** | Scheduling and patient-record information is held in separate systems, requiring staff to re-enter or reconcile data. | Cross-functional | IT and administrative staff profiles |
| **PP-09** | Operational reports are prepared manually, limiting management's access to a current view of performance. | Management reporting | Case brief; IT profile |
| **PP-10** | Patients report waiting more than 30 minutes, and nearly an hour in one case, without updates during the delay. | Check-in / consultation | Patient profile; 2 of 15 feedback comments mention waiting or delay |

**Current-state process note:** An online appointment system exists, but the case materials describe usability issues and network downtime. The As-Is model therefore represents the predominant booking route described in the case: administrative staff handling bookings by phone or in person.

**Evidence limitation:** The 60% appointment disruption rate measures outcomes in the sample; it does not establish why appointments were missed, cancelled, or rescheduled. Similarly, the resource data is too limited to establish actual capacity or quantify peak-time shortages. These findings should be interpreted alongside the case brief and stakeholder profiles. Operating-room, emergency-bed and supply issues raised in some profiles belong to other workflows and are not used as direct evidence for outpatient check-in.

## 5. Root Cause Analysis

The analysis examines three problem areas separately because the available evidence does not establish a single causal chain. Findings are treated as potential contributing factors where causation has not been confirmed.

### 5.1 Appointment Disruption

| Question | Finding |
|---|---|
| 1\. Why are 60% of sampled appointments disrupted? | 12 of 20 appointments were no-shows, cancelled, or rescheduled (Appointment data). The dataset does not record the reasons. |
| 2\. What may contribute to these outcomes? | Patients lack reliable reminders and convenient appointment changes. Hospital-side factors include inconsistent conflict checks and delayed communication of changes (Case brief and simulated stakeholder profiles). |
| Underlying gap | The process does not consistently support conflict checking, reminders, convenient appointment changes, and timely notifications. The contribution of each factor remains unknown. |

### 5.2 Interdepartmental Coordination

| Question | Finding |
|---|---|
| 1\. Why is information delayed or re-entered? | Doctors and nurses report late test results, cumbersome referrals and poorly coordinated patient transfers (simulated stakeholder profiles). In each case, information passes between departments through manual hand-offs. |
| 2\. Why are manual hand-offs needed? | Scheduling and patient-record systems are not integrated (IT Manager profile), and billing staff reconcile billing records with treatment data from several departments (Billing Administrator profile). Staff cannot easily access current information held by another department. |
| Underlying gap | Information is not consistently available to the next department when needed. The dataset does not quantify hand-off delays or repeated data entry. The Process Analysis uses discharge as an illustrative scenario for this gap; its steps are a modelling assumption and have not been validated with stakeholders. |

### 5.3 Patient Waiting Time

| Question | Finding |
|---|---|
| 1\. Why do patients wait beyond their scheduled times? | Patients report waits of more than 30 minutes past the appointment time, and nearly an hour in one case. Stakeholder inputs mention overbooked doctor schedules, diagnostic equipment unavailable at peak hours, and no updates during delays. Two of 15 feedback comments mention waiting or delay. |
| 2\. What may contribute to these delays? | Conflict checks and resource-availability visibility are inconsistent. Overbooked schedules, staffing and room capacity may also contribute, but their impact has not been quantified. Conflict checking prevents double booking; it does not by itself limit how many appointments a session holds. |
| Underlying gap | Scheduling and resource assignment lack consistently current availability information. No check-in or consultation-start timestamps are available to measure waiting time. |

## 6. Data Analysis Summary

The analysis uses 20 appointment records, 15 patient feedback records, and 10 resource records. The findings are directional and should not be treated as representative of hospital-wide performance.

### 6.1 Appointment data

Records analysed: 20 appointments, covering 1–20 January 2024 across five departments.

| Status | Count | Share |
|---|---|---|
| Completed | 8 | 40% |
| No Show | 4 | 20% |
| Rescheduled | 4 | 20% |
| Cancelled | 4 | 20% |
| Total disrupted | 12 | 60% |

**Key findings:**

- Appointment disruption: 12 of 20 appointments (60%) did not take place as originally scheduled. The no-show and cancellation rate was 40%, while rescheduled appointments accounted for 20%. Rescheduling is reported separately because a rescheduled appointment is not necessarily a negative outcome. The data does not show whether cancelled slots were reused.

- No reliable peak-hour or department comparison: Each department has one doctor, one time slot and the same outcome across all four of its records (for example, all Cardiology appointments are Completed and all Orthopedics appointments are No Show). Department and time-slot differences therefore reflect how the sample was constructed, not actual demand or department performance.

- Double bookings: The sample contains no identifiable scheduling conflicts. However, it does not capture booking attempts or conflict records, so reported double bookings cannot be adequately assessed.

### 6.2 Patient feedback data

Records analysed: 15 feedback records. Average satisfaction score: 7.0/10.

| Score band | Definition | Count | Share |
|---|---|---|---|
| Scores ≥ 8 | 8, 9 or 10 | 6 | 40% |
| Scores ≤ 7 | 7 or below | 9 | 60% |

**Key findings:**

- The average satisfaction score was 7.0/10, with 40% of records scoring 8 or above. The two score bands are analytical groupings, not a hospital standard, so a score of 7 should not be read as low satisfaction.

- Feedback cannot be reliably linked to a specific visit or appointment outcome. In an exploratory match, 9 of the 15 feedback records share PatientID and date with an appointment recorded as No Show, Cancelled or Rescheduled. Only three records are available per department, so department-level comparisons are unreliable.

- Two of 15 feedback comments mention waiting or delay. One of them ('Long wait times') shares PatientID and date with an appointment recorded as No Show, so this is weak evidence. No comment explicitly mentions notifications or communication; those issues are supported by stakeholder profiles and the case brief instead.

### 6.3 Resource data

The dataset contains 10 resource records, with two records per resource type. Recorded usage hours and availability statuses are available, but department attribution and capacity baselines are missing.

| Resource type | Avg. recorded usage (hrs/day) | Recorded availability | Observation |
|---|---|---|---|
| Technician | 10 | Available | Highest recorded usage of the five types |
| Doctor | 8 | Available | Usage recorded while available |
| Equipment | 6 | In Use | In use in both records |
| Room | 2 | Under Maintenance | Under maintenance in both records, yet 2 usage hours are recorded; the data does not show whether status and usage cover the same period |
| Nurse | 0 | Unavailable | Zero usage reflects the ‘Unavailable’ status, not spare capacity |

### 6.4 Data limitations

| Limitation | Implication |
|---|---|
| Small samples: 20 appointment, 15 feedback, and 10 resource records | Findings are directional and suitable for descriptive analysis only; they should not be treated as representative of hospital-wide performance. |
| Repeating data patterns | Department and time-slot comparisons reflect the constructed dataset, not actual operational differences, and should not be used to compare departments. |
| Feedback not linked to an appointment | Satisfaction cannot be tied to a specific visit or appointment outcome |
| No cancellation or rescheduling reasons, timing or slot reuse | The contribution of patient-side and hospital-side factors remains unknown, and the data cannot show whether cancelled slots were reused. The sample therefore does not establish a lost-capacity rate. |
| Limited resource data and historical period | Resource utilisation cannot be established, and baseline findings need validation against current operational data. |

### 6.5 Measurement gaps and open questions

The following measures cannot be established from the available data.

| Measure | Data Gap | Data Needed |
|---|---|---|
| Patient waiting time | Check-in and consultation start times are not recorded. | Check-in time and consultation start time for each attended appointment. |
| Double bookings | Booking attempts and conflicts are not recorded. | Records of booking attempts, including attempts rejected due to conflicts. |
| Satisfaction by visit | Feedback has no appointment reference. | An appointment reference on each feedback record. |

Until these data are available, reliable baselines cannot be established for these measures. FR-16 addresses waiting-time measurement using the proposed definition: waiting time = consultation start time − check-in time. The scheduled appointment time is already held in appointment records, so delay against the scheduled time could also be reported if stakeholders confirm it is needed. The other data needs are recorded for further consideration rather than treated as confirmed functional requirements.

**Open Questions**

- Who initiates cancellations and rescheduling: patients or the hospital?

- What factors drive patient satisfaction, and how can feedback be linked to individual visits?

- What is the hospital's monthly appointment volume?

- Who records appointment delays, and at what point in the process?

- How are bookings handled and checked for conflicts when the scheduling system is unavailable?

- Does the 20% target in the case brief refer to waiting time after check-in or to delay against the scheduled appointment time? This BRD uses waiting time from check-in until this is confirmed.

- Does 'overbooked schedules' (Cardiology doctor profile) mean double-booked slots or more appointments than a consultation session can accommodate?

- Does the case brief include the discharge process? Who prepares, completes, reviews and approves the discharge summary, and which discharge information must be available to administrative staff?

- Does the case brief state an appointment-outcome objective? BR-01 is currently worded from the sample data and needs confirmation.

These questions require further clarification before the related requirements and expected benefits can be fully validated.

## 7. Business Objectives and Baseline Indicators

### 7.1 Objectives and Proposed Acceptance Criteria

The objectives below define the intended business outcomes and proposed acceptance criteria. These criteria have not been validated with stakeholders or tested in a live system. Verification approaches are proposed for future validation; implementation and UAT execution are outside the scope of this case study.

| Objective | Proposed Acceptance criterion | Verification Approach |
|---|---|---|
| Reduce patient waiting time | Reduce average patient waiting time (check-in to consultation start) by 20%, per the case brief. The target and the metric definition should be confirmed with Hospital Management (Section 6.5). | Establish a baseline using check-in and consultation start times (FR-16) before assessing the target. |
| Reduce no-shows and cancellations | Track the no-show rate and the no-show and cancellation rate, and report rescheduling separately. Set reduction targets after the operational baseline is validated. | Review appointment outcome summaries (FR-14). |
| Improve appointment accessibility | Patients can book, reschedule, and cancel online, with an assisted channel available for those who need it. | Scenario-based UAT for FR-01, FR-02, FR-05, and NFR-04. |
| Improve patient communication | Bookings and appointment changes trigger notifications; staff-recorded delays trigger delay notifications. | Scenario-based UAT for FR-07, FR-08, and FR-09. |
| Improve resource visibility | Current doctor, room, and equipment availability is displayed at the point of booking or assignment. | Scenario-based UAT for FR-03, FR-10, and FR-11. |
| Improve access to information | Authorised staff can access current patient information according to their roles, without repeated data entry. | Scenario-based UAT for FR-12, FR-13, and NFR-02. |
| Improve operational visibility | Management can view current appointment outcomes without manually preparing reports. | Reconcile the appointment outcome summary against appointment records (FR-14). |

### 7.2 Baseline indicators

The following indicators are calculated from the available sample data. They are descriptive baselines and must be validated against current operational data before performance targets are finalised.

| Indicator | Baseline (sample) | Source | Limitation |
|---|---|---|---|
| Appointment disruption rate (sample) | 60% (12/20) | Appointment data | Descriptive only. Includes rescheduled appointments, which are not necessarily negative outcomes. |
| No-show rate (sample) | 20% (4/20) | Appointment data | Represents only appointments recorded as no-shows. |
| No-show and cancellation rate (sample) | 40% (8/20) | Appointment data | Appointments recorded as No Show or Cancelled. Slot reuse is not recorded, so this is not a lost-capacity measure. |
| Average satisfaction score | 7.0 / 10 | 15 feedback records | Feedback is not reliably linked to specific visits. |
| Share of feedback records scoring ≥ 8 | 40% (6/15) | 15 feedback records | Descriptive only; not a verified hospital-wide measure. |
| Average patient waiting time (check-in to consultation start) | Not measurable | No check-in or consultation start data | A baseline is required before the 20% reduction target can be assessed. |

The case brief specifies a target of reducing average patient waiting time by 20%. This target cannot yet be evaluated because a reliable baseline is unavailable. Targets for the no-show rate and the no-show and cancellation rate should be agreed after the sample findings have been validated against operational data.

## 8. Scope

**In scope**

- Appointment Management: Booking, rescheduling, cancellation, and conflict checking.
- Patient Communication: Booking confirmations, reminders, and notifications of appointment changes or delays.
- Waiting-Time Management: Recording waiting time and addressing delays related to scheduling, resource assignment, and communication.
- Resource Visibility: Current doctor, room, and equipment availability at the point of scheduling or assignment.
- Cross-Department Information Sharing: Access to current patient information and fewer manual hand-offs between departments.
- Operational Reporting: Monitoring appointment outcomes without manual report preparation.

**Out of scope**

- System or vendor selection, technical design, development, and implementation.
- Clinical diagnosis and treatment decisions.
- Staffing-level changes and major physical infrastructure changes.

**Raised but not taken forward:** The following requests were raised but excluded from the core scope because they are outside the selected problem areas or require further analysis: referral tracking, detailed diagnostic-result handling, patient transfers, billing reconciliation, staffing and supplies, trend analytics, and a follow-up support desk. The underlying need for information to reach the next department is in scope (BR-05); the detailed workflows listed here are not.

**Solution suggestions:** The IT Manager suggested an integrated Hospital Information System and a cloud-based appointment system. These are recorded as potential solution options, not selected solutions. This case study defines business needs and required capabilities without evaluating or selecting a specific system.

## 9. Requirements

### 9.1 Business requirements

| ID | Business requirement | Addresses | Source |
|---|---|---|---|
| **BR-01** | HealthFirst Care needs to monitor appointment outcomes and reduce appointments recorded as No Show or Cancelled, while tracking rescheduled appointments separately. | PP-02, PP-03 | Appointment data (wording to be confirmed) |
| **BR-02** | Patients need an accessible and reliable way to book and change appointments online, while retaining an assisted booking channel. | PP-01 | Patient profile |
| **BR-03** | Patients need timely confirmation, reminders, and notifications of appointment changes and delays. | PP-03, PP-10 | Patient profile |
| **BR-04** | Staff need current doctor, room, and equipment availability when scheduling appointments or assigning resources. | PP-04, PP-05, PP-06 | Admin and doctor profiles; case brief |
| **BR-05** | Authorised staff need access to current patient information across departments, with fewer manual hand-offs and repeated data entry. | PP-07, PP-08 | IT, admin, doctor, and nurse profiles |
| **BR-06** | Management needs a current view of appointment performance without manually preparing reports. | PP-09 | Case brief; IT profile |
| **BR-07** | HealthFirst Care needs to measure and reduce the time patients wait between check-in and the start of their consultation. | PP-05, PP-10 | Case brief; patient profile |

### 9.2 Functional requirements

The functional requirements define the system capabilities needed to support the business requirements. Priorities, supporting evidence, and verification methods are maintained in the Requirements Traceability Matrix (RTM).

| ID | Functional Requirement | Traces to |
|---|---|---|
| **FR-01** | Patients shall be able to book appointments through an online self-service channel. | BR-02 |
| **FR-02** | Administrative staff shall be able to book, reschedule, and cancel appointments on a patient's behalf. New bookings and rescheduled appointments shall be subject to FR-04. | BR-02 |
| **FR-03** | Current doctor availability shall be displayed to patients and staff when booking appointments. | BR-04, BR-07 |
| **FR-04** | New and rescheduled appointments shall be checked against existing doctor appointments. A booking that conflicts with an existing appointment shall be rejected. | BR-01, BR-07 |
| **FR-05** | Patients shall be able to reschedule or cancel appointments through the digital channel. | BR-01, BR-02 |
| **FR-06** | A slot released by a cancellation or rescheduling shall become available for booking again. | BR-04 |
| **FR-07** | Patients shall receive confirmation when a booking, rescheduling, or cancellation request is successfully processed. | BR-03 |
| **FR-08** | Patients shall receive a reminder before their scheduled appointment. | BR-03 |
| **FR-09** | Patients shall be notified when authorised staff record a hospital-initiated appointment change, cancellation, or delay. | BR-03, BR-07 |
| **FR-10** | The current status of examination rooms and equipment shall be displayed when resources are assigned. | BR-04, BR-07 |
| **FR-11** | Authorised staff shall be able to record and update room and equipment statuses: Available, In Use, or Under Maintenance. | BR-04 |
| **FR-12** | Authorised staff across departments shall be able to access current patient information according to their assigned roles. | BR-05; NFR-02 |
| **FR-13** | Information recorded by one department shall be available to the next authorised department without repeated manual entry. For example, discharge information recorded by clinical staff shall be available to administrative staff for billing clearance. | BR-05 |
| **FR-14** | Management shall be able to view a current summary of appointment outcomes - Completed, No-show, Cancelled, and Rescheduled - without manually preparing reports. | BR-01, BR-06 |
| **FR-16** | The check-in time (when check-in is completed) and the consultation start time (when the consultation begins) shall be recorded for each attended appointment to support waiting-time measurement (waiting time = consultation start time − check-in time). | BR-07 |

**Note:** FR-15, which proposed linking patient feedback to appointments, was withdrawn because it addressed a data limitation rather than an established business requirement. The associated data need remains documented in Section 6.5, and the ID is not reused.

**Note:** FR-05 directly supports BR-02. FR-05 and FR-04 also trace to BR-01 as possible supporting mechanisms only: the available data does not establish their effect on no-show or cancellation rates (see RTM rationale).

### 9.3 Non-functional Requirements

The following non-functional requirements define proposed quality, security, and availability expectations. Verification thresholds must be confirmed where they depend on stakeholder or IT decisions.

| ID | Non-functional requirement | Verification threshold |
|---|---|---|
| **NFR-01** | Patient information shall be handled in accordance with applicable healthcare privacy and security requirements. | Compliance review completed with no critical findings. |
| **NFR-02** | Access to patient information shall be restricted according to user roles. | Each role can access only the information permitted for that role, verified through role-based test scenarios. |
| **NFR-03** | The booking channel shall be available during hospital operating hours, with the assisted channel retained as a fallback. | Proposed availability threshold: at least 99% of operating hours, subject to agreement with the IT Team. |
| **NFR-04** | The booking channel shall support unaided booking by first-time patients and use by administrative staff after basic training. | A first-time patient and a trained scheduler can each complete a standard booking without assistance during usability testing. |

## 10. Assumptions, Constraints and Dependencies

| Type | Statement | Impact if Not Met |
|---|---|---|
| **Assumption** | Stakeholders will be available to review and validate the proposed requirements. | Requirement validation and approval may be delayed. |
| **Assumption** | Patients who can use the digital channel may adopt self-service booking and appointment changes. | The expected reduction in assisted booking workload may not be achieved; the assisted channel must remain available. |
| **Assumption** | The 20% waiting-time target refers to average waiting time from check-in to consultation start. | If the target refers to delay against the scheduled appointment time, BR-07, FR-16 and the KPI definition must be updated. Scheduled times are already held in appointment records. |
| **Assumption** | The discharge scenario in the Process Analysis reflects a typical hand-off between clinical and administrative staff. It has not been validated, and the roles that prepare, complete, review or approve the discharge summary are not confirmed. | The To-Be discharge process and the FR-13 example may need revision after stakeholder review. |
| **Constraint** | Funding is limited. | Requirements must be prioritised based on business value and available resources; priorities are recorded in the RTM. |
| **Constraint** | Patient information must comply with applicable healthcare privacy and security requirements. | NFR-01 and NFR-02 must be addressed in the proposed requirements. |
| **Constraint** | Staffing levels and room capacity are outside the project scope. | Improved resource visibility may help staff identify shortages, but it does not increase available capacity. |
| **Constraint** | Time available for stakeholder review and validation may be limited. | Validation activities may need to be prioritised. |
| **Dependency** | Resource visibility depends on staff maintaining accurate and up-to-date room and equipment statuses. | FR-10 depends on the status recording and update capability in FR-11. Outdated status information may lead to incorrect resource assignments. |

**Data limitation**: Sample findings must be validated against current operational data before being used to set performance targets. See Section 6.4.

---

[← Project Overview](01-project-overview.md) · [README](../README.md) · [RTM →](03-rtm.md)
