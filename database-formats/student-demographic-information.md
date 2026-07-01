# 2025-26 Student Demographic Information

Source: [FLDOE Database Manuals](https://www.fldoe.org/accountability/data-sys/database-manuals-updates/2025-26-student-info-system/student-demographic-info.stml)
Last Updated (per source page): 7/1/2025

## Description

1. For reporting periods 1-4 submit this record for each student receiving instruction/service during that reporting period. Also, send a Student Demographic Information record for each student for whom one or more of the following record formats is being submitted even if the student is not receiving instruction/service during the reporting period: Student Discipline/Resultant Action and Federal/State Indicator Status. Do not send a Student Demographic Information record for a student who is in Home Education unless the student is also receiving instruction/service from the school district during the reporting period.
2. For reporting periods 2 and 3, also submit this record for any student who was identified as migrant ages 0-21, was not enrolled in school and has not graduated from high school. These records should be submitted with a School Number, Current Enrollment of 9997.
3. For reporting period 5 submit this record for any student (a) who was in membership at any time during the school year, (b) who was expected to attend school but did not enter (DNE) as expected (c) for whom a Diploma Type of W43, W45, W52, W54, W55, W58, W59, W61, W62 or W63 is being reported on the Student End of Year Status record, (d) who was identified as migrant ages 0-21, was not enrolled in school and has not graduated from high school, (e) who was identified as migrant ages 0-21, and served in a home education setting, (f) who participated in a Title I, Part C (Migrant) program at a private school, (g) who has been identified as disabled and received services provided by a district through a services plan, or (h) who participated in a Title I program at a private school.
4. For reporting period 9 submit this record for each student for whom an Institution Number, Neglected/Delinquent code is being reported.
5. For reporting period 6 submit this record for each KG-12 student identified as in membership on the survey date. Do not send this record for students who were expected to attend school but did not enter (DNE) as expected for unknown reasons. Exceptional Student Education Prekindergarten (PK) students and PK children of students in the Teenage Parent Program who are in membership on the survey date should also be submitted. Required fields to be reported are: District Number, Current Instruction/Service; District Number, Current Enrollment; School Number, Current Enrollment; Survey Period Code; Year; Student Name, Legal; Sex; Grade Level; Birth Date and Florida Education Identifier (FLEID). If the Student Number Identifier, Local is reported, it will be included on designated reports as in all other survey periods. Data may be sent for other fields, but the data is not needed and default values will be loaded to the data base for these non-required elements.
6. For reporting period R, submit this record for each student for whom a Student Discipline/Resultant Action record is reported.
7. STUDENT NAME LEGAL: The district must submit student names for each student. The student name field will be used to ensure efficient editing and verification of records during reporting periods and to facilitate Department monitoring and auditing activities requiring access to district individual student records.
8. SCHOOL NUMBER, CURRENT ENROLLMENT: For Survey 9, for students for whom an Institution Number, Neglected/Delinquent code is being reported, report the school of enrollment as of the time the student attended the Neglected/Delinquent Institution. For private school students who participated in a Title I program use 9995 for the School Number, Current Enrollment. For private school students who participated in a Title I, Part C (Migrant) program use 9992 for the School Number, Current Enrollment. For home education students who participated in a Title I Part C (Migrant) program use 9993 for School Number, Current Enrollment.
9. YEAR: For reporting periods 1 through 4 and 9, this field will contain fiscal year. For reporting period 5, this field will contain school year. For Survey Period R, data element "Year" should be reported in terms of "Month and Year". "Month and Year" as in, for example, January 2025 would be 0122.
10. INSTITUTION NUMBER, NEGLECTED/DELINQUENT: The number assigned to the institution for neglected or delinquent children as defined in Title I, Parts A and D, of the Elementary and Secondary Education Act, as amended by Public Law 114-95. Report this number in survey period 9 for students who are ages 5-17 inclusive who resided or were present in a residential institution for neglected or delinquent children for at least one day during the designated 30 day count period in the reporting year. The count period (which may be set separately for each institution) is 30 consecutive calendar days at least one of which falls within the month of October. Submit up to three eligible institutions on a Student Demographic Information format. Matching records are not required for these students in survey period 9. For Survey Period 5 submit this number for any student who resided in a locally operated residential neglected or delinquent facility or was present in a locally operated non-residential neglected or delinquent program at any time between July 1 and June 30 of the reporting year. Also, submit this number for any student, under age 21, who resided in a state operated residential delinquent or neglected program at any time between July 1 and June 30 of the reporting year.
11. ZONED DISTRICT AND SCHOOL: Submit this information in Survey Periods 2 and 3 for each student enrolled in an alternative school or designated as hospital/homebound during survey week. These elements should be zero-filled for survey periods 1, 4, 5 and 9.
12. LUNCH STATUS: For Survey Period 5, report a student as eligible for free or reduced price lunch if the student was eligible at any time during the school year.
13. DATE ENTERED UNITED STATES SCHOOL: Submit this information in Survey Periods 2, 3 and 5 for students coded LY or LP on the English Language Learners, PK-12 data element. Also submit this information in Surveys 2, 3 and 5 for Immigrant Students reported on the Federal/State Indicator Status format with a code of Y, unless Grade Level = PK then date should be reported as all zeros.
14. KEY FIELDS: The key fields for this format are item numbers 1, 5, 6 and 46. If a key field needs to be changed, the record must be deleted and re-submitted as an add.
15. ERROR CODES: This field is used by the Department to report to districts the specific errors found in the record during the state edit process. This field should contain filler (spaces, blanks) when the record is transmitted to the Department.

`*` indicates key fields.

## Record Layout

| Item No. | From-To | Size | Field Char. | Field Description |
|---|---|---|---|---|
| 1 | 1-2 | 2 | N/R | District Number, Current Instruction/Service * |
| 2 | 3-4 | 2 | N/R | District Number, Current Enrollment |
| 3 | 5-8 | 4 | A/N/R | School Number, Current Enrollment |
| 4 | 9-18 | 10 | A/N | Filler |
| 5 | 19-19 | 1 | N | Survey Period Code * |
| 6 | 20-23 | 4 | N | Year * |
| 7 | 24-33 | 10 | A/N | Filler |
| 8 | 34-75 | 42 | A/N/L | Student Name, Legal |
| 9 | 76-77 | 2 | A/N | District Number, Zoned School |
| 10 | 78-81 | 4 | A/N | School Number, Zoned School |
| 11 | 82-82 | 1 | A | Sex |
| 12 | 83-83 | 1 | A | Filler |
| 13 | 84-93 | 10 | A/N | Student Number Identifier, Local |
| 14 | 94-96 | 3 | A/N | Filler |
| 15 | 97-98 | 2 | A | English Language Learners, PK-12 |
| 16 | 99-99 | 1 | A/N | Resident Status, State/County |
| 17 | 100-101 | 2 | A/N | Grade Level |
| 18 | 102-102 | 1 | A/N | Student Characteristic, Agency Programs |
| 19 | 103-103 | 1 | A | Transaction Code |
| 20 | 104-105 | 2 | A/N | Native Language, Student |
| 21 | 106-106 | 1 | A/N | Filler |
| 22 | 107-108 | 2 | A/N | Primary Language Spoken in Home |
| 23 | 109-110 | 2 | A/N | Country of Birth |
| 24 | 111-118 | 8 | A/N | English Language Learners: Home Language Survey Date |
| 25 | 119-126 | 8 | N | Birth Date |
| 26 | 127-129 | 3 | A/N | Filler |
| 27 | 130-137 | 8 | A/N | Qualifying Arrival Date (QAD) for Migrant Program Eligibility |
| 28 | 138-138 | 1 | A/N | Lunch Status |
| 29 | 139-139 | 1 | A | Filler |
| 30 | 140-140 | 1 | A | Additional School Year Student |
| 31 | 141-141 | 1 | A/N | Migrant Status Term |
| 32 | 142-142 | 1 | A/N | Graduation Option |
| 33 | 143-146 | 4 | A/N | Institution Number, Neglected/Delinquent (First) |
| 34 | 147-150 | 4 | A/N | Institution Number, Neglected/Delinquent (Second) |
| 35 | 151-152 | 2 | N | Residence County |
| 36 | 153-153 | 1 | A | Ethnicity |
| 37 | 154-154 | 1 | A | Race: American Indian or Alaska Native |
| 38 | 155-155 | 1 | A | Race: Asian |
| 39 | 156-156 | 1 | A | Race: Black or African American |
| 40 | 157-157 | 1 | A | Race: Native Hawaiian or Other Pacific Islander |
| 41 | 158-158 | 1 | A | Race: White |
| 42 | 159-167 | 9 | A/N | Filler |
| 43 | 168-171 | 4 | A/N | Institution Number, Neglected/Delinquent (Third) |
| 44 | 172-179 | 8 | N | Date Entered United States School |
| 45 | 180-218 | 39 | A/N | Filler |
| 46 | 219-232 | 14 | A/N | Florida Education Identifier * |
| 47 | 233-240 | 8 | A/N | Filler/Error Codes |

## Data Element Reference Notes

- Key fields for record matching: items 1, 5, 6, 46
- Survey Period 6 has a reduced required-field set: District Number Current Instruction/Service, District Number Current Enrollment, School Number Current Enrollment, Survey Period Code, Year, Student Name Legal, Sex, Grade Level, Birth Date, FLEID. Other fields sent are not loaded and default values are used instead.
- Race fields (items 37-41) are separate flag fields, one per race category, rather than a single coded field
- Institution Number, Neglected/Delinquent has three positional slots (items 33, 34, 43) to accommodate up to three eligible institutions per Survey 9 record
