# Career and Technical Education Student Course Schedule — Edits and Reject Rules

Source: [FLDOE Student Database — CTE Student Course Schedule Edits](https://origin.fldoe.org/file/20909/2627vscs.pdf)
Manual: Student Database 2026-2027

This document covers edits across three categories: Reject Rules (record rejected), State Validation (cross-format matching), and Exception Reports (advisory, does not reject). Edit numbering is non-sequential; gaps and alphanumeric IDs (e.g., 4G) are as published in the source.

---

## Reject Rules

### 1. District Number, Current Enrollment must be active on Appendix C *(Updated 07/01/2026)*
District Number, Current Enrollment must be numeric and active (A) on the Appendix C: District Name Table.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number, Current Enrollment and resubmit the record.

### 2. School Number, Current Enrollment range
School Number, Current Enrollment must be numeric in the range 0001 to 9899, excluding 9001 and 7006, or it must be N998 or N999.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Enrollment and resubmit the records.

### 4. Survey Period Code must be 5
Survey Period Code must be 5 and must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** The District must correct the Survey Period Code either on the transmission JCL or on the records and resubmit the records.

### 5. School Year must match submission
School Year must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** Correct the School Year either on the records coming in or the transmission JCL and resubmit all records.

### 6. District Number, Current Instruction/Service must be active and match submitter *(Updated 07/01/2026)*
District Number, Current Instruction/Service must be numeric and active (A) on the Appendix C: District Name Table and must be correct for the district submitting the data.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number, Current Instruction/Service and resubmit the record.

### 7. School Number, Current Instruction/Service range
The School Number, Current Instruction/Service must be numeric in the range 0001-9899, excluding 9001, or it must be C901-C928, U970-U981, or P001-P999.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Instruction/Service and resubmit the records.

### 8. CTE/AGE Program Code must be valid secondary program number
The Career and Technical Education/Adult General Education Program Code must be a valid secondary program number (Supplemental Indicator at position 20 = 'S') for the Course Number submitted, as listed on the Career and Technical Education/Adult General Education Program file (DPS.DISTRICT.GQ.F61730.Yyyyy).
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Career and Technical Education/Adult General Education Program Code and resubmit the record.

### 9. Course Number must be valid secondary course
Course Number must not contain blanks and must be a valid secondary Course Number (Supplemental Indicator at position 20 = 'S') on the Career and Technical Education/Adult General Education Program Edit file (DPS.DISTRICT.GQ.F61730.Yyyyy).
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Course Number and resubmit the records.

### 10. Section Number must not be all blanks
Section Number must not be all blanks. Allowable characters are 0-9, A-Z, space, hyphen, dollar sign, pound sign and colon.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Section Number and resubmit the record.

### 11. Period Number must be numeric and non-negative
Period Number must be numeric, and greater than or equal to zero.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Period Number and resubmit the records.

### 12. Filler positions 7-16 must be all spaces
Item 3 - Filler on this format in position numbers 7-16 must be all spaces.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must fill the positions noted with all spaces and resubmit the record.

### 13. Term must be valid code
Term must be either 1-9, B-O or S-Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Term and resubmit the records.

### 16. Internship Participant must be Y or N
The code for Internship Participant must be Y or N.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Internship Participant codes and resubmit the records.

### 17. Student Number Identifier, Local format
The Student Number Identifier, Local may be any combination of letters, numbers and blanks. (All blanks are allowable.) It must be left-justified with trailing blanks.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Student Number Identifier, Local and resubmit the record.

### 19. Grade Level must be 06-12
Grade Level must be 06-12.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Grade Level and resubmit the records.

### 20. Transaction Code validity
The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified then the record must not already exist on the database; if C or D is specified then the record must exist on the database.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Transaction Code and resubmit the records.

### 21. Record uniqueness
Each record must be unique based on Florida Education Identifier; School Year; District Number, Current Instruction/Service; School Number, Current Instruction/Service; Course Number; Section Number; Period Number and Term.
**Result:** First record accepted, all other duplicate records rejected

**District Responsibility:** If the records that were accepted and loaded to the database are the correct ones, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must delete any invalid records, correct any rejected records if necessary, and resubmit the corrected records.

### 25. Exceptional Student CTE Course Setting must be valid code
On the Career and Technical Student Course Schedule record, Exceptional Student Career and Technical Course Setting code must be one of the following: E, S, M or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Exceptional Student Career and Technical Course Setting code and resubmit the record.

### 39. FEFP Program Number must be valid
FEFP Program Number must be 102, 103, 112, 113, 130, 254, 255, 300, or 999.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the FEFP Program Number and resubmit the records.

### 40. School Number, Current Enrollment must be on Master School ID File
If the School Number, Current Enrollment is not N998 or N999, then it must exist on the Master School Identification File as a valid number in the District Number, Current Enrollment.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Enrollment and resubmit the records.

### 41. School Number, Current Instruction/Service must be active on Master School ID File
If the School Number, Current Instruction/Service is not C901-C928, U970-U981, or P001-P999, then it must exist as a valid active number in the District Number, Current Instruction/Service on the Master School Identification File.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Instruction/Service and resubmit the records.

### 43. Period Number digit range validity
The first two digits of Period Number must be 00-80 while the last two digits must be 00-80 or 88 and be greater than or equal to the first two digits.

Note: For more information on Period Number refer to the DOE Information Database Requirements: Volume I--Automated Student Information System Manual.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Period Number and resubmit the records.

### 45. FEFP Program Number 300 not valid for Grade Level below 09
If Grade Level is less than 09, then the FEFP Program Number must not be 300.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Grade Level or the FEFP Program Number and resubmit the record.

### 46. Apprenticeship Sponsor Code must be on Appendix O or blank
Apprenticeship Sponsor Code must be a valid apprenticeship sponsor code listed in Appendix O, or it must be blank. A code is defined as valid if it is on Appendix O and Program Status is not 'cancelled.'
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Apprenticeship Sponsor Code and resubmit the record.

### 47. Apprenticeship Sponsor Code and CTE Program Code combination must be valid
If the Apprenticeship Sponsor Code is not blank, then the combination of Apprenticeship Sponsor Code and Career and Technical Education/Adult General Education Program Code (FDOE Program Number on Appendix O) must be a valid combination as listed in Appendix O.
**Result:** Record rejected

**District Responsibility:** If the district wishes the data in the rejected record to be loaded to the database, the district must correct the Program Sponsor Code or the FDOE Program Number and resubmit the record.

### 4G. Florida Education Identifier (FLEID) format
Florida Education Identifier (FLEID) is alphanumeric and must be entered as "FL" in the first 2 positions followed by twelve numeric digits. No blanks, spaces or all zeros for the twelve numeric digits are allowable.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Florida Education Identifier and resubmit the record for processing.

---

## State Validation

### 50. Matching CTE Teacher Course record required
If School Number, Current Instruction/Service does not begin with C, P and U, then each Career and Technical Education Student Course record must have a matching Career and Technical Education Teacher Course record based on the key fields of District Number, Current Instruction/Service; School Number, Current Instruction/Service; School Year; Course Number; Section Number; Period Number and Term.
**Result:** State validation

**District Responsibility:** The district must correct the appropriate key field on the Career and Technical Education Student Course Schedule record or submit a matching Career and Technical Education Teacher Course record.

### 51. Matching Student Demographic Information record required
Each Career and Technical Student Course Schedule record must have a matching Student Demographic Information record based on District Number, Current Instruction; Florida Education Identifier; Survey Period Code; and Year.
**Result:** State validation

**District Responsibility:** The district must delete the Career and Technical Student Course Schedule records if they were submitted in error or submit Student Demographic Information records that match on the indicated fields.

---

## Exception Reports

### 60. Grade Level must agree with Student Demographic record
The student's Grade Level code on the Career and Technical Student Course record must agree with the Grade Level code on the Student Demographic record submitted by the district of instruction.
**Result:** Exception report

**District Responsibility:** The district should verify the student's Grade Level to assure that the Grade Level at the time the Career and Technical course was taken is actually different than the student's Grade Level at the end of the school year. If the Grade Level should be the same, correct the Grade Level. If the reported Grade Level is correct, no action is necessary.

### 63. FEFP Program Number expected for course number
If the Course Number is not 8502000 or 00000000, then the FEFP Program Number must be 300, 102, 103, 112, 113, 130, 254 or 255, unless School of Enrollment = 3450 or 3950, then FEFP must be 999.
**Result:** Exception report

**District Responsibility:** The district should verify the FEFP Program Number and the Course Number and correct if in error.
