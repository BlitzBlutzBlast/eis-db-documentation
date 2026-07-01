# 2025-26 Teacher Course

Source: [FLDOE Database Manuals](https://www.fldoe.org/accountability/data-sys/database-manuals-updates/2025-26-student-info-system/teacher-course.stml)
Last Updated (per source page): 7/1/2025

## Description

1. Submit a separate record for each combination of Course Number, Section Number, Period Number, Term and Social Security Number for teachers during reporting periods 1-4. The combination of Course Number, Section Number, Period Number and Term must be the same as that reported for each student in this class.
2. DAYS IN TERM: For PK-12 short courses, Days in Term will be the actual number of days scheduled. For Voluntary Prekindergarten courses, Days in Term will be the actual number of days scheduled for the term being reported. For reporting periods 1 and 4, Days in Term will be the actual Summer Session days.
3. KEY FIELDS: The key fields for this format are item numbers 1, 2, 3, 4, 5, 6, 7, 13, and 20. If a key field needs to be changed, the record must be deleted and re-submitted as an add.
4. ERROR CODES: This field is used by the Department to report to districts the specific errors found in the record during the state edit process. This field should contain filler (spaces, blanks) when the record is transmitted to the Department.

`*` indicates key fields.

## Record Layout

| Item No. | From-To | Size | Field Char. | Field Description |
|---|---|---|---|---|
| 1 | 1-2 | 2 | N/R | District Number, Current Instruction/Service * |
| 2 | 3-6 | 4 | A/N/R | School Number, Current Instruction/Service * |
| 3 | 7-7 | 1 | A/N | Survey Period Code * |
| 4 | 8-11 | 4 | N | Fiscal Year * |
| 5 | 12-18 | 7 | A/N | Course Number * |
| 6 | 19-23 | 5 | A/N | Section Number * |
| 7 | 24-27 | 4 | N | Period Number * |
| 8 | 28-29 | 2 | A/N/R | Facility Type |
| 9 | 30-32 | 3 | N/R | Days in Term (For FTE Purposes) |
| 10 | 33-33 | 1 | A/N | Fund Source: NCLB Title III |
| 11 | 34-34 | 1 | A/N | Filler |
| 12 | 35-44 | 10 | N/R | Florida Educators Certificate Number |
| 13 | 45-54 | 10 | A/N/L | Social Security Number * |
| 14 | 55-55 | 1 | A/N | Filler |
| 15 | 56-56 | 1 | A | Transaction Code |
| 16 | 57-57 | 1 | A/N | Certification/Licensure/Qualification Status |
| 17 | 58-60 | 3 | A/N | Filler |
| 18 | 61-61 | 1 | A | Primary Instructor Indicator |
| 19 | 62-81 | 20 | A/N | Filler |
| 20 | 82-82 | 1 | A/N | Term * |
| 21 | 83-83 | 1 | A/N | Filler |
| 22 | 84-104 | 21 | A/N | Classroom Identification (FISH) Number |
| 23 | 105-105 | 1 | A/N | Scheduling Method |
| 24 | 106-106 | 1 | A | Term/Survey Indicator |
| 25 | 107-107 | 1 | A/N | Team Teacher Training |
| 26 | 108-127 | 20 | A | Filler |
| 27 | 128-128 | 1 | A/N | Blended Learning Course |
| 28 | 129-142 | 14 | A/N | Florida Education Identifier |
| 29 | 143-152 | 10 | A/N | Staff Number Identifier, Local |
| 30 | 153-160 | 8 | A/N | Filler/Error Codes |

## Data Element Reference Notes

- Key fields for record matching: items 1, 2, 3, 4, 5, 6, 7, 13, 20
- The Course Number/Section Number/Period Number/Term combination must match what students in the same class are reporting on the Student Course Schedule format
