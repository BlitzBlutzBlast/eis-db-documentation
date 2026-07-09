# Staff Experience — Edits and Reject Rules

Source: https://www.fldoe.org/file/20908/2627se.pdf
Manual: Staff Database 2026-2027

This document covers 15 edits across three categories: Reject Rules (record rejected), State Validation (cross-format matching), and Exception Reports (advisory, does not reject). Edit numbering is non-sequential; Reject Rules run 1-11, State Validation runs 20-23, Exception Reports begin at 50.

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

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Survey Period Code on the records coming in or in the JCL and resubmit the records for processing.

### 4. Fiscal Year correct for submission
Fiscal Year must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Fiscal Year either on the JCL or the records being submitted and resubmit the records for processing.

### 5. Experience Type code validity
Experience Type code must be A, C, D, F, M, N, P, or S.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Experience Type code to be a valid code and resubmit the record for processing.

### 6. Experience Length numeric range
Experience Length must be numeric and be greater than or equal to zero and less than or equal to 75.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Experience Length and resubmit the records for processing.

### 7. Transaction Code validity and existence match
The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified then the record must not already exist on the database; if C or D is specified, then the record must exist on the database.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Transaction Code and resubmit the record for processing.

### 8. Record uniqueness
Each Staff Experience record must be unique based on District Number, Social Security Number (or Staff Number Identifier), Survey Period Code, Fiscal Year, and Experience Type code.
**Result:** First record accepted, all other duplicate records rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the record should have been submitted but with a different key, the record should be corrected and resubmitted. If the district wishes to update some item in this record, the record should be submitted with a Transaction Code of "C" rather than "A."

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

### 20. Matching Staff Demographic Information record required
Each Staff Experience record must have a matching Staff Demographic Information record based on District Number, Social Security Number, Survey Period Code and Fiscal Year.
**Result:** State validation

**District Responsibility:** The district must verify that the Staff Experience record is valid, then submit a matching Staff Demographic Information record based on District Number, Social Security Number, Survey Period Code and Fiscal Year.

### 21. Experience Length for Type F must be at least Experience Length for Type D
The Experience Length for Experience Type code of F must be greater than or equal to the Experience Length for Experience Type code of D.
**Result:** State validation

**District Responsibility:** The district must verify the Experience Type and Experience Length for both records to determine which is valid, then resubmit the corrected record for processing.

### 22. Experience Length must not exceed age minus 16 *(Updated 04/24/2026)*
Experience Length must not be greater than the number computed when subtracting 16 from the calculated age (using Birth Date from the Staff Demographic Information record). Edit assumption: staff member began employment in these positions no earlier than age 16.
**Result:** State validation

**District Responsibility:** The district must verify the Experience Length on the Staff Experience record and the Birth Date on the Staff Demographic Information record to determine which is valid, then resubmit the corrected record for processing.

### 23. Sum of Experience Types F, S, P, N must not exceed age minus 16 *(Updated 04/24/2026)*
The sum of the values for Experience Types F, S, P and N must not be greater than the number computed when subtracting 16 from the calculated age (using Birth Date from the Staff Demographic Information record). Edit assumption: staff member began employment in these positions no earlier than age 16.
**Result:** State validation

**District Responsibility:** The district must verify the values of each Experience Type on the Staff Experience record and the Birth Date on the Staff Demographic Information record to determine which are valid, then resubmit the corrected record(s) for processing.

---

## Exception Reports

### 50. Experience Length must not exceed 65 *(Updated 04/24/2026)*
Experience Length must not be greater than 65.
**Result:** Exception report

**District Responsibility:** The district should verify the Experience Length and if in error correct the record.
