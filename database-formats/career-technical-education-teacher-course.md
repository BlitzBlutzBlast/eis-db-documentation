# 2025-26 Career and Technical Education Teacher Course

Source: [FLDOE Database Manuals](https://www.fldoe.org/accountability/data-sys/database-manuals-updates/2025-26-student-info-system/career-technical-edu-teacher-course.stml)
Last Updated (per source page): 7/1/2025

## Description

1. Submit a separate record for each combination of Course Number, Section Number, Period Number, Social Security Number and Term on the Career and Technical Educational Teacher Course format for each combination of Course Number, Section Number, Period Number, and Term submitted on the Career and Technical Educational Student Course format during Survey 5. No Career and Technical Educational Teacher Course records are needed, however, for prior year courses reported on the Career and Technical Educational Student Course format, for Course Numbers of zero and for dual-enrollment courses.
2. SCHOOL YEAR: Career and Technical Education courses are to be reported for the School Year.
3. KEY FIELDS: The key fields for this format are item numbers 1, 2, 3, 4, 5, 6, 7, 8 and 13. If a key field needs to be changed, the record must be deleted and re-submitted as an add.
4. ERROR CODES: This field is used by the Department to report to districts the specific errors found in the record during the state edit process. This field should contain filler (spaces, blanks) when the record is transmitted to the Department.

`*` indicates key fields.

## Record Layout

| Item No. | From-To | Size | Field Char. | Field Description |
|---|---|---|---|---|
| 1 | 1-2 | 2 | N/R | District Number, Current Instruction/Service * |
| 2 | 3-6 | 4 | A/N/R | School Number, Current Instruction/Service * |
| 3 | 7-7 | 1 | A/N | Survey Period Code * |
| 4 | 8-11 | 4 | N | School Year * |
| 5 | 12-18 | 7 | A/N | Course Number * |
| 6 | 19-23 | 5 | A/N | Section Number * |
| 7 | 24-27 | 4 | N | Period Number * |
| 8 | 28-28 | 1 | A/N | Term * |
| 9 | 29-30 | 2 | A/N/R | Facility Type |
| 10 | 31-31 | 1 | A/N | Filler |
| 11 | 32-35 | 4 | A/N | Filler |
| 12 | 36-45 | 10 | N/R | Florida Educators Certificate Number |
| 13 | 46-55 | 10 | A/N/L | Social Security Number * |
| 14 | 56-56 | 1 | A | Transaction Code |
| 15 | 57-62 | 6 | A/N | Filler |
| 16 | 63-72 | 10 | A/N | Staff Number Identifier, Local |
| 17 | 73-86 | 14 | A/N | Florida Education Identifier |
| 18 | 87-152 | 66 | A/N | Filler |
| 19 | 153-160 | 8 | A/N | Filler/Error Codes |

## Data Element Reference Notes

- Key fields for record matching: items 1, 2, 3, 4, 5, 6, 7, 8, 13
- Record must correspond to a matching CTE Student Course record for the same Course Number, Section Number, Period Number, and Term
