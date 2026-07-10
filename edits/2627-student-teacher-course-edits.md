# Teacher Course — Edits and Reject Rules

Source: https://www.fldoe.org/file/20909/2627tc.pdf
Manual: Student Database 2026-2027

This document covers edits across three categories: Reject Rules (record rejected), State Validation (cross-format matching), and Exception Reports (advisory). Edit numbering is non-sequential; gaps and alphanumeric IDs (2A-2G, 4A-4B, 5A-5H) are as published in the source.

---

## Reject Rules

### 1. District Number, Current Instruction/Service range and active status *(Updated 07/01/2026)*
District Number, Current Instruction/Service must be numeric and active (A) on the Appendix C: District Name Table.
**Result:** Record rejected

**Example:** If district 01 is submitting records, District Number, Current Instruction/Service must be 01 for all records. A record submitted by district 01 with District Number 02 is rejected.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number, Current Instruction/Service and resubmit the record.

### 2. School Number, Current Instruction/Service range
School Number, Current Instruction/Service must be numeric in the range 0001 to 9899 (excluding 9001), 9996 or it must be C901 to C928, U970 to U981, P001-P999 or N999.
**Result:** Record rejected

**Example:**
| District Number, Current Instruction/Service | School Number, Current Instruction/Service | Survey Period Code | Fiscal Year |
|---|---|---|---|
| *31 | 0800 | 2 | **** |
| *31 | C801 | 2 | **** |
| 31 | 0021 | 2 | **** |

**** = Valid fiscal year for data submission. The third record would be loaded assuming no other reject rule would cause its rejection. The first and second would be rejected because the School Number, Current Instruction/Service is not within the specified range.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Instruction/Service and resubmit the records.

### 3. Survey Period Code must be 1-4
Survey Period Code must be 1, 2, 3, or 4 and it must be correct for the submission specified by the district.
**Result:** Record rejected

**Example:** The Survey Period Code as specified in the transmission JCL or in the statements for tape transmission is identified as Survey Period Code "2" and records are coded as Survey Period Code "3". All updates, adds, or deletes with this inconsistency would be rejected.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Survey Period Code and resubmit the records.

### 4. Fiscal Year correctness
Fiscal Year must be correct for the submission specified by the district.
**Result:** Record rejected

**Example:** The Fiscal Year as specified in the Transmission JCL or in the statements for tape transmission is identified as the valid year for data submission but records being submitted have the previous Fiscal Year coded. All updates, adds or deletes with this inconsistency would be rejected.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Fiscal Year and resubmit the records.

### 5. Course Number must not contain blanks
Course Number must not contain blanks.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Course Number and resubmit the record.

### 6. Section Number must not be all blanks
Section Number must not be all blanks. Allowable characters are 0-9, A-Z, space, hyphen (-), dollar sign ($), pound sign (#), ampersand (&), percent (%), forward slash (/) and colon.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Section Number and resubmit the records.

### 7. Period Number must be numeric
Period Number must be numeric and greater than or equal to zero.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Period Number and resubmit the records.

### 8. Florida Educators Certificate Number format
Florida Educators Certificate Number must be numeric with no embedded blanks.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Florida Educators Certificate Number and resubmit the records.

### 9. Transaction Code validity
The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified then the record must not already exist on the database; if C or D is specified then the record must exist on the database.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Transaction Code and resubmit the records.

### 10. Record uniqueness
Each Teacher Course record must be unique based on District Number, Current Instruction/Service; School Number, Current Instruction/Service; Survey Period Code; Fiscal Year; Term; Course Number; Section Number; Period Number; and Social Security Number (or Staff Number Identifier).
**Result:** First record accepted, all other duplicate records rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the key items and resubmit the record.

### 11. Social Security Number (SSN) format
Social Security Number (SSN) must be numeric and greater than zero, excluding the value 999999999, unless it is a Staff Number Identifier and the first two positions are "CS" and the last seven positions are numeric. Nine-character SSNs should be left-justified, with a trailing blank.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Social Security Number and resubmit the records.

### 12. Florida Educators Certificate Number range for School 7001 *(Updated 04/03/2026)*
If School Number, Current Instruction/Service = 7001, the Florida Educators Certificate Number must be a regular number assigned by the Bureau of Educator Certification in the ranges 0000000001-6001999999, 6002000001-6002999999, 6003000001-6003999999, 6004000001-6004999999, 6007000001-6007999999, or 7777777777, excluding 0000999999, and may not contain blanks.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Florida Educators Certificate Number and resubmit the record.

### 14. Term/Survey Indicator must be Y or N
If Survey Period Code is 1-4, the Term/Survey Indicator must be Y or N.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Term/Survey Indicator or the Survey Period code and resubmit the record.

### 15. Term/Survey Indicator Y required for Survey 1-4, Term 3
If Survey Period Code is 1-4 and Term is 3, the Term/Survey Indicator must be Y.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Term/Survey Indicator or the Term and resubmit the record.

### 16. Term/Survey Indicator Y required for Survey 2, Term 1
If Survey Period Code is 2 and Term is 1, the Term/Survey Indicator must be Y.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Survey Period Code, Term, or Term/Survey Indicator and resubmit the record.

### 17. Term/Survey Indicator Y required for Survey 3, Term 2
If Survey Period Code is 3 and Term is 2, the Term/Survey Indicator must be Y.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Survey Period Code, Term, or Term/Survey Indicator and resubmit the record.

### 18. Certification/Licensure/Qualification Status V required for Course 5100580/5100590
If Course Number is 5100580 or 5100590, then Certification/Licensure/Qualification Status code must be V.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Certification/Licensure/Qualification Status codes or the Course Numbers and resubmit the records.

### 19. Certification/Licensure/Qualification Status V prohibited for non-VPK courses
If Course Number does not equal 5100620, 5100580 or 5100590, then Certification/Licensure/Qualification Status code must not be V.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Certification/Licensure/Qualification Status code or the Course Number and resubmit the record.

### 20. Facility Type range
Facility Type code must be in the range 00 to 20.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Facility Type code and resubmit the record.

### 21. Days in Term (for FTE purposes) must be numeric
For Survey Periods 1-4, Days in Term (for FTE purposes) must be numeric, greater than zero and less than 300.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct Days in Term (for FTE Purposes) and resubmit the records.

### 23. Certification/Licensure/Qualification Status validity
Certification/Licensure/Qualification Status code must be A, B, C, H, I, L, M, N, O, P, S, T or V.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Certification/Licensure/Qualification Status code and resubmit the record.

### 26. Classroom Identification (FISH) Number format by Survey Period
If Survey Period Code is 2 or 3, then the first five positions and positions 7-16 of Classroom Identification (FISH) Number must be numeric. Positions 17-21 may be alpha or numeric. If position 6 is O, positions 17-21 may be symbols. If Survey Period Code is 1 or 4, then each position must contain blank (space), Z or zero.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Classroom Identification (FISH) Number and resubmit the record.

### 27. FISH Number position 6 validity
If Survey Period Code is 2 or 3, then position 6 of the Classroom Identification (FISH) Number must be A, C, F or O.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Classroom Identification (FISH) Number and resubmit the record.

### 28. Scheduling Method validity by Survey Period
If Survey Period Code is 2 or 3, then Scheduling Method must be A, B, C, D, G, I, M, S or W. If Survey Period Code is 1 or 4, then Scheduling Method must be Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Scheduling Method and resubmit the records.

### 29. Facility Type requirements by FISH position 6
If Survey Period Code is 2 or 3 and position 6 of the Classroom Identification (FISH) Number is O, then Facility Type must not be 00. If Survey Period Code is 2 or 3 and position 6 is C, then Facility Type must be 19.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct either the Classroom Identification (FISH) Number or the Facility Type code and resubmit the record.

### 2A. FISH Number must be valid on FLDOE FISH database
If Survey Period is 2 or 3, and position 6 of the Classroom Identification (FISH) Number is A, C or F, the number must be a valid FISH number on the FLDOE FISH database.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Classroom Identification (FISH) Number and resubmit the record.

### 2B. Certificate Number restrictions for status H/I/M/O/P/S
If Certification/Licensure/Qualification Status is H, I, M, O, P or S, then the Florida Educators Certificate Number must not be 0000000000, 0000999999, 7777777777, 8888888888 or 9999999999.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Certification/Licensure/Qualification Status code or the Course Number and resubmit the record.

### 2C. Certificate Number 7777777777 required for status A/T
If Certification/Licensure/Qualification Status code is A or T, then the Florida Educators Certificate Number must be 7777777777.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Certification/Licensure/Qualification Status code or the Course Number and resubmit the record.

### 2D. Certificate Number 8888888888 required for status L
If Certification/Licensure/Qualification Status code is L, then the Florida Educators Certificate Number must be 8888888888.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Certification/Licensure/Qualification Status code or the Course Number and resubmit the record.

### 2E. Primary Instructor Indicator Y required for Scheduling Method C/S
If Scheduling Method is C or S, then the Primary Instructor Indicator code must be Y.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Scheduling Method or Primary Instructor Indicator and resubmit the records.

### 2F. Primary Instructor Indicator Y required for non-Z Team Teacher Training with Scheduling Method C
If the Team Teacher Training code is not Z and Scheduling Method equals C, then Primary Instructor Indicator code must equal Y.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Team Teacher Training code, Scheduling Method or Primary Instructor Indicator code and resubmit the record.

### 2G. MSID Classical Indicator required for Certification Status C
If Certification/Licensure/Qualification Status code is C, then the Classical indicator in the MSID file must be Y.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Certification/Licensure/Qualification Status code or correct/confirm the MSID Classical indicator on the MSID database and resubmit the record.

### 31. Staff Number Identifier, Local format
The Staff Number Identifier, Local may be any combination of letters, numbers and blanks. All blanks are not allowable. It must be left-justified with trailing blanks.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Staff Number Identifier, Local and resubmit the records.

### 33. Team Teacher Training code required for core courses with Scheduling Method C/I
If Course Number Class Size Core Course Indicator on the Course Code Directory = Y, the last two digits of Period Number are not 88, Survey Period Code is 2 or 3, and Scheduling Method is C or I, then the Team Teacher Training code must be A-D.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Team Teacher Training code or the Scheduling Method code and resubmit the record.

### 34. Team Teacher Training validity by Survey Period
For Survey Period Codes 2 and 3, Team Teacher Training must be A-D or Z. For Survey Period Codes 1 and 4, Team Teacher Training must be Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Team Teacher Training codes and resubmit the records.

### 35. Facility Type 20 prohibited for standard schools *(Updated 07/01/2026)*
If District Number, Current Instruction/Service is active (A) on the Appendix C: District Name Table, and School Number, Current Instruction/Service is not 7001, 7006, 7004, or 7023, and the school does not have School Function Setting V with Charter School Status not equal to Z on MSID, then Facility Type must not equal 20.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Facility Type or the School Number, Current Instruction/Service and resubmit the record.

### 36. Facility Type 20 required for District 71 or virtual charter schools
If District Number, Current Instruction/Service is 71, or the School Number, Current Instruction/Service is one for which School Function Setting = V and Charter School Status does not equal Z on MSID, then Facility Type must equal 20.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Facility Type and resubmit the record.

### 37. Fund Source: ESSA Title III validity by Survey Period
If Survey Period Code is 2 or 3, then Fund Source: ESSA Title III must be coded Y or N. If Survey Period Code is 1 or 4, then it must be Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Fund Source: ESSA Title III code and resubmit the record.

### 38. Florida Education Identifier (FLEID) format
Florida Education Identifier (FLEID) is alphanumeric and must be entered as "FL" in the first 2 positions followed by twelve numeric digits. No blanks or spaces are allowable.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Florida Education Identifier and resubmit the record for processing.

### 39. Certification/Licensure/Qualification Status I or V required for Course 5100620
If Course Number equals 5100620, then Certification/Licensure/Qualification Status code must be I or V.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Certification/Licensure/Qualification Status code or the Course Number and resubmit the record.

### 40. School Number, Current Instruction/Service validity against Master School Identification File
School Number, Current Instruction/Service must be valid and active on the Master School Identification File or must be C901 to C928, U970 to U981, P001-P999, 9996, or N999.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Instruction/Service and resubmit the records.

### 41. Numeric Course Numbers must be on Course Code Directory
All numeric Course Numbers must be on the Course Code Directory file unless School Number, Current Instruction/Service is P001-P999.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Course Number and resubmit the records.

### 42. Period Number digit ranges
The first two digits of Period Number must be 00 to 80. The last two digits must be 00 to 80, or 88 and must be greater than or equal to the first two digits.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Period Number and resubmit the records.

### 46. Alphanumeric Course Numbers must be on Course Code Directory or Statewide Course Numbering System
All alphanumeric Course Numbers must be either on the Course Code Directory file or on the Statewide Course Numbering System file unless the School Number, Current Instruction/Service equals N999 or P001-P999.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Course Number and resubmit the records.

### 48. Primary Instructor Indicator validity
Primary Instructor Indicator code must be Y or N.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Primary Instructor Indicator code and resubmit the record.

### 49. Term validity
Term must be either 1-9, B-O or S-X.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Term and resubmit the record.

### 4A. Blended Learning Course code validity
Blended Learning Course code must be Y or N.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Blended Learning Course code and resubmit the record.

### 4B. Blended Learning Course N required for virtual/out-of-district settings
If School Number, Current Instruction/Service = 7001, 7004, 7006 or 7023; or District Number, Current Instruction/Service = 71; or Charter School Status is not Z and School Function/Setting equals V on MSID, then Blended Learning Course must equal N.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Blended Learning Course code and resubmit the record.

---

## State Validation

### 51. Matching Student Course Schedule record required
Each Teacher Course Schedule record must have a matching Student Course Schedule record based on District Number, Current Instruction/Service; School Number, Current Instruction/Service; Survey Period Code; Fiscal Year; Term; Course Number; Section Number and Period Number.
**Result:** State validation

**District Responsibility:** The district must verify if the Teacher Course Schedule record is valid, then submit a matching Student Course Schedule record for that class.

### 53. Scheduling Method consistency for co-taught core courses
Under a specified set of conditions (non-DJJ/Virtual, non-blended, core course indicator Y, appropriate Facility Type, etc.), for each Teacher Course record with Scheduling Method A, all matching records (same district/school/period/term/classroom/survey/fiscal year) must have the same Scheduling Method unless the Scheduling Method is I. For Scheduling Method C or M, at least one matching record must exist with the same Scheduling Method of C or M.
**Result:** State validation

**District Responsibility:** The district must verify whether the Teacher Course record is valid and, if so, submit a matching Teacher Course record based on School Number, Current Instruction/Service; Period Number; Term; Classroom Identification Number, Survey Period Code and Fiscal Year.

### 54. Term 6/7 Term/Survey Indicator mutual exclusivity
For matching Teacher Course records (same district/school/fiscal year/survey/FISH number/course/period), if Survey Period Code is 2 or 3, Term is 6, and Term/Survey Indicator is Y, then records with Term 7 must have Term/Survey Indicator N. Conversely for Term 7 with Term 6.
**Result:** State validation

**District Responsibility:** The district must review the records and correct the Term and/or Term/Survey Indicator code that is in error.

### 55. Term 8/9 Term/Survey Indicator mutual exclusivity
For matching Teacher Course records, if Survey Period Code is 2 or 3, Term is 8, and Term/Survey Indicator is Y, then records with Term 9 must have Term/Survey Indicator N. Conversely for Term 9 with Term 8.
**Result:** State validation

**District Responsibility:** The district must review the records and correct the Term and/or Term/Survey Indicator code that is in error.

### 56. Term J/K/L Term/Survey Indicator single-Y constraint
For matching Teacher Course records, if Survey Period Code is 2 and Term is J, K, or L, only one of these Terms may have a Term/Survey Indicator of Y.
**Result:** State validation

**District Responsibility:** The district must review the records and correct the Term and/or Term/Survey Indicator code that is in error.

### 57. Term M/N/O Term/Survey Indicator single-Y constraint
For matching Teacher Course records, if Survey Period Code is 3 and Term is M, N, or O, only one of these Terms may have a Term/Survey Indicator of Y.
**Result:** State validation

**District Responsibility:** The district must review the records and correct the Term and/or Term/Survey Indicator code that is in error.

### 58. Term E/F/G/H/I Term/Survey Indicator single-Y constraint
For matching Teacher Course records, if Survey Period Code is 2 or 3 and Term is E, F, G, H, or I, only one of these Terms may have a Term/Survey Indicator of Y.
**Result:** State validation

**District Responsibility:** The district must review the records and correct the Term and/or Term/Survey Indicator code that is in error.

### 59. Term B/C/D Term/Survey Indicator single-Y constraint
For matching Teacher Course records, if Survey Period Code is 2 or 3 and Term is B, C or D, only one of these Terms may have a Term/Survey Indicator of Y.
**Result:** State validation

**District Responsibility:** The district must review the records and correct the Term and/or Term/Survey Indicator code that is in error.

### 5A. Term T/U/V/W/X Term/Survey Indicator single-Y constraint
For matching Teacher Course records, if Survey Period Code is 2 or 3 and Term is T, U, V, W or X, only one of these Terms may have a Term/Survey Indicator of Y.
**Result:** State validation

**District Responsibility:** The district must review the records and correct the Term and/or Term/Survey Indicator code that is in error.

### 5B. Matching records must have same Term/Survey Indicator
If Survey Period Code is 2 or 3, then all Teacher Course records that match on district/school/fiscal year/survey/FISH number/course/period/term must have the same Term/Survey Indicator.
**Result:** State validation

**District Responsibility:** The district must review the records and correct the Term and/or Term/Survey code that is in error.

### 5C. At least one Primary Instructor Indicator Y required per class group
If Survey Period Code is 2 or 3, then at least one Primary Instructor Indicator Code must be Y for Teacher Course Schedule records matched on district/school/survey/fiscal year/term/FISH number/period.
**Result:** State validation

**District Responsibility:** The district must determine which teacher is the primary instructor for the class listed and change the Primary Instructor Indicator on that Teacher Course Schedule record to Y.

### 5E. Same FISH number required for matching key-field records
If Survey Period Code is 2 or 3 and Teacher Course records match on district/school/fiscal year/survey/term/course/section/period, then Classroom Identification (FISH) Number must be the same.
**Result:** State validation

**District Responsibility:** If the two teachers are teaching the same class then the district must correct the Classroom Identification (FISH) Number on one of the Teacher Course records so that the two records have the same FISH number. If one record should not have been submitted, the district should delete the incorrect record.

### 5F. Matching Staff Demographic Information record required
Under a specified set of exclusion conditions (not dual enrollment, not certain virtual/DJJ schools, not Charter Status R/C/T/B with Function Setting V, not Location of Student T), each Teacher Course Schedule record must have a matching Staff Demographic Information record based on District Number, Current Instruction/Service; Survey Period Code; Fiscal Year; Social Security Number and Staff Number Identifier, Local.
**Result:** State validation

**District Responsibility:** The district must verify that the Teacher Course Schedule record is valid and submit a matching Staff Demographic Information record on the Staff Information Database.

### 5G. Scheduling Method D requires matching Staff Demographic record with Job Code 59050
If Survey Period Code is 2 or 3, and Scheduling Method code is D, there must be a matching Staff Demographic Information record based on district/survey/fiscal year/SSN/Staff Number Identifier for which the Job Code must be 59050.
**Result:** State validation

**District Responsibility:** The district must verify the relationship between the Scheduling Method code on the Teacher Course record and the Job Code on the matching Staff Demographic Information record. If the Job Code is incorrect, the district must correct it. If the Scheduling Method is incorrect, the district must correct it to a valid code other than D for that staff member, then resubmit.

### 5H. Scheduling Method D requires a paired co-teacher record
If Survey Period Code is 2 or 3, for each Teacher Course record with Scheduling Method equal to D there must exist at least one other Teacher Course record with a different Social Security Number and a different Scheduling Method that is not G, I, or D, matched on district/school/survey/fiscal year/term/course/section/period.
**Result:** State validation

**District Responsibility:** The district must verify whether the Teacher Course record is valid, and, if so, whether a matching Teacher Course record is needed.

---

## Exception Reports

### 63. Florida Educators Certificate Number range *(Updated 04/03/2026)*
Florida Educators Certificate Number must be in the ranges 0000000001-0000999998, 0001000000-6001999999, 6002000001-6002999999, 6003000001-6003999999, 6004000001-6004999999, 6007000001-6007999999, or must be one of 0000000000, 0000999999, 7777777777, 8888888888 or 9999999999.
**Result:** Exception report

**District Responsibility:** The district should verify the Florida Educators Certificate Numbers and correct if in error.

### 65. Scheduling Method C/M requires a paired teacher record
If Survey Period Code equals 2 or 3, for each Teacher Course record with a Scheduling Method equal to C or M there must exist at least one other Teacher Course record with a different Social Security Number and the same Scheduling Method (at least 2 C's or 2 M's), matched on district/school/period/FISH number/survey/fiscal year.
**Result:** Exception report

**District Responsibility:** The district must verify whether the Teacher Course record is valid, and, if so, whether a matching Teacher Course record is needed.

### 66. Scheduling Method I requires a paired non-I record
If Survey Period Code equals 2 or 3 and District Number, Current Instruction/Service is not 71, for each Teacher Course record with Scheduling Method I and end period not 88, there must exist at least one other matching record (different SSN) with Scheduling Method A, B, C, M, S or W.
**Result:** Exception report

**District Responsibility:** The district must verify whether the Teacher Course record is valid, and, if so, whether a matching Teacher Course record is needed.

### 67. Scheduling Method A requires a paired A record with different Course/Section
If Survey Period Code equals 2 or 3, for each Teacher Course record with Scheduling Method A, there must exist at least one other matching record with a different Course/Section combination and the same Scheduling Method (at least 2 A's).
**Result:** Exception report

**District Responsibility:** The district must verify whether the Teacher Course record is valid, and, if so, whether a matching Teacher Course record is needed.

### 68. Co-taught core course (Scheduling Method C) requires certification and experience thresholds
Under a specified set of exclusion conditions (non-DJJ/Virtual, non-blended, appropriate Facility Type, core course indicator Y), for matching Teacher Course records with Scheduling Method C: at least one record must have Certification/Licensure/Qualification Status A, H, I, L, M, P, S, T or V, and at least one teacher in the group must have a sum of three or more years of experience on the Staff Experience format (Experience Type F, N, P or S). The same teacher does not need to satisfy both conditions.
**Result:** Exception report

**District Responsibility:** The district should verify the Certification/Licensure/Qualification Status on the Teacher Course record and the Experience Length on the Staff Experience format, and correct if in error.

### 69. Co-taught core course (Scheduling Method I) requires certification and experience thresholds
Same structure as Edit 68, applied to matching Teacher Course records with Scheduling Method I under the same exclusion conditions.
**Result:** Exception report

**District Responsibility:** The district should verify the Certification/Licensure/Qualification Status on the Teacher Course record and the Experience Length on the Staff Experience format, and correct if in error.
