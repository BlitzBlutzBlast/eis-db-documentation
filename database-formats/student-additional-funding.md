# 2025-26 Student Additional Funding

Source: [FLDOE Database Manuals](https://www.fldoe.org/accountability/data-sys/database-manuals-updates/2025-26-student-info-system/student-additional-funding.stml)
Last Updated (per source page): 7/1/2025

## Description

1. This record should be reported in Survey Period 5 for students who are eligible for additional funding in one or more of the categories listed below.
   1. Advanced Placement (AP)
   2. International Baccalaureate (IB)
   3. Advanced International Certificate of Education (AICE)
   4. Early Graduates
   5. Academic Dual Enrollment Associate Degree
   6. Academic Dual Enrollment Course
   7. College Board Advanced Placement Capstone Diploma
2. ERROR CODES: This field is used by the Department to report to districts the specific errors found in the record during the state edit process. This field should contain filler (spaces, blanks) when the record is transmitted to the Department.
3. KEY FIELDS: The key fields for this format are item numbers 1, 2, 5, 6 and 16. If a key field needs to be changed, the record must be deleted and re-submitted as an add.

`*` indicates key fields.

## Record Layout

| Item No. | From-To | Size | Field Char. | Field Description |
|---|---|---|---|---|
| 1 | 1-2 | 2 | N/R | District Number, Current Instruction/Service * |
| 2 | 3-6 | 4 | A/N/R | School Number, Current Instruction/Service * |
| 3 | 7-8 | 2 | N/R | District Number, Current Enrollment |
| 4 | 9-18 | 10 | A/N | Filler |
| 5 | 19-19 | 1 | N | Survey Period Code * |
| 6 | 20-23 | 4 | N | School Year * |
| 7 | 24-26 | 3 | N/R | Value Earned, College Entrance Examination Board Advanced Placement Test |
| 8 | 27-29 | 3 | N/R | Value Earned, International Baccalaureate Diploma |
| 9 | 30-32 | 3 | N/R | Value Earned, International Baccalaureate Score |
| 10 | 33-35 | 3 | N | Value Earned, Advanced International Certificate of Education Diploma |
| 11 | 36-38 | 3 | N | Value Earned, Advanced International Certificate of Education Score |
| 12 | 39-43 | 5 | N | Value Earned, Early Graduates |
| 13 | 44-44 | 1 | A | Transaction Code |
| 14 | 45-47 | 3 | A/N | Value Earned, CTE Pathway Concentrator Completion (Deleted 25-26) |
| 15 | 48-48 | 1 | A/N | Filler |
| 16 | 49-58 | 10 | A/N | Student Number Identifier, Local * |
| 17 | 59-72 | 14 | A/N | Florida Education Identifier * |
| 18 | 73-75 | 3 | N | Value Earned, Academic Dual Enrollment Associate Degree |
| 19 | 76-78 | 3 | N | FTE Earned, Academic Dual Enrollment Course (Deleted for 25-26) |
| 20 | 79-81 | 3 | N | Value Earned, College Board Advanced Placement Capstone Diploma |
| 21 | 82-84 | 3 | N | Value Earned, Career Dual Enrollment Course |
| 22 | 85-87 | 3 | N | Value Earned, Early College Program Dual Enrollment |
| 23 | 88-90 | 3 | N | Value Earned, Non Early College Program Dual Enrollment |
| 24 | 91-93 | 3 | N | Value Earned, CAPE Pathway Completer |
| 25 | 94-152 | 59 | A/N | Filler |
| 26 | 153-160 | 8 | A/N | Filler/Error Codes |

## Data Element Reference Notes

- Key fields for record matching: items 1, 2, 5, 6, 16 (note: item 17, FEID, is also marked with an asterisk on the source page alongside item 16)
- Items 14 and 19 are marked as deleted for 2025-26 (CTE Pathway Concentrator Completion and FTE Earned, Academic Dual Enrollment Course), retained here as their current positional layout
