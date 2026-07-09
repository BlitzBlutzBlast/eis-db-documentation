# Dropout Prevention Program Data — Edits and Reject Rules

Source: https://www.fldoe.org/file/20909/2627dppd.pdf
Manual: Student Database 2026-2027

This document covers 25 edits across three categories: Reject Rules (record rejected), State Validation (cross-format matching), and Exception Reports (advisory, does not reject). Edit numbering is non-sequential; Reject Rules run 1-2, 4-13, 15-16, 21, 23-29, 35, 37-40 (gaps at 3, 14, 17-20, 22, 30-34, 36), State Validation runs 50-51, Exception Reports run 74, 76, 78.

---

## Reject Rules

### 1. District Number, Current Enrollment must be active on Appendix C *(Updated 07/01/2026)*
District Number, Current Enrollment must be numeric and active (A) on the Appendix C: District Name Table.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the District Number, Current Enrollment and resubmit the records.

### 2. School Number, Current Enrollment range
The School Number, Current Enrollment must be alphanumeric and in the range 0001-9899, excluding 9001 and 7006, or it may be 9992, 9993, 9994 or 9995.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Enrollment and resubmit the records.

### 4. Survey Period Code must be 5
Survey Period Code must be 5 and must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Survey Period Code either on the records coming in or the transmission JCL and all records should be resubmitted.

### 5. School Year correct for submission
School Year must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Year either on the records coming in or the transmission JCL and resubmit all records in a batch transaction or add them on-line.

### 6. Dropout Prevention Program Enrollment Date validity for specified program codes *(Updated 07/01/2026)*
If Dropout Prevention/Juvenile Justice Programs code is A, D, E, J, N, P, R, S, T, U or W, then Dropout Prevention Program Enrollment Date must be numeric, a valid date, greater than or equal to 07/01/2015 and less than 08/31/2027.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Dropout Prevention Program Enrollment Date and resubmit the records.

### 7. Dropout Prevention/Juvenile Justice Programs code validity
Dropout Prevention/Juvenile Justice Programs must be A, D, E, J, N, P, R, S, T, U, or W.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Dropout Prevention/Juvenile Justice Programs codes and resubmit the records.

### 8. Dropout Prevention Length of Prescribed Program must be numeric
Dropout Prevention Length of Prescribed Program must be numeric and greater than or equal to zero.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Dropout Prevention Length of Prescribed Program and resubmit the record.

### 9. Fund Source code validity
Fund Source code must be D or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Fund Source and resubmit the record.

### 10. Progress Level, Math code validity
Progress Level - Math code must be C, D, F, G, H, or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Progress Level - Math code and resubmit the record.

### 11. Item 3 filler must be all spaces
Item 3 - Filler on this format in position numbers 7-16 must be all spaces.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must fill the positions noted with all spaces and resubmit the record.

### 12. Progress Level, Reading code validity
Progress Level - Reading code must be C, D, F, G, H or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Progress Level - Reading code and resubmit the record.

### 13. Pretest and Progress codes required after 90+ days in Fund Source D
If Fund Source equals D and Dropout Prevention - Length of Program Participation is equal to or greater than 90, then the codes for Pretest Outcome - Math and Reading and the codes for Progress Level - Math and Reading must not equal Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct either the Dropout Prevention - Length of Program Participation or the codes for Pretest Outcome - Math or Reading and Progress Level - Math or Reading and resubmit the record.

### 15. Length of Program Participation capped at 70 for Term S
If Term equal S, then Dropout Prevention - Length of Program Participation must be numeric, equal to or greater than zero and equal to or less than 70.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Dropout Prevention - Length of Program Participation and resubmit the record.

### 16. Dropout Prevention Program Withdrawal Date validity
Dropout Prevention Program Withdrawal Date must be numeric, a valid date, greater than or equal to 07/01/**** and less than or equal to 08/31/****. Dates will vary depending upon the districts' school calendars.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Dropout Prevention Program Withdrawal Date and resubmit the record.

### 21. Transaction Code validity and existence match
The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified then the record must not already exist on the database; if C or D is specified then the record must exist on the database. An original transaction is the first submission of a record during a survey period. After original transmission of records, changes to the record for elements other than the key elements must be done with a "C" as the Transaction Code. To delete a record, the Transaction Code must be a "D". To change key elements in a batch transaction, the record must FIRST be deleted with a "D" and then added with an "A".
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Transaction Code and resubmit the records.

### 23. Withdrawal Date must not precede Enrollment Date
Dropout Prevention Program Withdrawal Date must be greater than or equal to Dropout Prevention Program Enrollment Date.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Dropout Prevention Program Enrollment Date and/or the Dropout Prevention Program Withdrawal Date and resubmit the record.

### 24. District Number, Current Instruction/Service must match submitting district *(Updated 07/01/2026)*
District Number, Current Instruction/Service must be numeric and active (A) on the Appendix C: District Name Table and must be correct for the district submitting the data.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number, Current Instruction/Service and resubmit the record.

### 25. School Number, Current Instruction/Service range
The School Number, Current Instruction/Service must be alphanumeric and in the range 0001-9899, excluding 9001, or it may be 9992, 9993, 9994 or 9995.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Instruction/Service and resubmit the records.

### 26. Term validity
Term must be 3 or S.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Term and resubmit the record.

### 27. School Number, Current Enrollment must be active except reserved codes
If School Number, Current Enrollment is not 9992, 9993, 9994 or 9995, then the School Number, Current Enrollment must exist on the Master School Identification File as a valid active school number for the District Number, Current Enrollment.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Enrollment and resubmit the records.

### 28. School Number, Current Instruction/Service must be active except reserved codes
If School Number, Current Instruction/Service is not 9992, 9993, 9994 or 9995, then it must exist on the Master School Identification File as a valid active school in the district of instruction.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Instruction/Service and resubmit the records.

### 29. Record uniqueness
Each Dropout Prevention Program Data record must be unique based on the keys of Florida Education Identifier; Survey Period Code; School Year; Dropout Prevention/Juvenile Justice Programs; District Number, Current Instruction/Service; School Number, Current Instruction/Service; and Term.
**Result:** First record accepted, all other duplicate records rejected

**District Responsibility:** If the records loaded to the database are correct, no action is required. However, if the district wishes the rejected records to be loaded to the database, the district must delete any invalid records, correct any rejected records if necessary and resubmit the records.

### 35. Student Number Identifier, Local format
The Student Number Identifier, Local may be any combination of letters, numbers and blanks. (All blanks are allowable.) It must be left-justified with trailing blanks.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Student Number Identifier, Local and resubmit the record.

### 37. Pretest Outcome, Math code validity
Pretest Outcome - Math code must be A, B, H or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Pretest Outcome - Math code and resubmit the record.

### 38. Pretest Outcome, Reading code validity
Pretest Outcome - Reading code must be A, B, H or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Pretest Outcome - Reading code and resubmit the record.

### 39. Length of Program Participation capped at 180 for Term 3
If Term equal 3, then Dropout Prevention - Length of Program Participation must be numeric, equal to or greater than zero and equal to or less than 180.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Dropout Prevention - Length of Program Participation and resubmit the record.

### 40. Florida Education Identifier format
Florida Education Identifier (FLEID) is alphanumeric and must be entered as "FL" in the first 2 positions followed by twelve numeric digits. No blanks, spaces or all zeros for the twelve numeric digits are allowable.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Florida Education Identifier and resubmit the record for processing.

---

## State Validation

### 50. Matching Student Demographic record required
Each Dropout Prevention Program Data record must have a matching Student Demographic record based on District Number, Current Instruction/Service; Florida Education Identifier; Survey Period Code; and School Year.
**Result:** State validation

**District Responsibility:** The district must delete the Dropout Prevention Program Data record or add a Student Demographic record to match the above key fields.

### 51. Grade Level must not be PK/KG for specified program codes
If Dropout Prevention/Juvenile Justice Programs is A, D, E, J, R, T, U or W, then Grade Level may not equal PK or KG.
**Result:** State validation

**District Responsibility:** The district must correct the records so that the appropriate relationship exists between Dropout Prevention/Juvenile Justice Programs and Grade Level.

---

## Exception Reports

### 74. Length of Prescribed Program should be greater than zero except specified programs
If the Dropout Prevention/Juvenile Justice Programs is not equal to D, J, N, S or W, then the Dropout Prevention Length of Prescribed Program must be greater than zero.
**Result:** Exception report

**District Responsibility:** The district should verify the Dropout Prevention Length of Prescribed Program and, if in error, correct the record.

### 76. Length of Prescribed Program should be 1-70 for specified programs during Term S
If Dropout Prevention/Juvenile Justice Programs equals A, E, P, R, T or U and if Term equals S, then the Dropout Prevention Length of Prescribed Program must be greater than zero and less than or equal to 70.
**Result:** Exception report

**District Responsibility:** The district should verify the Dropout Prevention Length of Prescribed Program, and if in error correct the record.

### 78. Length of Prescribed Program should be 1-180 for specified programs during Term 3
If Dropout Prevention/Juvenile Justice Program code equals A, E, P, R, T or U, and if Term equals 3, then Dropout Prevention Length of Prescribed Program must be greater than zero and less than or equal to 180.
**Result:** Exception report

**District Responsibility:** The district should verify the Dropout Prevention Length of Prescribed Program, and if in error correct the record.
