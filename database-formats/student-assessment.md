# 2025-26 Student Assessment

Source: [FLDOE Database Manuals](https://www.fldoe.org/accountability/data-sys/database-manuals-updates/2025-26-student-info-system/student-assessment.stml)
Last Updated (per source page): 7/1/2025

## Description

1. Submit student assessment records during reporting period 5 for students who took one or more Advanced Placement Test (APT), Cambridge Advanced International Certificate of Education (AICE), International Baccalaureate Program (IBP) or Armed Services Vocational Aptitude Battery Test (ASV) exams during the school year. See the test reference table below for specific reporting information.
2. TEST SCORE: Submit up to two Test Score/Test Score Type combinations for the Test Subject Content area being reported. Zeroes may be a valid test score. If only one Test Score is being submitted on a record, report all zeroes for the second Test Score.
3. TEST SCORE: Test scores must be reported as numbers, not letters, on this format and must be four digits, right-justified with leading zeroes. Test score conversions from letters to numbers for the AICE and IBP exams are provided in the table below.
4. TEST SCORE TYPES: Test score types to be used for the APT, AICE and IBP exams are provided in the table below.
5. TEST PUBLICATION YEAR: For the AICE, APT and IBP exams the Test Publication Year is the year in which the exam was taken.
6. TEST DATE: For the AICE exam use June 1 or June 2 for the June administration of the exam and November 1 or November 2 for the November administration of the exam along with the year in which the exam was taken. This allows for the reporting of students who take both levels of the AICE exam in the same month.
7. TEST SUBJECT CONTENT: Codes are provided in Appendix L.
8. TEST FORM: If no Test Form applies report 'Z' in this field.
9. TEST LEVEL: If no Test Level applies, report 'ZZ' in this field.
10. ERROR CODES: This field is used by the Department to report to districts the specific errors found in the record during the state edit process. This field should contain filler (spaces, blanks) when the record is transmitted to the Department.
11. KEY FIELDS: The key fields for this format are items 1, 2, 4, 5, 6, 8, 9 and 20.

`*` indicates key fields.

## Record Layout

| Item No. | From-To | Size | Field Char. | Field Description |
|---|---|---|---|---|
| 1 | 1-2 | 2 | N/R | District Number, Current Enrollment * |
| 2 | 3-6 | 4 | A/N/R | School Number, Current Enrollment * |
| 3 | 7-16 | 10 | A/N | Filler |
| 4 | 17-17 | 1 | N | Survey Period Code * |
| 5 | 18-21 | 4 | N | School Year * |
| 6 | 22-24 | 3 | A/N | Test Name * |
| 7 | 25-28 | 4 | A/N | Test Publication Year |
| 8 | 29-36 | 8 | A/N | Test Date * |
| 9 | 37-38 | 2 | A/N | Test Subject Content * |
| 10 | 39-39 | 1 | A/N | Test Form |
| 11 | 40-41 | 2 | A/N | Filler |
| 12 | 42-43 | 2 | A/N | Test Level |
| 13 | 44-45 | 2 | A/N | Test Score Type (1) |
| 14 | 46-49 | 4 | N/R | Test Score (1) |
| 15 | 50-51 | 2 | A/N | Test Score Type (2) |
| 16 | 52-55 | 4 | N/R | Test Score (2) |
| 17 | 56-56 | 1 | A/N | Transaction Code |
| 18 | 57-62 | 6 | A/N | Filler |
| 19 | 63-72 | 10 | A/N | Student Number Identifier, Local |
| 20 | 73-86 | 14 | A/N | Florida Education Identifier * |
| 21 | 87-152 | 66 | A/N | Filler |
| 22 | 153-160 | 8 | A/N | Filler/Error Codes |

## Data Element Reference Notes

- Key fields for record matching: items 1, 2, 4, 5, 6, 8, 9, 20

### Test Reference Table

| Test Name | Test Code | Test Form | Test Level(s) | Test Score Type | Test Score |
|---|---|---|---|---|---|
| Cambridge Advanced International Certificate of Education (AICE) | CAI | Z | A and AS | SS (Type 1) and ZZ (Type 2) | 8 (A*), 7 (A), 6 (B), 5 (C), 4 (D), 3 (E), 2 (F), 1 (G), 0 (U) |
| Advanced Placement Test (AP) | APT | Z | ZZ | SS (Type 1) and ZZ (Type 2) | 1, 2, 3, 4, 5 |
| Armed Services Vocational Aptitude Battery Test (ASV) | ASV | Z | ZZ | ZZ | 1-99 |
| International Baccalaureate Program (IBP) | IBP | Z | SL and HL | SS (Type 1) and ZZ (Type 2) | 1, 2, 3, 4, 5, 6, 7, 8(P), 9(N), 10(A), 11(B), 12(C), 13(D), 14(E) |
