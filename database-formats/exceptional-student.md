# 2025-26 Exceptional Student

Source: [FLDOE Database Manuals](https://www.fldoe.org/accountability/data-sys/database-manuals-updates/2025-26-student-info-system/exceptional-student.stml)
Last Updated (per source page): 7/1/2025

## Description

1. Submit this record during reporting periods 1-4 for any PK-12 student who has an Exceptionality, Primary code other than Z. Include any student who has a current individual educational plan (IEP), individual family support plan (IFSP), educational plan (EP), or services plan under the Individuals with Disabilities Education Act (IDEA) in effect. Include students enrolled in both public and private schools (including School Number, Current Enrollment of 3900 and N999) who have a current IEP, IFSP, EP or services plan under IDEA. If the student does not have one of these plans, do not report the student on this format.
2. For reporting period 5, submit this record for any PK-12 student who, during the school year just ended, was in membership at any time during the year and had an Exceptionality, Primary code other than Z. For any student dismissed from all programs during the year, report the last Exceptionality, Primary and Exceptionality, Other the student was placed in prior to dismissal. Also report this record in Survey Period 5 for any student who is not already an Exceptional Student and 1) was referred but is pending evaluation, 2) was evaluated and pending eligibility determination, 3) was evaluated and determined ineligible, or 4) was determined eligible but has not been placed (Exceptional Student Placement Status = R, E, I, or N).
3. YEAR: For reporting periods 1-4 this field must contain the fiscal year. For reporting period 5 this field must contain the school year.
4. EXCEPTIONAL STUDENT, DISMISSAL DATE: Report the most recent Exceptional Student, Dismissal Date in Survey 5 for any student who has exited all Exceptional Education programs during the school year and is no longer receiving special education and related services.
5. TIME, TOTAL SCHOOL WEEK AND TIME WITH NON-DISABLED PEERS are reported only in Survey 2. For all other surveys, zero-fill these fields. Also, zero-fill these fields for students whose only exceptionality is gifted (code L).
6. EXCEPTIONAL STUDENT, IDEA EDUCATIONAL ENVIRONMENTS: Report only in Survey 2. For all other Surveys, Z-fill this field.
7. ALTERNATE ASSESSMENT ADMINISTERED is only reported in Surveys 2 and 3. For all other surveys, Z-fill this field.
8. ERROR CODES: This field is used by the Department to report to districts the specific errors found in the record during the state edit process. This field should contain filler (spaces, blanks) when the record is transmitted to the Department.
9. KEY FIELDS: The key fields for this format are item numbers 1, 4, 5 and 16. If a key field needs to be changed, the record must be deleted and re-submitted as an add.

`*` indicates key fields.

## Record Layout

| Item No. | From-To | Size | Field Char. | Field Description |
|---|---|---|---|---|
| 1 | 1-2 | 2 | N/R | District Number, Current Enrollment * |
| 2 | 3-6 | 4 | A/N/R | School Number, Current Enrollment |
| 3 | 7-16 | 10 | A/N | Filler |
| 4 | 17-17 | 1 | A/N | Survey Period Code * |
| 5 | 18-21 | 4 | N | Year * |
| 6 | 22-26 | 5 | A/N | Filler |
| 7 | 27-27 | 1 | A | Exceptional Student, IDEA Educational Environments |
| 8 | 28-28 | 1 | A | Exceptionality, Primary |
| 9 | 29-29 | 1 | A | Alternate Assessment Administered |
| 10 | 30-30 | 1 | A | Gifted Eligibility |
| 11 | 31-34 | 4 | N | Time, Total School Week |
| 12 | 35-38 | 4 | N | Time With Non-Disabled Peers |
| 13 | 39-55 | 17 | A/N | Filler |
| 14 | 56-56 | 1 | A | Transaction Code |
| 15 | 57-59 | 3 | A/N | Filler |
| 16 | 60-73 | 14 | A/N | Florida Education Identifier * |
| 17 | 74-81 | 8 | N | Exceptional Student, Dismissal Date |
| 18 | 82-89 | 8 | N | Exceptional Student Plan Date |
| 19 | 90-90 | 1 | A | Exceptional Student Placement Status |
| 20 | 91-91 | 1 | A | Exceptional Student Referral Reason |
| 21 | 92-99 | 8 | N | Evaluation Completion Date |
| 22 | 100-107 | 8 | N | Exceptional Student Placement Date |
| 23 | 108-115 | 8 | N | Exceptional Student Eligibility Determination Date |
| 24 | 116-123 | 8 | N | Evaluation Consent Date |
| 25 | 124-124 | 1 | A | Exceptional Student, 60-Day Exception/Extension |
| 26 | 125-125 | 1 | A/N | Filler |
| 27 | 126-135 | 10 | A/N | Student Number Identifier, Local |
| 28 | 136-143 | 8 | A/N | Filler |
| 29 | 144-152 | 9 | A/L | Exceptionality, Other |
| 30 | 153-160 | 8 | A/N | Filler/Error Codes |

## Data Element Reference Notes

- Key fields for record matching: items 1, 4, 5, 16
- Survey-specific reporting: Time, Total School Week and Time With Non-Disabled Peers report only in Survey 2 (zero-fill otherwise, and zero-fill for gifted-only students); IDEA Educational Environments reports only in Survey 2 (Z-fill otherwise); Alternate Assessment Administered reports only in Surveys 2 and 3 (Z-fill otherwise)
