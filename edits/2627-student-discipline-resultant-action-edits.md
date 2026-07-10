# Student Discipline/Resultant Action — Edits and Reject Rules

Source: https://www.fldoe.org/file/20909/2627sdra.pdf
Manual: Student Database 2026-2027

This document covers edits across four categories: Reject Rules (record rejected), State Validation (cross-format matching), Exception Reports (advisory), and one Aggregate Exception Report (district-level check). Edit numbering is non-sequential; gaps and alphanumeric IDs (2A-2L, 3A, 4-suffix codes) are as published in the source.

---

## Reject Rules

### 1. District Number, Current Enrollment range and active status *(Updated 07/01/2026)*
District Number, Current Enrollment must be numeric, active (A) on the Appendix C: District Name Table and must be correct for the district submitting the data.
**Result:** Record Rejected

**Example:**
| District Number, Current Enrollment | School Number, Current Enrollment | Florida Education Identifier |
|---|---|---|
| 01 | 0021 | FL123456789100 |
| 01 | 0021 | FL123456789200 |
| *00 | 0021 | FL123456789300 |

The first two records would be loaded assuming no other reject rule would cause their rejection. The third record would be rejected since the District Number, Current Enrollment is not active (A) on the Appendix C: District Name Table.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district should correct the District Number, Current Enrollment and resubmit the record.

### 2. School Number, Current Enrollment range
School Number, Current Enrollment must be numeric in the range 0001 to 9899, excluding 9001 and 7006, or it must be N998 or N999.
**Result:** Record Rejected

**Example:**
| District Number, Current Enrollment | School Number, Current Enrollment | Florida Education Identifier |
|---|---|---|
| 01 | 0021 | FL123456789100 |
| 01 | 0021 | FL123456789200 |
| *01 | 9999 | FL123456789300 |
| *01 | C901 | FL123456789400 |

The first two records would be loaded assuming no other reject rules would cause their rejection. The third record would be rejected because the School Number, Current Enrollment is not in the appropriate numerical range. The fourth would be rejected because it is not numeric.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district should correct the School Number, Current Enrollment and resubmit the records.

### 4. Survey Period Code must be 2, 3 or 5
Survey Period Code must be 2, 3 or 5 and must be correct for the submission specified by the district.
**Result:** Record Rejected

**Example:** The Survey Period Code as specified in the transmission JCL or in statements for tape transmission is identified as Survey Period "5". However, records on the transmission have a Survey Period Code "1". All updates, adds or deletes with this inconsistency would be rejected.

**District Responsibility:** The district must correct Survey Period Code either on the records coming in or the Transmission JCL and all records must be submitted.

### 5. School Year correctness
School Year must be correct for the submission specified by the district.
**Result:** Record Rejected

**Example:** The School Year as specified in the transmission JCL or in statements for tape transmission is identified as the valid year for data submission. However, records on the transmission have the previous School Year coded. All updates, adds or deletes with this inconsistency will be rejected.

**District Responsibility:** The district must correct the School Year either on the records coming in or the transmission JCL and resubmit all the records.

### 6. Discipline/Resultant Action Code validity
The Discipline/Resultant Action Code must be alphabetic and must be C, E, F, H, I, N, O, P, S or U.
**Result:** Record Rejected

**Example:**
| District Number, Current Enrollment | Florida Education Identifier | Discipline/Resultant Action Code |
|---|---|---|
| *40 | FL123456789100 | B |
| *40 | FL123456789200 | W |
| 40 | FL123456789300 | C |

The third record would be loaded assuming no other reject rule would cause its rejection. The first two records would be rejected because the Discipline/Resultant Action code is invalid.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district should correct the Discipline/Resultant Action Code and resubmit the records.

### 7. Record uniqueness
Each Student Discipline/Resultant Action record must be unique based on the keys of District Number, Current Enrollment; Florida Education Identifier; Discipline/Resultant Action Code; School Number, Where Discipline/Resultant Action Occurred; Incident, Identifier; Survey Period Code and School Year.
**Result:** Record Rejected

**Example:** Two duplicate records among a set of five would be rejected as duplicates (same District Number, Current Enrollment; Florida Education Identifier; Discipline/Resultant Action Code; School Number, Where Discipline/Resultant Action Occurred; Incident, Identifier; and School Year), while the first, third and fourth records would be loaded assuming no other reject rule would cause their rejection.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must delete any invalid records, correct any rejected records if necessary, and resubmit the corrected records.

### 8. Transaction Code validity
The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified then the record must not already exist on the database; if C or D is specified then the record must exist on the database.
**Result:** Record Rejected

**Example:** For all original transmissions, the Transaction Code must be "A". An original transaction is the first submission of a record during a survey period. After the original transmission of records, changes to the record for elements other than the key elements must be done with a "C" as the Transaction Code. To delete a record, the Transaction Code must be a "D". To change key elements in a batch transaction, the record must FIRST be deleted with a "D" and then added with an "A".

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district should correct the Transaction Code and resubmit the records.

### 9. Incident, Identifier format
Incident, Identifier must be alphanumeric, may not be zero, and must not contain blanks.
**Result:** Record Rejected

**Example:**
| District Number, Current Enrollment | Florida Education Identifier | Incident, Identifier |
|---|---|---|
| *01 | FL123456789100 | 00000000 |
| *01 | FL123456789200 | 46 |
| 01 | FL123456789400 | 00000045 |

The first record would be rejected because the Incident, Identifier code is all zeroes. The second record would be rejected because it contains leading blanks. The third would be loaded assuming no other edit caused it to be rejected.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Incident, Identifier and resubmit the records.

### 10. Incident, Date validity
Incident, Date must be numeric, must be a valid date, in the range of 07/01/**** to 08/31/**** and not greater than the last day of the survey period.
**Result:** Record Rejected

**Example:**
| District Number, Current Enrollment | Survey Period Code | School Number, Where Incident Occurred | Incident, Identifier | Incident, Date |
|---|---|---|---|---|
| 01 | 03 | 0271 | A0000001 | 0122**** |
| *01 | 03 | 0271 | X0000002 | 0308**** |
| *01 | 03 | 0271 | D0000003 | 0230**** |

**** = Valid year for data submission. The first record would be loaded assuming no other reject rule would cause its rejection. The second would be rejected because the Incident, Date is greater than the last day of the survey period. The third would be rejected because Incident, Date is not a valid date.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Incident, Date and resubmit the records.

### 11. Duration, Discipline Action must be numeric
The Duration, Discipline Action must be a three-digit numeric code indicating length of Discipline action.
**Result:** Record Rejected

**Example:**
| District Number, Current Enrollment | School Number, Current Enrollment | Florida Education Identifier | Duration Discipline Action |
|---|---|---|---|
| 01 | 0271 | FL123456789100 | 008 |
| 01 | 0271 | FL123456789200 | 001 |
| *01 | 0271 | FL123456789300 | C01 |

The first two records would be loaded assuming no other reject rule would cause their rejection. The third would be rejected because Duration, Discipline Action is not a valid code.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Duration, Discipline Action code and resubmit the record.

### 12. Item 3 - Filler must be all spaces
Item 3 - Filler on this format in position numbers 7-16 must be all spaces.
**Result:** Record Rejected

**Example:**
| District Number, Current Enrollment | School Number, Current Enrollment | Filler, Item #3 |
|---|---|---|
| 01 | 0151 | |
| *01 | 0151 | 265456789X |

The first record would be loaded assuming no other reject rule would cause its rejection. The second record would be rejected because the data reported is not all spaces.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must fill the positions noted with all spaces and resubmit the record.

### 13. Student, Involved in Hate Crime code validity
Student, Involved in Hate Crime code must be Y or N.
**Result:** Record Rejected

**Example:** A record with an invalid code (Z) is rejected; records coded Y or N are loaded assuming no other reject rule causes rejection.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Student, Involved in Hate Crime code and resubmit the record.

### 14. Student, Use of Alcohol code validity
Student, Use of Alcohol code must be Y or N.
**Result:** Record Rejected

**Example:** A record with an invalid code (Z) is rejected; records coded Y or N are loaded assuming no other reject rule causes rejection.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Student, Use of Alcohol code and resubmit the record.

### 15. Student, Use of Drugs code validity
Student, Use of Drugs code must be Y or N.
**Result:** Record Rejected

**Example:** A record with an invalid code (Z) is rejected; records coded Y or N are loaded assuming no other reject rule causes rejection.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Student, Use of Drugs code and resubmit the record.

### 16. Student, Weapon Use code validity
Student, Weapon Use code must be Y or N.
**Result:** Record Rejected

**Example:** A record with an invalid code (Z) is rejected; records coded Y or N are loaded assuming no other reject rule causes rejection.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Student, Weapon Use code and resubmit the record.

### 17. Discipline Codes C/N require zero Duration
If the Discipline/Resultant Action code is C or N, then Duration, Discipline Action must be zero.
**Result:** Record Rejected

**Example:**
| District Number, Current Enrollment | Florida Education Identifier | Discipline Resultant Action Code | Duration, Discipline Action |
|---|---|---|---|
| 36 | FL123456789100 | C | 000 |
| *36 | FL123456789200 | C | 010 |
| 36 | FL123456789300 | E | 090 |

The first and third records would be loaded assuming no other reject rule would cause their rejection. The second would be rejected because Duration, Discipline Action is greater than zero.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Duration, Discipline Action or the Discipline/Resultant Action Code and resubmit the record.

### 18. Discipline Code O requires Duration 1-10
If the Discipline/Resultant Action code is O, then Duration, Discipline Action must be greater than zero and less than or equal to 10.
**Result:** Record Rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Duration, Discipline Action or the Discipline/Resultant Action Code and resubmit the record.

### 19. Discipline Code I requires Duration 1-10
If the Discipline/Resultant Action code is I, then Duration, Discipline Action must be greater than zero and less than or equal to 10.
**Result:** Record Rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Duration, Discipline Action or the Discipline/Resultant Action Code and resubmit the record.

### 20. School Number, Current Enrollment validity against Master School Identification File
If the School Number, Current Enrollment is not N998 or N999, then it must exist on the Master School Identification File as a valid active school number in the district of enrollment.
**Result:** Record Rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district should correct the School Number, Current Enrollment and resubmit the record.

### 21. School Number, Where Discipline/Resultant Action Occurred validity
The School Number, Where Discipline/Resultant Action Occurred must exist on the Master School Identification File as a valid active school number in the district of enrollment.
**Result:** Record Rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district should correct the School Number, Where Discipline/Resultant Action Occurred and resubmit the record.

### 22. Discipline Code S requires Duration 0-90
If the Discipline/Resultant Action code is S, the Duration, Discipline Action must be equal to or greater than zero and less than or equal to 90.
**Result:** Record Rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Duration, Discipline Action or the Discipline/Resultant Action Code and resubmit the record.

### 23. Birth Date validity
Birth Date must be numeric and a valid date in the format MMDDYYYY.
**Result:** Record Rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Birth Date and resubmit the records.

### 24. Sex code validity
Sex code must be M or F.
**Result:** Record Rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the sex code and resubmit the records.

### 25. District Number, Where Incident Occurred validity *(Updated 07/01/2026)*
District Number, Where Incident Occurred must be numeric and active (A) on the Appendix C: District Name Table.
**Result:** Record Rejected

**Example:**
| District Number, Where Incident Occurred | School Number, Where Incident Occurred | Incident, Identifier |
|---|---|---|
| 01 | 0271 | A0000001 |
| 37 | 0531 | A0000002 |
| *70 | 0011 | D0000003 |

The first two records would be loaded assuming no other reject rule would cause their rejection. The third would be rejected because the District Number, Where Incident Occurred is not active (A) on the Appendix C: District Name Table.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number, Where Incident Occurred and resubmit the records.

### 26. English Language Learners, PK-12 code validity
English Language Learners, PK-12 code must be LA, LY, LF, LP, LZ, or ZZ.
**Result:** Record Rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the English Language Learners, PK-12 codes and resubmit the records.

### 27. Lunch Status validity
Lunch Status must be 0, 1, 3, 4, C, D, E, F, N or R.
**Result:** Record Rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Lunch Status codes and resubmit the records.

### 28. Birth Date must be less than or equal to survey date
Birth Date must be less than or equal to the survey date.
**Result:** Record Rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Birth Date and resubmit the record.

### 29. Grade Level code validity
If Survey Period Code = 2 or 3, Grade Level code must be PK, KG or 01-12. If Survey Period Code = 5, Grade Level code must be PK, KG or 01-12.
**Result:** Record Rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Grade Level codes and resubmit the records.

### 2A. Discipline Code U requires Duration 1-45
If the Discipline/Resultant Action code is U, the Duration, Discipline Action must be greater than zero and less than or equal to 45.
**Result:** Record Rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Duration, Discipline Action or the Discipline/Resultant Action Code and resubmit the record.

### 2B. Grade Level / age association
There must be a valid association between Grade Level and the student's age. For Survey Periods 2 and 3, age will be determined as of Date Certain (Friday) of the survey period. For Survey Period 5, age will be determined as of June 30. Valid age ranges per Grade Level run from PK (not equal to 9+) through Grade 12 (not equal to 0-4, 30+), per the source table.
**Result:** Record Rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the students' Grade Level or Birth Date and resubmit the records.

### 2C. Discipline Code H requires Duration 1-90
If the Discipline/Resultant Action code is H, then Duration, Discipline Action must be greater than zero and less than or equal to 90.
**Result:** Record Rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Duration, Discipline Action element or Discipline/Resultant Action code and resubmit the records.

### 2D. Student Number Identifier, Local format
The Student Number Identifier, Local may be any combination of letters, numbers and blanks. (All blanks are allowable.) It must be left-justified with trailing blanks.
**Result:** Record Rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Student Number Identifier, Local and resubmit the records.

### 2F. School Number, Where Discipline/Resultant Action Occurred range
School Number, Where Discipline/Resultant Action Occurred must be numeric and a valid school number in the range 0001 to 9899, excluding 9001.
**Result:** Record Rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district should correct the School Number, Where Discipline/Resultant Action Occurred and resubmit the records.

### 2G. Student, Involved in Bullying validity
Student, Involved in Bullying must be Y or N.
**Result:** Record Rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Student, Involved in Bullying code and resubmit the record.

### 2H. School Number, Where Incident Occurred range
School Number, Where Incident Occurred must be numeric in the range 0001–9899.
**Result:** Record Rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Where Incident Occurred and resubmit the records.

### 2I. School Number, Where Incident Occurred validity against Master School Identification File
School Number, Where Incident Occurred must exist on the Master School Identification File as a valid active school in the District Number, Current Enrollment.
**Result:** Record Rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the School Number, Where Incident Occurred and resubmit the record.

### 2J. Zero-Tolerance: Expulsions code validity
Zero-Tolerance: Expulsions code must be Y, N or Z.
**Result:** Record Rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Zero-Tolerance: Expulsions code and resubmit the record.

### 2K. Zero-Tolerance: Expulsions and Discipline Code cross-check
If the Zero-Tolerance: Expulsions code is Y or N, then Discipline/Resultant Action Code must be E, F or U. If the Discipline/Resultant Action Code is E, F or U then the Zero-Tolerance: Expulsions code must be Y or N.
**Result:** Record Rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Discipline/Resultant Action Code or the Zero-Tolerance: Expulsions code and resubmit the record.

### 2L. Florida Education Identifier (FLEID) format
Florida Education Identifier (FLEID) is alphanumeric and must be entered as "FL" in the first 2 positions followed by twelve numeric digits. No blanks, spaces or all zeros for the twelve numeric digits are allowable.
**Result:** Record Rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Florida Education Identifier and resubmit the record for processing.

---

## State Validation

### 31. Matching Student Demographic (and End of Year Status) record required
For surveys 2 and 3, each Student Discipline/Resultant Action record must have a matching Student Demographic record based on District Number, Current Enrollment; Florida Education Identifier; Survey Period Code and School Year, unless School Number, Current Enrollment is N998 or N999. For survey 5, each such record must have a matching Student Demographic and Student End of Year Status record under the same key fields and exception.
**Result:** State Validation

**District Responsibility:** The district must delete the Student Discipline/Resultant Action records or add matching Student Demographic Information records.

### 33. Drug Description code required for Student, Use of Drugs = Y
If the Student, Use of Drugs code is Y, then the Drug Description code on the matching School Environmental Safety Incident Report (SESIR) format must be M, N, O or P. The match is done using District Number, Current Enrollment matched to District Number, Where Incident Occurred, along with School Year, Survey Period Code and Incident, Identifier.
**Result:** State Validation

**District Responsibility:** The district should review the Student, Use of Drugs code and the Drug Description code and correct the code that is in error.

### 34. Weapon Use / Weapon-Related cross-check
If Incident, Weapon-Related code on the SESIR record is 1, 2, 3 or 4, then Student, Weapon Use may be Y or N. If Incident, Weapon-Related code is N, then Student, Weapon Use code must be N. The records match on District Number, Current Enrollment/Where Incident Occurred; Survey Period Code; School Year; Incident Identifier; and Incident Date.
**Result:** State Validation

**District Responsibility:** The district must review the Student, Weapon Use and Incident, Weapon-Related codes and correct the one that is in error by submitting a change to the incorrect record.

### 35. Discipline Code E requires matching Withdrawal Code W21
If Survey = 2 or 3 and the Discipline/Resultant Action code is E, then Withdrawal Code, PK-12 on at least one Prior School Status/Student Attendance (PSS/SA) record must = W21. If Survey = 5 and Discipline/Resultant Action code is E, the same requirement applies. The records match on District Number, Current Enrollment; Florida Education Identifier; Survey Period Code; and School Year.
**Result:** State Validation

**District Responsibility:** The district should review the Discipline/Resultant Action code and the Withdrawal Code, PK-12 and correct the code that is in error.

### 36. Discipline Code E prohibits matching non-Gifted Exceptional Student record
If the Discipline/Resultant Action code is E, then there must not be a matching Exceptional Student record unless Exceptionality, Primary = L (Gifted) and Exceptionality, Other = Z. The match is on District Number, Current Enrollment; Survey Period Code; School Year matched to Year; and Florida Education Identifier.
**Result:** State Validation

**District Responsibility:** The district should review the Discipline/Resultant Action code, the Exceptionality, Primary and the Exceptionality, Other and correct the code that is in error.

### 37. Weapon Use = Y requires non-Z Weapon Description
If Student, Weapon Use on the Student Discipline Resultant Action format = Y, then Weapon, Description on the SESIR format must not = Z. The records match on District Number/School Number, Where Incident Occurred matched to Where Discipline/Resultant Action Occurred; Survey Period Code; School Year; Incident Identifier; and Incident Date.
**Result:** State Validation

**District Responsibility:** The district must review the Student, Weapon Use and Weapon, Description codes and correct the one that is in error by submitting a change to the incorrect record.

### 38. Discipline Code U requires matching Exceptional Student record with active placement
If the Discipline/Resultant Action code is U, then there must be a matching Exceptional Student record with Exceptionality, Primary not equal to L, or Primary = L with Exceptionality, Other not equal to Z; an Exceptional Student Dismissal Date of zero or after the Incident Date; and a Placement Date on or before the Incident Date. The match is on District Number, Current Enrollment; Florida Education Identifier; Survey Period Code; and School Year matched to Year.
**Result:** State Validation

**District Responsibility:** The district should review the Discipline/Resultant Action code, the Exceptionality, Primary and the Exceptionality, Other and correct the item that is in error.

### 39. Discipline Code U requires drug/weapon/injury indicator
If the Discipline/Resultant Action Code is U, then one of the following must be true: Student, Use of Drugs = Y; or Student, Weapon Use = Y; or there is a matching SESIR record with an Incident, Injury-Related code of A or B. The records match on District Number/School Number, Where Incident Occurred matched to Where Discipline/Resultant Action Occurred; Survey Period Code; School Year; Incident Identifier; and Incident Date.
**Result:** State Validation

**District Responsibility:** The district must review the Discipline/Resultant Action Code; Student, Use of Drugs code; Student, Weapon Use code and the Incident, Injury-Related code and correct the one that is in error by submitting a change to the incorrect record.

### 3A. Discipline Code S requires matching SESIR record
If Discipline/Resultant Action Code on the Student Discipline/Resultant Action format = S, then there must be a matching record on the School Environmental Safety Incident Report (SESIR) format. The records match on District Number/School Number, Where Incident Occurred matched to Where Discipline/Resultant Action Occurred; Survey Period Code; School Year; Incident Identifier; and Incident Date.
**Result:** State Validation

**District Responsibility:** The district must determine if the Student Discipline/Resultant Action record is in error or if a School Environmental Safety Incident Report record should be added and respond with the appropriate action.

---

## Exception Reports

### 40. Discipline Codes F/P require Duration 1-210
If the Discipline/Resultant Action code is F or P, then Duration, Discipline Action must be greater than zero and less than or equal to 210.
**Result:** Exception Report

**District Responsibility:** The district should verify the Discipline/Resultant Action Code and the Duration, Discipline Action code and correct if in error.

### 41. Discipline Code E requires Duration 1-210
If the Discipline/Resultant Action code is E, then Duration, Discipline Action must be greater than zero and less than or equal to 210.
**Result:** Exception Report

**District Responsibility:** The district should verify the Discipline/Resultant Action Code and the Duration, Discipline Action code and correct if in error.

### 42. Minimum age for KG-12 enrollment
If Grade Level is KG-12, the student must be at least 5 years old on or before September 1 of the school year being reported. Students who transfer to Florida from states with different minimum starting ages are accepted into the grade into which they are transferring.
**Result:** Exception Report

**District Responsibility:** The district should verify the Birth Date and Grade Level and correct one of these if there is an error.

### 44. Discipline Code H requires matching record with E, F or P
If Survey Period Code is 5, and Discipline/Resultant Action code is H, then there must be a matching Student Discipline/Resultant Action record with code E, F, or P. The match is done using District Number, Current Enrollment; Florida Education Identifier; School Number, Where Discipline/Resultant Action Occurred; Incident, Identifier; Survey Period Code; Incident Date; and School Year.
**Result:** Exception Report

**District Responsibility:** The district should verify the Discipline/Resultant Action Code of H and correct it if it is in error. If it is not in error, the district should submit a matching record with a Discipline/Resultant Action Code of E, F or P, if appropriate.

### 45. Discipline Code E requires Withdrawal Reason W21 on End of Year Status
If Survey = 5 and the Discipline/Resultant Action code is E, then the Withdrawal Reason on the Student End of Year Status record must = W21. The records match on District Number, Current Enrollment; Florida Education Identifier; Survey Period Code; and School Year.
**Result:** Exception Report

**District Responsibility:** The district should review the Discipline/Resultant Action code and the Withdrawal Reason code and, if one is found to be in error, revise the incorrect code.

---

## Aggregate Exception Report

### 60. At least one expulsion record required per district in Survey 5
If Survey Period is 5, for each district there must be at least one record with a Discipline/Resultant Action Code of E or F (expelled from school with or without services). An error message will be printed on the exception report for districts that do not meet this aggregate exception edit.
**Result:** Exception Report (aggregate, district-level)

**District Responsibility:** The district must review official expulsion records for the year and submit any missing Student Discipline/Resultant Action records.
