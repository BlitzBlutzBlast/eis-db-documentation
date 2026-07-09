# Staff Professional Development — Edits and Reject Rules

Source: https://www.fldoe.org/file/20908/2627pd.pdf
Manual: Staff Database 2026-2027

This document covers 20 edits across two categories: Reject Rules (record rejected) and State Validation (cross-format matching). Edit numbering is non-sequential; Reject Rules run 1-18, State Validation runs 30-31. No Exception Reports section exists in this document.

---

## Reject Rules

### 1. District Number range and status *(Updated 07/01/2026)*
District Number must be numeric, active (A) on the Appendix B: District Name Table and must be correct for the district submitting the data.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number and resubmit the record for processing.

### 2. School Number, Primary/Home must be valid active school
School Number, Primary/Home must exist on the Master School Identification File as a valid active in the district of submission.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the School Number, Primary/Home and resubmit the record for processing.

### 3. Social Security Number numeric and left-justified
Social Security Number (SSN) must be numeric and greater than zero, excluding the value 999999999, unless it is a Staff Number Identifier and the first two positions are "CS" and the last seven positions are numeric. Nine-character SSN's should be left-justified, with a trailing blank.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Social Security Numbers by making them numeric, greater than zero and left-justified. Resubmit the records for processing.

### 4. Survey Period Code must be 5
Survey Period Code must be 5 and must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Survey Period Code on the records being submitted and resubmit the records for processing.

### 5. Fiscal Year correct for submission
Fiscal Year must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Fiscal Year either on the JCL or the records being submitted and resubmit the records for processing.

### 6. Professional Development, Learning Method validity
Professional Development, Learning Method must be A, B, C, D, F, G, H, I or J.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Professional Development, Learning Method and resubmit the records for processing.

### 7. Professional Development, Evaluation Method, Staff validity
Professional Development, Evaluation Method, Staff must be A, B, C, D, E, F or G.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Professional Development, Evaluation Method, Staff and resubmit the records for processing.

### 8. Professional Development, Participation Hours numeric
Professional Development, Participation Hours must be numeric, greater than zero (000) and contain no blanks.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Professional Development, Participation Hours and resubmit the records for processing.

### 9. Florida Education Identifier format
Florida Education Identifier (FLEID) is alphanumeric and must be entered as "FL" in the first 2 positions followed by twelve numeric digits. No blanks or spaces are allowable.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Florida Education Identifier and resubmit the record for processing.

### 10. Transaction Code validity and existence match
The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified then the record must not already exist on the database; if C or D is specified, then the record must exist on the database.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Transaction Code and resubmit the record for processing with the correct Transaction Code.

### 11. Record uniqueness
Each Professional Development record must be unique based on District Number; Social Security Number (or Staff Number Identifier); Survey Period Code; Fiscal Year and Professional Development, Component Number.
**Result:** First record accepted, all other duplicate records rejected

**District Responsibility:** If, in fact, the last record above should not have been submitted, the district would not have to take any action. The record was rejected. However, if the record should have been submitted but with a different key, the record should be corrected and resubmitted. If the district wishes to update some item in this record, the record should be submitted with a Transaction Code of "C" rather than "A."

### 12. Professional Development, Component Number structure
Position one of the Professional Development, Component Number must be 1-9. Positions two, three and four must be 000, 002-017, 100-106, 200-211, 300-308, 400-424, 500-521, 600-602, 700-705 or 800-805. Positions five, six and seven must be 001-999.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Professional Development, Component Number and resubmit the records for processing.

### 13. Professional Development, Implementation Method validity
Professional Development, Implementation Method must be M, N, O, P, Q, R, S or T.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Professional Development, Implementation Method and resubmit the records for processing.

### 14. District Number, Where Professional Development Completed validity *(Updated 07/01/2026)*
District Number, Where Professional Development Completed must be numeric and active (A) on the Appendix B: District Name Table.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the District Number, Where Professional Development Completed and resubmit the records for processing.

### 15. Professional Development Credits, Primary Purpose validity
Professional Development Credits, Primary Purpose must be A, B, C, D, E, G or H.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Professional Development Credits, Primary Purpose and resubmit the records for processing.

### 16. Professional Development, Evaluation Method, Student validity
Professional Development, Evaluation Method, Student must be A, B, C, D, F, G or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Professional Development, Evaluation Method, Student and resubmit the records for processing.

### 17. Staff Number Identifier, Local format
The Staff Number Identifier, Local may be any combination of letters, numbers and blanks. All blanks are not allowable. It must be left-justified with trailing blanks.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Staff Number Identifier, Local and resubmit the records.

### 18. Staff Number Identifier, Local must not equal SSN
The Staff Number Identifier, Local must not be identical to the Social Security Number.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Staff Number Identifier, Local or the Social Security Number and resubmit the record.

---

## State Validation

### 30. Matching Staff Demographic Information record required
Each Professional Development record must have a matching Staff Demographic Information record based on District Number, Social Security Number, Survey Period Code and Fiscal Year.
**Result:** State validation

**District Responsibility:** The district must verify that the Staff Professional Development record is valid, then submit a matching Staff Demographic Information record based on District Number, Social Security Number, Survey Period Code and Fiscal Year.

### 31. Component Number 8521001 requires EEO-5 lines 21-43
If the Professional Development, Component Number is 8521001, then the employee's Job Code must place the employee on lines 21-43, inclusive, of the Public Schools Staff Survey - EEO-5 on the Staff Demographic Information record. The match should be based on District Number, Social Security Number, Fiscal Year and Survey Period Code.
**Result:** State validation

**District Responsibility:** The district must verify if the Staff Professional Development record is valid or if the Staff Demographic record is valid, and then make the appropriate correction.
