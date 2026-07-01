# 2025-26 English Language Learners Information

Source: [FLDOE Database Manuals](https://www.fldoe.org/accountability/data-sys/database-manuals-updates/2025-26-student-info-system/eng-language-learners-info.stml)
Last Updated (per source page): 7/1/2025

## Description

1. Submit a separate record during reporting periods 2, 3 and 5 for each student in KG-12 membership identified as "LY" for the English Language Learners, PK-12 data element. Also, submit a separate record for each student identified as "LF" for the English Language Learners, PK-12 data element, who has exited the program within the last two school years. After two years change LF to LA.
2. Submit a separate record during reporting periods 2, 3 and 5 for each 3-12 grade student in membership identified as "LP" for the data element English Language Learners, PK-12, if the "LP" student is enrolled in an English for Speakers of Other Languages (ESOL) program pending assessment. (If the grade 3-12 student is identified as "LP" and enrolled in a regular program, do not submit a record.)
3. If the student is identified as "LA or LZ" for the English Language Learners, PK-12 data element, do not submit an English Language Learners Information Format because the English Language Learners: Post Reclassification Dates are for Local Accountability and District Records Transfer purposes only. Do not submit a record for English Language Learners Format if the student is identified as "ZZ".
4. In Surveys 2, 3 and 5 for students identified as LY report the following entry test information:
   1. For students in grades KG-02 report the aural/oral test scores that determined the student eligible and in need of services. These are reported in the test fields for Listening and Speaking. No Reading and Writing scores are applicable for entry.
   2. For students in grades 03-12, report aural/oral test scores in the test fields for Listening and Speaking. Also, report Reading and Writing test scores for students who tested proficient in aural/oral skills based on assessment.
   3. For students who have a reclassification date and an English Language Learners: Basis of Entry code of "L", test scores are optional.

   Report initial entry test information in each Survey period until the student is identified as LF. Zeros may be valid test scores.
5. In Surveys 2, 3 and 5 for students identified as LF, report exit test information as appropriate for the student's English Language Learners: Basis of Exit codes.
6. Report one or two English Language Learners: Basis of Exit codes. If code L is reported, all test information may be Z-filled or zero-filled, as appropriate.
7. ERROR CODES: This field is used by the Department to report to districts the specific errors found in the record during the state edit process. This field should contain filler (spaces, blanks) when the record is transmitted to the Department.
8. KEY FIELDS: The key fields for this format are items 4, 5, 50 and 52.

`*` indicates key fields.

## Record Layout

| Item No. | From-To | Size | Field Char. | Field Description |
|---|---|---|---|---|
| 1 | 1-2 | 2 | N/R | District Number, Current Enrollment |
| 2 | 3-6 | 4 | A/N/R | School Number, Current Enrollment |
| 3 | 7-16 | 10 | A/N | Filler |
| 4 | 17-17 | 1 | A/N | Survey Period Code * |
| 5 | 18-21 | 4 | N | School Year * |
| 6 | 22-29 | 8 | N | English Language Learners: Entry Date |
| 7 | 30-30 | 1 | A | English Language Learners: Tier Placement |
| 8 | 31-38 | 8 | N | English Language Learners: Student Plan Date |
| 9 | 39-46 | 8 | N | English Language Learners: Classification Date |
| 10 | 47-54 | 8 | N | English Language Learners: Exit Date |
| 11 | 55-62 | 8 | N | English Language Learners: Reevaluation Date |
| 12 | 63-63 | 1 | A/N | English Language Learners: Extension of Instruction |
| 13 | 64-71 | 8 | N | English Language Learners: Reclassification Date |
| 14 | 72-79 | 8 | N | English Language Learners: Reclassification Exit Date |
| 15 | 80-80 | 1 | A/N | English Language Learners: Basis of Entry |
| 16 | 81-81 | 1 | A/N | English Language Learners: Basis of Exit (First) |
| 17 | 82-84 | 3 | A/N | Test Name: Listening |
| 18 | 85-86 | 2 | A/N | Test Score Type: Listening |
| 19 | 87-88 | 2 | A/N | Test Subject Content: Listening |
| 20 | 89-92 | 4 | N/R | Test Score: Listening |
| 21 | 93-100 | 8 | A/N | Test Date: Listening |
| 22 | 101-103 | 3 | A/N | Test Name: Speaking |
| 23 | 104-105 | 2 | A/N | Test Score Type: Speaking |
| 24 | 106-107 | 2 | A/N | Test Subject Content: Speaking |
| 25 | 108-111 | 4 | N/R | Test Score: Speaking |
| 26 | 112-119 | 8 | A/N | Test Date: Speaking |
| 27 | 120-122 | 3 | A/N | Test Name: Reading |
| 28 | 123-124 | 2 | A/N | Test Score Type: Reading |
| 29 | 125-126 | 2 | A/N | Test Subject Content: Reading |
| 30 | 127-130 | 4 | N/R | Test Score: Reading |
| 31 | 131-138 | 8 | A/N | Test Date: Reading |
| 32 | 139-141 | 3 | A/N | Test Name: Writing |
| 33 | 142-143 | 2 | A/N | Test Score Type: Writing |
| 34 | 144-145 | 2 | A/N | Test Subject Content: Writing |
| 35 | 146-149 | 4 | N/R | Test Score: Writing |
| 36 | 150-157 | 8 | A/N | Test Date: Writing |
| 37 | 158-158 | 1 | A | Transaction Code |
| 38 | 159-159 | 1 | A | Fund Source |
| 39 | 160-160 | 1 | A/N | English Language Learners: Program Participation |
| 40 | 161-161 | 1 | A/N | English Language Learners: Basis of Exit (Second) |
| 41 | 162-162 | 1 | A | Test Form: Listening |
| 42 | 163-164 | 2 | A | Test Level: Listening |
| 43 | 165-165 | 1 | A | Test Form: Speaking |
| 44 | 166-167 | 2 | A | Test Level: Speaking |
| 45 | 168-168 | 1 | A | Test Form: Reading |
| 46 | 169-170 | 2 | A | Test Level: Reading |
| 47 | 171-171 | 1 | A | Test Form: Writing |
| 48 | 172-173 | 2 | A | Test Level: Writing |
| 49 | 174-181 | 8 | A/N | Filler |
| 50 | 182-183 | 2 | N/R | District Number, Current Instruction/Service * |
| 51 | 184-208 | 25 | A/N | Filler |
| 52 | 209-222 | 14 | A/N | Florida Education Identifier * |
| 53 | 223-232 | 10 | A/N | Student Number Identifier, Local |
| 54 | 233-240 | 8 | A/N | Filler/Error Codes |

## Data Element Reference Notes

- Key fields for record matching: items 4, 5, 50, 52
- Test blocks repeat identically across four skill areas: Listening, Speaking, Reading, Writing, each with Name, Score Type, Subject Content, Score, Date, and (separately) Form and Level fields
