# Student Course Schedule — Edits and Reject Rules

Source: https://www.fldoe.org/file/20909/2627scs.pdf
Manual: Student Database 2026-2027

This document covers edits across three categories: Reject Rules (record rejected), State Validation (also labeled "Validation/NULL Edit" in this source, cross-format matching), and one uniqueness rule with a non-standard result type ("Record having highest weighted FTE accepted, all other duplicate records rejected"). Edit numbering is non-sequential; gaps and alphanumeric IDs (1A, 2A-2M, 3A-3C, 4A-4I, 5B-5Z) are as published in the source.

**Extraction note:** This file was converted from the source PDF via automated extraction. Reject Rules 1 through 3C/40-59/5B-5Z are captured in full through edit 5Z. State Validation/NULL edits 60, 61, 66, 67, and 69 are captured; edit 69 is cut off mid-sentence in the extracted source ("...Florida Educatio[n Identifier]...") and any edits beyond 69, plus the remainder of 69 itself, were not retrievable in this pass and should be verified against the source PDF directly before being treated as complete.

---

## Reject Rules

### 1. District Number, Current Enrollment range and active status *(Updated 07/01/2026)*
District Number, Current Enrollment must be numeric and active (A) on the Appendix C: District Name Table.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number, Current Enrollment and resubmit the record.

### 2. School Number, Current Enrollment numeric range
School Number, Current Enrollment must be numeric in the range 0001 to 9899 (excluding 3900, 7006 and 9001) or it must be N998 or N999.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Enrollment and resubmit the records.

### 4. Survey Period Code must be 1-4
Survey Period Code must be 1, 2, 3, or 4 and it must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** Correct the Survey Period Code either on the records coming in or the transmission JCL and resubmit all of the records.

### 5. Fiscal Year correct for submission
The Fiscal Year must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** Correct the Fiscal Year either on the transmission JCL or the records being submitted and resubmit all records for processing.

### 6. District Number, Current Instruction/Service correctness
District Number, Current Instruction/Service must be correct for the district submitting the data.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the District Number, Current Instruction/Service and resubmit the records.

### 7. School Number, Current Instruction/Service range by Survey Period
If Survey Period Code is 1, then School Number, Current Instruction/Service must be numeric in the range 0001-9899 or 9996 (excluding 3450, 3900, 3950, 7001, 7004, 7006, 7023, 9001) and excluding schools where the Charter School Status is not Z and School Function/Setting equals V on the Master School Identification file, or School Number, Current Instruction/Service must be C901-C928, U970-U981, or P001-P999. If Survey Period Code = 2 or 3, then School Number, Current Instruction/Service must be numeric in the range 0001-9899 (excluding 3450, 3900, 3950 and 9001), 9996, C901-C928, U970-U981, P001-P999. If Survey Period Code is 4, then School Number, Current Instruction/Service must be numeric in the range 0001-9899 (excluding 3450, 3900, 3950 and 9001), 9996, or School Number, Current Instruction/Service must be C901-C928, U970-U981, or P001-P999.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Instruction/Service and resubmit the records.

### 8. School Number Current Instruction/Service C901-C928 etc. requires correct District Number, Current Enrollment
If the School Number, Current Instruction/Service is C901-C928, U970-U981, P001-P999, 9996, or N999, the District Number, Current Enrollment must be correct for the district submitting the data. If Survey Period Code = 2 or 3 and School Number, Current Instruction/Service is a private school number, the District Number, Current Enrollment must be correct for the district submitting the data.
**Result:** Record rejected

Note: If School Number, Current Instruction/Service is a private school number, Course Number must be 2222222.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Student Course record or the transmission JCL where the mismatch occurs and resubmit the record.

### 9. Course Number must not contain blanks
Course Number must not contain blanks.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Course Number and resubmit the record.

### 10. Section Number must not be all blank
Section Number must not be all blanks. Allowable characters are 0-9, A-Z, space, hyphen (-), dollar sign ($), pound sign (#), ampersand (&), percent (%), forward slash (/) and colon (:).
**Result:** Record rejected

Note: Section Number may be submitted with blanks in one to four of the five positions but may not be submitted with five blanks.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Section Number and resubmit the record.

### 11. Period Number must be numeric
Period Number must be numeric and greater than or equal to zero.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Period Number and resubmit the records.

### 12. Course Number must not be a local use only transfer course
If the School Number Current Instruction/Service does not begin with "P" the Course Number must not be a "local use only transfer" course. If the School Number Current Instruction/Service does not begin with "P" then the Course Number must not begin with 00.
**Result:** Record rejected

Note: Local use only transfer course numbers for Grade Levels 09-12 are numeric course numbers that end in 980 or 990. Local use only transfer course numbers for Grade Levels 30-31 are alphanumeric course numbers that begin with one alpha character and end with six zeroes.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Course Number and resubmit the records.

### 13. Transaction Code validity and existence match
The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified then the record must not already exist on the database; if C or D is specified then the record must exist on the database.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Transaction Code and resubmit the records.

### 14. Record uniqueness
Each Student Course Schedule record must be unique based on Florida Education Identifier; Survey Period Code; Fiscal Year; District Number, Current Instruction/Service; School Number, Current Instruction/Service; Course Number; Section Number; Period Number; and Term.
**Result:** Record having highest weighted FTE accepted, all other duplicate records rejected

**District Responsibility:** If the records that were accepted and loaded to the database are the correct ones, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must delete any invalid records, correct any rejected records if necessary, and resubmit the corrected records.

### 15. Dual Enrollment Indicator validity
Dual Enrollment Indicator must be A, B, C, E, or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Dual Enrollment Indicator and resubmit the record.

### 16. Alphanumeric Course Numbers must be on Course Code Directory or Statewide Course Numbering System
All alphanumeric Course Numbers must either be on the Course Code Directory or on the Statewide Course Numbering System file unless School Number, Current Instruction/Service equals N999 or P001-P999.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Course Numbers and resubmit the records.

### 17. Courses that do not generate FTE require zero FTE and Program Number 999
If Course Number is a course number from the Courses That Do Not Generate FTE file (F71424) or School Number, Current Enrollment is 3450 or 3950, then FTE Reported, Course must be 0000 and FEFP Program Number must be 999.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must appropriately correct the element(s) listed in the edit and resubmit the records.

### 18. FEFP Program Number for Course Number 0800300 or 8502000
If Course Number equals 0800300 or 8502000, then FEFP Program Number must equal 102, 103, 112, 113, 254, 255, or 999.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct either the FEFP Program Number or the Course Number and resubmit the record.

### 19. Course Number 2222222 requires private school number and vice versa
If Course Number equals 2222222, then School Number, Current Instruction/Service must be a private school number and vice versa.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct either the School Number, Current Instruction/Service or the Course Number and resubmit the record.

### 1A. Item 3 filler must be all spaces
Item 3 - Filler on this format in position numbers 7-16 must be all spaces.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must fill the positions noted with all spaces and resubmit the record.

### 20. FEFP Program Number for Dual Enrollment Indicator A, B, C, or E
FEFP Program Number must be 102, 103, 112, 113 or 999 if Dual Enrollment Indicator code = A, B, C, or E.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct either the Dual Enrollment Indicator code or FEFP Program Number and resubmit the record.

### 21. Dual Enrollment Indicator A requires postsecondary School Number
If Dual Enrollment Indicator equals A, then School Number, Current Instruction/Service must be C901-C928, U970-U981 or P001-P999.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the School Number, Current Instruction/Service and resubmit the record.

### 22. Class Minutes, Weekly must be numeric
Class Minutes, Weekly must be numeric and greater than or equal to zero.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Class Minutes, Weekly and resubmit the records.

### 23. FEFP Program Number validity
FEFP Program Number must be 101-103, 111-113, 130, 254-255, 300, or 999.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the FEFP Program Number and resubmit the records.

### 24. FTE Reported, Course must be numeric
FTE Reported, Course must be numeric and greater than or equal to zero. If Period Number is 9800, FTE Reported, Course must be greater than zero and less than or equal to .1667.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the records by assigning a value greater than or equal to zero for FTE Reported, Course and resubmit the records.

### 25. Reading Intervention Component validity by Grade Level
If Grade Level on the Student Course Schedule record is PK, then Reading Intervention Component code must be Z. Otherwise, Reading Intervention Component code must be A, B or N.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Reading Intervention Component codes and resubmit the records.

### 27. VPK Course Numbers require Grade Level PK
If Course Number is 5100520, 5100530, 5100560, 5100570, 5100580, 5100590, 5100600 or 5100610, Grade Level must be PK.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Grade Level or Course Number and resubmit the record.

### 28. School Number, Current Instruction/Service 9996 requires School Number, Current Enrollment N999
If School Number, Current Instruction/Service equals 9996, then School Number, Current Enrollment must be N999.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct either the School Number, Current Enrollment or the School Number, Current Instruction/Service and resubmit the record.

### 29. Grade Level validity
Grade Level must be PK, KG, or 01-12.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Grade Level code and resubmit the records.

### 2A. Dual Enrollment Indicator A requires alphabetic Course Number
If Dual Enrollment Indicator is A and if School Number, Current Instruction/Service is not P001-P999 then Course Number must start with an alphabetic character.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Dual Enrollment Indicator or the Course Number and resubmit the record.

### 2B. Course Grade code validity and justification
The Course Grade code must be A+, A, A-, B+, B, B-, C+, C, C-, D+, D, D-, F, I, IP, N, NNN, U, P, S, E, WP, FL, NG, W, WF or Z and must be right justified with leading blanks.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Course Grade and resubmit the records.

### 2C. Course Grade must not be Z for specified virtual/DJJ/out-of-district settings *(Updated 07/01/2026)*
If Dual Enrollment Indicator = Z and School Number, Current Instruction/Service = 7001, 7004, 7006 or 7023 or District Number, Current Instruction/Service = 71; or if School Number, Current Instruction/Service has a Charter School Status is not Z and School Function/Setting equals V on the Master School Identification file; or Location of Student equals T, and District Number, Current Instruction is not 71, and School Number, Current Instruction does not equal 7001, 7004, 7006, or 7023; then Course Grade may not equal Z. All other schools must equal Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Course Grade and resubmit the record.

### 2D. FTE must be zero for non-fundable automotive service technology courses
If Survey Period Code is 1, 2, 3 or 4; and Course Number is 9504110, 9504120, 9504130, 9504140, 9504150, or 9504160; and District Number, Current Instruction/Service and School Number, Current Instruction/Service exists on the Non-Fundable Automotive Service Technology file (F71340); then FTE Reported, Course must be .0000.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct FTE Reported, Course and resubmit the records.

### 2E. Virtual Instruction Provider code required for virtual charter schools
If the School Number, Current Instruction/Service has a School Function/Setting of V and Charter School Status not equal to Z on the Master School Identification file, then the Virtual Instruction Provider code must be a valid assigned code as specified in Appendix CC.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Virtual Instruction Provider code and resubmit the record.

### 2F. FTE must be zero for failing/incomplete grades in specified virtual/DJJ/out-of-district settings *(Updated 07/01/2026)*
If Dual Enrollment Indicator = Z, Course Number does not equal 2222222 and School Number, Current Instruction/Service = 7001, 7004, 7006 or 7023, or District Number, Current Instruction/Service = 71, or if School Number, Current Instruction/Service has a Charter School Status is not Z and School Function/Setting equals V on the Master School Identification file, or Location of Student equals T and District Number, Current Instruction is not 71 and School Number, Current Instruction does not equal 7001, 7004, 7006, or 7023; and Course Grade is F, I, IP, N, U, WP, FL, NG, W, or WF; then FTE Reported, Course must be .0000.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct FTE Reported, Course and resubmit the records.

### 2G. Online Course Provider code validity by School Number
If the School Number, Current Instruction/Service is 7006, then the Online Course Provider code must be a valid code in Appendix GG. If the School Number, Current Instruction/Service is not 7006, then the Online Course Provider code must be ZZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Online Course Provider or the School Number, Current Instruction/Service and resubmit the record.

### 2H. Course Grade must not be IP for Survey 4 in specified virtual/out-of-district settings *(Updated 07/01/2026)*
If Survey Period = 4 and School Number, Current Instruction/Service = 7001, 7004, 7006 or 7023; or if District Number, Current Instruction/Service = 71 and School Number, Current Instruction/Service = 0300, 0400 or 0801; or School Number, Current Instruction/Service has a Charter School Status other than Z and School Function/Setting equals V on the Master School Identification file; or Location of Student equals T and District Number, Current Instruction is not 71 and School Number, Current Instruction does not equal 7001, 7004, 7006, or 7023; then Course Grade must not equal IP.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct Course Grade and resubmit the record.

### 2I. Grade Level may not be PK in specified virtual/out-of-district settings *(Updated 07/01/2026)*
If School Number, Current Instruction/Service = 7001, 7004, 7006 or 7023 or District Number, Current Instruction/Service = 71; or if School Number, Current Instruction/Service has a Charter School Status other than Z and School Function/Setting equals V on the Master School Identification file; or Location of Student equals T and District Number, Current Instruction is not 71 and School Number, Current Instruction does not equal 7001, 7004, 7006, nor 7023; then Grade Level may not equal PK.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Grade Level and resubmit the record.

### 2L. Grade Level may not be PK for DJJ or county jail/state prison settings
If on the Master School Identification file the School Function/Setting equals D (DJJ) or J (County Jail/State Prison) then Grade Level may not equal PK.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Grade Level and resubmit the record.

### 2M. Dual Enrollment Indicator A/B/C/E requires non-numeric Course Number
If Dual Enrollment Indicator Code equals A, B, C or E, then Course Number must not be all numeric.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Dual Enrollment Indicator and resubmit the record.

### 30. FEFP Program Number 999 requires zero FTE
If Survey Period Code = 1-4 and FEFP Program Number is 999, then FTE Reported, Course must be zero.
**Result:** Record rejected

Note: The use of the FEFP Program Number "999" is for individual students who are not eligible for FTE funding for reasons other than attendance or program membership. These students would include those pre-kindergarten students who are being served in a program for which the student cannot earn FTE.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the relationship between FEFP Program Number and FTE Reported, Course and resubmit the records.

### 31. FEFP Program Number / Grade Level association
In surveys 1 through 4 if the FEFP Program Number is not 999, then there must be a valid association between the FEFP Program Number and the student's Grade Level: 101 (PK-03), 102 (04-08), 103 (09-12), 111 (PK-03), 112 (04-08), 113 (09-12), 130 (KG-12), 254-255 (PK-12), 300 (09-12).
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the FEFP Program Number or the Grade Level so that there is a valid relationship between these two data elements and resubmit the records.

### 32. Grade Level under 06 with FTE prohibits college/university School Number
If Survey Period Code is 1-4, Grade Level is less than 06 and FTE Reported, Course is greater than zero, then School Number, Current Instruction/Service must not be a college nor university (C901-C928, U970-U981 nor P001-P999).
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the relationship between Grade Level; FTE Reported, Course and School Number Current Instruction/Service and resubmit the records.

### 33. Course Number 5100580 requires Survey Period 2 or 3
If Course Number is 5100580 then Survey Period code must be 2 or 3.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Survey Period Code or Course Number and resubmit the records.

### 34. Course Number 5100590 requires Survey Period 1 or 4
If the Course Number is 5100590 then the Survey Period Code must be 1 or 4.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Survey Period Code or Course Number and resubmit the records.

### 35. Term validity
Term must be either 1-9, B-O or S-X.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Term and resubmit the record.

### 36. English Language Learners: Instructional Model validity
English Language Learners: Instructional Model must be E, S, I, C, O, T, or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the English Language Learners: Instructional Model and resubmit the records.

### 37. Year-Round/Extended School Year FTE Indicator validity
Year-Round/Extended School Year FTE Indicator must be A, B or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Year-Round/Extended School Year FTE Indicator codes and resubmit the records.

### 38. Student Number Identifier, Local format
The Student Number Identifier, Local may be any combination of letters, numbers and blanks. (All blanks are allowable.) It must be left-justified with trailing blanks.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Student Number Identifier, Local and resubmit the records.

### 39. FTE must be zero for specified virtual/out-of-district Survey 2/3 settings *(Updated 07/01/2026)*
If Survey Period is 2 or 3, and if Dual Enrollment Indicator is not B nor C, and District Number, Current Instruction/Service = 71 and School Number, Current Instruction/Service = 0300, 0400 or 0801; or if School Number, Current Instruction/Service is 7001 (district virtual instruction program - contracted provider), or 7004 (franchise of Florida Virtual School), or 7006 (KG-12 virtual course offerings), or 7023 (district virtual instruction program - district provider), or Location of Student = T and District Number, Current Instruction is not 71 and School Number Current Instruction does not equal 7001, 7004, 7006 or 7023; then FTE Reported, Course must be 0000. If Survey Period is 2 or 3 and the School Number, Current Instruction/Service has a School Function/Setting of V on the Master School Identification file and the School Number, Current Instruction/Service has a Charter School Status does not equal to Z on the Master School Identification file and Dual Enrollment Indicator is not "B" nor "C", then FTE Reported, Course must be 0000.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Instruction/Service or the FTE Reported, Course and resubmit the records.

### 3A. Year-Round FTE Indicator B requires Survey Period 1 or 4
If Year-Round/Extended School Year FTE Indicator is B, then Survey Period Code must be 1 or 4.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Year-Round/Extended School Year FTE Indicator code and resubmit the record.

### 3B. Apprenticeship Sponsor Code validity by Survey Period
If Survey Period Code is 2 or 3, Apprenticeship Sponsor Code must be a valid apprenticeship sponsor code listed in Appendix O, or it must be blank. A code is defined as valid if it is on Appendix O and Program Status is not 'cancelled.' For Surveys 1 and 4 the Apprenticeship Sponsor Code must be blank.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Apprenticeship Sponsor Code and resubmit the record.

### 3C. Course Number ending in R requires blank Apprenticeship Sponsor Code
If Course Number begins with one alphabetic character and ends with R, then the Apprenticeship Sponsor Code must be blank.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Course Number or the Apprenticeship Sponsor Code and resubmit the record.

### 40. School Number, Current Enrollment must be active except reserved codes
If the School Number, Current Enrollment is not N998 or N999, then it must exist on the Master School Identification File as a valid active number in the District Number, Current Enrollment.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Enrollment and resubmit the records.

### 41. Career and Technical Education/Adult General Education Program Code validity
The Career and Technical Education/Adult General Education Program Code must be a program number from the Career and Technical Education/Adult General Education Program Edit file (F61730) or must be zero-filled.
**Result:** Record rejected

Note: For more information on Vocational/Adult General Education Program Codes refer to the Career and Technical Education Database Handbook Appendices.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Career and Technical Education/Adult General Education Program Code and resubmit the record.

### 42. School Number, Current Instruction/Service must be active or valid alphanumeric
School Number, Current Instruction/Service must exist on the Master School Identification File as a valid active number in the District Number, Current Instruction/Service or it must be C901-C928, U970-U981, P001-P999, or 9996. If Survey Period Code = 2 or 3, then School Number, Current Instruction/Service may be a private school number anywhere in Florida.
**Result:** Record rejected

Note: If School Number, Current Instruction/Service is a private school number, Course Number must be 2222222.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Instruction/Service so that it exists as a valid and active number in the District Number, Current Instruction/Service or is a valid and active alphanumeric school number and resubmit the records.

### 43. Numeric Course Numbers must be on Course Code Directory
All numeric Course Numbers must be on the Course Code Directory file, unless School Number, Current Instruction/Service begins with P.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Course Number and resubmit the records.

### 44. Dual Enrollment Indicator must be Z for Grade Level PK-05
If Grade Level equals PK-05, then the Dual Enrollment Indicator must equal Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the relationship between the Grade Level and the Dual Enrollment Indicator and resubmit the record.

### 45. FEFP Program Number for alphabetic postsecondary Course Numbers
If the Course Number begins with an alpha character and is on the Course Code Directory file, and the School Number, Current Instruction/Service does not begin with P, the FEFP Program Number must be 102, 103, 112 or 113, unless School of Enrollment = 3450 or 3950, then FEFP must be 999.
**Result:** Record rejected

Note: Enrollment of secondary students in postsecondary vocational courses must be reported in the Workforce Development Information System. The parallel allowable dual enrollment hours at the high school are to be reported under the same postsecondary vocational course number but must be funded under the basic program weights of 102, 103, 112 or 113.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Course Number and/or the FEFP Program Number and resubmit the records.

### 46. Period Number digit ranges
The first two digits of the Period Number must be 00-80 while the last two digits must be 00-80 or 88 and be greater than or equal to the first two digits. For Survey 4, period 9800 may also be reported.
**Result:** Record rejected

Note: For more information on Period number refer to the DOE Information Database Requirements: Volume I -- Automated Student Information System Manual.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Period Number and resubmit the records.

### 47. Grade Level 06-12 required when Dual Enrollment Indicator is not Z
If Dual Enrollment Indicator code does not equal Z, then Grade Level must equal 06-12.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the relationship between the Grade Level and the Dual Enrollment Indicator and resubmit the record.

### 48. Dual Enrollment Indicator E requires postsecondary or School Function/Setting T
If Dual Enrollment Indicator equals E, then School Number, Current Instruction/Service must be C901-C928, U970-U981 or P001-P999, or a school on the Master School Identification file that has School Function/Setting equal to T.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the School Number, Current Instruction/Service or the Dual Enrollment Indicator code and resubmit the record.

### 49. Days Per Week validity
Days Per Week must be 1-7. If Period Number is 9800, Days Per Week must equal zero.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Days Per Week and resubmit the record.

### 4A. GED Prep courses require DJJ School Function/Setting
If Course Number = 9900130-9900135 (GED Prep courses), then School Number, Current Instruction/Service must be a valid active school on the Master School Identification (MSID) file with School Function/Setting = D (DJJ).
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Course Numbers on the Student Course Schedule records or the school type on the Master School Identification file and resubmit the records for processing.

### 4B. Location of Student validity
Location of Student must be N, S, T or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Location of Student code and resubmit the record.

### 4C. Florida Education Identifier format
Florida Education Identifier (FLEID) is alphanumeric and must be entered as "FL" in the first 2 positions followed by twelve numeric digits. No blanks, spaces or all zeros for the twelve numeric digits are allowable.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Florida Education Identifier and resubmit the record for processing.

### 4D. Period 9800 requires specific Course Number and Program Number
If Period Number is 9800, Course Number must be 1200310, 2000310, 1206310 or 2100310 and FEFP Program Number must be 102 or 103.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Course Number and resubmit the record for processing.

### 4F. Period 9800 requires all Day of Week Scheduled fields N
If Period Number is 9800, then all of the following must be N: Day of Week Scheduled, Monday; Day of Week Scheduled, Tuesday; Day of Week Scheduled, Wednesday; Day of Week Scheduled, Thursday; Day of Week Scheduled, Friday; Day of Week Scheduled, Saturday.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Day of Week Scheduled, Monday and resubmit the record for processing.

### 4G. Period 9800 requires Day of Week Scheduled, Alternate Date Certain = Z
If Period Number is 9800, Day of Week Scheduled, Alternate Date Certain must be Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Day of Week Scheduled, Alternate Date Certain and resubmit the record for processing.

### 4I. Location of Student validity by School Number
If School Number Current Instruction/Service equals 7001, 7004, 7006, or 7023; or if District Number Current Instruction/Service equals 71; or Charter School Status is not Z and School Function/Setting = V on the Master School Identification file, then Location of Student must be N or S. All other schools must be T, or Z.
**Result:** Record rejected

**District Responsibility:** The district must review the Location of Student code and the School Number and correct the item that is in error.

### 51. Class Minutes, Weekly required for Grade Level 7-12
If Survey Period = 1-4 and the student's Grade Level is 7-12, Class Minutes, Weekly must be greater than zero. If Period Number is 9800, Class Minutes, Weekly must be equal to zero.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the relationships between Grade Level and Class Minutes, Weekly and resubmit the records.

### 52. Private school students require Dual Enrollment Indicator Z
If the School Number, Current Enrollment is N999 (private school), then Dual Enrollment Indicator must be Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Dual Enrollment Indicator or the School Number, Current Enrollment and resubmit the record.

### 53. CTE/AGE Program Code validity by Course Number pattern
If Course Number begins with a number; and is a course number from the Career and Technical Education/Adult General Education Program Edit file (F61730), other than 0200320, 0200335, 1006300, 1700510, 2000350, 2000360, 2102360, 2102370, 3027010 or 3027020; or FEFP Program Number is 300 and course number is one of those listed exceptions; then the Career and Technical Education/Adult General Education Program Code must be a valid program number, other than 9900010 or 9900099, for the Course Number submitted, as listed in file F61730. If Course Number begins with three alphabetic characters followed by a zero in the fourth position, and is a course number from F61730, then the Program Code must be a valid program number for the Course Number submitted, as listed in F61730. If Course Number begins with one alphabetic character followed by a numeric digit, and is a course number from F61730, then the Program Code must be the same as the Course Number.
**Result:** Record rejected

**District Responsibility:** If a record is rejected, the district must verify the correct CTE/AGE Program Code associated with the specific Course Number as defined in the F61730 file. The district must then correct the code and resubmit the record for processing.

### 54. Grade Level validity by Virtual Instruction Provider code *(Updated 07/01/2026)*
If the Virtual Instruction Provider code is 071 (Florida Virtual School), 302 (K12 Florida, LLC), 308 (Somerset Academy, Inc.), 309 (Imagine Learning), 311 (Mater Virtual Academy), or 313 (District VIP - Florida Connections Academy, LLC), then Grade Level must be KG-12. If 320 (Graduation Alliance), Grade Level must be 09-12. If 322 (Accel Online East) or 323 (Optima Academy Online), Grade Level must be KG-12. If 326 (K12 Preparatory Academy), Grade Level must be 9-12. If 327 (UCP of Central Florida), Grade Level must be KG-5. If 328 (Second Mile Education), Grade Level must be 7-12.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Virtual Instruction Provider or the Grade Level and resubmit the record.

### 55. Survey Period Code validity by Term and School Number combination *(Updated 07/01/2026)*
If District Number, Current Instruction is not 71 and School Number, Current Instruction is not 7001, 7004, 7006, or 7023 and if Term equals 4, 5, or S, then Survey Period Code must be 1 or 4. If District Number, Current Instruction is 71 and School Number, Current Instruction equals 0500, 0600 or 0700 and if Term equals 4, 5, or S, then Survey Period Code must be 1, 2, 3 or 4. If District Number, Current Instruction is 71 and School Number, Current Instruction equals 0300 or 0400 or 0801, or if District Number, Current Instruction is not 71 and if School Number, Current Instruction is 7001, 7004, 7006, or 7023 and if Term equals 4, 5 or S, then Survey Period Code must be 4.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Term or Survey Period Code and resubmit the records.

### 56. FEFP Program Number for Grade Level PK
If Grade Level code is PK and the FEFP Program Number is not 111, 254 or 255, then FEFP Program Number must be 101 or 999.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct either the Grade Level or the FEFP Program Number and resubmit the record.

### 57. Virtual Instruction Provider code validity for School Number 7001
If School Number, Current Instruction/Service is 7001, then the Virtual Instruction Provider code must be a valid code in Appendix CC. All other schools except Virtual Charter Schools (where on the Master School ID file School Function/Setting = V and Charter School Status is not equal to Z) must be ZZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Virtual Instruction Provider or the School Number, Current Instruction/Service and resubmit the record.

### 59. Year-Round FTE Indicator A requires Year Round School code Y
If Year-Round/Extended School Year FTE Indicator is A then the Year Round School code on the Master School Identification file must be Y for the reported School Number, Current Instruction/Service. Match to the Master School Identification file using District Number, Current Instruction/Service and School Number, Current Instruction/Service.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Year-Round/Extended School Year FTE Indicator code or the Year Round School code on the Master School Identification file and resubmit the record.

### 5B. Dual Enrollment Indicator required for alphabetic Course Number, Grade 06-12
If Grade Level = 06-12 and Course Number contains an alpha character in the first position, then Dual Enrollment Indicator must be other than Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the relationship between Course Number, Grade Level, and Dual Enrollment Indicator and resubmit the record.

### 5C. English Language Learners Instructional Model validity for Program Number 130
If FEFP Program Number is 130, English Language Learners: Instructional Model code must be C, E, I, O, S, or T.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct either the FEFP Program Number or the English Language Learners: Instructional Model and resubmit the record.

### 5D. Day of Week Scheduled, Monday validity
If Survey Period Code is 2 or 3, then Day of Week Scheduled, Monday must be Y or N.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Day of Week Scheduled, Monday and resubmit the record.

### 5E. Day of Week Scheduled, Tuesday validity
If Survey Period Code is 2 or 3, then Day of Week Scheduled, Tuesday must be Y or N.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Day of Week Scheduled, Tuesday and resubmit the record.

### 5F. Day of Week Scheduled, Wednesday validity
If Survey Period Code is 2 or 3, then Day of Week Scheduled, Wednesday must be Y or N.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Day of Week Scheduled, Wednesday and resubmit the record.

### 5G. Day of Week Scheduled, Thursday validity
If Survey Period Code is 2 or 3, then Day of Week Scheduled, Thursday must be Y or N.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Day of Week Scheduled, Thursday and resubmit the record.

### 5H. Day of Week Scheduled, Friday validity
If Survey Period Code is 2 or 3, then Day of Week Scheduled, Friday must be Y or N.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Day of Week Scheduled, Friday and resubmit the record.

### 5I. Day of Week Scheduled, Saturday validity
If Survey Period Code is 2 or 3, then Day of Week Scheduled, Saturday must be Y or N.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Day of Week Scheduled, Saturday and resubmit the record.

### 5K. At least one Day of Week Scheduled must be Y for non-virtual settings
If Survey Period Code is 2 or 3, and if the School Number, Current Instruction/Service is not 7001, 7004, 7006 or 7023; or the School Number, Current Instruction/Service has a School Function/Setting of V and a Charter School Status not equal to Z on the Master School Identification file; then at least one of the following must be Y: Day of Week Scheduled, Monday; Tuesday; Wednesday; Thursday; Friday; or Saturday.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct at least one Day of Week Scheduled and resubmit the record.

### 5L. Day of Week Scheduled, Alternate Date Certain validity
If Survey Period Code is 2 or 3, then Day of Week Scheduled, Alternate Date Certain must be Y, N or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Day of Week Scheduled, Alternate Date Certain and resubmit the record.

### 5M. Day of Week Scheduled Friday Y requires Alternate Date Certain N or Z
If Survey Period code is 2 or 3 and Day of Week, Scheduled Friday is Y, then Day of Week Scheduled, Alternate Date Certain must be N or Z.
**Result:** Record rejected

Note: Although Day of Week Scheduled, Friday being N does not automatically mean Day of Week Scheduled, Alternate Date Certain is Y, unless all of the students in the entire school are not scheduled in any core classes (See Appendix S) on Friday.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the record so that the correct relationship exists between Day of Week Scheduled, Friday and Day of Week Scheduled, Alternate Date Certain and resubmit the record.

### 5P. FEFP Program Number for District 71 School 0500/0600/0700
If District Number, Current Instruction/Service is equal to 71 and School Number, Current Instruction/Service equals 0500, 0600, or 0700 then FEFP Program Number must equal 101, 102, 103, 111, 112, 113 or 300, unless School of Enrollment = 3450 or 3950, then FEFP must be 999.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the FEFP Program Number and resubmit the record.

### 5Q. FEFP Program Number for School Number 7004 with differing enrollment school
If the School Number, Current Instruction/Service is equal to 7004 and School Number, Current Enrollment is not equal to 7004, then FEFP Program Number must be 101, 102, 103, 111, 112, 113, or 300, unless School of Enrollment = 3450 or 3950, then FEFP must be 999.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the FEFP Program Number and resubmit the record.

### 5S. Course Number 5100580/5100590 requires Program Number 999, zero FTE, and Grade Level PK
If Course Number is 5100580 or 5100590 then FEFP Program Number must be 999 and FTE Reported, Course must be 0000 and Grade Level must be PK.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the FEFP Program Number and the FTE Reported, Course and resubmit the records.

### 5U. Program Number 130 requires Appendix DD Course Number
If Survey Period Code is 2 or 3 and if FEFP Program Number is 130, then the Course Number must be a course in Appendix DD.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct either the Course Number or the FEFP Program Number and resubmit the record.

### 5V. ELL Instructional Model S/C requires Math/Science/Social Studies/Computer Education course
If Survey Period is 2, 3 or 4 and if English Language Learners: Instructional Model is S or C, then Course Number must be a Mathematics, Science, Social Studies or Computer Education course in Appendix DD. If Survey Period is 1 and if English Language Learners: Instructional Model is S or C, then Course Number must be a Mathematics, Science, Social Studies or Computer Education course in the current or prior year in Appendix DD.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct either the English Language Learners: Instructional Model code or the Course Number and resubmit the record.

### 5W. ELL Instructional Model E/I requires Language Arts course
If Survey Period is 2, 3 or 4 and if English Language Learners: Instructional Model is E or I, then Course Number must be a Language Arts Course Number in Appendix DD. If Survey Period is 1 and if English Language Learners: Instructional Model is E or I, then Course Number must be a Language Arts Course Number in the current or prior year in Appendix DD.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct either the English Language Learners: Instructional Model code or the Course Number and resubmit the record.

### 5Y. FEFP Program Number for School Number 7001/7023 mismatch
If School Number, Current Enrollment is not equal to 7001 or 7023 and if School Number, Current Instruction/Service is equal to 7001 or 7023, then FEFP Program Number must be 101, 102, 103, 111, 112, 113, or 300, unless School of Enrollment = 3450 or 3950, then FEFP must be 999.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the FEFP Program Number or School Number, Current Instruction/Service and resubmit the record.

### 5Z. Postsecondary School Number requires non-Z Dual Enrollment Indicator
If the School Number, Current Instruction/Service is C901-C928, U970-U981 or P001-P999, then the Dual Enrollment Indicator must be other than Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Dual Enrollment Indicator and resubmit the record.

---

## State Validation (Validation/NULL Edit)

Edits in this section are labeled "State Validation/NULL" in the source. Rather than rejecting the record outright, a failed edit sets FTE Reported, Course to a NULL value (either for the specific record or, in some cases, for all Student Course Schedule records for the student) at the close of the State Records Processing Cycle.

### 60. Grade Level must agree with Student Demographic record
The student's Grade Level on the Student Course record must agree with the Grade Level on the Student Demographic record submitted by the district of instruction unless Year-Round/Extended School Year FTE Indicator on the Student Course record = A or if Survey Period Code = 1 or 4.
**Result:** State Validation/NULL — FTE Reported, Course on all Student Course records set to NULL value for these records at the close of the State Records Processing Cycle.

**District Responsibility:** The Grade Level codes which do not agree must be corrected. If the Grade Level code on the Student Demographic record is correct, then the Grade Level code on the Student Course record must be updated so that it agrees. If the Grade Level code on the Student Course record is correct, then the Student Demographic record must be updated so that the Grade Level codes agree.

### 61. FTE greater than zero for students under 3 requires Grade Level PK and specified Program Numbers
During Surveys 1 through 4 if FTE Reported, Course is greater than zero and the student is less than 3 years old, then Grade Level must be PK and FEFP Program Number must be 101, 111 or 254-255.
**Result:** State Validation/NULL — FTE Reported, Course set to NULL after the close of the State Records Processing Cycle.

**District Responsibility:** The district must correct the records so that the correct relationship between Grade Level, FEFP Program Number and FTE Reported, Course exists.

### 66. Matching Teacher Course record required *(Updated 07/01/2026)*
If Period Number is not 9800, then each Student Course record must have a matching Teacher Course record based on the key fields of District Number, Current Instruction/Service; School Number, Current Instruction/Service; Survey Period Code; Fiscal Year; Course Number; Section Number; Period Number; and Term.
**Result:** State Validation/NULL — FTE Reported, Course set to NULL following the close of the State Records Processing Cycle.

**District Responsibility:** If the Student Course record is valid, submit the Matching Teacher Course Schedule record for that class. If the Student Course record is invalid, delete the record from the database. If an error has been made in one or more of the data elements required to match on either the Student Course record or the Teacher Course record, then the record(s) should be corrected so that the two types of records match for each of the data elements of District Number, Current Instruction/Service; School Number, Current Instruction/Service; Survey Period Code; Fiscal Year; Course Number; Section Number; Period Number; and Term.

### 67. Matching Student Demographic record required
Each Student Course Schedule must have a matching Student Demographic record based on District Number, Current Enrollment; School Number, Current Enrollment; Florida Education Identifier (FLEID); Survey Period Code; Fiscal Year; and District Number, Current Instruction/Service.
**Result:** State Validation/NULL — FTE Reported, Course set to NULL for ALL Student Course Schedule records for this student.

**District Responsibility:** The district must verify the various key comparisons from the Student Course record, correct those in error and resubmit the correction. For more detailed explanation of the proper submission of the various keys, consult the front pages of both the Student Demographic Information and Student Course Schedule formats.

### 69. Matching Exceptional Student record required for specified Program Numbers *(incomplete — see extraction note)*
If Survey Period Code = 1-4, each Student Course Schedule record with FEFP Program Number equal to 111-113 or 254-255 must have a matching Exceptional Student record based on District Number, Current Enrollment; School Number, Current Enrollment; Florida Education Identifier [text cut off in source extraction — remainder of rule text, Result line, and District Responsibility not captured; verify against source PDF]
**Result:** Not captured in this extraction pass — verify against source PDF.

**District Responsibility:** Not captured in this extraction pass — verify against source PDF.

---

## Note on edits beyond 69

The source document may contain additional State Validation/NULL edits and/or Exception Reports beyond edit 69 (the 2626-27 Student Course Schedule format has historically included matching-record edits for Federal/State Indicator Status, Prior School Status/Student Attendance, and similar cross-format checks in this range, plus possible Exception Report and Aggregate Exception Report sections). These were not retrievable in this extraction pass due to PDF truncation and must be fetched and added in a follow-up pass before this file is treated as a complete replica of the source.
