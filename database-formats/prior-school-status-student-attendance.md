# 2025-26 Prior School Status/Student Attendance

Source: [FLDOE Database Manuals](https://www.fldoe.org/accountability/data-sys/database-manuals-updates/2025-26-student-info-system/prior-school-status-student-attendance.stml)
Last Updated (per source page): 7/1/2025

## Description

1. Submit this record during reporting survey periods 2, 3 and 5 for each PK-12 student who was in membership in any school or enrolled in any course in the district (District Number, Current Enrollment) from the first day of the school year to the last day of the survey period as well as any student who withdrew between school years. Students in School Number, Current Enrollment N998 and N999 should be reported if they enrolled in any course in the district. A separate record must be submitted for each school of enrollment and each entry/reentry date.
2. For students enrolled in a year-round school program, separate records should be submitted for each intersession. Students enrolled in separate summer terms must have two separate records reported.
3. WITHDRAWAL CODE, PK-12: Report ZZZ for Surveys 2 and 3 if no withdrawal code is applicable. Every record must have a Withdrawal Code other than ZZZ for Survey 5. Students who were expected to attend school but did not enter as expected (code DNE) should be reported on all surveys (2, 3, and 5).
4. TERM: To indicate the student entered/reentered during the regular school year, use code 3 (annual). To indicate summer school or intersession (for year round school) use code S (combined summer schedule). Use code Y to indicate a record being submitted with a withdrawal code for a student who was not enrolled this year. For Survey 2, Term should equal Z and Days Absent, Annual - Unexcused Not Related to Discipline should be 0-filled.
5. DAYS PRESENT and DAYS ABSENT: Report Days Present, Annual and Days Absent, Annual during Survey Periods 3 and 5. For Survey Period 2, these elements should be 0 filled.
6. RECORDS WITH TERM CODE = Y: For those records being reported with a Term code of Y, send the last School Number, Current Enrollment for the student in the district. The following fields should be Z-filled: Entry (Re-Entry) Code, PK-12 and Prior School/Location: Country. The following fields should be 0-filled: Days Present, Annual; Days Absent, Annual; Days Present, Summer Terms; Days Absent, Summer Terms; Days Absent, Annual - Unexcused Not Related to Discipline and Entry (Re-Entry) Date. In addition, use the date of the first day of the district's regular school year for Withdrawal Date.
7. ERROR CODES: This field is used by the Department to report to districts the specific errors found in the record during the state edit process. This field should contain filler (spaces, blanks) when the record is transmitted to the Department.
8. KEY FIELDS: The key fields for this format are item numbers 1, 2, 10, 11, 13 and 33. If a key field needs to be changed, the record must be deleted and resubmitted as an add.

`*` indicates key fields.

## Record Layout

| Item No. | From-To | Size | Field Char. | Field Description |
|---|---|---|---|---|
| 1 | 1-2 | 2 | N/R | District Number, Current Enrollment * |
| 2 | 3-6 | 4 | A/N/R | School Number, Current Enrollment * |
| 3 | 7-16 | 10 | A/N | Filler |
| 4 | 17-26 | 10 | A/N | Filler |
| 5 | 27-68 | 42 | A/N/L | Student Name, Legal |
| 6 | 69-69 | 1 | A | Sex |
| 7 | 70-70 | 1 | A | Filler |
| 8 | 71-78 | 8 | N | Birth Date |
| 9 | 79-80 | 2 | A/N | Grade Level |
| 10 | 81-81 | 1 | N | Survey Period Code * |
| 11 | 82-85 | 4 | N | School Year * |
| 12 | 86-88 | 3 | A/N | Entry (Re-Entry) Code, PK-12 |
| 13 | 89-96 | 8 | A/N | Entry (Re-Entry) Date * |
| 14 | 97-98 | 2 | A/N | Prior School/Location: District/County |
| 15 | 99-100 | 2 | A | Prior School/Location: State/Territory or Commonwealth |
| 16 | 101-102 | 2 | A | Prior School/Location: Country |
| 17 | 103-105 | 3 | A/N | Withdrawal Code, PK-12 |
| 18 | 106-113 | 8 | N | Withdrawal Date |
| 19 | 114-116 | 3 | N | Days Present, Annual |
| 20 | 117-119 | 3 | N | Days Absent, Annual |
| 21 | 120-120 | 1 | A | Transaction Code |
| 22 | 121-123 | 3 | N | Days Present, Summer Terms |
| 23 | 124-126 | 3 | N | Days Absent, Summer Terms |
| 24 | 127-127 | 1 | A/N | Term |
| 25 | 128-128 | 1 | A | Educational Choice |
| 26 | 129-129 | 1 | A | Disaster Affected Student |
| 27 | 130-130 | 1 | A | Student Offender Transfer |
| 28 | 131-133 | 3 | N | Days Absent, Annual Unexcused Not Related to Discipline |
| 29 | 134-135 | 2 | A/N | District Number, Current Instruction/Service |
| 30 | 136-136 | 1 | A | Habitual Truant |
| 31 | 137-142 | 6 | A/N | Filler |
| 32 | 143-152 | 10 | A/N | Student Number Identifier, Local |
| 33 | 153-166 | 14 | A/N | Florida Education Identifier * |
| 34 | 167-168 | 2 | A/N | District Number, Zoned School |
| 35 | 169-172 | 4 | A/N | School Number, Zoned School |
| 36 | 173-232 | 60 | A/N | Filler |
| 37 | 233-240 | 8 | A/N | Filler/Error Codes |

## Data Element Reference Notes

- Key fields for record matching: items 1, 2, 10, 11, 13, 33
- Term code Y is a special case: used for a withdrawal-only record for a student not enrolled the current year, with a specific set of Z-filled and 0-filled companion fields plus Withdrawal Date set to the first day of the district's regular school year
- Survey-specific reporting: Days Present/Absent Annual are 0-filled in Survey 2, populated in Surveys 3 and 5
