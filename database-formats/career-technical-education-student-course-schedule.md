# 2025-26 Career and Technical Education Student Course Schedule

Source: [FLDOE Database Manuals](https://www.fldoe.org/accountability/data-sys/database-manuals-updates/2025-26-student-info-system/career-technical-edu-student-course-sc.stml)
Last Updated (per source page): 7/1/2025

## Description

1. Submit a separate record during reporting period 5 for each Career and Technical Education (CTE) and applicable Career and Technical Education exceptional education course in which the student was in membership during the current school year and the associated summer session(s) for the current school year.
2. COURSE NUMBER: Report the career and technical education course number.
3. CAREER AND TECHNICAL EDUCATION/ADULT GENERAL EDUCATION PROGRAM CODE: Report the CTE/AGE Program Code for the CTE course number as listed in the Career and Technical Education/Adult General Education Program Edit file (F61730).
4. KEY FIELDS: The key fields for this format are item numbers 4, 5, 6, 7, 8, 9, 10, 11 and 12. If a key field needs to be changed, the record must be deleted and re-submitted as an add.
5. ERROR CODES: This field is used by the Department to report to districts the specific errors found in the record during the state edit process. This field should contain filler (spaces, blanks) when the record is transmitted to the Department.

`*` indicates key fields.

## Record Layout

| Item No. | From-To | Size | Field Char. | Field Description |
|---|---|---|---|---|
| 1 | 1-2 | 2 | N/R | District Number, Current Enrollment |
| 2 | 3-6 | 4 | A/N/R | School Number, Current Enrollment |
| 3 | 7-16 | 10 | A/N | Filler |
| 4 | 17-17 | 1 | N | Survey Period Code * |
| 5 | 18-21 | 4 | N | School Year – Record Submission * |
| 6 | 22-23 | 2 | N/R | District Number, Current Instruction/Service * |
| 7 | 24-27 | 4 | A/N/R | School Number, Current Instruction/Service * |
| 8 | 28-34 | 7 | A/N | Course Number * |
| 9 | 35-39 | 5 | A/N | Section Number * |
| 10 | 40-43 | 4 | N | Period Number * |
| 11 | 44-44 | 1 | A/N | Term * |
| 12 | 45-58 | 14 | A/N | Florida Education Identifier * |
| 13 | 59-61 | 3 | A/N | Filler |
| 14 | 62-63 | 2 | A/N | Grade Level |
| 15 | 64-68 | 5 | A/N | Filler |
| 16 | 69-75 | 7 | A/N | Career and Technical Education/Adult General Education Program Code |
| 17 | 76-76 | 1 | A/N | Transaction Code |
| 18 | 77-89 | 13 | A/N | Filler |
| 19 | 90-92 | 3 | N | FEFP Program Number |
| 20 | 93-96 | 4 | A/N | Filler |
| 21 | 97-102 | 6 | A/N | Apprenticeship Sponsor Code |
| 22 | 103-107 | 5 | N | Filler |
| 23 | 108-108 | 1 | A | Exceptional Student Career and Technical Education Course Setting |
| 24 | 109-109 | 1 | A/N | Internship Participant |
| 25 | 110-142 | 33 | A/N | Filler |
| 26 | 143-152 | 10 | A/N | Student Number Identifier, Local |
| 27 | 153-160 | 8 | A/N | Filler/Error Codes |

## Data Element Reference Links

Each field name above links to its individual data element definition PDF on the source page. Notable references:

- Course Number: uses the standard course code structure
- Career and Technical Education/Adult General Education Program Code: cross-references the CTE/AGE Program Edit file (F61730)
- Key fields for record matching: items 4, 5, 6, 7, 8, 9, 10, 11, 12
