# 2025-26 Student Course Schedule

Source: [FLDOE Database Manuals](https://www.fldoe.org/accountability/data-sys/database-manuals-updates/2025-26-student-info-system/student-course-schedule.stml)
Last Updated (per source page): 7/1/2025

## Description

1. Submit a separate record for each course for which the student in grades PK-12 is in membership during reporting periods 1-4 regardless of whether the student is FTE eligible.
2. FEFP PROGRAM NUMBER: Record the appropriate number of the FEFP program for the course in which the student is in membership. See [Appendix E: FEFP Program Numbers](https://www.fldoe.org/core/fileparse.php/20844/urlt/2526-appende.xls).
3. FTE Reported, COURSE: See the current year's "FTE General Instructions," for information on calculating FTE Reported, Course.
4. GRADE LEVEL: Record the grade level of the student as reported on the Student Demographic Information format. Only grade levels PK-12 are valid for reporting on this format.
5. COURSE GRADE: Record the Course Grade for any KG-12 virtual course or virtual charter school course reported in periods 1-4. If the virtual course is not yet completed, but in progress, record the Course Grade as Course in Progress. Do not record a Course Grade for Blended Learning or traditional brick and mortar (seat time) courses.
6. BLENDED LEARNING COURSE: KG-12 virtual school or virtual charter school courses are not considered Blended Learning Courses.
7. ERROR CODES: This field is used by the department to report to districts the specific errors found in the record during the state edit process. This field should contain filler (spaces, blanks) when the record is transmitted to the department.
8. KEY FIELDS: The key fields for this format are item numbers 4, 5, 6, 7, 8, 9, 10, 25 and 35. If a key field needs to be changed, the record must be deleted and re-submitted as an add.

`*` indicates key fields.

## Record Layout

| Item No. | From-To | Size | Field Char. | Field Description |
|---|---|---|---|---|
| 1 | 1-2 | 2 | N/R | District Number, Current Enrollment |
| 2 | 3-6 | 4 | A/N/R | School Number, Current Enrollment |
| 3 | 7-16 | 10 | A/N | Filler |
| 4 | 17-17 | 1 | N | Survey Period Code * |
| 5 | 18-21 | 4 | N | Fiscal Year * |
| 6 | 22-23 | 2 | N/R | District Number, Current Instruction/Service * |
| 7 | 24-27 | 4 | A/N/R | School Number, Current Instruction/Service * |
| 8 | 28-34 | 7 | A/N | Course Number * |
| 9 | 35-39 | 5 | A/N/L | Section Number * |
| 10 | 40-43 | 4 | N | Period Number * |
| 11 | 44-44 | 1 | N | Days Per Week |
| 12 | 45-45 | 1 | A | Location of Student |
| 13 | 46-49 | 4 | A/N | Filler |
| 14 | 50-53 | 4 | N/R | Class Minutes, Weekly |
| 15 | 54-56 | 3 | N | FEFP Program Number |
| 16 | 57-60 | 4 | N/R | FTE Reported, Course |
| 17 | 61-63 | 3 | N/R | Online Course Provider |
| 18 | 64-64 | 1 | A/N | Filler |
| 19 | 65-66 | 2 | A/N | Grade Level |
| 20 | 67-69 | 3 | A/N | Virtual Instruction Provider |
| 21 | 70-70 | 1 | A | Transaction Code |
| 22 | 71-71 | 1 | A/N | English Language Learner: Instructional Model |
| 23 | 72-72 | 1 | A/N | Year-Round/Extended School Year FTE Indicator |
| 24 | 73-73 | 1 | A/N | Dual Enrollment Indicator |
| 25 | 74-74 | 1 | A/N | Term * |
| 26 | 75-81 | 7 | A/N | Career and Technical Education/Adult General Education Program Code |
| 27 | 82-82 | 1 | A | Day of Week Scheduled, Monday |
| 28 | 83-83 | 1 | A | Day of Week Scheduled, Tuesday |
| 29 | 84-84 | 1 | A | Day of Week Scheduled, Wednesday |
| 30 | 85-85 | 1 | A | Day of Week Scheduled, Thursday |
| 31 | 86-86 | 1 | A | Day of Week Scheduled, Friday |
| 32 | 87-87 | 1 | A | Day of Week Scheduled, Saturday |
| 33 | 88-88 | 1 | A | Day of Week Scheduled, Alternate Date Certain |
| 34 | 89-89 | 1 | A | Reading Intervention Component |
| 35 | 90-103 | 14 | A/N | Florida Education Identifier * |
| 36 | 104-106 | 3 | A/N | Course Grade |
| 37 | 107-112 | 6 | A/N | Apprenticeship Sponsor Code |
| 38 | 113-142 | 30 | A/N | Filler |
| 39 | 143-152 | 10 | A/N | Student Number Identifier, Local |
| 40 | 153-160 | 8 | A/N | Filler/Error Codes |

## Data Element Reference Notes

- Key fields for record matching: items 4, 5, 6, 7, 8, 9, 10, 25, 35
- Course Grade (item 36) applies only to KG-12 virtual courses or virtual charter school courses; not used for Blended Learning or traditional seat-time courses
- Day of Week Scheduled fields (items 27-33) each correspond to one day, one field per day plus an "Alternate Date Certain" flag
