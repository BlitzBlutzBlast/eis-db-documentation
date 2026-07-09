# Staff Benefits — Edits and Reject Rules

Source: https://www.fldoe.org/file/20908/2627sb.pdf
Manual: Staff Database 2026-2027

This document covers 12 edits across two categories: Reject Rules (record rejected) and State Validation (cross-format matching). Edit numbering is non-sequential; Reject Rules run 1-11 then jump to 13 (12 does not exist in source), State Validation begins at 20. No Exception Reports section exists in this document.

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

### 3. Survey Period Code correct for submission
Survey Period Code must be correct for the submission specified by the district and must be 2 or 3.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Survey Period Code either on the JCL or the records being submitted and resubmit the records for processing.

### 4. Fiscal Year correct for submission
Fiscal Year must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Fiscal Year either on the JCL or the records being submitted and resubmit the records for processing.

### 5. Selected Benefits, Type valid code
Selected Benefits, Type must be A, B, C, D, E, F, G, K, L, M, or N.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Selected Benefits, Type and resubmit the records for processing.

### 6. Selected Benefits, Frequency numeric range
Selected Benefits, Frequency code must be numeric, greater than zero, and less than or equal to 5200.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Selected Benefits, Frequency codes and resubmit the records for processing.

### 7. Selected Benefits, Value numeric and greater than zero
Selected Benefits, Value must be numeric and greater than zero.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Selected Benefits, Value and resubmit the records for processing.

### 8. Transaction Code validity and existence match
The Transaction Code must be A, C, or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified then the record must not already exist on the database; if C or D is specified, then the record must exist on the database.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Transaction Code and resubmit the record for processing.

### 9. Record uniqueness
Each Staff Benefits record must be unique based on District Number; Social Security Number (or Staff Number Identifier); Survey Period Code; Fiscal Year; and Selected Benefits, Type code.
**Result:** Record rejected

**District Responsibility:** If, in fact, the duplicate record should not have been submitted, the district would not have to take any action. The record was rejected. However, if the record should have been submitted but with a different key, the record should be corrected and resubmitted. If the district wishes to update some item in this record, the record should be submitted for processing with a Transaction Code of "C" rather than "A."

### 10. Staff Number Identifier, Local format
The Staff Number Identifier, Local may be any combination of letters, numbers and blanks. All blanks are not allowable. It must be left-justified with trailing blanks.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Staff Number Identifier, Local and resubmit the records.

### 11. Staff Number Identifier, Local must not equal SSN
The Staff Number Identifier, Local must not be identical to the Social Security Number.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Staff Number Identifier, Local or the Social Security Number and resubmit the record.

### 13. Florida Education Identifier format
Florida Education Identifier (FLEID) is alphanumeric and must be entered as "FL" in the first 2 positions followed by twelve numeric digits. No blanks or spaces are allowable.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Florida Education Identifier and resubmit the record for processing.

---

## State Validation

### 20. Matching Staff Demographic Information record required
Each Staff Benefits record must have a matching Staff Demographic Information record based on District Number, Social Security Number, Survey Period Code, and Fiscal Year.
**Result:** State validation

**District Responsibility:** The district must verify that the Staff Benefits record is valid, then submit a Staff Demographic Information record based on District Number, Social Security Number, Survey Period Code, and Fiscal Year.
