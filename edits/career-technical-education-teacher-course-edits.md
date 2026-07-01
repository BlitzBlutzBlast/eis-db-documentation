# Career and Technical Education Teacher Course — Edits and Reject Rules

Source: [FLDOE Student Database — CTE Teacher Course Edits](https://origin.fldoe.org/file/20909/2627vtc.pdf)
Manual: Student Database 2026-2027

This document covers edits across three categories: Reject Rules (record rejected), State Validation (cross-format matching), and Exception Reports (advisory, does not reject). Edit numbering is non-sequential; gaps are as published in the source.

---

## Reject Rules

### 1. District Number, Current Instruction/Service must be active and match submitter *(Updated 07/01/2026)*
District Number, Current Instruction/Service must be numeric and active (A) on the Appendix C: District Name Table and must be correct for the district submitting the data.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number, Current Instruction/Service and resubmit the record.

### 2. School Number, Current Instruction/Service range
School Number, Current Instruction/Service must be numeric in the range 0001 to 9899, excluding 9001.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Instruction/Service and resubmit the records.

### 3. Survey Period Code must be 5
Survey Period Code must be 5 and must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** The district must correct the Survey Period Code either on the records coming in or in the JCL and resubmit the corrected records.

### 4. School Year must match submission
School Year must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** Correct the School Year codes either on the JCL or the records being submitted and resubmit the records.

### 5. Course Number must be valid on F61730
Course Number must not contain blanks and must be a valid course number (other than "local use only transfer" courses) on the Career and Technical/Adult General Education Program Edit file (F61730).

Note: For more information on Course Number refer to the Career and Technical Database Handbook.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Course Number and resubmit the records.

### 6. Section Number must not be all blanks
Section Number must not be all blanks. Allowable characters are 0-9, A-Z, space, hyphen, dollar sign, pound sign and colon.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Section Number and resubmit the records.

### 7. Period Number must be numeric, non-negative, and not 9999
Period Number must be numeric, greater than or equal to zero, and may not be 9999.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Period Number and resubmit the records.

### 8. Term must be valid code
Term must be either 1-9, B-O, or S-Y.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Term code and resubmit the records.

### 9. Facility Type code must be in range 00-20
Facility Type code must be in the range 00 to 20.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Facility Type code and resubmit the records.

### 13. Florida Educators Certificate Number must be numeric with no embedded blanks
Florida Educators Certificate Number must be numeric with no embedded blanks.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Florida Educators Certificate Number and resubmit the records.

### 14. Transaction Code validity
The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified then the record must not already exist on the database; if C or D is specified then the record must exist on the database.
**Result:** Record rejected

**District Responsibility:** If the rejected records should have been submitted, the district must correct the Transaction Code and resubmit the records with the correct Transaction Code.

### 15. Record uniqueness
Each Career and Technical Education Teacher Course record must be unique based on the following: District Number, Current Instruction/Service; School Number, Current Instruction/Service; School Year; Course Number; Section Number; Period Number; Social Security Number (or Staff Number Identifier); and Term.
**Result:** First record accepted, all other duplicate records rejected

**District Responsibility:** If the records that were accepted and loaded to the database are the correct ones no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must delete the invalid record, correct the rejected record if necessary, and resubmit the corrected record.

### 16. Social Security Number format
Social Security Number (SSN) must be numeric and greater than zero, excluding the value 999999999, unless it is a Staff Number Identifier and the first two positions are "CS" and the last seven positions are numeric. Nine-character SSN's should be left-justified, with a trailing blank.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Social Security Number and resubmit the records.

### 19. Course Numbers M810015 and M810016 not valid for districts
Course Number cannot be = M810015 (Insurance Claims Adjustor) or M810016 (Insurance Customer Service Representative).

Note: These courses are approved only for accredited institutions.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Course Number and resubmit.

### 20. Staff Number Identifier, Local format
The Staff Number Identifier, Local may be any combination of letters, numbers and blanks. All blanks are not allowable. It must be left-justified with trailing blanks.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Staff Number Identifier, Local and resubmit the record.

### 22. Facility Type must not equal 20 for standard active schools *(Updated 07/01/2026)*
If District Number, Current Instruction/Service is active (A) on the Appendix C: District Name Table and if School Number, Current Instruction/Service is not 7001, 7004, 7006, or 7023 and if not a Virtual Charter School (Virtual Charter Schools are identified on MSID by Charter School Status not "Z" and School Function Setting equal to "V"), then Facility Type must not equal 20.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Facility Type or the School Number, Current Instruction/Service and resubmit the record.

### 23. Facility Type must equal 20 for FLVS and Virtual Charter Schools
If District Number, Current Instruction/Service is 71, or if the School Number, Current Instruction/Service is one for which the School Function Setting = V and Charter School Status does not equal Z on the Master School Identification file, then Facility Type must equal 20.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Facility Type and resubmit the record.

### 40. School Number, Current Instruction/Service must be active on Master School ID File
School Number, Current Instruction/Service must exist and be active on the Master School Identification File for the district reported in District Number, Current Instruction/Service.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the School Number, Current Instruction/Service and resubmit the record.

### 42. Period Number digit range validity
The first two digits of Period Number must be 00 to 80. The last two digits of Period Number must be 00 to 80 or 88 and must be greater than or equal to the first two digits.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Period Number and resubmit the records.

### 43. Florida Education Identifier (FLEID) format
Florida Education Identifier (FLEID) is alphanumeric and must be entered as "FL" in the first 2 positions followed by twelve numeric digits. No blanks or spaces are allowable.

Example of valid FLEID: FL 012345678910
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Florida Education Identifier and resubmit the record for processing.

---

## State Validation

### 60. Matching CTE Student Course record required
Each Career and Technical Teacher Course record must have a matching Career and Technical Student Course record based on District Number, Current Instruction/Service; School Number, Current Instruction/Service; School Year; Course Number; Section Number; Period Number and Term.
**Result:** State validation

**District Responsibility:** If the Career and Technical Teacher Course record is valid, submit the matching Career and Technical Student Course records for that class. If the Career and Technical Teacher Course record is invalid, delete the Career and Technical Teacher Course record from the database.

---

## Exception Reports

### 61. Florida Educators Certificate Number must be in valid ranges *(Updated 03/13/2026)*
Florida Educators Certificate Number must be in the following ranges: 0000000001 – 0000999998, 0001000000 - 6001999999, 6002000001 - 6002999999, 6003000001 - 6003999999, 6004000001 - 6004999999, 6007000001 – 6007999999, or 0000000000, 0000999999, 7777777777, 8888888888 or 9999999999.
**Result:** Exception report

**District Responsibility:** The district should verify the Florida Educators Certificate Numbers submitted and correct the records if in error.
