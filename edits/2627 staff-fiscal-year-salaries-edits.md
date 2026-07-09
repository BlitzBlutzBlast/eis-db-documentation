# Staff Fiscal Year Salaries — Edits and Reject Rules

Source: https://www.fldoe.org/file/20908/2627fys.pdf
Manual: Staff Database 2026-2027

This document covers 41 edits across three categories: Reject Rules (record rejected), State Validation (cross-format matching), and Exception Reports (advisory, does not reject). Edit numbering is non-sequential; Reject Rules run 1-19, then 1A-1B, then 20-29, 32-38, and 41 (gaps at 30-31, 39-40), State Validation runs 52-53, Exception Reports run 81-82.

---

## Reject Rules

### 1. District Number range and status *(Updated 07/01/2026)*
District Number must be numeric, active (A) on the Appendix B: District Name Table and must be correct for the district submitting the data.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number and resubmit the record for processing.

### 2. Social Security Number numeric and left-justified
Social Security Number (SSN) must be numeric and greater than zero, excluding the value 999999999, unless it is a Staff Number Identifier, and the first two positions are "CS", and the last seven positions are numeric. Nine-character SSN's should be left-justified, with a trailing blank.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Social Security Numbers by making them numeric, greater than zero and left-justified. Resubmit the records for processing.

### 3. Survey Period Code must be 5
Survey Period Code must be 5 and must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Survey Period Code on the records being submitted and resubmit the records for processing.

### 4. Fiscal Year correct for submission
Fiscal Year must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Fiscal Year either on the JCL or the records being submitted and resubmit the records for processing.

### 5. School Number, Primary/Home must be valid active school
School Number, Primary/Home must exist on the Master School Identification File as a valid active school in the district of submission.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the School Number, Primary/Home and resubmit the record for processing.

### 6. Job Code must be on Job Code Assignments table
Job Code must equal one of the codes on the Job Code Assignments table as listed in Appendix E of the DOE Information Database Requirements: Volume II Automated Staff Information System Manual.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct Job Code by reporting a valid number from the Job Code Assignments table and resubmit the records for processing.

### 7. Fiscal Year Salary numeric range
Fiscal Year Salary must be numeric, greater than or equal to 000000000 and less than or equal to 045000000.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Fiscal Year Salary to be less than 045000000 and resubmit the record for processing.

### 8. Job Code Fund Source valid codes
Each of the three Job Code Fund Source codes must be one of the following: B, C, E, G, H, M, N, O, P, Q, R, S, T, U or zero.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Job Code Fund Source and resubmit the records for processing.

### 9. Job Code Fund Source percentages numeric
Each of the three Job Code Fund Source percentages must be numeric and greater than or equal to zero.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Job Code Fund Source percentages and resubmit the records for processing.

### 10. At least one Job Code Fund Source code must be nonzero
At least one of the three Job Code Fund Source codes must be nonzero, unless the Fiscal Year Salary is 000000000.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Job Code Fund Source so that is has a valid nonzero code in at least one of the three Job Code Fund Source positions and resubmit the record for processing.

### 11. Job Code Fund Source code may not repeat
Any one Job Code Fund Source code can appear only once on a Staff Fiscal Year Salaries record. For purposes of this edit, zero (used where there are fewer than three fund sources) is NOT treated as a Job Code Fund Source code.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Job Code Fund Source so there is no repetition within that record and resubmit the record for processing.

### 12. Job Code Fund Source percentages must total 100
The three Job Code Fund Source percentages on a Fiscal Year Salaries record must add up to 100 percent. However, if the Fiscal Year Salary is zero, the three Job Code Fund Source percentages may add to zero.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Job Code Fund Source percentages so that they add up to 100 and resubmit the record for processing.

### 13. Additional Compensation Type valid code
Additional Compensation Type code must be A, B, E - K, N - W, Y, Z, 1-4, 6, 7 or zero.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Additional Compensation Type and resubmit the record for processing.

### 14. Additional Compensation Value numeric range
Additional Compensation Value must be numeric, greater than or equal to 0000000 and less than or equal to 9999900.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Additional Compensation Value and resubmit the record for processing.

### 15. Transaction Code validity and existence match
The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified then the record must not already exist on the database; if C or D is specified, then the record must exist on the database.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Transaction Code and resubmit the record with the correct Transaction Code for processing.

### 16. Record uniqueness
Each Staff Fiscal Year Salaries record must be unique based on District Number, Social Security Number (or Staff Number Identifier), Survey Period Code, Fiscal Year, Job Code and Employee Type code.
**Result:** First record accepted, all other duplicate records rejected

**District Responsibility:** If, in fact, the last record above should not have been submitted, the district would not have to take any action. The record was rejected. However, if the record should have been submitted but with a different key, the record should be corrected and resubmitted for processing.

### 17. Additional Compensation Value must be zero or greater than zero to match Type
If Additional Compensation Type equals zero, then Additional Compensation Value should equal zero, and if Additional Compensation Type is not zero, Additional Compensation Value should be greater than zero.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Additional Compensation Value and resubmit the record for processing.

### 18. Additional Compensation Value required when Fiscal Year Salary is zero
If Fiscal Year Salary is 000000000, then at least one Additional Compensation Value must be greater than zero.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Additional Compensation Type/Value or the Fiscal Year Salary and resubmit the record for processing.

### 19. Employment Status Code validity
Employment Status Code must be A, L, P or T.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Employment Status Code and resubmit the record.

### 1A. Job Code FTE numeric range
Job Code FTE must be numeric and less than or equal to 100. If Job Code FTE is not equal to zero, then it must be greater than 004.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Job Code FTE and resubmit the records for processing.

### 1B. Employee Type code validity
Employee Type code must be RF, RP, TF, TP, CF, CP or ST.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Employee Type and resubmit the records for processing.

### 20. Migrant Summer code validity
Migrant Summer code must be A - H, or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Migrant Summer code and resubmit the record for processing.

### 21. Migrant Regular School Year code validity
Migrant Regular School Year code must be A - H, or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Migrant Regular School Year code and resubmit the record for processing.

### 22. Title I School-Wide code validity
Title I School-Wide code must be A, B, C, D, E, F, or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Title I School-Wide code and resubmit the record for processing.

### 23. Title I Targeted Assistance code validity
Title I Targeted Assistance code must be A, B, C, D, E, F or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Title I Targeted Assistance code and resubmit the record for processing.

### 24. Migrant Summer FTE percentage range
Migrant Summer FTE percentage must be numeric and greater than zero but less than or equal to 100, unless the Migrant Summer code is Z, then FTE percentage must be 000.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the FTE percentage for the Migrant Summer code and resubmit the record for processing.

### 25. Migrant Regular School Year FTE percentage range
Migrant Regular School Year FTE percentage must be numeric and greater than zero but less than or equal to 100, unless the Migrant Regular School Year code is Z, then FTE percentage must be 000.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the FTE percentage for the Migrant Regular School Year code and resubmit the record for processing.

### 26. Title I School-Wide FTE percentage range
Title I School-Wide FTE percentage must be numeric and greater than zero but less than or equal to 100, unless the Title I School-Wide code is Z, then FTE percentage must be 000.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the FTE percentage for the Title I School-Wide code and resubmit the record for processing.

### 27. Title I Targeted Assistance FTE percentage range
Title I Targeted Assistance FTE percentage must be numeric and greater than zero but less than or equal to 100, unless the Title I Targeted Assistance code is Z, then FTE percentage must be 000.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the FTE percentage for the Title I Targeted Assistance code and resubmit the record for processing.

### 28. Staff Number Identifier, Local format
The Staff Number Identifier, Local may be any combination of letters, numbers and blanks. All blanks are not allowable. It must be left-justified with trailing blanks.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Staff Number Identifier, Local and resubmit the records.

### 29. Staff Number Identifier, Local must not equal SSN
The Staff Number Identifier, Local must not be identical to the Social Security Number.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Staff Number Identifier, Local or the Social Security Number and resubmit the record.

### 32. Additional Compensation Value must equal $1,000 for Type 6
If Additional Compensation Type code equals 6, then Additional Compensation Value must be equal to $1,000.00.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Additional Compensation Type code or Value and resubmit the records for processing.

### 33. Additional Compensation Value must equal $500 for Type 7
If Additional Compensation Type code equals 7, then Additional Compensation Value must be equal to $500.00.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Additional Compensation Type code or Value and resubmit the record for processing.

### 34. Additional Compensation Types 6 and 7 mutually exclusive
If Additional Compensation Type equals 6, then no other Additional Compensation Type code can equal 7 or vice versa.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Additional Compensation Type code and resubmit the record for processing.

### 35. Job Code FTE numeric range (second occurrence)
Job Code FTE must be numeric, greater than or equal to zero, and less than or equal to 100. If Job Code FTE is not equal to zero, then it must be greater than 004.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Job Code FTE and resubmit the records for processing.

### 36. Job Code FTE greater than zero except specified employee types
Job Code FTE may be equal to or greater than zero for temporary part-time employees, student employees and substitute teachers (Job Code equals to 51080, 52080, 53080, 54080, 55080 or 59080), but must be greater than zero for all other employees.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Job Code FTE and resubmit the record for processing.

### 37. Duty Days numeric range for non-administrative, non-temporary employees
If Job Code is not 71001 or 72000 and if the Employee Type is not ST, TF or TP, then Duty Days must be numeric, greater than zero and not more than 265, unless Fiscal Year Salary is 000000000 or Employment Status Code = P.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Duty Days and resubmit the records for processing.

### 38. Duty Days greater than zero except temporary/substitute employees
Duty Days may be greater than or equal to zero for temporary or student employees (Employee Type = ST, TF or TP) and substitute teachers (Job Code equals to 51080, 52080, 53080, 54080, 55080 or 59080), but must be greater than zero for all other employees, unless Fiscal Year Salary is 000000000 or Employment Status Code = P.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Duty Days to be the standard number of working days for a regular full-time employee and resubmit the record for processing.

### 41. Florida Education Identifier format
Florida Education Identifier (FLEID) is alphanumeric and must be entered as "FL" in the first 2 positions followed by twelve numeric digits. No blanks or spaces are allowable.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Florida Education Identifier and resubmit the record for processing.

---

## State Validation

### 52. Matching Staff Demographic Information record required
Each Fiscal Year Salaries record must have a matching Staff Demographic Information record based on District Number, Social Security Number, Survey Period Code, and Fiscal Year.
**Result:** State validation

**District Responsibility:** The district must verify that the Staff Fiscal Year Salaries record is valid, then submit a Staff Demographic Information record based on District Number, Social Security Number, Survey Code, and Fiscal Year.

### 53. Title I Targeted Assistance requires district-level Targeted-Assistance school
If the Title I Targeted Assistance code is not Z, then at least one active school in the employee's district must have a Targeted-Assistance Program according to the Master School Identification file (identified by code T under Title I Status).
**Result:** State validation

**District Responsibility:** The district must review the information on the Staff Fiscal Year Salaries record and the Master School Identification file to determine where the error is occurring then update the record to reflect the correct relationship in the edit.

---

## Exception Reports

### 81. Job Code 64021-64023 should have Fund Source R or S
If the Job Code is 64021, 64022 or 64023, then one of the Job Code Fund Source codes should be R or S.
**Result:** Exception report

**District Responsibility:** The district should review the data for the second record to verify the entries for Job Code and Job Code Fund Source. If there is an error in the data the district should submit an update to the record.

### 82. Fiscal Year Salary should not be less than $4,000 for RF employees
If Employee Type is RF, then the sum of Fiscal Year Salary on all Staff Fiscal Year Salaries format records for the employee must not be less than $4,000.
**Result:** Exception report

**District Responsibility:** The district should review the data for the second record to verify the entries for Fiscal Year Salary and Employee Type. If there is an error in the data the district should submit an update to the record.
