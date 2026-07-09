# Staff Fiscal Year Benefits — Edits and Reject Rules

Source: https://www.fldoe.org/file/20908/2627fyb.pdf
Manual: Staff Database 2026-2027

This document covers 17 edits across three categories: Reject Rules (record rejected), State Validation (cross-format matching), and Exception Reports (advisory, does not reject). Edit numbering is non-sequential; Reject Rules run 1-14, State Validation is 22, Exception Reports run 40-41.

---

## Reject Rules

### 1. District Number range and status *(Updated 07/01/2026)*
District Number must be numeric, active (A) on the Appendix B: District Name Table and must be correct for the district submitting the data.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number and resubmit the record for processing.

### 2. Social Security Number numeric and left-justified
Social Security Number (SSN) must be numeric and greater than zero, excluding the value 999999999, unless it is a Staff Number Identifier and the first two positions are "CS" and the last seven positions are numeric. Nine-character SSN's should be left-justified, with a trailing blank.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Social Security Numbers by making them numeric, greater than zero, and left-justified. Resubmit the records for processing.

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
Job Code must equal one of the codes on the Job Code Assignments table as listed in Appendix E of the DOE Information Database Requirements: Volume II-Automated Staff Information System Manual.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct Job Code by reporting a valid number from the Job Code Assignments table and resubmit the records for processing.

### 7. Selected Benefits, Type validity and uniqueness
The first occurrence of Selected Benefits, Type must be A, B, C, D, E, F, G, K, L, M, or N; any subsequent occurrences may be Z. However, each Selected Benefits, Type must otherwise be unique.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Selected Benefits, Type and resubmit the records for processing.

### 8. Selected Benefits, Value numeric range
The first occurrence of Selected Benefits, Value must be numeric and greater than zero, any subsequent occurrences must be numeric and greater than or equal to zero.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Selected Benefits, Value and resubmit the records for processing.

### 9. Transaction Code validity and existence match
The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified then the record must not already exist on the database; if C or D is specified, then the record must exist on the database.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Transaction Code and resubmit the records for processing.

### 10. Record uniqueness
Each Staff Fiscal Year Benefits record must be unique based on District Number; Social Security Number (or Staff Number Identifier); Survey Period Code; Fiscal Year; and Job Code.
**Result:** First record accepted, all other duplicate records rejected

**District Responsibility:** If the records that were accepted and loaded to the database are the correct ones, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must delete any invalid records, correct any rejected records if necessary, and resubmit the corrected record for processing.

### 11. Selected Benefits, Value must be greater than zero for non-Z types
For each Selected Benefits, Type code that is not Z, the Selected Benefits, Value must be greater than zero.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Selected Benefits, Value and resubmit the record for processing.

### 12. Staff Number Identifier, Local format
The Staff Number Identifier, Local may be any combination of letters, numbers and blanks. All blanks are not allowable. It must be left-justified with trailing blanks.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Staff Number Identifier, Local and resubmit the records.

### 13. Staff Number Identifier, Local must not equal SSN
The Staff Number Identifier, Local must not be identical to the Social Security Number.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Staff Number Identifier, Local or the Social Security Number and resubmit the record.

### 14. Florida Education Identifier format
Florida Education Identifier (FLEID) is alphanumeric and must be entered as "FL" in the first 2 positions followed by twelve numeric digits. No blanks or spaces are allowable.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Florida Education Identifier and resubmit the record for processing.

---

## State Validation

### 22. Matching Staff Demographic Information record required
Each Fiscal Year Benefits record must have a matching Staff Demographic Information record based on District Number, Social Security Number, Survey Period Code, and Fiscal Year.
**Result:** State validation

**District Responsibility:** The district must verify that the Staff Fiscal Year Benefits record is valid, then submit a matching Staff Demographic Information record based on District Number, Social Security Number, Survey Period Code, and Fiscal Year.

---

## Exception Reports

### 40. Matching Fiscal Year Salaries record required unless separated
Each Fiscal Year Benefits record must have a matching Fiscal Year Salaries record based on District Number, Social Security Number, Survey Period Code, and Fiscal Year unless the Separation Date on the Staff Demographic Information record is prior to the reported Fiscal Year and not equal to zero.
**Result:** Exception report

**District Responsibility:** The district must verify that the Staff Fiscal Year Benefits record is valid and that the employee had no salary for this fiscal year. If the employee did earn salary during the fiscal year, the district must submit a matching Fiscal Year Salaries record based on District Number, Social Security Number, Survey Period Code, and Fiscal Year.

### 41. Sum of benefits should not exceed a percentage of salary
If Employee Type is RF and if the employee's Job Code places the employee on lines 1-43, inclusive, of the Public Schools Staff Survey - EEO-5, then the sum of staff benefits (Selected Benefits, Type/Value) cannot exceed fifty percent of the employee's Fiscal Year Salary. If Employee Type is RF and if the employee's Job Code places the employee on lines 44-54, inclusive, of the Public Schools Staff Survey - EEO-5, then the sum of staff benefits (Selected Benefits, Type/Value) cannot exceed seventy-five percent of the employee's Fiscal Year Salary. The Fiscal Year Benefits, Fiscal Year Salaries and Staff Demographic Information records should be matched based on District Number, Social Security Number, Survey Period Code and Fiscal Year.
**Result:** Exception report

**District Responsibility:** The district must review the information on the Staff Fiscal Year Salaries record and the Staff Fiscal Year Benefits record to determine whether an error exists in the data or this represents an exception to the general relationship described in the edit. If the data are incorrect the district must update the record to reflect the correct relationship in the edit.
