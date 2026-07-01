# 2025-26 Student Course Transcript Information

Source: [FLDOE Database Manuals](https://www.fldoe.org/accountability/data-sys/database-manuals-updates/2025-26-student-info-system/student-course-transcript-info.stml)
Last Updated (per source page): 7/1/2025

## Description

1. Submit course information during reporting period 5 for all students in grades 9-12 enrolled in the district during the School Year, including summer school courses, all courses transferred in from other schools, and courses taken for high school credit when the student was in grades below grade 9.

   | Grade Level | Course Information to Send |
   |---|---|
   | 12 | Grades 9, 10, 11, 12 and any courses below ninth grade that the student took in order to earn credit toward a high school diploma |
   | 11 | Grades 9, 10, 11 and any courses below ninth grade that the student took in order to earn credit toward a high school diploma |
   | 10 | Grades 9, 10 and any other courses below ninth grade that the student took in order to earn credit toward a high school diploma |
   | 9 | Grade 9 and any courses below ninth grade that the student took in order to earn credit toward a high school diploma |
2. Also submit a record for each Algebra course taken by a student in Grade Levels 7 and 8 at any time during the school year and accompanying summer sessions. Algebra courses are course numbers 1200310, 1200320, 1200370, 1200380, 1200386, 1200390 and 1209810.
3. Send all courses the student has taken in order to earn credit toward a high school diploma. For example, if a student took Algebra in Grade 8 and is currently in Grade 9, report the Algebra course along with the courses the student took in Grade 9.
4. SCHOOL YEAR: Report both the school year in which the course was taken (School Year - Course Taken) and the school year for which the record is being submitted (School Year - Record Submission).
5. COURSE GRADE: The Course Grade field may contain I for incomplete, NG for no grade assigned or similar grades other than A, B, C, D and F as defined in the DOE Information Data Base Requirements: Volume I - Automated Student Information System.
6. GRADE LEVEL: The Grade Level field should contain the Grade Level the student was in at the time the course was taken. Only report credits on grade 30 if the student left a secondary K-12 program, entered the Adult High School program as grade 30 and subsequently returned to a secondary K-12 program prior to graduation.
7. SCHOOL NUMBER, WHERE CREDIT EARNED: The School Number, Where Credit Earned field may contain 0001-9899, 9900, N997, N998, N999, C901-C928 Florida public colleges, U970-U981 Florida public state universities or P001-P999 eligible postsecondary non-public institutions.
8. COURSE NUMBER, SUBSTITUTED: This field is used with the Course Flag field. The presence of an asterisk (*) as one of the four flags in the Course Flag field indicates that the course specified by the number in the Course Number field is a Department of Education approved substitute for the course specified by the number in this field. Example: Course Number is 1802300 (JROTC Naval Science 1), Course Flag is *, and Course Number Substituted is 1500450 (JROTC PE Year 1 Waiver). This indicates that the Naval Science 1 course will substitute for the Personal Fitness/Physical Education Activity Elective and HOPE graduation requirement (students under personal fitness option must still take Personal Fitness class).
9. KEY FIELDS: The key fields for this format are item numbers 2-4, 8 and 10-15. If a key field needs to be changed, the record must be deleted and re-submitted as an add.
10. ERROR CODES: This field is used by the Department to report to districts the specific errors found in the record during the state edit process. This field should contain filler (spaces, blanks) when the record is transmitted to the Department.

`*` indicates key fields.

## Record Layout

| Item No. | From-To | Size | Field Char. | Field Description |
|---|---|---|---|---|
| 1 | 1-14 | 14 | A/N | Filler |
| 2 | 15-15 | 1 | N/R | Survey Period Code * |
| 3 | 16-17 | 2 | N/R | District Number, Current Enrollment * |
| 4 | 18-21 | 4 | A/N/R | School Number, Current Enrollment * |
| 5 | 22-31 | 10 | A/N | Filler |
| 6 | 32-33 | 2 | N/R | District Number, Where Credit Earned |
| 7 | 34-37 | 4 | A/N/R | School Number, Where Credit Earned |
| 8 | 38-51 | 14 | A/N | Florida Education Identifier * |
| 9 | 52-58 | 7 | A/N | Filler |
| 10 | 59-62 | 4 | N | School Year - Record Submission * |
| 11 | 63-66 | 4 | N | School Year - Course Taken * |
| 12 | 67-68 | 2 | A/N | Grade Level * |
| 13 | 69-69 | 1 | A/N | Term * |
| 14 | 70-76 | 7 | A/N | Course Number * |
| 15 | 77-81 | 5 | A/N | Course, Sequence Number * |
| 16 | 82-88 | 7 | A/N | Course Number, Substituted |
| 17 | 89-96 | 8 | A/N | Filler |
| 18 | 97-98 | 2 | A/N | Course, State Subject Area Requirements |
| 19 | 99-102 | 4 | A/N | Course, Flag |
| 20 | 103-103 | 1 | A/N | Filler |
| 21 | 104-106 | 3 | N | Credit Attempted, Course |
| 22 | 107-109 | 3 | N | Credit Earned, Course |
| 23 | 110-112 | 3 | A/N/R | Course Grade |
| 24 | 113-113 | 1 | A | Transaction Code |
| 25 | 114-115 | 2 | A | Course Substituted, State Subject Area Requirements |
| 26 | 116-116 | 1 | A | Filler |
| 27 | 117-142 | 26 | A/N | Filler |
| 28 | 143-152 | 10 | A/N | Student Number Identifier, Local |
| 29 | 153-160 | 8 | A/N | Filler/Error Codes |

## Data Element Reference Notes

- Key fields for record matching: items 2, 3, 4, 8, 10, 11, 12, 13, 14, 15
- Algebra course numbers requiring reporting for grades 7-8: 1200310, 1200320, 1200370, 1200380, 1200386, 1200390, 1209810
- Course Flag (item 19) asterisk indicates a DOE-approved substitute relationship to the course named in Course Number, Substituted (item 16)
