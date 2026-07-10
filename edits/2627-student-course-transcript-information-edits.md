# Student Course Transcript Information — Edits and Reject Rules

Source: https://www.fldoe.org/file/20909/2627scti.pdf
Manual: Student Database 2026-2027

This document covers edits across three categories: Reject Rules (record rejected), State Validation (cross-format matching), and Exception Reports (advisory, does not reject). Edit numbering is non-sequential; gaps (edits 4, 31-35) are as published in the source.

---

## Reject Rules

### 1. Survey Period Code must be 5
Survey Period Code must be 5 and must be correct for the submission specified by the district.
**Result:** Record rejected

**Example:** The Survey Period Code as specified in the transmission JCL or in statements for tape transmission is identified as Survey Period "5". However, if records on the transmission have a Survey Period Code "3", all records updated, added, or deleted with this inconsistency would be rejected.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the Survey Period Code must be corrected either on the records coming in or the transmission JCL and all records must be resubmitted in a batch transaction or added on-line.

### 2. District Number, Current Enrollment range and active status *(Updated 07/01/2026)*
District Number, Current Enrollment must be numeric and active (A) on the Appendix C: District Name Table and must be correct for the district submitting the data.
**Result:** Record rejected

**Example:**
| District Number, Current Enrollment | School Number, Current Enrollment | Florida Education Identifier |
|---|---|---|
| 01 | 0021 | FL123456789100 |
| 01 | 0021 | FL123456789200 |
| *00 | 0021 | FL123456789300 |

The first two records would be loaded assuming no other reject rule would cause their rejection. The third record would be rejected since the District Number, Current Enrollment is not active (A) on the Appendix C: District Name Table.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number, Current Enrollment and resubmit the record.

### 3. School Number, Current Enrollment range
School Number, Current Enrollment must be numeric in the range 0001 to 9899, excluding 9001 and 7006.
**Result:** Record rejected

**Example:**
| District Number, Current Enrollment | School Number, Current Enrollment | Florida Education Identifier |
|---|---|---|
| 01 | 0021 | FL123456789100 |
| 01 | 0021 | FL123456789200 |
| *01 | 9999 | FL123456789300 |
| *01 | C901 | FL123456789000 |

The first two records would be loaded assuming no other reject rule would cause the records to be rejected. The third record would be rejected because the School Number, Current Enrollment is not in the appropriate numerical range. The fourth record would be rejected because it is not numeric.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Enrollment and resubmit the records.

### 5. District Number, Where Credit Earned validity *(Updated 07/01/2026)*
The District Number, Where Credit Earned must be active (A) on the Appendix C: District Name Table for Florida public school districts, 99 for credit earned in Florida non-public schools, alpha codes AK-WY for credit earned out-of-state, or AA-ZB for credit earned out-of-country, or AQ to WQ for credit earned at United States Commonwealth and Territories. (See Appendices G, H and Q of the DOE Information Database Requirements: Volume I--Automated Student Information System Manual for valid Foreign Country, State codes and United States Commonwealth and Territories.)
**Result:** Record rejected

**Example:**
| District Number, Where Credit Earned | School Number, Current Enrollment | School Year | Term |
|---|---|---|---|
| 01 | 0151 | 0203 | 2 |
| *70 | 7542 | 0203 | 1 |
| 99 | 9999 | 0203 | 4 |

The first and third records would be loaded assuming no other reject rule would cause their rejection. The second record would be rejected since the District Number, Where Credit Earned is not active (A) on the Appendix C: District Name Table.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the District Number, Where Credit Earned entries and resubmit the records.

### 6. School Number, Where Credit Earned validity
The School Number, Where Credit Earned must be alphanumeric in the range of 0001-9899 for Florida public school district sites, N999 or in the range of 0001-9899 for credit earned in Florida PK-12 non-public schools, 9900 for credit earned in out-of-state schools, N998 for credit earned in home education, N997 for credit earned in an American school abroad, C901-C928 for Florida public community colleges, U970-U981 for Florida public state universities, or P001-P999 for eligible postsecondary nonpublic institutions.
**Result:** Record rejected

**Example:**
| District Number, Where Credit Earned | School Number, Current Enrollment | School Year | Term |
|---|---|---|---|
| *01 | 151 | **** | 2 |
| 64 | 6881 | **** | 1 |
| *99 | M999 | **** | 4 |
| ID | N999 | **** | 2 |

**** = Valid fiscal year for data submission. The second and fourth records would be loaded assuming no other reject rule would cause their rejection. The first record would be rejected since the School Number, Where Credit Earned contains a blank. The third record would be rejected since it has an invalid code.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Where Credit Earned and resubmit the records.

### 7. School Year – Course Taken validity
School Year – Course Taken must be a valid school year, numeric, and less than or equal to the current school year.
**Result:** Record rejected

**Example:**
| District Number, Where Credit Earned | School Number, Current Enrollment | School Year Course Taken |
|---|---|---|
| 01 | 0021 | 0203 |
| *01 | 0021 | 9597 |
| *01 | 0021 | 9492 |
| 01 | 0021 | 9899 |
| 01 | 0021 | 0910 |

The first, fourth and fifth records would be loaded assuming no other reject rule would cause their rejection. The second and third records would be rejected since the school year is invalid.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Year – Course Taken and resubmit the records.

### 8. Grade Level validity
Grade Level must be 01-12 or 30.
**Result:** Record rejected

**Example:**
| School Year | Grade Level | Term |
|---|---|---|
| *0001 | 8 | 1 |
| 0001 | 10 | 2 |
| 0203 | 11 | 1 |
| *0203 | 40 | 2 |

The second and third records would be loaded assuming no other reject rule would cause their rejection. The first record would be rejected because the Grade Level does not contain two characters as required. The fourth record would be rejected since the Grade Level is not a valid grade.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Grade Level and resubmit the records.

### 9. Term validity
Term must be 1-9, B-O, or S-X.
**Result:** Record rejected

**Example:**
| School Year | Grade Level | Term |
|---|---|---|
| *0001 | 8 | |
| 0001 | 10 | 2 |
| 0203 | 11 | 1 |
| *0203 | 12 | A |

The second and third records would be loaded assuming no other reject rule would cause their rejection. The first record would be rejected because Term was left blank. The fourth record would be rejected since the Term code is not valid.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Term codes and resubmit the records.

### 10. Course Number format
Course Number must be alphanumeric and contain no blanks.
**Result:** Record rejected

**Example:** Six of seven example records would be loaded assuming no other reject rule would cause their rejection. The first and seventh records would be rejected since the Course Number contains blanks.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district should correct the Course Number and resubmit the record.

### 11. Course Sequence Number format
The Course Sequence Number must be alphanumeric and contain no blanks. Allowable characters are 0-9, A-Z, hyphen, dollar sign, pound sign, and colon.
**Result:** Record rejected

**Example:** Five of seven example records would be loaded assuming no other reject rule would cause their rejection. The first and seventh records would be rejected since the Course Sequence Number contains blanks.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Course Sequence Number and resubmit the records.

### 12. Alphanumeric Course Numbers must be on Course Code Directory or Statewide Course Numbering System
All alphanumeric Course Numbers must either be on the Course Code Directory or on the Statewide Course Numbering System file unless School Number, Where Credit Earned equals P001-P999.
**Result:** Record rejected

**Example:**
| Florida Education Identifier | District Number, Where Credit Earned | School Number, Where Credit Earned | Course Number |
|---|---|---|---|
| *FL123456789100 | 66 | 0061 | FF10011 |
| FL123456789200 | 66 | 0061 | I460103 |
| FL123456789300 | 66 | 0201 | B070614 |
| *FL123456789000 | 66 | C901 | ABCDE12 |

The second and third records would be loaded assuming no other reject rule would cause their rejection. The first and fourth records would be rejected because the Course Numbers are not on the Course Code Directory or on the Statewide Course Numbering System files.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Course Numbers and resubmit the records.

### 13. Course, State Subject Area Requirements validity when reported in same year *(Updated 07/01/25)*
If School Year-Course Taken = School Year-Record Submission, then Course, State Subject Area Requirements must equal A1, AG, AH, BI, CT, EC, EL, EN, EQ, FE, GE, MA, NC, PE, PF, PL, or WH.
**Result:** Record rejected

**Example:** Four of seven example records would be loaded assuming no other reject rule would cause them to be rejected. Three records would be rejected since the Course, State Subject Area Requirements codes are invalid.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Course, State Subject Area Requirements and resubmit the records.

### 14. Course Flag validity when reported in same year
If School Year-Course Taken = School Year-Record Submission, then Course Flag must be 7, 9, G-I, N, P, T, W, X, * or blank.
**Result:** Record rejected

**Example:** Two of three example records would be loaded assuming no other reject rules would cause them to be rejected. One record would be rejected since the Course Flag contains invalid characters.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Course Flag entry and resubmit the record.

### 15. No repeated Course Flags
For each Student Course Transcript Information record, no Course Flag, except blanks, may be repeated.
**Result:** Record rejected

**Example:** Two of three example records would be loaded assuming no other reject rule would cause them to be rejected. One record would be rejected since the Course Flag contains two H codes.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Course Flag and resubmit the record.

### 16. Credit Attempted, Course must be numeric
Credit Attempted, Course must be numeric.
**Result:** Record rejected

Note: Two decimal places assumed.

**Example:** Four of seven example records would be loaded assuming no other reject rule would cause them to be rejected. Three records would be rejected since the Credit Attempted, Course is not numeric.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Credit Attempted, Course and resubmit the records.

### 17. Credit Earned, Course must be numeric
Credit Earned, Course must be numeric.
**Result:** Record rejected

Note: Two decimal places assumed.

**Example:** Four of seven example records would be loaded assuming no other reject rule would cause them to be rejected. Three records would be rejected since the Credit Earned, Course is not numeric.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Credit Earned, Course and resubmit the records.

### 18. Course Grade code validity and justification
The Course Grade code must be A+, A, A-, B+, B, B-, C+, C, C-, D+, D, D-, F, I, N, NNN, U, P, S, SB, T, E, WP, FL, NG, W or WF and must be right justified with leading blanks.
**Result:** Record rejected

**Example:**
| Course Number | Credit Attempted, Course | Credit Earned, Course |
|---|---|---|
| *1005300 | 100 | (Course Grade: OOA) |
| 0900310 | 050 | (Course Grade: B+) |
| *0400330 | 100 | (Course Grade: C+, not right justified) |
| *1200350 | 050 | (Course Grade: WC) |
| 1200350 | 050 | (Course Grade: P) |

Two of five records would be loaded assuming no other reject rule would cause them to be rejected. Two records would be rejected since they contain invalid codes; one would be rejected since the Course Grade is not right justified with leading blanks.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Course Grade and resubmit the records.

### 19. Transaction Code validity
The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified then the record must not already exist on the database; if C or D is specified then the record must exist on the database.
**Result:** Record rejected

**Example:** For all original transmissions, the Transaction Code must be "A". An original transaction is the first submission of a record during a survey period. After original transmission of records, changes to the record for elements other than the key elements must be done with a "C" as the Transaction Code. To delete a record, the Transaction Code must be a "D". To change key elements in a batch transaction, the record must FIRST be deleted with a "D" and then added with an "A". Records with an incorrect Transaction Code would be rejected.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Transaction Code and resubmit the records.

### 20. Record uniqueness
Each Student Course Transcript Information record must be unique based on Survey Period Code; District Number, Current Enrollment; School Number, Current Enrollment; Florida Education Identifier; School Year – Record Submission; School Year – Course Taken; Grade Level; Term; Course Number; and Course Sequence Number.
**Result:** First record accepted, all other duplicate records rejected

**Example:** Five of seven example records would be loaded assuming no other reject rule would cause them to be rejected. Two records would be rejected since they are duplicates of two of the accepted records.

**District Responsibility:** If the records loaded to the database are correct, no action is necessary. However, if the district wishes the rejected records to be loaded to the database, the district must delete any invalid records, correct any rejected records if necessary, and resubmit the corrected records.

### 21. School Number, Current Enrollment validity against Master School Identification File
School Number, Current Enrollment must exist on the Master School Identification File as a valid active school number for the District Number, Current Enrollment.
**Result:** Record rejected

**Example:**
| District Number, Current Enrollment | School Number, Current Enrollment |
|---|---|
| *09 | 8131 |
| *13 | 0021 |
| *15 | C999 |
| 57 | 0051 |
| 63 | 0031 |

The fourth and fifth records would be loaded assuming no other reject rule would cause them to be rejected. Records one, two, and three would be rejected because the School Number, Current Enrollment does not exist on the Master School Identification File as a valid active school number for the District Number, Current Enrollment.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Enrollment and resubmit the records.

### 22. Item 5 - Filler must be all spaces
Item 5 - Filler on this format in position numbers 22-31 must be all spaces.
**Result:** Record rejected

**Example:**
| District Number, Current Enrollment | School Number, Current Enrollment | Filler, Item #5 |
|---|---|---|
| 01 | 0151 | |
| *01 | 0151 | 265456789X |

The first record would be loaded assuming no other reject rule would cause its rejection. The second record would be rejected because the data reported is not all spaces.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must fill the positions noted with all spaces and resubmit the record.

### 23. Student Number Identifier, Local format
The Student Number Identifier, Local may be any combination of letters, numbers and blanks. (All blanks are allowable.) It must be left-justified with trailing blanks.
**Result:** Record rejected

**Example:**
| District Number, Current Enrollment | School Number Identifier, Local |
|---|---|
| 01 | 0123456789 |
| 01 | ABC123DEF9 |
| 01 | 3001 28K |
| *01 | 2121@XYZ |
| *01 | 123456 |

The first three records would be loaded assuming no other edit would cause their rejection. The fourth record would be rejected because the Student Number Identifier, Local contains a symbol (@). The fifth record would be rejected because it is right-justified rather than left-justified.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Student Number Identifier, Local and resubmit the records.

### 24. School Number, Where Credit Earned requires District Number 99 for college/university/postsecondary
If School Number, Where Credit Earned equals C901-C928, U970-U981, or P001-P999, then District Number, Where Credit Earned must equal 99.
**Result:** Record rejected

**Example:**
| District Number, Where Credit Earned | School Number, Where Credit Earned | Florida Education Identifier |
|---|---|---|
| 99 | U970 | FL123456789100 |
| *16 | C901 | FL123456789200 |

The first record would pass the edit. The second record would be rejected because the School Number, Where Credit Earned is not correct for the District Number, Where Credit Earned.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number, Where Credit Earned or the School Number, Where Credit Earned and resubmit the record.

### 25. Course Grade W requires college/university/postsecondary/nonpublic School Number
If the Course Grade code equals W, then the School Number, Where Credit Earned must be U970-U981, C901-C928, P001-P999, 9900 or N999.
**Result:** Record rejected

**Example:** Two of four example records would be loaded assuming no other reject rule would cause them to be rejected. Two records would be rejected because the Course Grade is not valid for the reported School Number, Where Credit Earned.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Course Grade or the School Number, Where Credit Earned and resubmit the records.

### 26. Course Number, Substituted validity
Course Number, Substituted must be a course in the Course Code Directory or it must be blank.
**Result:** Record rejected

**Example:**
| Florida Education Identifier | District Number, Where Credit Earned | School Number, Where Credit Earned | Course Number Substituted |
|---|---|---|---|
| *FL123456789100 | 66 | 0101 | FF10011 |
| FL123456789200 | 66 | 0101 | 0800300 |
| *FL123456789300 | 66 | C917 | ABCDE12 |

The second record would be loaded assuming no other reject rule would cause its rejection. The first and third records would be rejected because the Course Numbers, Substituted are not in the Course Code Directory.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Course Number, Substituted fields and resubmit the records.

### 27. Course Number, Substituted not blank requires asterisk Course Flag
If the Course Number, Substituted is not blank, then at least one Course Flag must be "*".
**Result:** Record rejected

**Example:**
| Florida Education Identifier | Course Number | Course Number Substituted | Grade Level | Course Flag |
|---|---|---|---|---|
| FL123456789100 | 1802300 | 0800300 | 09 | * |
| *FL123456789200 | 1802300 | 0800300 | 10 | |
| FL123456789300 | 1802300 | 0800300 | 11 | * |

The first and third records would be loaded assuming no other reject rule would cause their rejection. The second record would be rejected because there is no asterisk (*) Course Flag.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Course Number, Substituted or the Course Flag field and resubmit the record.

### 28. Asterisk Course Flag requires non-blank Course Number, Substituted
If any of the four Course Flags are "*", then the Course Number, Substituted must not be blank.
**Result:** Record rejected

**Example:**
| Florida Education Identifier | Course Number | Course Number Substituted | Grade Level | Course Flag |
|---|---|---|---|---|
| FL123456789100 | 1802300 | 0800300 | 09 | * |
| *FL123456789200 | 1802300 | 0800300 | 10 | * |
| FL123456789300 | 1802300 | | 11 | * |

The first two records would be loaded assuming no other reject rule would cause their rejection. The third record would be rejected because the Course Number, Substituted must not be blank when there is a Course Flag of '*'.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Course Number, Substituted or the Course Flag field and resubmit the record.

### 29. Course Substituted, State Subject Area Requirements validity *(Updated 07/01/25)*
If School Year-Course Taken = School Year-Record Submission, then Course Substituted, State Subject Area Requirements must equal A1, AG, AH, BI, CT, EC, EL, EN, EQ, FE, FL, GE, MA, NC, PE, PF, PL, or WH, or blank. If Course Number, Substituted is blank, Course Substituted, State Subject Area Requirements must be blank. If Course Substituted, State Subject Area Requirements is blank, then Course Number, Substituted must be blank.
**Result:** Record rejected

**Example:**
| Course Number | Course Number Substituted | Course Substituted, State Subject Area Requirements |
|---|---|---|
| 0800300 | 1802300 | PE |
| *0800300 | 1802300 | PP |

The first record would be loaded assuming no other reject rule would cause it to be rejected. The second record would be rejected since the Course Substituted, State Subject Area Requirements code is invalid.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Course Substituted, State Subject Area Requirements code and resubmit the record.

### 30. School Year – Record Submission correctness
The School Year – Record Submission must be correct for the submission specified by the district.
**Result:** Record rejected

**Example:** The School Year – Record Submission on the JCL and the records being submitted for processing must match. Otherwise, the records will be rejected.

**District Responsibility:** Correct the School Year – Record Submission either on the transmission JCL or the records being submitted and resubmit all records for processing.

### 36. Course Number restrictions for study hall/elementary/middle courses
If School Number, Where Credit Earned does not begin with P, then Course Number must not equal 5022000, or 2200300-2200330 (study hall) and must not have a Sort Level of 1 (Basic Education PK-5) or 2 (Basic Education 6-8) on the Course Code Directory file DPS.DISTRICT.K9.F62806.Yyyyy.
**Result:** Record rejected

**Example:** Two of four example records would be loaded assuming no other reject rule would cause their rejection. One record would be rejected because it is a Study Hall course; another would be rejected because it is a middle/junior high school course.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district should correct the Course Numbers and resubmit the records.

### 37. Florida Education Identifier (FLEID) format
Florida Education Identifier (FLEID) is alphanumeric and must be entered as "FL" in the first 2 positions followed by twelve numeric digits. No blanks, spaces or all zeros for the twelve numeric digits are allowable.
**Result:** Record rejected

**Example:**
| District Number, Current Enrollment | Florida Education Identifier |
|---|---|
| 01 | FL340945895734 |
| 01 | FL004583948567 |
| *01 | FL000000000000 |

The first two records would be loaded assuming no other reject rule would cause their rejection. The third record would be rejected because the Florida Education Identifier (FLEID) is not a valid FLEID.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Florida Education Identifier and resubmit the record for processing.

---

## State Validation

### 50. Matching Student Demographic record required
Each Student Course Transcript must have a matching Student Demographic Record based on District Number, Current Enrollment; Florida Education Identifier; Survey Period Code and School Year – Record Submission matched to Year.
**Result:** State validation

**Example:**

Student Course Transcript Information records:
| District Number, Current Enrollment | Florida Education Identifier | School Year-Record Submission | Survey Period Code |
|---|---|---|---|
| *01 | FL123456789100 | 1011 | 5 |
| 01 | FL123456789200 | 1011 | 5 |
| 01 | FL123456789300 | 1011 | 5 |

Student Demographic Information records:
| District Number, Current Enrollment | Florida Education Identifier | Year | Survey Period Code |
|---|---|---|---|
| 01 | FL123456789200 | 1011 | 5 |
| 01 | FL123456789300 | 1011 | 5 |

The Student Course Transcript Information record marked with an asterisk would cause a message to be generated because it does not have a matching Student Demographic Information record.

**District Responsibility:** The district must delete the Student Course Transcript Information record or add a Student Demographic Information record to match the key fields on the Student Course Transcript Information record.

---

## Exception Reports

### 80. Grade Level range
Grade Level must be in the range 06-12, or 30.
**Result:** Exception report

**Example:**
| School Year | Grade Level | Term | Credit Earned, Course |
|---|---|---|---|
| *9900 | 05 | 1 | 050 |
| 9900 | 10 | 2 | 050 |
| 0001 | 11 | 1 | 050 |
| 0203 | 08 | 2 | 050 |

The second, third and fourth records would pass this edit. The first record would cause an error message to be generated because the student is reported as being in grade level 05.

**District Responsibility:** The district should verify the Grade Level submitted and correct the record if in error.

### 81. Course Flag 9 required for Credit Earned below Grade 09
If Grade Level is less than 09 and Credit Earned, Course is greater than zero, then Course Flag must be 9.
**Result:** Exception report

**Example:**
| School Year | Course Number | Grade Level | Course Flag | Credit Earned, Course |
|---|---|---|---|---|
| **** | 1200310 | 07 | | 050 |
| **** | 1001350 | 10 | R | 050 |
| **** | 1001370 | 11 | | 050 |
| **** | 1200310 | 08 | 9 | 050 |

**** = Valid fiscal year for data submission. The second, third and fourth records would pass this edit. The first record would cause an error message to be generated because the student is reported as being in grade level 07 but does not have a Course Flag code of 9.

**District Responsibility:** The district should verify the Course Flag code submitted and correct the record if in error.

### 82. Course Flag I requires matching Course Flag X
For each Course Flag of I, there must be a Course Flag of X on another course record for the same District Number, Current Enrollment; School Number, Current Enrollment; Florida Education Identifier; School Year – Record Submission and Course, State Subject Area Requirements.
**Result:** Exception report

**Example:** The second and third of four example records would pass this edit. The first and fourth records would cause an error message to be generated because for the same Florida Education Identifier and the same Course Number there are no matching Course Flags of I and X.

**District Responsibility:** The district should verify the Course Flags submitted along with other elements listed in the edit statement and correct the records if in error.

### 83. Course Flag N requires zero Credit Earned
If Course Flag is N then Credit Earned, Course must be zero.
**Result:** Exception report

**Example:**
| Florida Education Identifier | School Year | Course Number | Course Grade | Course Flag | Credit Earned Course |
|---|---|---|---|---|---|
| *FL123456789100 | 00001 | 1200310 | A | N | 100 |
| FL123456789200 | 0203 | 1001340 | B- | | 100 |
| FL123456789100 | 0001 | 1200320 | B | | 100 |

The second and third records would pass this edit. The first record would cause an error message to be generated because there is a Course Flag of N, but Credit Earned, Course does not equal zero.

**District Responsibility:** The district should verify the Course Flag and the Credit Earned, Course and correct the record if in error.

### 84. Credit Attempted limit for non-multiple-credit courses *(Updated 07/01/2026)*
If the Course Number is not one of the listed Basic Education, Vocational, or Exceptional Education courses offering multiple credit (see source PDF for the full course number list), the Credit Attempted, Course must be less than or equal to 100.
**Result:** Exception report

**Example:** In the source example, a record with Credit Attempted, Course greater than 100 and a Course Number not on the multiple-credit exception list would not pass this edit.

**District Responsibility:** The district should verify the Credit Attempted, Course submitted and correct the records if in error.

### 85. Credit Earned limit for non-multiple-credit courses *(Updated 07/01/2026)*
If the Course Number is not one of the listed Basic Education, Vocational, or Exceptional Education courses offering multiple credit (see source PDF for the full course number list), the Credit Earned, Course must be less than or equal to 100.
**Result:** Exception report

**Example:**
| Course Number | Credit Attempted, Course | Credit Earned, Course |
|---|---|---|
| *7921060 | 100 | 200 |
| *7920060 | 100 | 150 |
| 8100410 | 200 | 200 |

The third record would pass this edit. The first and second records would not pass this edit because Credit Earned, Course is greater than 100 and the Course Number is not one of the exceptions.

**District Responsibility:** The district should verify the Credit Earned, Course submitted and correct the records if in error.
