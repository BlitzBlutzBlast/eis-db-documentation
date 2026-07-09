# Staff Additional Compensation — Edits and Reject Rules

Source: https://www.fldoe.org/file/20908/2627ac.pdf
Manual: Staff Database 2026-2027

This document covers 13 edits across two categories: Reject Rules (record rejected) and State Validation (cross-format matching). Edit numbering is non-sequential; Reject Rules run 1-11, State Validation begins at 50. No Exception Reports section exists in this document.

---

## Reject Rules

### 1. District Number range and status *(Updated 07/01/2026)*
District Number must be numeric, active (A) on the Appendix B: District Name Table, and must be correct for the district submitting the data.
**Result:** Record rejected

**District Responsibility:** The first two records listed below would be loaded to the database assuming no other reject rule would cause their rejection. The third record would be rejected since the District Number is not in the appropriate range.

### 2. Social Security Number numeric and left-justified
Social Security Number (SSN) must be numeric and greater than zero, excluding the value 999999999, unless it is a Staff Number Identifier and the first two positions are "CS" and the last seven positions are numeric. Nine-character SSN's should be left-justified, with a trailing blank.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Social Security Numbers by making them numeric, greater than zero and left-justified. Resubmit the records for processing.

### 3. Survey Period Code correct for submission
Survey Period Code must be correct for the submission specified by the district and must be 2 or 3.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Survey Period Code either on the JCL or the records being submitted and resubmit the records for processing.

### 4. Fiscal Year correct for submission
Fiscal Year must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Fiscal Year either on the JCL or the records being submitted and resubmit the records for processing.

### 5. Additional Compensation Type valid code
Additional Compensation Type code must be A, B, E - K, N – W, Y, Z, or 1-4.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Additional Compensation Type and resubmit the record for processing.

### 6. Additional Compensation Value must be numeric
Additional Compensation Value must be numeric.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Additional Compensation Value to be greater than zero and resubmit the record for processing.

### 7. Transaction Code validity and existence match
The Transaction Code must be A, C, or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified then the record must not already exist on the database; if C or D is specified, then the record must exist on the database.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Transaction Code and resubmit the record for processing.

### 8. Record uniqueness
Each Staff Additional Compensation record must be unique based on District Number, Social Security Number (or Staff Number Identifier), Survey Period Code, Fiscal Year, and Additional Compensation Type code.
**Result:** First record accepted, all other duplicate records rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the record should have been submitted but with a different key, the record should be corrected and resubmitted. If the district wishes to update some item in this record, the record should be submitted with a Transaction Code of C rather than A.

### 9. Staff Number Identifier, Local format
The Staff Number Identifier, Local may be any combination of letters, numbers and blanks. All blanks are not allowable. It must be left-justified with trailing blanks.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Staff Number Identifier, Local and resubmit the records.

### 10. Staff Number Identifier, Local must not equal SSN
The Staff Number Identifier, Local must not be identical to the Social Security Number.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Staff Number Identifier, Local or the Social Security Number and resubmit the record.

### 11. Florida Education Identifier format
Florida Education Identifier (FLEID) is alphanumeric and must be entered as "FL" in the first 2 positions followed by twelve numeric digits. No blanks or spaces are allowable.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Florida Education Identifier and resubmit the record for processing.

---

## State Validation

### 50. Matching Staff Demographic Information record required
Each Staff Additional Compensation record must have a matching Staff Demographic Information record based on District Number, Social Security Number, Survey Period Code and Fiscal Year.
**Result:** State validation

**District Responsibility:** The district must verify that the Staff Additional Compensation record is valid, then submit a matching Staff Demographic Information record based on District Number, Social Security Number, Survey Period Code, and Fiscal Year.

### 51. Additional Compensation Type Y requires matching Salary Schedule Pay Type
If the Additional Compensation Type code is Y, then the Salary Schedule Pay Type on the Staff Payroll Information record must be 0, A, or B. The match should be done using District Number, Social Security Number, Survey Period Code and Fiscal Year.
**Result:** State validation

**District Responsibility:** The district must determine which record is in error, the Additional Compensation Type or the Staff Payroll Information, and then correct it so that the proper relationship exists between these two formats.
