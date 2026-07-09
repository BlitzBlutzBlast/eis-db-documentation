# Staff Additional Job Assignments — Edits and Reject Rules

Source: https://www.fldoe.org/file/20908/2627aja.pdf
Manual: Staff Database 2026-2027

This document covers 20 edits across three categories: Reject Rules (record rejected), State Validation (cross-format matching), and Exception Reports (advisory, does not reject). Edit numbering is non-sequential; Reject Rules run 1-15 then jump to 30-36, State Validation runs 50-52, Exception Reports begin at 80.

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

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Survey Period either on the JCL or the records being submitted and resubmit the records for processing.

### 4. Fiscal Year correct for submission
Fiscal Year must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Fiscal Year either on the JCL or the records being submitted and resubmit the records for processing.

### 5. School Number, Primary/Home must be valid active school
School Number, Primary/Home must exist on the Master School Identification File as a valid active school in the district of submission.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the School Number, Primary/Home and resubmit the record for processing.

### 6. Job Code, Additional must be on Job Code Assignments table
Job Code, Additional must equal one of the codes on the Job Code Assignments table as listed in Appendix E of the DOE Information Database Requirements: Volume II--Automated Staff Information System manual.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct Job Code, Additional by reporting a valid number from the Job Code Assignments table and resubmit the records for processing.

### 7. Job Code FTE numeric range
Job Code FTE must be numeric and less than or equal to 100. If Job Code FTE is not equal to zero, then it must be greater than 004.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Job Code FTE and resubmit the records for processing.

### 8. Job Code Fund Source valid codes
Each of the three Job Code Fund Source codes must be one of the following: B, C, E, G, H, M, N, O, P, Q, R, S, T, U or zero.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the invalid code to be a valid code. Where a Job Code Fund Source position is not needed, zeros should be placed in that position. Resubmit both records for processing.

### 9. Job Code Fund Source percentages numeric
Each of the three Job Code Fund Source percentages must be numeric and greater than or equal to zero.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Job Code Fund Source percentages by supplying the numeric percentage rather than "Z's," and by reporting all three Job Code Fund Source percentages (using zeros if appropriate). Resubmit the records for processing.

### 10. Transaction Code validity and existence match
The Transaction Code must be A, C, or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified then the record must not already exist on the database; if C or D is specified, then the record must exist on the database.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Transaction Code and resubmit the record for processing.

### 11. Paraprofessional Qualification valid code
Paraprofessional Qualification code must be A, B, C, E, or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Paraprofessional Qualification code and resubmit the records for processing.

### 12. Paraprofessional Qualification code for Job Codes 51111, 51112, 51113
Paraprofessional Qualification code must be A, B, C, or E for Job Codes 51111, 51112 and 51113.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the relationship between the Paraprofessional Qualification code and the Job Code and resubmit the record for processing.

### 13. Paraprofessional Qualification requires Job Code prefix 51-55/59
If the Paraprofessional Qualification code is A, B, C, or E then the Job Code must begin with 51, 52, 53, 54, 55 or 59.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the relationship between the Paraprofessional Qualification and the Job Code and resubmit the record for processing.

### 14. Paraprofessional Qualification must be Z for EEO-5 lines 21-33
Paraprofessional Qualification code must be Z for Job Codes that place the employee on lines 21-33 of the Public Schools Staff Survey (EEO-5).
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the relationship between the Paraprofessional Qualification code and the Job Code and resubmit the record for processing.

### 15. Florida Education Identifier format
Florida Education Identifier (FLEID) is alphanumeric and must be entered as "FL" in the first 2 positions followed by twelve numeric digits. No blanks or spaces are allowable.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Florida Education Identifier and resubmit the record for processing.

### 30. At least one Job Code Fund Source code must be nonzero
At least one of the three Job Code Fund Source codes must be nonzero.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the record so that a valid nonzero Job Code Fund Source code is reported in at least one of the three Job Code Fund Source code positions. Resubmit the record for processing.

### 31. Job Code Fund Source code may not repeat
Any one Job Code Fund Source code can appear only once on a Staff Additional Job Assignment record. For purposes of this edit, zero (used where there are fewer than three fund sources) is NOT treated as a Job Code Fund Source code.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must change the repeated Job Code Fund Source to another valid Job Code Fund Source or combine the percentages attributed to that Job Code Fund Source into the first four positions so that the Job Code Fund Source is not repeated within that record. Resubmit the record for processing.

### 32. Job Code Fund Source percentages must total 100
The three Job Code Fund Source percentages on a Staff Additional Job Assignment record must add up to 100 percent.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Job Code Fund Source percentages so that they add up to 100 percent for that record and resubmit the record for processing.

### 33. Record uniqueness
Each Staff Additional Job Assignment record must be unique based on District Number, Social Security Number (or Staff Number Identifier), Survey Period Code, Fiscal Year, and Job Code, Additional.
**Result:** First record accepted, all other duplicate records rejected

**District Responsibility:** If, in fact, the duplicate record should not have been submitted, the district would not have to take any action. The record was rejected. However, if the record should have been submitted but with a different key, the record should be corrected and resubmitted. If the district wishes to update some item in this record, the record should be submitted with a Transaction Code of C rather than A.

### 34. Job Code FTE greater than zero except substitute teachers
Job Code FTE may be equal to or greater than zero for substitute teachers (Job Code, Additional codes equal to 51080, 52080, 53080, 54080, 55080 or 59080), but must be greater than zero for all other employees.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Job Code FTE and resubmit the record for processing.

### 35. Staff Number Identifier, Local format
The Staff Number Identifier, Local may be any combination of letters, numbers and blanks. All blanks are not allowable. It must be left-justified with trailing blanks.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Staff Number Identifier, Local and resubmit the records.

### 36. Staff Number Identifier, Local must not equal SSN
The Staff Number Identifier, Local must not be identical to the Social Security Number.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Staff Number Identifier, Local or the Social Security Number and resubmit the record.

---

## State Validation

### 50. Matching Staff Demographic Information record required
Each Staff Additional Job Assignment record must have a matching Staff Demographic Information record based on District Number, Social Security Number, Survey Period Code, and Fiscal Year.
**Result:** State validation

**District Responsibility:** The district must verify that the Staff Additional Job Assignment record is valid, then submit a matching Staff Demographic Information record based on District Number, Social Security Number, Survey Period Code, and Fiscal Year.

### 51. Matching Staff Payroll record required
Each Staff Additional Job Assignment record must have at least one matching Staff Payroll record based on District Number, Social Security Number, Survey Period Code, and Fiscal Year.
**Result:** State validation

**District Responsibility:** The district must verify that the Staff Additional Job Assignment record is valid, then submit a matching Staff Payroll record based on the key items of District Number, Social Security Number, Survey Period Code, and Fiscal Year.

### 52. Job Code, Additional must not equal Job Code, Primary
No Staff Additional Job Assignment record may have a matching Staff Payroll record where the employee's Job Code, Additional is the same as the employee's Job Code, Primary.
**Result:** State validation

**District Responsibility:** The district must verify that the Staff Additional Job Assignment record is valid and correct the Job Code, Additional so that it is not identical to the Job Code, Primary.

---

## Exception Reports

### 80. Job Code, Additional 64021-64023 should have Fund Source R or S
If the Job Code, Additional is 64021, 64022 or 64023, then one of the Job Code Fund Source codes should be R or S.
**Result:** Exception report

**District Responsibility:** The district should review the data to verify the entries for Job Code, Additional and Job Code Fund Source. If there is an error in the data the district should submit an update to the record.
