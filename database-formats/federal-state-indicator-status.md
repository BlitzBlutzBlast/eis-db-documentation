# 2025-26 Federal/State Indicator Status

Source: [FLDOE Database Manuals](https://www.fldoe.org/accountability/data-sys/database-manuals-updates/2025-26-student-info-system/federal-state-indicator-status.stml)
Last Updated (per source page): 7/1/2025

## Description

1. Submit this record during reporting periods 2, 3 and 5 for each PK-12th grade student in membership in the school district at any time during the school year. For students who supplement their course schedule outside of the district, only one record is submitted. In this situation the primary district of enrollment should submit the record. Do not send this record for students who were expected to attend school but did not enter (DNE) as expected for unknown reasons.
2. IMMUNIZATION STATUS: It is very important to report the current status for all kindergarten and seventh grade students in membership in the school district during reporting period 2.
3. DROPOUT PREVENTION/JUVENILE JUSTICE PROGRAMS: Report the program, if any, the student attended during survey week. These codes are used to identify the proper status of students in the school grading system. For students in more than one of these programs, report code E (Alternative to Expulsion) and code R (Dropout Retrieval) prior to any of the other program codes. For survey 5, report code Z for all students on this format.
4. HOMELESS STUDENT, PK-12: All districts must report all homeless students regardless of whether the district receives grant funding to serve this student population.
5. HOMELESSNESS CAUSE: Each student who is reported as a Homeless Student, PK-12 (any code other than N) must have corresponding Homelessness Cause (a code other than Z).
6. ERROR CODES: This field is used by the Department to report to districts the specific errors found in the record during the state edit process. This field should contain filler (spaces, blanks) when the record is transmitted to the Department.
7. KEY FIELDS: The key fields for this format are item numbers 1, 4, 5 and 34. If a key field needs to be changed, the record must be deleted and re-submitted as an add.

`*` indicates key fields.

## Record Layout

| Item No. | From-To | Size | Field Char. | Field Description |
|---|---|---|---|---|
| 1 | 1-2 | 2 | N/R | District Number, Current Enrollment * |
| 2 | 3-6 | 4 | A/N/R | School Number, Current Enrollment |
| 3 | 7-16 | 10 | A/N | Filler |
| 4 | 17-17 | 1 | A/N | Survey Period Code * |
| 5 | 18-21 | 4 | N | Fiscal Year * |
| 6 | 22-22 | 1 | A | Military Family Student |
| 7 | 23-23 | 1 | A/N | Immunization Status |
| 8 | 24-25 | 2 | A/N | Filler |
| 9 | 26-26 | 1 | A | Homeless Student, PK-12 |
| 10 | 27-27 | 1 | A | Homeless Unaccompanied Youth |
| 11 | 28-33 | 6 | A/N | Filler |
| 12 | 34-34 | 1 | A | Transaction Code |
| 13 | 35-36 | 2 | A/N/R | District Number, Current Instruction/Service: CAPE (First) (Deleted 24-25) |
| 14 | 37-38 | 2 | A/N/R | District Number, Current Instruction/Service: CAPE (Second) (Deleted 24-25) |
| 15 | 39-39 | 1 | A | Physical Education Waiver |
| 16 | 40-40 | 1 | A | Bullied or Harassed - Disability |
| 17 | 41-41 | 1 | A | Bullied or Harassed - Race |
| 18 | 42-42 | 1 | A | Bullied or Harassed - Sex |
| 19 | 43-43 | 1 | A | Fund Source |
| 20 | 44-44 | 1 | A/N | Section 504 Eligible |
| 21 | 45-45 | 1 | A | Bullied or Harassed - Religion |
| 22 | 46-46 | 1 | A | School Related Arrest |
| 23 | 47-47 | 1 | A/N | Career and Professional Academy Participant |
| 24 | 48-54 | 7 | A/N | Filler |
| 25 | 55-55 | 1 | A/N | Immigrant Student |
| 26 | 56-56 | 1 | A | Dropout Prevention/Juvenile Justice Programs |
| 27 | 57-57 | 1 | A/N | Test Accommodations |
| 28 | 58-58 | 1 | A | Medical Complexity Exemptions |
| 29 | 59-59 | 1 | A/N | Homelessness Cause |
| 30 | 60-60 | 1 | A | Bullied or Harassed - Sexual Orientation |
| 31 | 61-61 | 1 | A/N | Filler |
| 32 | 62-62 | 1 | A | Federally Connected Student Indicator |
| 33 | 63-72 | 10 | A/N | Student Number Identifier, Local |
| 34 | 73-86 | 14 | A/N | Florida Education Identifier * |
| 35 | 87-152 | 66 | A/N | Filler |
| 36 | 153-160 | 8 | A/N | Filler/Error Codes |

## Data Element Reference Notes

- Key fields for record matching: items 1, 4, 5, 34
- Items 13 and 14 (CAPE District Number, Current Instruction/Service) are marked as deleted for 2024-25, retained here as filler positions in the current layout
- Homelessness Cause (item 29) must be populated with a non-Z code whenever Homeless Student, PK-12 (item 9) is coded other than N
