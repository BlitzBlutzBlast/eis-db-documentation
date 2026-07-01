# 2025-26 Dropout Prevention Program Data

Source: [FLDOE Database Manuals](https://www.fldoe.org/accountability/data-sys/database-manuals-updates/2025-26-student-info-system/dropout-prevention-program-data.stml)
Last Updated (per source page): 7/1/2025

## Description

1. Submit a separate format during survey period 5, by school, for each program in which the student was enrolled for any length of time.
2. TERM: To show the student participated in a dropout prevention program during the regular school year, use code 3 (annual). To indicate summer or intersession (for year round schools) participation, use code S (Combined Summer Sessions). If the student participated in dropout prevention programs during the regular school year and summer school/intersessions, send separate records by Term.
3. SCHOOL NUMBER, CURRENT ENROLLMENT and SCHOOL NUMBER CURRENT INSTRUCTION/SERVICE: Use code 9994 for private school students served with Fund Source D (Title I, Part D, Neglected and Delinquent) funds or Title I, Part A, Neglected set-aside funds. This is the only format where code 9994 is applied. When reporting private Neglected or Delinquent school data on other formats use N999 as the School Number, Current Enrollment.
4. DROPOUT PREVENTION LENGTH OF PRESCRIBED PROGRAM: The length in school days of the prescribed dropout prevention program must be greater than zero and less than 181. However, non-adjudicated students in juvenile detention, county jail or city jail programs and students in neglected institutions may have a prescribed program length of zero. The length of the prescribed dropout prevention program is the number of days the student is expected to participate in order to benefit substantially.
5. DROPOUT PREVENTION LENGTH OF PROGRAM PARTICIPATION: The length in school days of the student's actual participation (attendance) in the dropout prevention program being reported. The length in school days of participation in the dropout prevention program must be greater than or equal to zero and less than 181.
6. DROPOUT PREVENTION ENROLLMENT DATE: The date the student was first enrolled in each dropout prevention program in which he/she participated within each school. If the student was enrolled in more than one program, report the enrollment date for each program within each school. For students in non-school institutions for neglected or delinquent students report the student's date of entry into the non-school institution.
7. DROPOUT PREVENTION WITHDRAWAL DATE: The last date the student was officially withdrawn or dismissed from each dropout prevention program within each school. For a student enrolled in multiple programs, report the withdrawal date for each program. For students in non-school institutions for neglected or delinquent students report the student's date of exit from the non-school institution.
8. PRETEST OUTCOMES AND PROGRESS LEVELS: These elements, for both reading and math, should be reported for students in Title I, Part D funded programs. Code "Z" may be used for students who were served fewer than 90 consecutive calendar days.
9. ERROR CODES: This field is used by the Department to report to districts the specific errors found in the record during the state edit process. This field should contain filler (spaces, blanks) when the record is transmitted to the Department.
10. KEY FIELDS: The key fields for this format are item numbers 4, 5, 7, 12, 13, 14 and 25.

`*` indicates key fields.

## Record Layout

| Item No. | From-To | Size | Field Char. | Field Description |
|---|---|---|---|---|
| 1 | 1-2 | 2 | N/R | District Number, Current Enrollment |
| 2 | 3-6 | 4 | A/N/R | School Number, Current Enrollment |
| 3 | 7-16 | 10 | A/N | Filler |
| 4 | 17-17 | 1 | A/N | Survey Period Code - Always '5' * |
| 5 | 18-21 | 4 | N | School Year * |
| 6 | 22-27 | 6 | A/N | Filler |
| 7 | 28-28 | 1 | A | Dropout Prevention/Juvenile Justice Programs * |
| 8 | 29-31 | 3 | N | Dropout Prevention Length of Prescribed Program |
| 9 | 32-34 | 3 | N | Dropout Prevention Length of Program Participation |
| 10 | 35-56 | 22 | A/N | Filler |
| 11 | 57-57 | 1 | A | Transaction Code |
| 12 | 58-59 | 2 | N/R | District Number, Current Instruction/Service * |
| 13 | 60-63 | 4 | N/R | School Number, Current Instruction/Service * |
| 14 | 64-64 | 1 | A/N | Term * |
| 15 | 65-65 | 1 | A/N | Filler |
| 16 | 66-73 | 8 | A/N | Dropout Prevention Program Enrollment Date |
| 17 | 74-81 | 8 | A/N | Dropout Prevention Program Withdrawal Date |
| 18 | 82-85 | 4 | A | Filler |
| 19 | 86-86 | 1 | A | Fund Source |
| 20 | 87-87 | 1 | A | Progress Level - Reading |
| 21 | 88-88 | 1 | A | Progress Level - Math |
| 22 | 89-89 | 1 | A | Pretest Outcome - Reading |
| 23 | 90-90 | 1 | A | Pretest Outcome - Math |
| 24 | 91-128 | 38 | A/N | Filler |
| 25 | 129-142 | 14 | A/N | Florida Education Identifier * |
| 26 | 143-152 | 10 | A/N | Student Number Identifier, Local |
| 27 | 153-160 | 8 | A/N | Filler/Error Codes |

## Data Element Reference Notes

- Key fields for record matching: items 4, 5, 7, 12, 13, 14, 25
- Special case: School Number code 9994 applies only on this format, for private school students served with Fund Source D (Title I, Part D, Neglected and Delinquent) or Title I, Part A Neglected set-aside funds
