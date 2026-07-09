# Staff Email Address Data Collection — Edits and Reject Rules

Source: https://www.fldoe.org/file/20908/2627eadc.pdf
Manual: Staff Database 2026-2027

This document covers 12 Reject Rules only. There is no State Validation or Exception Reports section in this document.

---

## Reject Rules

### 1. District Number range and status *(Updated 07/01/2026)*
District Number must be numeric, active (A) on the Appendix B: District Name Table and must be correct for the district submitting the data.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number and resubmit the record for processing.

### 2. School Number, Primary/Home must be valid active school
School Number, Primary/Home must exist on the Master School Identification File as a valid active school in the district of submission.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the School Number, Primary/Home and resubmit the record for processing.

### 3. Job Code, Primary must be on Job Code Assignments table
Job Code, Primary must equal one of the codes on the Job Code Assignments table as listed in Appendix E of the FDOE Information Database Requirements: Volume II--Automated Staff Information System Manual.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Job Code, Primary by reporting a valid number from the Job Code Assignments table and resubmit the records for processing.

### 4. Employee Name, Legal: Last Name cannot be blank
For the Employee Name, Legal; the Last Name cannot be blank. Allowable characters include double or single quotation marks, commas, slashes, periods, hyphens and accent marks. (Z-fill is not allowed.)
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the records by providing valid Last Names and resubmit the records for processing.

### 5. Employee Name, Legal: Appendage validity
For the Employee Name, Legal; the Appendage may be blank but must not include nondisplayable characters. Allowable characters include double or single quotation marks, commas, slashes, periods, hyphens and accent marks.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the records by including a valid Appendage and resubmit the records for processing.

### 6. Employee Name, Legal: First Name cannot be blank
For the Employee Name, Legal; the First Name cannot be blank. Allowable characters include double or single quotation marks, commas, slashes, periods, hyphens and accent marks. (Z-fill is not allowed.)
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the records by including valid First Names and resubmit the records for processing.

### 7. Employee Name, Legal: Middle/Maiden Name or Initial validity
For the Employee Name, Legal; Middle/Maiden Name or Initial may be blank but may not include nondisplayable characters. Allowable characters include double or single quotation marks, commas, slashes, periods, hyphens and accent marks.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the records by including a valid Middle/Maiden Name or Initial and resubmit the records for processing.

### 8. Email Address format
The Email Address must contain an @ and have no embedded spaces.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Email Address and resubmit the record for processing.

### 9. Exempt from Public Records Law, Employee validity
Exempt from Public Records Law, Employee, must be Y or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Exempt from Public Records Law, Employee codes and resubmit the records for processing.

### 10. Social Security Number numeric and left-justified
Social Security Number (SSN) must be numeric and greater than zero, excluding the value 999999999, unless it is a Staff Number Identifier and the first two positions are "CS" and the last seven positions are numeric. Nine-character SSN's should be left-justified, with a trailing blank.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Social Security Numbers by making them numeric, greater than zero and left-justified. Resubmit the records for processing.

### 11. Record uniqueness
Each Staff Email Address Data Collection record must be unique based on District Number and Social Security Number (or Staff Number Identifier).
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Social Security Number and resubmit the records for processing.

### 12. Florida Education Identifier format
Florida Education Identifier (FLEID) is alphanumeric and must be entered as "FL" in the first 2 positions followed by twelve numeric digits. No blanks or spaces are allowable.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Florida Education Identifier and resubmit the records for processing.
