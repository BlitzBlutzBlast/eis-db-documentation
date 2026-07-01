# 2025-26 Industry Certification

Source: [FLDOE Database Manuals](https://www.fldoe.org/accountability/data-sys/database-manuals-updates/2025-26-student-info-system/industry-certification.stml)
Last Updated (per source page): 7/1/2025

## Description

1. Submit a record during reporting period 5 for each Industry Certification Identifier and Industry Certification Outcome, including those linked to a career-themed course. Applies to students in grades KG-12. The outcome reported should be the final outcome for the reporting year.
2. SCHOOL YEAR: Report both the school year in which the course was taken and the school year of record submission. The school years will be the same for most records. The school year will be different when reporting students who took or attempted an industry certification or technical skill attainment assessment in a year subsequent to the school year in which the student took the course.
3. Include dual enrollment courses if the student took an industry certification or technical skill assessment listed in Appendix Z that is related to the dual enrollment course. Also refer to data element, Dual Enrollment Institution Type.
4. COURSE NUMBER: Report the career and technical education course number, career-themed course number or basic course number in which the certification was attempted/earned. If the course is not a career and technical education course report all zeros for the program number.
5. INDUSTRY CERTIFICATION IDENTIFIER: Report the Industry Certification Identifier from Appendix Z for students who took or attempted an industry certification or technical skill attainment assessment the current school year in the reporting district in an area that applies to the course in which the student participated.
6. KEY FIELDS: The key fields for this format are item numbers 4, 5, 6, 7, 8, 9, 10 and 20. If a key field needs to be changed, the record must be deleted and re-submitted as an add.
7. ERROR CODES: This field is used by the Department to report to districts the specific errors found in the record during the state edit process. This field should contain filler (spaces, blanks) when the record is transmitted to the Department.

`*` indicates key fields.

## Record Layout

| Item No. | From-To | Size | Field Char. | Field Description |
|---|---|---|---|---|
| 1 | 1-2 | 2 | N/R | District Number, Current Enrollment |
| 2 | 3-6 | 4 | A/N/R | School Number, Current Enrollment |
| 3 | 7-16 | 10 | A/N | Filler |
| 4 | 17-17 | 1 | N | Survey Period Code * |
| 5 | 18-21 | 4 | N | School Year - Record Submission * |
| 6 | 22-29 | 8 | A | Industry Certification Identifier * |
| 7 | 30-30 | 1 | A/N | Industry Certification Outcome * |
| 8 | 31-32 | 2 | N/R | District Number, Current Instruction/Service * |
| 9 | 33-36 | 4 | A/N/R | School Number, Current Instruction/Service * |
| 10 | 37-43 | 7 | A/N | Course Number * |
| 11 | 44-47 | 4 | N | School Year - Course Taken |
| 12 | 48-49 | 2 | A/N | Grade Level |
| 13 | 50-56 | 7 | A/N | Career and Technical Education/Adult General Education Program Code |
| 14 | 57-59 | 3 | A/N | Filler |
| 15 | 60-60 | 1 | A/N | Transaction Code |
| 16 | 61-61 | 1 | A | Dual Enrollment Institution Type |
| 17 | 62-69 | 8 | A/N | Industry Certification Date Earned |
| 18 | 70-128 | 59 | A/N | Filler |
| 19 | 129-138 | 10 | A/N | Student Number Identifier, Local |
| 20 | 139-152 | 14 | A/N | Florida Education Identifier * |
| 21 | 153-160 | 8 | A/N | Filler/Error Codes |

## Data Element Reference Notes

- Key fields for record matching: items 4, 5, 6, 7, 8, 9, 10, 20
- Industry Certification Identifier cross-references Appendix Z
- Two School Year fields with different meanings: item 5 is the school year of record submission, item 11 is the school year the course was actually taken (differs when the certification/assessment is attempted in a later year than the course)
