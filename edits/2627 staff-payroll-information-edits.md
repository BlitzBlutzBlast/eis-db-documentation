# Staff Payroll Information — Edits and Reject Rules

Source: https://www.fldoe.org/file/20908/2627pi.pdf
Manual: Staff Database 2026-2027

This document covers 47 edits across three categories: Reject Rules (record rejected), State Validation (cross-format matching), and Exception Reports (advisory, does not reject). Edit numbering is non-sequential; Reject Rules run 1-19, then 1A, then 20-25, 27-35, 37-39, 42-44, 46-49 (with gaps at 26, 36, 40-41, 45), State Validation runs 50-54 and 57-58, Exception Reports run 60, 62, 64, 65, 66.

---

## Reject Rules

### 1. District Number range and status *(Updated 07/01/2026)*
District Number must be numeric, active (A) on the Appendix B: District Name Table and must be correct for the district submitting the data.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number and resubmit the record for processing.

### 2. Social Security Number numeric and left-justified
Social Security Number (SSN) must be numeric and greater than zero, excluding the value 999999999, unless it is a Staff Number Identifier and the first two positions are "CS" and the last seven positions are numeric. Nine-character SSN's should be left-justified, with a trailing blank.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Social Security Numbers by making them numeric, greater than zero and left-justified. Resubmit the records for processing.

### 3. Survey Period Code correct for submission
Survey Period Code must be correct for the submission specified by the district and must be 2 or 3.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Survey Period Code either on the records coming in or in the JCL and resubmit the records for processing.

### 4. Fiscal Year correct for submission
Fiscal Year must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Fiscal Year either on the JCL or the records being submitted and resubmit the records for processing.

### 5. School Number, Primary/Home must be valid active school
School Number, Primary/Home must exist on the Master School Identification File as a valid active school in the district of submission.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the School Number, Primary/Home and resubmit the record.

### 6. Job Code, Primary must be on Job Code Assignments table
Job Code, Primary must equal one of the codes on the Job Code Assignments table as listed in Appendix E of the DOE Information Database Requirements: Volume II-- Automated Staff Information System Manual.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct Job Code, Primary by reporting a valid number from the Job Code Assignments table and resubmit the records for processing.

### 7. Job Code FTE numeric range
Job Code FTE must be numeric, greater than or equal to zero, and less than or equal to 100. If Job Code FTE is not equal to zero, then it must be greater than 004.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Job Code FTE and resubmit the records for processing.

### 8. Job Code Fund Source valid codes
Each of the three Job Code Fund Source codes must be one of the following: B, C, E, G, H, M, N, O, P, Q, R, S, T, U or zero.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Job Code Fund Source and resubmit the records for processing.

### 9. Job Code Fund Source percentages numeric
Each of the three Job Code Fund Source percentages must be numeric and greater than or equal to zero.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Job Code Fund Source percentages and resubmit the records for processing.

### 10. Grandfathered Salary Schedule Pay Type Indicator validity
Grandfathered Salary Schedule Pay Type Indicator must be Y, N or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Salary Schedule Pay Type Indicator and resubmit the records for processing.

### 11. Salary Schedule Pay Type must be B when Indicator is Y
If Grandfathered Salary Schedule Pay Type Indicator = Y, then Salary Schedule Pay Type must be B.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Grandfathered Salary Schedule Pay Type Indicator or the Salary Schedule Pay Type and resubmit the record for processing.

### 12. Salary Schedule Pay Type range when Indicator is N
If Grandfathered Salary Schedule Pay Type Indicator equals N, then Salary Schedule Pay Type must equal 1-7, A or B.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Grandfathered Salary Schedule Pay Type Indicator or the Salary Schedule Pay Type and resubmit the record for processing.

### 13. Salary Schedule Pay Type range when Indicator is Z
If Grandfathered Salary Schedule Pay Type Indicator = Z, then Salary Schedule Pay Type must equal 0, 8 or B.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Grandfathered Salary Schedule Pay Type Indicator or the Salary Schedule Pay Type and resubmit the record for processing.

### 14. Duty Days numeric range
If Job Code, Primary is not 71001 or 72000, then Duty Days must be numeric, greater than or equal to zero, and not more than 265.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Duty Days and resubmit the records for processing.

### 15. Employment Length numeric range and rounding
Employment Length must be numeric, greater than or equal to zero and less than or equal to 12.0. Since this value must be rounded to the nearest half month, all values must end in either zero or five.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Employment Length and resubmit the records for processing.

### 16. Employment Status Code validity
Employment Status Code must be A or P.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Employment Status Codes and resubmit the records for processing.

### 17. Employee Type code validity
Employee Type code must be RF, RP, TF, TP, CF, CP or ST.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Employee Type and resubmit the records for processing.

### 18. School Number must be 9001 for Job Code 71001
If Job Code, Primary = 71001, then School Number, Primary/Home must be 9001.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the School Number, Primary/Home or the Job Code, Primary and resubmit the record for processing.

### 19. Salary Schedule Pay Type validity
Salary Schedule Pay Type must be 0-8, A or B.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Salary Schedule Pay Type and resubmit the records for processing.

### 1A. Salary Adjustment/Type codes A and B mutually exclusive for instructional Job Codes
If the employee's Job Code places the employee on lines 09-19 or 21-43, inclusive, of the Public Schools Staff Survey - EEO-5, excluding Job Codes 73026 (Registrar), 51080, 52080, 53080, 54080, 55080 or 59080 (Substitute Teachers) and the Salary Adjustment/Type code is A, then a subsequent Salary Adjustment/Type code cannot be B; or if the Salary Adjustment/Type code is B, then a subsequent Salary Adjustment/Type code cannot be A.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Salary Adjustment/Type code and resubmit the records for processing.

### 20. Salary Schedule Step numeric range
Salary Schedule Step must be numeric, from 00 through 99.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Salary Schedule Step and resubmit the records for processing.

### 21. Transaction Code validity and existence match
The Transaction Code must be A, C, or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified then the record must not already exist on the database; if C or D is specified, then the record must exist on the database.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Transaction Code and resubmit the records for processing with the correct Transaction Code.

### 22. Address, Mailing street portion must not be blank for EEO-5 lines 1-43
If the employee's Job Code places the employee on lines 1-43, inclusive, of the Public Schools Staff Survey - EEO-5, then the first 25 characters of Address, Mailing must not all be blank.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Address, Mailing so that the first 25 characters contain the employee's street number and name, P.O. box, or apartment number, etc. and resubmit the record for processing.

### 23. Address, Mailing city must not be blank for EEO-5 lines 1-43
If the employee's Job Code places the employee on lines 1-43, inclusive, of the Public Schools Staff Survey - EEO-5, then the city in Address, Mailing must not be all blanks.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Address, Mailing to contain the employee's city and resubmit the record for processing.

### 24. Address, Mailing state code validity
If the employee's Job Code places the employee on lines 1-43, inclusive, of the Public Schools Staff Survey - EEO-5, then the state code in Address, Mailing must be one of those listed in Appendix H: State Codes in the DOE Information Database Requirements: Volume II - Automated Staff Information System. If the employee's Job Code does not place the employee on lines 1-43, inclusive, of the Public Schools Staff Survey - EEO-5, then the state code must either be blank or it must be a valid state code as listed in Appendix H: State Codes.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Address, Mailing to contain a valid state code and resubmit the record for processing.

### 25. Address, Mailing zip code validity
If the employee's Job Code places the employee on lines 1-43, inclusive, of the Public Schools Staff Survey - EEO-5, then each character of zip code in Address, Mailing must be numerical and the first five characters taken together must contain a number greater than zero. If the employee's Job Code does not place the employee on lines 1-43, inclusive, of the Public Schools Staff Survey - EEO-5, then the zip code must either be blank or must follow the above edit rule.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Address, Mailing to contain a valid zip code and resubmit the record for processing.

### 27. Salary, Annual numeric range
Salary, Annual must be numeric, greater than 000000000 and less than or equal to 045000000, unless Employee Type = TP or ST then Salary, Annual may be zero.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Salary, Annual and resubmit the record for processing.

### 28. Staff Number Identifier, Local format
The Staff Number Identifier, Local may be any combination of letters, numbers and blanks. All blanks are not allowable. It must be left-justified with trailing blanks.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Staff Number Identifier, Local and resubmit the records.

### 29. Staff Number Identifier, Local must not equal SSN
The Staff Number Identifier, Local must not be identical to the Social Security Number.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Staff Number Identifier, Local or the Social Security Number and resubmit the record.

### 30. At least one Job Code Fund Source code must be nonzero
At least one of the three Job Code Fund Source codes must be nonzero.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Job Code Fund Source so that there is a valid nonzero job code in at least one of the three Job Code Fund Source positions and resubmit the record for processing.

### 31. Job Code Fund Source code may not repeat
Any one Job Code Fund Source code can appear only once on a Staff Payroll record. For purposes of this edit, zero (used where there are fewer than three fund sources) is NOT treated as a Job Code Fund Source code.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Job Code Fund Source so there is no repetition within that record and resubmit the record for processing.

### 32. Job Code Fund Source percentages must total 100
The three Job Code Fund Source percentages on a Staff Payroll record must add up to 100 percent.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Job Code Fund Source percentages so that they add up to 100 and resubmit the record for processing.

### 33. Salary, Annual may be zero only for temporary part-time or student employees
Salary, Annual may be zero for temporary part-time or student employees only.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the relationship between the Salary, Annual and the Employee Type and resubmit the record for processing.

### 34. Salary Adjustment/Type code validity and uniqueness
The Salary Adjustment/Type code must be A, B, C, D, E, F, or Z. Each Salary Adjustment/Type code must be unique, unless the code is Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Salary Adjustment/Type code and resubmit the record for processing.

### 35. Salary Adjustment/Type value numeric requirement
Salary Adjustment/Type value must be numeric and greater than zero if Salary Adjustment/Type code is A, B, C, D, E or F. If Salary Adjustment/Type code is Z, then Salary Adjustment/Type value must be zero.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Salary Adjustment/Type value and resubmit the record for processing.

### 37. Job Code FTE greater than zero except specified employee types
Job Code FTE may be equal to or greater than zero for temporary part-time employees, student employees and substitute teachers (Job Code, Primary codes equal to 51080, 52080, 53080, 54080, 55080 or 59080), but must be greater than zero for all other employees.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Job Code FTE and resubmit the record for processing.

### 38. Duty Days greater than zero except temporary/substitute employees
Duty Days may be zero or greater than zero for temporary or student employees and substitute teachers (Job Code, Primary codes equal to 51080, 52080, 53080, 54080, 55080 or 59080), but must be greater than zero for all other employees.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Duty Days to be the standard number of working days for a regular full-time employee and resubmit the record for processing.

### 39. Employment Length greater than zero except temporary/substitute employees
Employment Length may be zero for temporary employees, student employees, and substitute teachers (Job Code, Primary equal to 51080, 52080, 53080, 54080, 55080 or 59080), but must be greater than zero for all other employees.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Employment Length to be the standard number of months for a regular full-time employee and resubmit the record for processing.

### 42. Salary Schedule Step must match Salary Schedule Pay Type
If Salary Schedule Pay Type equals 1-7 or A, then Salary Schedule Step must be 00-97. If Salary Schedule Pay Type equals 8, then Salary Schedule Step must be 98. If Salary Schedule Pay Type equals B, then Salary Schedule Step must be 00-97 or 99. If Salary Schedule Pay Type equals 0, then Salary Schedule Step must be 99.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the relationship between the Salary Schedule Pay Type and Salary Schedule Step and resubmit the records for processing.

### 43. Record uniqueness
Each Staff Payroll record must be unique based on District Number; Social Security Number (or Staff Number Identifier); Survey Period Code; Fiscal Year; Job Code, Primary and Employee Type code.
**Result:** Record rejected

**District Responsibility:** If, in fact, the last record should not have been submitted, the district would not have to take any action. The record was rejected. However, if the record should have been submitted but with a different key, the record should be corrected and resubmitted. If the district wishes to update some item in this record, the record should be submitted with a Transaction Code of "C" rather than "A."

### 44. Salary, Annual cap for EEO-5 lines 21-43
If the employee's Job Code places the employee on lines 21-43, inclusive, of the Public Schools Staff Survey - EEO-5, then the Salary, Annual must not be greater than $175,000.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Salary, Annual and resubmit the records for processing.

### 46. Salary Adjustment/Type A or B requires instructional Job Code
If Salary Adjustment/Type code is A or B, then the employee's Job Code must place the employee on lines 09-19 or 21-43, inclusive, of the Public Schools Staff Survey - EEO 5, excluding Job Codes 73026 (Registrar), 51080, 52080, 53080, 54080, 55080 or 59080 (Substitute Teachers).
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Salary Adjustment/Type code or the Job Code, Primary and resubmit the record for processing.

### 47. Florida Education Identifier format
Florida Education Identifier (FLEID) is alphanumeric and must be entered as "FL" in the first 2 positions followed by twelve numeric digits. No blanks or spaces are allowable.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Florida Education Identifier and resubmit the record for processing.

### 48. Contract Status code validity
Contract Status code must be AC, CC, MY, PC, PS, SS, or ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Contract Status and resubmit the records for processing.

### 49. Contract Status code must match Salary Schedule Pay Type
Contract Status code must be AC, CC, MY, PC, PS, or SS for employees whose Salary Schedule Pay Type equals 1-7, A or B, unless the employee's Job Code places the employee on lines 09-20, inclusive, of the Public Schools Staff Survey - EEO-5, then Contract Status code must be ZZ. All others must be ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Contract Status and resubmit the records for processing.

---

## State Validation

### 50. Matching Staff Demographic Information record required
Each Staff Payroll record must have a matching Staff Demographic Information record based on District Number, Social Security Number, Survey Period Code, and Fiscal Year.
**Result:** State validation

**District Responsibility:** The district must verify that the Staff Payroll record is valid, then submit a Staff Demographic Information record based on District Number, Social Security Number, Survey Period Code and Fiscal Year.

### 51. Job Code, Primary must not equal Job Code, Additional
No Staff Payroll record may have a matching Staff Additional Job Assignment record where the employee's Job Code, Primary is the same as the employee's Job Code, Additional.
**Result:** State validation

**District Responsibility:** The district must verify that the Staff Payroll record is valid and correct the Job Code, Additional on the Staff Additional Job Assignment record so that it is not identical to the Job Code, Primary.

### 52. Additional Job Assignment record not permitted when all Payroll FTE is zero
If Job Code FTE equals zero on all Payroll records for an employee, then there must not be an Additional Job Assignment record for that employee.
**Result:** State validation

**District Responsibility:** The district must determine whether the Staff Additional Job Assignment record is valid and correct the Job Code, FTE on the appropriate record or change the Job Code, Primary and Job Code, Additional to accurately reflect the jobs the employee holds.

### 53. Matching Staff Demographic record required by Employee Type
For each employee, at least one Staff Payroll record must have a matching Staff Demographic Information record based on District Number, School Number, Primary/Home, Social Security Number, Fiscal Year, Survey Period Code and Employee Type.
**Result:** State validation

**District Responsibility:** The district must verify that the Staff Payroll record is valid, then submit a Staff Demographic Information record based on District Number, Social Security Number and Employee Type or change the Employee Type on one of the records so that a match exists.

### 54. Grandfathered indicator required for pre-2014 instructional employees
If the employee's Job Code places the employee on lines 09-19 or 21-43, inclusive, of the Public Schools Staff Survey - EEO-5, excluding Job Codes 73026 (Registrar), 51080, 52080, 53080, 54080, 55080 or 59080 (Substitute Teachers), and if Employee Type = RF or TF and Salary Schedule Pay Type is not 0 or 8, and the Employment Date, Original Position on the Staff Demographic Information record is prior to 07012014, then Grandfathered Salary Schedule Pay Type Indicator code must equal Y or N. The match should be based on District Number, Social Security Number, Fiscal Year and Survey Period Code.
**Result:** State validation

**District Responsibility:** The district must verify if the Staff Payroll record is valid or if the Staff Demographic record is valid, and then make the appropriate correction.

### 57. Salary Schedule Pay Type 1-7/A requires pre-2014 Employment Date
If Salary Schedule Pay Type equals 1-7 or A, then Employment Date, Original Position on the Staff Demographic Information record must be prior to 07012014. The match should be based on District Number, Social Security Number, Fiscal Year and Survey Period Code.
**Result:** State validation

**District Responsibility:** The district must verify if the Staff Payroll record is valid or if the Staff Demographic record is valid, and then make the appropriate correction.

### 58. Salary Schedule Pay Type B required for post-2014 instructional employees
If the employee's Job Code places the employee on lines 09-19 or 21-43, inclusive, of the Public Schools Staff Survey - EEO-5, and if Employee Type = RF or TF and Salary Schedule Pay Type is not 0 or 8, and the Employment Date, Original Position on the Staff Demographic Information record is on or after 07012014, then Salary Schedule Pay Type must equal B. The match should be based on District Number, Social Security Number, Fiscal Year and Survey Period Code.
**Result:** State validation

**District Responsibility:** The district must verify if the Staff Payroll record is valid or if the Staff Demographic record is valid, and then make the appropriate correction.

---

## Exception Reports

### 60. Matching Staff Experience record expected for instructional/administrative staff
If Survey Period is 2 or 3 and the employee's Job Code places the employee on lines 8-43, inclusive, of the Public Schools Staff Survey - EEO-5, excluding substitute teachers (Job Code, Primary code equal to 51080, 52080, 53080, 54080, 55080 or 59080) and Registrar (Job Code, Primary code equals 73026), then the Payroll record should have a matching Experience format based on District Number, Social Security Number, Survey Period Code, and Fiscal Year.
**Result:** Exception report

**District Responsibility:** The district should verify the Job Code, Primary and correct it if in error or submit a matching Staff Experience record.

### 62. Employment Length should exceed 4.0 for EEO-5 lines 21-43
If the employee's Job Code places the employee on lines 21-43, inclusive, of the Public Schools Staff Survey - EEO-5, excluding substitute teachers (Job Code, Primary code equal to 51080, 52080, 53080, 54080, 55080 or 59080), then the Employment Length must be greater than 04.0, unless Employee Type = TP or ST.
**Result:** Exception report

**District Responsibility:** The district should verify the Employment Length and if in error correct the record.

### 64. Job Code 64021-64023 should have Fund Source R or S
If Job Code, Primary is 64021, 64022 or 64023, then one of the Job Code Fund Source codes should be R or S.
**Result:** Exception report

**District Responsibility:** The district should review the data in the second record to verify the entries for Job Code, Primary and Job Code Fund Source. If there is an error in the data the district should submit an update to the record.

### 65. Salary, Annual should not be less than $4,000 for RF employees
If Employee Type is RF, then Salary, Annual must not be less than $4,000.
**Result:** Exception report

**District Responsibility:** The district should verify the information for Employee Type and Salary, Annual and if in error correct the records.

### 66. Sum of benefits should not exceed a percentage of Salary, Annual
If Employee Type is RF and if the employee's Job Code places the employee on lines 1-43, inclusive, of the Public Schools Staff Survey - EEO-5, then the sum of staff benefits (Selected Benefits, Frequency multiplied by Selected Benefits, Value) across all Staff Benefits records for the employee cannot exceed fifty percent of the Salary, Annual for the employee. If Employee Type is RF and if the employee's Job Code places the employee on lines 44-54, inclusive, of the Public Schools Staff Survey - EEO-5, then the sum of staff benefits (Selected Benefits, Frequency multiplied by Selected Benefits, Value) across all Staff Benefits records for the employee cannot exceed seventy-five percent of the Salary, Annual for the employee. The Staff Benefits and Staff Payroll records should be matched based on District Number, Social Security Number, Survey Period Code and Fiscal Year.
**Result:** Exception report

**District Responsibility:** The district must review the Staff Payroll record information and the benefits information on all Staff Benefits records for the employee and if in error correct the appropriate record.
