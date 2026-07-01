# Dropout Prevention Program Data — Edits and Reject Rules

Source: [FLDOE Student Database — Dropout Prevention Program Data Edits](https://origin.fldoe.org/file/20909/2627dppd.pdf)
Manual: Student Database 2026-2027

This document covers edits across three categories: Reject Rules (record rejected), State Validation (cross-format matching), and Exception Reports (advisory, does not reject). Edit numbering is non-sequential; gaps are as published in the source.

---

## Reject Rules

### 1. District Number, Current Enrollment must be active on Appendix C *(Updated 07/01/2026)*
District Number, Current Enrollment must be numeric and active (A) on the Appendix C: District Name Table.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the District Number, Current Enrollment and resubmit the records.

### 2. School Number, Current Enrollment range
The School Number, Current Enrollment must be alphanumeric and in the range 0001–9899, excluding 9001 and 7006, or it may be 9992, 9993, 9994 or 9995.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Enrollment and resubmit the records.

### 4. Survey Period Code must be 5
Survey Period Code must be 5 and must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Survey Period Code either on the records coming in or the transmission JCL and all records should be resubmitted.

### 5. School Year must match submission
School Year must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Year either on the records coming in or the transmission JCL and resubmit all records in a batch transaction or add them on-line.

### 6. Dropout Prevention Program Enrollment Date validity *(Updated 07/01/2026)*
If Dropout Prevention/Juvenile Justice Programs code is A, D, E, J, N, P, R, S, T, U or W, then Dropout Prevention Program Enrollment Date must be numeric, a valid date, greater than or equal to 07/01/2015 and less than 08/31/2027.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Dropout Prevention Program Enrollment Date and resubmit the records.

### 7. Dropout Prevention/Juvenile Justice Programs must be valid code
Dropout Prevention/Juvenile Justice Programs must be A, D, E, J, N, P, R, S, T, U, or W.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Dropout Prevention/Juvenile Justice Programs codes and resubmit the records.

### 8. Dropout Prevention Length of Prescribed Program must be numeric
Dropout Prevention Length of Prescribed Program must be numeric and greater than or equal to zero.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Dropout Prevention Length of Prescribed Program and resubmit the record.

### 9. Fund Source code must be D or Z
Fund Source code must be D or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Fund Source and resubmit the record.

### 10. Progress Level – Math must be valid code
Progress Level – Math code must be C, D, F, G, H, or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Progress Level – Math code and resubmit the record.

### 11. Filler positions 7-16 must be all spaces
Item 3 – Filler on this format in position numbers 7–16 must be all spaces.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must fill the positions noted with all spaces and resubmit the record.

### 12. Progress Level – Reading must be valid code
Progress Level – Reading code must be C, D, F, G, H or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Progress Level – Reading code and resubmit the record.

### 13. Pretest Outcome and Progress Level required when Fund Source D and participation >= 90 days
If Fund Source equals D and Dropout Prevention – Length of Program Participation is equal to or greater than 90, then the codes for Pretest Outcome – Math and Reading and the codes for Progress Level – Math and Reading must not equal Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct either the Dropout Prevention – Length of Program Participation or the codes for Pretest Outcome – Math or Reading and Progress Level – Math or Reading and resubmit the record.

### 15. Length of Program Participation limit for Term S
If Term equal S, then Dropout Prevention – Length of Program Participation must be numeric, equal to or greater than zero and equal to or less than 70.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Dropout Prevention – Length of Program Participation and resubmit the record.

### 16. Dropout Prevention Program Withdrawal Date range
Dropout Prevention Program Withdrawal Date must be numeric, a valid date, greater than or equal to 07/01/**** and less than or equal to 08/31/****.

Note: Dates will vary depending upon the districts' school calendars.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Dropout Prevention Program Withdrawal Date and resubmit the record.

### 21. Transaction Code validity
The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified then the record must not already exist on the database; if C or D is specified then the record must exist on the database.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Transaction Code and resubmit the records.

### 23. Withdrawal Date must be on or after Enrollment Date
Dropout Prevention Program Withdrawal Date must be greater than or equal to Dropout Prevention Program Enrollment Date.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Dropout Prevention Program Enrollment Date and/or the Dropout Prevention Program Withdrawal Date and resubmit the record.

### 24. District Number, Current Instruction/Service must be active and match submitter *(Updated 07/01/2026)*
District Number, Current Instruction/Service must be numeric and active (A) on the Appendix C: District Name Table and must be correct for the district submitting the data.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number, Current Instruction/Service and resubmit the record.

### 25. School Number, Current Instruction/Service range
The School Number, Current Instruction/Service must be alphanumeric and in the range 0001–9899, excluding 9001, or it may be 9992, 9993, 9994 or 9995.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Instruction/Service and resubmit the records.

### 26. Term must be 3 or S
Term must be 3 or S.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Term and resubmit the record.

### 27. School Number, Current Enrollment must be active on Master School ID File
If School Number, Current Enrollment is not 9992, 9993, 9994 or 9995, then the School Number, Current Enrollment must exist on the Master School Identification File as a valid active school number for the District Number, Current Enrollment.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Enrollment and resubmit the records.

### 28. School Number, Current Instruction/Service must be active on Master School ID File
If School Number, Current Instruction/Service is not 9992, 9993, 9994 or 9995, then it must exist on the Master School Identification File as a valid active school in the district of instruction.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Instruction/Service and resubmit the records.

### 29. Record uniqueness
Each Dropout Prevention Program Data record must be unique based on the keys of Florida Education Identifier; Survey Period Code; School Year; Dropout Prevention/Juvenile Justice Programs; District Number, Current Instruction/Service; School Number, Current Instruction/Service; and Term.
**Result:** First record accepted, all other duplicate records rejected

**District Responsibility:** If the records loaded to the database are correct, no action is required. However, if the district wishes the rejected records to be loaded to the database, the district must delete any invalid records, correct any rejected records if necessary and resubmit the records.

### 35. Student Number Identifier, Local format
The Student Number Identifier, Local may be any combination of letters, numbers and blanks. (All blanks are allowable.) It must be left–justified with trailing blanks.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Student Number Identifier, Local and resubmit the record.

### 37. Pretest Outcome – Math must be valid code
Pretest Outcome – Math code must be A, B, H or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Pretest Outcome – Math code and resubmit the record.

### 38. Pretest Outcome – Reading must be valid code
Pretest Outcome – Reading code must be A, B, H or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Pretest Outcome – Reading code and resubmit the record.

### 39. Length of Program Participation limit for Term 3
If Term equal 3, then Dropout Prevention – Length of Program Participation must be numeric, equal to or greater than zero and equal to or less than 180.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Dropout Prevention – Length of Program Participation and resubmit the record.

### 40. Florida Education Identifier (FLEID) format
Florida Education Identifier (FLEID) is alphanumeric and must be entered as "FL" in the first 2 positions followed by twelve numeric digits. No blanks, spaces or all zeros for the twelve numeric digits are allowable.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Florida Education Identifier and resubmit the record for processing.

---

## State Validation

### 50. Matching Student Demographic record required
Each Dropout Prevention Program Data record must have a matching Student Demographic record based on District Number, Current Instruction/Service; Florida Education Identifier; Survey Period Code; and School Year.
**Result:** State validation

**District Responsibility:** The district must delete the Dropout Prevention Program Data record or add a Student Demographic record to match the above key fields.

### 51. Grade Level restriction for certain program codes
If Dropout Prevention/Juvenile Justice Programs is A, D, E, J, R, T, U or W, then Grade Level may not equal PK or KG.
**Result:** State validation

**District Responsibility:** The district must correct the records so that the appropriate relationship exists between Dropout Prevention/Juvenile Justice Programs and Grade Level.

---

## Exception Reports

### 74. Length of Prescribed Program should be greater than zero for most program codes
If the Dropout Prevention/Juvenile Justice Programs is not equal to D, J, N, S or W, then the Dropout Prevention Length of Prescribed Program must be greater than zero.
**Result:** Exception report

**District Responsibility:** The district should verify the Dropout Prevention Length of Prescribed Program and, if in error, correct the record.

### 76. Prescribed Program length for Term S must be 1-70 for certain program codes
If Dropout Prevention/Juvenile Justice Programs equals A, E, P, R, T or U and if Term equals S, then the Dropout Prevention Length of Prescribed Program must be greater than zero and less than or equal to 70.
**Result:** Exception report

**District Responsibility:** The district should verify the Dropout Prevention Length of Prescribed Program, and if in error correct the record.

### 78. Prescribed Program length for Term 3 must be 1-180 for certain program codes
If Dropout Prevention/Juvenile Justice Program code equals A, E, P, R, T or U, and if Term equals 3, then Dropout Prevention Length of Prescribed Program must be greater than zero and less than or equal to 180.
**Result:** Exception report

**District Responsibility:** The district should verify the Dropout Prevention Length of Prescribed Program, and if in error correct the record.
