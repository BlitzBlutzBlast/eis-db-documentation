# Staff Multidistrict Employee — Edits and Reject Rules

Source: https://www.fldoe.org/file/20908/2627me.pdf
Manual: Staff Database 2026-2027

This document covers 13 edits across two categories: Reject Rules (record rejected) and State Validation (cross-format matching). Edit numbering is non-sequential; Reject Rules run 1-11, State Validation runs 20-21. No Exception Reports section exists in this document.

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

### 3. Survey Period Code must be 2
Survey Period Code must be 2 and must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Survey Period Code in the JCL and resubmit the records for processing.

### 4. Fiscal Year correct for submission
Fiscal Year must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Fiscal Year either on the JCL or the records being submitted and resubmit the records for processing.

### 5. Multidistrict Employee, Assignment Identifier validity
Multidistrict Employee, Assignment Identifier must be X or Y.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Multidistrict Employee, Assignment Identifier and resubmit the record for processing.

### 6. Multidistrict Employee, District Number validity *(Updated 07/01/2026)*
Multidistrict Employee, District Number must be numeric and active (A) on the Appendix B: District Name Table.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Multidistrict Employee, District Number and resubmit the record for processing.

### 7. Transaction Code validity and existence match
The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified then the record must not already exist on the database; if C or D is specified, then the record must exist on the database.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Transaction Code and resubmit the record for processing.

### 8. Record uniqueness
Each Staff Multidistrict Employee record must be unique based on District Number; Social Security Number (or Staff Number Identifier); Survey Period Code; Fiscal Year; and Multidistrict Employee, District Number.
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
Each Multidistrict Employee record must have a matching Staff Demographic Information record based on District Number, Social Security Number, Survey Period Code and Fiscal Year.
**Result:** State validation

**District Responsibility:** The district must determine whether the Staff Multidistrict Employee record is valid. If it is valid the district must submit a Staff Demographic Information record based on District Number, Social Security Number, Survey Period Code and Fiscal Year.

### 21. Assignment Identifier must be identical across all records for an employee
Multidistrict Employee, Assignment Identifier must be identical on all of an employee's Multidistrict Employee records.
**Result:** State validation

**District Responsibility:** Correct the Multidistrict Employee, Assignment Identifier so that they are all the same.
