# 2025-26 Student Discipline/Resultant Action

Source: [FLDOE Database Manuals](https://www.fldoe.org/accountability/data-sys/database-manuals-updates/2025-26-student-info-system/student-discipline-resultant-action.stml)
Last Updated (per source page): 7/1/2025

## Description

1. Submit this record during reporting periods 2, 3, and 5 for each student receiving a discipline/resultant action from the first day of the school year to the last day of the survey period. Report all discipline/resultant actions and total duration days that resulted from any incident that occurred during the school year or the subsequent summer session(s) even if the discipline/resultant action is intended to begin in the next school year. Submit a separate record for each occurrence of the discipline/resultant action. A Student Discipline/Resultant Action record should not be submitted for SESIR incidents with an Incident, Involvement Type of N or U.

   For reporting period R, submit this record monthly for students with related incidents reported on the SESIR format.
2. INCIDENT, IDENTIFIER: If the discipline/resultant action is related to a School Environmental Safety Incident Report (SESIR) item then the Incident, Identifier and the School Number, Where Incident Occurred should be the same on both records.
3. GRADE LEVEL: Use the grade level of the student at the time the incident occurred.
4. SCHOOL YEAR: For Survey Period R, data element "School Year" should be reported in terms of "Month and Year". "Month and Year" as in, for example, January 2024 would be 0124.
5. ERROR CODES: This field is used by the Department to report to districts the specific errors found in the record during the state edit process. This field should contain filler (spaces, blanks) when the record is transmitted to the Department.
6. KEY FIELDS: The key fields for this format are item numbers 1, 4, 5, 6, 7, 9 and 29. If a key field needs to be changed, the record must be deleted and re-submitted as an add.

`*` indicates key fields.

## Record Layout

| Item No. | From-To | Size | Field Char. | Field Description |
|---|---|---|---|---|
| 1 | 1-2 | 2 | N/R | District Number, Current Enrollment * |
| 2 | 3-6 | 4 | A/N/R | School Number, Current Enrollment |
| 3 | 7-16 | 10 | A/N | Filler |
| 4 | 17-17 | 1 | N | Survey Period Code * |
| 5 | 18-21 | 4 | N | School Year * |
| 6 | 22-22 | 1 | A | Discipline/Resultant Action Code * |
| 7 | 23-26 | 4 | N | School Number, Where Discipline/Resultant Action Occurred * |
| 8 | 27-27 | 1 | A | Transaction Code |
| 9 | 28-35 | 8 | A/N | Incident, Identifier * |
| 10 | 36-43 | 8 | A/N | Incident, Date |
| 11 | 44-46 | 3 | N | Duration, Discipline Action |
| 12 | 47-47 | 1 | A | Filler |
| 13 | 48-48 | 1 | A | Student, Involved in Hate Crime |
| 14 | 49-49 | 1 | A | Student, Use of Alcohol |
| 15 | 50-50 | 1 | A | Student, Use of Drugs |
| 16 | 51-51 | 1 | A | Student, Weapon Use |
| 17 | 52-53 | 2 | A/N | Grade Level |
| 18 | 54-54 | 1 | A | Filler |
| 19 | 55-55 | 1 | A | Sex |
| 20 | 56-63 | 8 | N | Birth Date |
| 21 | 64-64 | 1 | A/N | Lunch Status |
| 22 | 65-66 | 2 | A | English Language Learner, PK-12 |
| 23 | 67-70 | 4 | A/N | School Number, Where Incident Occurred |
| 24 | 71-72 | 2 | N/R | District Number, Where Incident Occurred |
| 25 | 73-76 | 4 | A/N | Filler |
| 26 | 77-77 | 1 | A | Student, Involved in Bullying |
| 27 | 78-78 | 1 | A | Zero-Tolerance: Expulsions |
| 28 | 79-128 | 50 | A/N | Filler |
| 29 | 129-142 | 14 | A/N | Florida Education Identifier * |
| 30 | 143-152 | 10 | A/N | Student Number Identifier, Local |
| 31 | 153-160 | 8 | A/N | Filler/Error Codes |

## Data Element Reference Notes

- Key fields for record matching: items 1, 4, 5, 6, 7, 9, 29
- When a discipline record ties back to a SESIR incident, Incident Identifier (item 9) and School Number, Where Incident Occurred (item 23) must match the corresponding SESIR record
- Exclusion rule: no Discipline/Resultant Action record should be submitted for SESIR incidents coded with Incident, Involvement Type of N or U
