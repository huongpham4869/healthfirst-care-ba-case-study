# Requirements Traceability Matrix (RTM)

*HealthFirst Care - Requirement source, evidence, related data, priority and verification*

[← BRD](02-brd.md) · [README](../README.md) · [Stakeholder Analysis →](04-stakeholder-analysis.md)

---

26 active requirements: 7 business, 15 functional and 4 non-functional, plus 1 withdrawn (FR-15). Each requirement has a MoSCoW priority with a rationale, supporting evidence, an evidence type and a verification method. The requirement wording is also in the [BRD](02-brd.md#9-requirements).

## Summary

| MoSCoW priority | BR | FR | NFR | Total |
|---|---|---|---|---|
| Must Have | 5 | 11 | 3 | 19 |
| Should Have | 2 | 4 | 1 | 7 |
| **Total** | **7** | **15** | **4** | **26** |

| Evidence type | Requirements |
|---|---|
| Data | 3 |
| Data + Elicitation | 7 |
| Elicitation | 12 |
| Case brief | 3 |
| Constraint | 1 |

Status: 26 Proposed (not yet validated by stakeholders).

## Requirement list

| ID | Requirement | Traces to | Priority | Evidence type | Status |
|---|---|---|---|---|---|
| [BR-01](#br-01) | HealthFirst Care needs to monitor appointment outcomes and reduce appointments recorded as No Show or Cancelled, while tracking rescheduled appointments separately. | PP-02; PP-03 | Must Have | Data | Proposed |
| [BR-02](#br-02) | Patients need an accessible and reliable way to book and change appointments online, while retaining an assisted booking channel. | PP-01 | Must Have | Elicitation | Proposed |
| [BR-03](#br-03) | Patients need timely confirmation, reminders, and notifications of appointment changes and delays. | PP-03; PP-10 | Must Have | Data + Elicitation | Proposed |
| [BR-04](#br-04) | Staff need current doctor, room, and equipment availability when scheduling appointments or assigning resources. | PP-04; PP-05; PP-06 | Must Have | Data + Elicitation | Proposed |
| [BR-05](#br-05) | Authorised staff need access to current patient information across departments, with fewer manual hand-offs and repeated data entry. | PP-07; PP-08 | Should Have | Elicitation | Proposed |
| [BR-06](#br-06) | Management needs a current view of appointment performance without manually preparing reports. | PP-09 | Should Have | Case brief | Proposed |
| [BR-07](#br-07) | HealthFirst Care needs to measure and reduce the time patients wait between check-in and the start of their consultation. | PP-05; PP-10 | Must Have | Data + Elicitation | Proposed |
| [FR-01](#fr-01) | Patients shall be able to book appointments through an online self-service channel. | BR-02 | Must Have | Elicitation | Proposed |
| [FR-02](#fr-02) | Administrative staff shall be able to book, reschedule, and cancel appointments on a patient's behalf. New bookings and rescheduled appointments shall be subject to FR-04. | BR-02 | Must Have | Elicitation | Proposed |
| [FR-03](#fr-03) | Current doctor availability shall be displayed to patients and staff when booking appointments. | BR-04; BR-07 | Must Have | Elicitation | Proposed |
| [FR-04](#fr-04) | New and rescheduled appointments shall be checked against existing doctor appointments. A booking that conflicts with an existing appointment shall be rejected. | BR-01; BR-07 | Must Have | Elicitation | Proposed |
| [FR-05](#fr-05) | Patients shall be able to reschedule or cancel appointments through the digital channel. | BR-01; BR-02 | Must Have | Data + Elicitation | Proposed |
| [FR-06](#fr-06) | A slot released by a cancellation or rescheduling shall become available for booking again. | BR-04 | Should Have | Data | Proposed |
| [FR-07](#fr-07) | Patients shall receive confirmation when a booking, rescheduling, or cancellation request is successfully processed. | BR-03 | Must Have | Case brief | Proposed |
| [FR-08](#fr-08) | Patients shall receive a reminder before their scheduled appointment. | BR-03 | Must Have | Data + Elicitation | Proposed |
| [FR-09](#fr-09) | Patients shall be notified when authorised staff record a hospital-initiated appointment change, cancellation, or delay. | BR-03; BR-07 | Must Have | Elicitation | Proposed |
| [FR-10](#fr-10) | The current status of examination rooms and equipment shall be displayed when resources are assigned. | BR-04; BR-07 | Must Have | Data + Elicitation | Proposed |
| [FR-11](#fr-11) | Authorised staff shall be able to record and update room and equipment statuses: Available, In Use, or Under Maintenance. | BR-04 | Must Have | Data | Proposed |
| [FR-12](#fr-12) | Authorised staff across departments shall be able to access current patient information according to their assigned roles. | BR-05; NFR-02 | Should Have | Elicitation | Proposed |
| [FR-13](#fr-13) | Information recorded by one department shall be available to the next authorised department without repeated manual entry. For example, discharge information recorded by clinical staff shall be available to administrative staff for billing clearance. | BR-05 | Should Have | Elicitation | Proposed |
| [FR-14](#fr-14) | Management shall be able to view a current summary of appointment outcomes - Completed, No-show, Cancelled, and Rescheduled - without manually preparing reports. | BR-01; BR-06 | Should Have | Case brief | Proposed |
| [FR-15](#fr-15) | Record patient feedback against the appointment it relates to | - | Could Have | Data | Withdrawn |
| [FR-16](#fr-16) | The check-in time (when check-in is completed) and the consultation start time (when the consultation begins) shall be recorded for each attended appointment to support waiting-time measurement (waiting time = consultation start time − check-in time). | BR-07 | Must Have | Data + Elicitation | Proposed |
| [NFR-01](#nfr-01) | Patient information shall be handled in accordance with applicable healthcare privacy and security requirements. | BR-02; BR-03; BR-05 | Must Have | Constraint | Proposed |
| [NFR-02](#nfr-02) | Access to patient information shall be restricted according to user roles. | BR-05 | Must Have | Elicitation | Proposed |
| [NFR-03](#nfr-03) | The booking channel shall be available during hospital operating hours, with the assisted channel retained as a fallback. | BR-02 | Should Have | Elicitation | Proposed |
| [NFR-04](#nfr-04) | The booking channel shall support unaided booking by first-time patients and use by administrative staff after basic training. | BR-02 | Must Have | Elicitation | Proposed |

## Requirement details

### BR-01

**HealthFirst Care needs to monitor appointment outcomes and reduce appointments recorded as No Show or Cancelled, while tracking rescheduled appointments separately.**

- **Traces to:** PP-02; PP-03
- **Source / stakeholder:** Hospital Management; Admin Staff
- **Priority (MoSCoW):** Must Have
- **Prioritisation rationale:** The sample records 40% of appointments as No Show or Cancelled, but it is too small to set a reliable target, and slot reuse is not recorded. Rescheduling is tracked separately because a rescheduled appointment is not necessarily a negative outcome.
- **Supporting evidence:** 8 of 20 sampled appointments (40%) were recorded as No Show (20%) or Cancelled (20%); a further 20% were rescheduled. Cancellation reasons and slot reuse are not recorded.
- **Related data file:** appointment_data
- **Evidence type:** Data
- **Verification method:** Track the no-show rate and the no-show and cancellation rate against a validated operational baseline (FR-14), and report rescheduling separately. Agree reduction targets after the baseline is confirmed.
- **Status:** Proposed

### BR-02

**Patients need an accessible and reliable way to book and change appointments online, while retaining an assisted booking channel.**

- **Traces to:** PP-01
- **Source / stakeholder:** Patients
- **Priority (MoSCoW):** Must Have
- **Prioritisation rationale:** Removes the access barrier patients report; the assisted channel keeps access for patients who prefer not to book online
- **Supporting evidence:** Patients report difficulty booking online and fall back on calling the hospital or booking in person
- **Related data file:** -
- **Evidence type:** Elicitation
- **Verification method:** Patients can book, reschedule and cancel online; patients who cannot are served by admin staff (FR-02)
- **Status:** Proposed

### BR-03

**Patients need timely confirmation, reminders, and notifications of appointment changes and delays.**

- **Traces to:** PP-03; PP-10
- **Source / stakeholder:** Patients
- **Priority (MoSCoW):** Must Have
- **Prioritisation rationale:** Targets the communication gap identified in RCA Section 5.1; the link to the no-show rate rests on elicitation and is not proven by the data
- **Supporting evidence:** Patient profiles report cancellations without timely notice and no updates during delays. The 20% no-show rate is contextual evidence only and does not establish communication as the cause.
- **Related data file:** appointment_data
- **Evidence type:** Data + Elicitation
- **Verification method:** Verify that successful bookings, rescheduling, and cancellations generate confirmations; reminders are sent at the agreed lead time; and staff-recorded hospital-initiated changes or delays trigger notifications (FR-07 to FR-09).
- **Status:** Proposed

### BR-04

**Staff need current doctor, room, and equipment availability when scheduling appointments or assigning resources.**

- **Traces to:** PP-04; PP-05; PP-06
- **Source / stakeholder:** Admin Staff; Nurses; Doctors
- **Priority (MoSCoW):** Must Have
- **Prioritisation rationale:** Current doctor availability supports scheduling and conflict prevention; room and equipment status supports resource assignment.
- **Supporting evidence:** Administrative staff report limited visibility of doctor availability. The Cardiology doctor profile reports diagnostic equipment unavailable at peak hours, and the As-Is check-in process shows rooms assigned without current status. Operating-room and emergency-bed issues in other profiles belong to different workflows. Resource records show recorded statuses but do not establish peak-time shortages.
- **Related data file:** resource_data
- **Evidence type:** Data + Elicitation
- **Verification method:** Current availability is shown at the point of booking and at the point of assignment
- **Status:** Proposed

### BR-05

**Authorised staff need access to current patient information across departments, with fewer manual hand-offs and repeated data entry.**

- **Traces to:** PP-07; PP-08
- **Source / stakeholder:** Admin Staff; Doctors; Nurses; IT Team
- **Priority (MoSCoW):** Should Have
- **Prioritisation rationale:** Addresses the coordination gap in RCA Section 5.2; rests on elicitation only, so it ranks below the waiting-time, appointment and resource needs
- **Supporting evidence:** Scheduling and record systems are not integrated (IT Manager); late test results, cumbersome referrals and transfer hand-offs (doctors, nurses); billing records hard to reconcile with treatment data (Billing Administrator). These workflows show the gap; their detailed redesign is out of scope.
- **Related data file:** -
- **Evidence type:** Elicitation
- **Verification method:** Proposed verification: In the illustrative discharge scenario, confirm that authorised administrative staff can access the discharge information needed for billing clearance without repeated manual entry, subject to role-based access permissions (NFR-02). Validate the scenario, required information, and access rules with stakeholders before approving the requirement. This verification has not been executed.
- **Status:** Proposed

### BR-06

**Management needs a current view of appointment performance without manually preparing reports.**

- **Traces to:** PP-09
- **Source / stakeholder:** Case brief
- **Priority (MoSCoW):** Should Have
- **Prioritisation rationale:** Needed to track the baseline indicators over time; manual reporting can continue in the meantime
- **Supporting evidence:** The case brief states that operational reporting is manual and management lacks a current view of performance.
- **Related data file:** -
- **Evidence type:** Case brief
- **Verification method:** Management can view appointment outcomes without a manually prepared report
- **Status:** Proposed

### BR-07

**HealthFirst Care needs to measure and reduce the time patients wait between check-in and the start of their consultation.**

- **Traces to:** PP-05; PP-10
- **Source / stakeholder:** Patients; Hospital Management
- **Priority (MoSCoW):** Must Have
- **Prioritisation rationale:** The first goal named in the case brief and the main frustration patients report. The requirements address waits linked to double booking and to assigning rooms without knowing their status; waits caused by session overbooking, staffing or room capacity are not resolved by these requirements
- **Supporting evidence:** Patients report waits of more than 30 minutes past the appointment time and nearly an hour in one case (elicitation); 2 of 15 feedback comments mention waiting or delay, one of them on the same date as the patient's No Show appointment (data)
- **Related data file:** appointment_data; feedback_data
- **Evidence type:** Data + Elicitation
- **Verification method:** Calculate average waiting time per attended appointment as consultation start time − check-in time. Compare the result against a validated operational baseline to assess the 20% reduction target, after Hospital Management confirms the metric definition.
- **Status:** Proposed

### FR-01

**Patients shall be able to book appointments through an online self-service channel.**

- **Traces to:** BR-02
- **Source / stakeholder:** Patients; IT Team
- **Priority (MoSCoW):** Must Have
- **Prioritisation rationale:** An online system exists, but patients cannot use it reliably, so BR-02 is not met today
- **Supporting evidence:** Patients report difficulty booking online and often call instead; the IT Team confirms the interface is not user-friendly
- **Related data file:** -
- **Evidence type:** Elicitation
- **Verification method:** UAT: A patient completes a valid online booking end-to-end using an available slot. Usability without assistance is assessed separately under NFR-04.
- **Status:** Proposed

### FR-02

**Administrative staff shall be able to book, reschedule, and cancel appointments on a patient's behalf. New bookings and rescheduled appointments shall be subject to FR-04.**

- **Traces to:** BR-02
- **Source / stakeholder:** Patients; Admin Staff
- **Priority (MoSCoW):** Must Have
- **Prioritisation rationale:** Keeps access for patients who prefer not to book online; without it BR-02 would exclude the patients it is meant to help
- **Supporting evidence:** One patient profile finds online scheduling confusing and prefers in-person scheduling
- **Related data file:** -
- **Evidence type:** Elicitation
- **Verification method:** UAT: Administrative staff can create, reschedule, and cancel appointments on behalf of a patient. New and rescheduled appointments undergo the FR-04 conflict check.
- **Status:** Proposed

### FR-03

**Current doctor availability shall be displayed to patients and staff when booking appointments.**

- **Traces to:** BR-04; BR-07
- **Source / stakeholder:** Admin Staff; Doctors
- **Priority (MoSCoW):** Must Have
- **Prioritisation rationale:** Makes current doctor availability visible at booking. FR-04 remains the control that rejects conflicting bookings.
- **Supporting evidence:** Admin staff report limited visibility of doctors' real-time availability, leading to scheduling conflicts
- **Related data file:** -
- **Evidence type:** Elicitation
- **Verification method:** UAT: Current doctor availability is displayed at booking, and unavailable slots are not presented as bookable. Verify conflict rejection separately under FR-04.
- **Status:** Proposed

### FR-04

**New and rescheduled appointments shall be checked against existing doctor appointments. A booking that conflicts with an existing appointment shall be rejected.**

- **Traces to:** BR-01; BR-07
- **Source / stakeholder:** Admin Staff; Doctors
- **Priority (MoSCoW):** Must Have
- **Prioritisation rationale:** Prevents the double bookings reported by administrative staff. Linked to BR-01 because inconsistent conflict checks are a possible hospital-side factor in cancellations and rescheduling (RCA Section 5.1); this effect is not established. It does not limit how many appointments a session holds; whether 'overbooked schedules' needs a capacity rule is an open question (BRD Section 6.5).
- **Supporting evidence:** Admin staff report frequent double bookings; the sample contains no double booking, so the data cannot confirm how often it happens
- **Related data file:** appointment_data
- **Evidence type:** Elicitation
- **Verification method:** UAT: A booking attempt for a slot already occupied by the same doctor is rejected; a non-conflicting available slot can be booked.
- **Status:** Proposed

### FR-05

**Patients shall be able to reschedule or cancel appointments through the digital channel.**

- **Traces to:** BR-01; BR-02
- **Source / stakeholder:** Patients
- **Priority (MoSCoW):** Must Have
- **Prioritisation rationale:** Directly supports BR-02: patients can change an appointment without phone or in-person contact. Also traced to BR-01 as a possible supporting mechanism: digital rescheduling may help some patients change appointments rather than miss them, but its effect on no-show and cancellation rates has not been established by the available data.
- **Supporting evidence:** 20% cancelled and 20% rescheduled appointments (data); patients fall back on calling the hospital (elicitation)
- **Related data file:** appointment_data
- **Evidence type:** Data + Elicitation
- **Verification method:** UAT: a patient reschedules and cancels without telephone contact
- **Status:** Proposed

### FR-06

**A slot released by a cancellation or rescheduling shall become available for booking again.**

- **Traces to:** BR-04
- **Source / stakeholder:** Admin Staff; Patients
- **Priority (MoSCoW):** Should Have
- **Prioritisation rationale:** Keeps displayed availability current after a cancellation or reschedule, so the slot can be booked again (BR-04). The data does not show whether released slots are currently reused.
- **Supporting evidence:** 20% cancelled and 20% rescheduled appointments
- **Related data file:** appointment_data
- **Evidence type:** Data
- **Verification method:** UAT: a cancelled slot can be booked by another patient
- **Status:** Proposed

### FR-07

**Patients shall receive confirmation when a booking, rescheduling, or cancellation request is successfully processed.**

- **Traces to:** BR-03
- **Source / stakeholder:** Patients
- **Priority (MoSCoW):** Must Have
- **Prioritisation rationale:** The current booking process ends without a confirmation to the patient
- **Supporting evidence:** The case brief describes the current scheduling process as lacking notifications; no profile mentions receiving a confirmation
- **Related data file:** -
- **Evidence type:** Case brief
- **Verification method:** UAT: Successful booking, rescheduling, and cancellation each trigger a confirmation. Failed requests do not generate a success confirmation.
- **Status:** Proposed

### FR-08

**Patients shall receive a reminder before their scheduled appointment.**

- **Traces to:** BR-03
- **Source / stakeholder:** Patients; IT Team
- **Priority (MoSCoW):** Must Have
- **Prioritisation rationale:** Part of the patient communication need (BR-03): the current process ends without a reminder, and patients report not being kept informed. The priority rests on this gap, not on a proven link to no-shows; the 20% sample no-show rate is context only.
- **Supporting evidence:** The case brief describes the current scheduling process as lacking notifications; a patient prefers instructions by email or SMS and the developer suggests email/SMS notifications (elicitation); 20% sample no-show rate (context only)
- **Related data file:** appointment_data
- **Evidence type:** Data + Elicitation
- **Verification method:** Verify that reminders are sent at the agreed lead time (24 hours proposed) and that delivery status is recorded. Confirm the lead time with stakeholders.
- **Status:** Proposed

### FR-09

**Patients shall be notified when authorised staff record a hospital-initiated appointment change, cancellation, or delay.**

- **Traces to:** BR-03; BR-07
- **Source / stakeholder:** Patients
- **Priority (MoSCoW):** Must Have
- **Prioritisation rationale:** Addresses the notification gap patients report; supported by elicitation only, as no feedback comment mentions communication
- **Supporting evidence:** Patients report appointments cancelled without timely notice and no updates during delays
- **Related data file:** -
- **Evidence type:** Elicitation
- **Verification method:** UAT: Each recorded hospital-initiated cancellation or change, and each recorded delay, triggers a patient notification. Agree any delivery-time threshold before approval.
- **Status:** Proposed

### FR-10

**The current status of examination rooms and equipment shall be displayed when resources are assigned.**

- **Traces to:** BR-04; BR-07
- **Source / stakeholder:** Nurses; Doctors
- **Priority (MoSCoW):** Must Have
- **Prioritisation rationale:** Supports resource assignment using current recorded status. Its effectiveness depends on FR-11 keeping status information up to date.
- **Supporting evidence:** The Cardiology doctor profile reports diagnostic equipment unavailable at peak hours; the As-Is check-in process assigns rooms without current status. Resource records provide status snapshots but do not establish peak-time shortages.
- **Related data file:** resource_data
- **Evidence type:** Data + Elicitation
- **Verification method:** UAT: Current room and equipment status is displayed at assignment. Resources marked In Use or Under Maintenance cannot be assigned, and saved status updates become visible.
- **Status:** Proposed

### FR-11

**Authorised staff shall be able to record and update room and equipment statuses: Available, In Use, or Under Maintenance.**

- **Traces to:** BR-04
- **Source / stakeholder:** Nurses; Admin Staff
- **Priority (MoSCoW):** Must Have
- **Prioritisation rationale:** FR-10 depends on accurate, up-to-date resource status. The requirement does not assume automatic status detection.
- **Supporting evidence:** The resource sample holds one status per record with no history of changes; two Room records show 'Under Maintenance' with usage hours, so the timing of status updates is unclear
- **Related data file:** resource_data
- **Evidence type:** Data
- **Verification method:** Verify that a status change entered by authorised staff is saved with its update timestamp and is reflected in the displayed status.
- **Status:** Proposed

### FR-12

**Authorised staff across departments shall be able to access current patient information according to their assigned roles.**

- **Traces to:** BR-05; NFR-02
- **Source / stakeholder:** Admin Staff; Doctors; Nurses
- **Priority (MoSCoW):** Should Have
- **Prioritisation rationale:** Removes re-entry and late information between departments; supported by elicitation only
- **Supporting evidence:** The patient record system is reported as outdated and slow at busy times; scheduling and record systems are not integrated
- **Related data file:** -
- **Evidence type:** Elicitation
- **Verification method:** UAT: authorised staff in two departments see the same current patient record
- **Status:** Proposed

### FR-13

**Information recorded by one department shall be available to the next authorised department without repeated manual entry. For example, discharge information recorded by clinical staff shall be available to administrative staff for billing clearance.**

- **Traces to:** BR-05
- **Source / stakeholder:** Doctors; Nurses; Admin Staff
- **Priority (MoSCoW):** Should Have
- **Prioritisation rationale:** Removes the manual hand-off shown in the illustrative As-Is discharge scenario; a manual workaround exists today
- **Supporting evidence:** Doctors and nurses report delays in receiving results and inefficient hand-offs between departments
- **Related data file:** -
- **Evidence type:** Elicitation
- **Verification method:** UAT (discharge scenario): after clinical staff record discharge information, administrative staff can view it for billing clearance without re-entering it.
- **Status:** Proposed

### FR-14

**Management shall be able to view a current summary of appointment outcomes - Completed, No-show, Cancelled, and Rescheduled - without manually preparing reports.**

- **Traces to:** BR-01; BR-06
- **Source / stakeholder:** Hospital Management
- **Priority (MoSCoW):** Should Have
- **Prioritisation rationale:** The minimum reporting needed to monitor appointment outcomes (BR-01) and track the baseline indicators (BR-06); manual reporting can continue in the meantime
- **Supporting evidence:** The case brief states that reporting is manual and that management wants to track performance
- **Related data file:** appointment_data
- **Evidence type:** Case brief
- **Verification method:** Summary figures match the underlying appointment records for the same period
- **Status:** Proposed

### FR-15

**Record patient feedback against the appointment it relates to**

- **Traces to:** -
- **Source / stakeholder:** Hospital Management; Patients
- **Priority (MoSCoW):** Could Have
- **Prioritisation rationale:** Withdrawn: addresses a data limitation, not a business need. Kept as a data need (BRD Section 6.5); the ID is not reused
- **Supporting evidence:** Feedback data has no AppointmentID. In an exploratory match, 9 of 15 feedback records share PatientID and date with an appointment recorded as No Show, Cancelled or Rescheduled.
- **Related data file:** feedback_data; appointment_data
- **Evidence type:** Data
- **Verification method:** -
- **Status:** Withdrawn

### FR-16

**The check-in time (when check-in is completed) and the consultation start time (when the consultation begins) shall be recorded for each attended appointment to support waiting-time measurement (waiting time = consultation start time − check-in time).**

- **Traces to:** BR-07
- **Source / stakeholder:** Hospital Management; Patients
- **Priority (MoSCoW):** Must Have
- **Prioritisation rationale:** Required to establish and monitor the 20% waiting-time target. The current data does not contain the timestamps needed to calculate a baseline.
- **Supporting evidence:** Patients report waits of more than 30 minutes past the appointment time (elicitation); no dataset records check-in or consultation start times (data)
- **Related data file:** appointment_data; feedback_data
- **Evidence type:** Data + Elicitation
- **Verification method:** For each attended appointment, check that the check-in time is recorded when check-in is completed and the consultation start time when the consultation begins, then calculate waiting time = consultation start time − check-in time. Verify that the average can be produced for a defined reporting period.
- **Status:** Proposed

### NFR-01

**Patient information shall be handled in accordance with applicable healthcare privacy and security requirements.**

- **Traces to:** BR-02; BR-03; BR-05
- **Source / stakeholder:** IT Team; Hospital Management
- **Priority (MoSCoW):** Must Have
- **Prioritisation rationale:** Regulatory obligation; not negotiable regardless of budget
- **Supporting evidence:** Privacy and security compliance is a stated constraint (BRD Section 10)
- **Related data file:** -
- **Evidence type:** Constraint
- **Verification method:** Compliance review completed with no critical findings
- **Status:** Proposed

### NFR-02

**Access to patient information shall be restricted according to user roles.**

- **Traces to:** BR-05
- **Source / stakeholder:** IT Team
- **Priority (MoSCoW):** Must Have
- **Prioritisation rationale:** Needed before patient information is shared across departments under FR-12
- **Supporting evidence:** The IT Team reports security vulnerabilities in the legacy systems that need urgent attention
- **Related data file:** -
- **Evidence type:** Elicitation
- **Verification method:** UAT: each role can see only the information it is permitted to see
- **Status:** Proposed

### NFR-03

**The booking channel shall be available during hospital operating hours, with the assisted channel retained as a fallback.**

- **Traces to:** BR-02
- **Source / stakeholder:** IT Team
- **Priority (MoSCoW):** Should Have
- **Prioritisation rationale:** Supports reliable access to online booking. The assisted channel serves patients who need help using self-service; its ability to handle system outages must be confirmed separately.
- **Supporting evidence:** The IT Manager reports frequent network downtime affecting online services; no availability baseline exists
- **Related data file:** -
- **Evidence type:** Elicitation
- **Verification method:** Measure online booking-channel availability monthly against a stakeholder-approved threshold. The proposed 99% target remains subject to confirmation.
- **Status:** Proposed

### NFR-04

**The booking channel shall support unaided booking by first-time patients and use by administrative staff after basic training.**

- **Traces to:** BR-02
- **Source / stakeholder:** Patients; IT Team
- **Priority (MoSCoW):** Must Have
- **Prioritisation rationale:** Addresses the root cause of PP-01: a channel that is hard to use sends patients back to the phone, which is what happens today
- **Supporting evidence:** Patients find the online scheduling system confusing; the IT Team reports the interface is not user-friendly
- **Related data file:** -
- **Evidence type:** Elicitation
- **Verification method:** Usability testing: A first-time patient completes a standard online booking without help. An administrative scheduler completes the same task after basic training without additional IT support.
- **Status:** Proposed

---

[← BRD](02-brd.md) · [README](../README.md) · [Stakeholder Analysis →](04-stakeholder-analysis.md)
