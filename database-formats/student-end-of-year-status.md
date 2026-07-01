# 2025-26 Student End of Year Status

Source: [FLDOE Database Manuals](https://www.fldoe.org/accountability/data-sys/database-manuals-updates/2025-26-student-info-system/student-end-of-year-status.stml)
Last Updated (per source page): 7/1/2025

## Description

1. Submit this record during reporting period 5 for all PK-12 students who were in membership in the district at any time during either the regular school year or its associated summer session, any PK-12 student who was expected to attend school but did not enter (DNE) as expected for unknown reasons, and any student for whom a Diploma Type of W43, W45, W52, W54, W55, W58, W59, W61, W62 or W63 is being reported.
2. Two Student End of Year Status records may be submitted for a student. This can occur when a high school student leaves the PK-12 program and receives an Adult Standard High School Diploma (Diploma Type W43, W52, W54, W55, W58, W59, W61, W62 or W63) or a State of Florida Diploma (GED) (Diploma Type W45). In this instance, one End of Year Status record will be submitted with Grade Level PK-12 and one with Grade Level 30-31.
3. SCHOOL NUMBER, CURRENT ENROLLMENT: For the PK-12 student, report the last PK-12 school that the student was enrolled in during the regular 180 day school year unless the student was only enrolled in the district during the summer term.
4. GRADE LEVEL: For the PK-12 student, report the last Grade Level of the student during the regular 180 day School Year.
5. GRADE PROMOTION STATUS: Report code P for any PK-12 student who earned a diploma or certificate at any time during the school year.
6. ERROR CODES: This field is used by the Department to report to districts the specific errors found in the record during the state edit process. This field should contain filler (spaces, blanks) when the record is transmitted to the Department.
7. KEY FIELDS: The key fields for this format are item numbers 1, 4, 5, 13 and 19. If a key field needs to be changed, the record must be deleted and re-submitted as an add.

`*` indicates key fields.

## Record Layout

| Item No. | From-To | Size | Field Char. | Field Description |
|---|---|---|---|---|
| 1 | 1-2 | 2 | N/R | District Number, Current Enrollment * |
| 2 | 3-6 | 4 | A/N/R | School Number, Current Enrollment |
| 3 | 7-16 | 10 | A/N | Filler |
| 4 | 17-17 | 1 | N | Survey Period Code * |
| 5 | 18-21 | 4 | N | School Year * |
| 6 | 22-22 | 1 | A | Grade Promotion Status |
| 7 | 23-25 | 3 | A/N | Diploma Type |
| 8 | 26-28 | 3 | A/N | Certificate of Completion, Type (Deleted for 25-26) |
| 9 | 29-31 | 3 | A/N | Virtual Instruction Provider |
| 10 | 32-34 | 3 | A/N | Filler |
| 11 | 35-37 | 3 | A/N | Withdrawal Reason |
| 12 | 38-43 | 6 | A/N | Filler |
| 13 | 44-44 | 1 | A | Transaction Code |
| 14 | 45-58 | 14 | A/N | Florida Education Identifier * |
| 15 | 59-62 | 4 | A/N | Filler |
| 16 | 63-70 | 8 | N | Year Entered Ninth Grade, Graduation Requirements Determination |
| 17 | 71-72 | 2 | A/N | Filler |
| 18 | 73-77 | 5 | N/R | Grade Point Average State, Cumulative |
| 19 | 78-83 | 6 | A/N | Filler |
| 20 | 84-85 | 2 | A/N | Grade Level * |
| 21 | 86-101 | 16 | A/N | Filler |
| 22 | 102-109 | 8 | A/N | Withdrawal Date |
| 23 | 110-119 | 10 | A/N | Filler |
| 24 | 120-120 | 1 | A | Diploma Florida Seal of Fine Arts Designation |
| 25 | 121-121 | 1 | A | Diploma Biliteracy Seal Designation |
| 26 | 122-122 | 1 | A | Single Parent and Single Pregnant Woman |
| 27 | 123-123 | 1 | A | Dropout Prevention: Performance-Based Exit Option Test Results |
| 28 | 124-129 | 6 | A/N | Filler |
| 29 | 130-130 | 1 | N | Grade Promotion Status: Good Cause Exemption |
| 30 | 131-136 | 6 | A/N | Filler |
| 31 | 137-137 | 1 | A | Filler |
| 32 | 138-138 | 1 | A | Diploma Designation |
| 33 | 139-142 | 4 | A/N | Filler |
| 34 | 143-152 | 10 | A/N | Student Number Identifier, Local |
| 35 | 153-160 | 8 | A/N | Filler/Error Codes |

## Data Element Reference Notes

- Key fields for record matching: items 1, 4, 5, 13, 19 (note: item 19 is listed as filler in the current layout on the source page; verify against the current-year edit specification if this appears inconsistent)
- Item 8 (Certificate of Completion, Type) is marked as deleted for 2025-26, retained here as its current positional layout
- Dual-record scenario: a student receiving an Adult Standard High School Diploma or State of Florida Diploma (GED) may generate two End of Year Status records, one at Grade Level PK-12 and one at Grade Level 30-31
