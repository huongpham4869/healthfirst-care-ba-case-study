# Data

The three sample datasets provided with the case brief. They are used in the [Data Analysis](../docs/06-data-analysis.md) and in [BRD Section 6](../docs/02-brd.md#6-data-analysis-summary).

> **Small sample.** The files hold 20, 15 and 10 records. The findings are directional baselines, not hospital-wide performance. The cleaned and linked analysis, with the dashboard, is on the [Data Analysis](../docs/06-data-analysis.md) page.

## Files

| File | Records | Period | Content |
|---|---|---|---|
| [`appointment_data.csv`](appointment_data.csv) | 20 | 1–20 January 2024 | Appointments by patient, doctor, department, date, time and status |
| [`feedback_data.csv`](feedback_data.csv) | 15 | 1–15 January 2024 | Patient satisfaction score and comment by department |
| [`resource_data.csv`](resource_data.csv) | 10 | 1–10 January 2024 | Recorded availability and usage hours of doctors, nurses, equipment, rooms and technicians |

Dates use the DD-MM-YY format of the source files (for example, `13-01-24` = 13 January 2024).

## Columns

**appointment_data.csv**

| Column | Values |
|---|---|
| `AppointmentID`, `PatientID`, `DoctorID` | Identifiers |
| `Department` | Cardiology, Orthopedics, Neurology, Pediatrics, General |
| `Date` | DD-MM-YY |
| `Time` | For example `10:00 AM`, `2:00 PM` |
| `Status` | Completed, No Show, Rescheduled, Cancelled |

**feedback_data.csv**

| Column | Values |
|---|---|
| `FeedbackID`, `PatientID` | Identifiers (no `AppointmentID`) |
| `Department` | Same five departments |
| `SatisfactionScore` | Score out of 10 |
| `Comments` | Free text |
| `Date` | DD-MM-YY |

**resource_data.csv**

| Column | Values |
|---|---|
| `ResourceID` | Identifier |
| `ResourceType` | Doctor, Nurse, Equipment, Room, Technician (two records each) |
| `Availability` | Available, Unavailable, In Use, Under Maintenance |
| `UsageHours` | Recorded usage hours |
| `Date` | DD-MM-YY |

## What the data cannot show

- **Waiting time:** check-in and consultation start times are not recorded, so a waiting-time baseline cannot be calculated.
- **Double bookings:** booking attempts and conflicts are not recorded.
- **Satisfaction by visit:** feedback has no appointment reference, so it cannot be reliably tied to a specific visit.
- **Reasons and slot reuse:** cancellation and rescheduling reasons are not recorded, and the data does not show whether cancelled slots were reused.
- **Department comparisons:** each department has one doctor, one time slot and the same outcome across all four of its appointments, so department and time-slot differences reflect how the sample was constructed.
- **Capacity:** the resource data has no department field and no capacity baseline, so usage hours are not a utilisation rate.

The full list is in [BRD Section 6.4](../docs/02-brd.md#64-data-limitations) and [6.5](../docs/02-brd.md#65-measurement-gaps-and-open-questions).
