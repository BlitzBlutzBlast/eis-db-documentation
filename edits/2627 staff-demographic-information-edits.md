# Staff Demographic Information — Edits and Reject Rules

Source: https://www.fldoe.org/file/20908/2627di.pdf
Manual: Staff Database 2026-2027

This document covers 68 edits across four categories: Reject Rules (record rejected), State Validation (cross-format matching), Aggregate Validation (school-level counts), and Exception Reports (advisory, does not reject). Edit numbering is non-sequential; Reject Rules run 1-29 interleaved with alphanumeric IDs (1A-1W, 1#, 1$, 2A-2Z, 3A-3E) and include a gap at 11, State Validation runs 30-38, Aggregate Validation is 40, and Exception Reports run 50-59.

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
Survey Period Code must be correct for the submission specified by the district and must be 2, 3, or 5.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Survey Period Code on the records coming in or in the JCL and resubmit the records for processing.

### 4. Fiscal Year correct for submission
Fiscal Year must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Fiscal Year either on the JCL or the records being submitted and resubmit the records for processing.

### 5. School Number, Primary/Home must be valid active school
School Number, Primary/Home must exist on the Master School Identification File as a valid active school in the district of submission.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the School Number, Primary/Home and resubmit the record for processing.

### 6. Florida Educators Certificate Number range *(Updated 03/13/2026)*
Florida Educators Certificate Number must be numeric, and in the range 0000000001 - 0000999998, 0001000000 - 6001999999, 6002000001 - 6002999999, 6003000001 - 6003999999, 6004000001 - 6004999999, 6007000001 - 6007999999, or 0000000000, 0000999999, 7777777777, 8888888888 or 9999999999.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Florida Educators Certificate Numbers to be valid numbers and resubmit the records for processing.

### 7. Employee Name, Legal: Last Name cannot be blank
For the Employee Name, Legal; the Last Name cannot be blank. Allowable characters include double or single quotation marks, commas, slashes, periods, hyphens and accent marks. (Z-fill is not allowed.)
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the records by providing valid Last Names and resubmit the records for processing.

### 8. Employee Name, Legal: Appendage validity
For the Employee Name, Legal; the Appendage may be blank but must not include nondisplayable characters. Allowable characters include double or single quotation marks, commas, slashes, periods, hyphens and accent marks.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the records by including a valid Appendage and resubmit the records for processing.

### 9. Birth Date must be a valid date
Birth Date must be numeric and a valid date.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Birth Dates to be valid dates and resubmit the records for processing.

### 10. Sex code validity
Sex code must be M or F.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the records by including valid Sex codes and resubmit the records for processing.

### 12. Employment Date, Current Position validity
Employment Date, Current Position must be numeric and a valid date which is prior to the current date unless Separation Date is prior to the Fiscal Year being reported, in which case, Employment Date, Current Position may be all zeros.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Employment Date, Current Position and resubmit the record for processing.

### 13. Employment Date, Continuous Employment validity
Employment Date, Continuous Employment must be numeric and a valid date which is prior to the current date unless Separation Date is prior to the Fiscal Year being reported, in which case, Employment Date, Continuous Employment may be all zeros.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct Employment Date, Continuous Employment and resubmit the record for processing.

### 14. Employment Date, Original Position validity
Employment Date, Original Position must be numeric and a valid date which is prior to the current date.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct Employment Date, Original Position and resubmit the records for processing.

### 15. Separation Date validity
Separation Date must be numeric and a valid date which is prior to the current date, or it must be all zeros.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Separation Date and resubmit the records for processing.

### 16. Separation Reason code validity
Separation Reason code must be A-P or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Separation Reason and resubmit the record for processing.

### 17. Job Code, Primary must be on Job Code Assignments table
Job Code, Primary must equal one of the codes on the Job Code Assignments table as listed in Appendix E of the DOE Information Database Requirements: Volume II--Automated Staff Information System Manual.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Job Code, Primary by reporting a valid number from the Job Code Assignments table and resubmit the records for processing.

### 18. Transaction Code validity and existence match
The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified then the record must not already exist on the database; if C or D is specified, then the record must exist on the database. An original transaction is the first submission of a record during a survey period. After original transmission of records, changes to the record for elements other than the key elements must be done with a "C" as the Transaction Code. To delete a record, the Transaction Code must be a "D". To change key elements in a batch transaction, the record must FIRST be deleted with a "D" and then added with an "A".
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Transaction Code and resubmit the record for processing.

### 19. Exempt from Public Records Law, Employee validity
Exempt from Public Records Law, Employee, must be Y or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Exempt from Public Records Law, Employee codes and resubmit the records for processing.

### 1A. School Number must be 9001 for Job Code 71001 at non-charter schools
If Job Code, Primary = 71001 and Charter School Status is not C or R (located on the Master School Identification File), then School Number, Primary/Home must be 9001.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the School Number, Primary/Home or the Job Code, Primary and resubmit the record for processing.

### 1B. Ethnicity code validity
Ethnicity code must be Y or N.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Ethnicity code and resubmit the record for processing.

### 1C. Race data elements validity
Race: American Indian or Alaska Native; Race: Asian; Race: Black or African American; Race: Native Hawaiian or Other Pacific Islander, and Race: White must be Y or N.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the invalid Race code and resubmit the record for processing.

### 1D. At least one Race element must be Y
There must be a Y code for at least one of the Race data elements (Race: American Indian or Alaska Native, Race: Asian, Race: Black or African American, Race: Native Hawaiian or Other Pacific Islander and Race: White).
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must enter a Y code for one of the Race data elements and resubmit the record for processing.

### 1M. Mentor/Supervising Educator code validity
Mentor/Supervising Educator code must be Y, N or Z. If Survey Period Code is 5, Mentor/Supervising Educator code must be Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Mentor/Supervising Educator code and resubmit the record for processing.

### 1N. Florida Education Identifier format
Florida Education Identifier (FLEID) is alphanumeric and must be entered as "FL" in the first 2 positions followed by twelve numeric digits. No blanks or spaces are allowable.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Florida Education Identifier and resubmit the record for processing.

### 1O. Personnel Evaluation code validity by Survey Period and Job Code
Personnel Evaluation code must be C-I or Z. If Survey Period Code = 2, then Personnel Evaluation code must be Z. If Survey Period Code = 5, and if the employee's Job Code places the employee on lines 09-19 or 21-43, inclusive, of the Public Schools Staff Survey - EEO-5, and if the Job Code is not 73026 (Registrar); or 52015 or 55052 (PK Teachers); or 51080, 52080, 53080, 54080, 55080 or 59080 (Substitute Teachers) then the Personnel Evaluation code must be C-I.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Personnel Evaluation code or the Job Code and resubmit the record for processing.

### 1P. Personnel Evaluation must be Z for specified Job Codes
If the employee's Job Code, Primary is 51080, 52015, 52080, 53080, 54080, 55052, 55080, 59080, or 73026, then the Personnel Evaluation code must be Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Personnel Evaluation code or Job Code and resubmit the records for processing.

### 1Q. Personnel Evaluation, Instructional Leadership Component range
If Survey Period Code = 5 and if the employee's Job Code places the employee on lines 09-19, inclusive, of the Public Schools Staff Survey - EEO-5, and if the Job Code, Primary is not 73026 (Registrar), and if the District Number is not 68, then the Personnel Evaluation, Instructional Leadership Component must be numeric, greater than or equal to 33 and less than or equal to 67, unless Personnel Evaluation code = H or I, then must be zero. For all other employees, the Personnel Evaluation, Instructional Leadership Component must be zero. If Survey Period Code = 2 or 3, then the Personnel Evaluation, Instructional Leadership Component must be zero.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Job Code or the Personnel Evaluation, Instructional Leadership Component value and resubmit the record for processing.

### 1R. Personnel Evaluation, Instructional Practice Component range
If Survey Period Code = 5 and if the employee's Job Code places the employee on lines 21-43, inclusive, of the Public Schools Staff Survey - EEO-5, and if the Job Code is not 52015 or 55052 (PK Teachers), or 51080, 52080, 53080, 54080, 55080 or 59080 (Substitute Teachers), and if the District Number is not 68, then the Personnel Evaluation, Instructional Practice Component must be numeric, greater than or equal to 33 and less than or equal to 67, unless Personnel Evaluation code = H or I, then must be zero. For all other employees the Personnel Evaluation, Instructional Practice Component must be zero. If Survey Period Code = 2 or 3, then the Personnel Evaluation, Instructional Practice Component must be zero.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Job Code or the Personnel Evaluation, Instructional Practice Component value and resubmit the record for processing.

### 1S. Personnel Evaluation, Professional and Job Responsibilities Component range
If Survey Period Code = 5 and if the employee's Job Code places the employee on lines 09-19 or 21-43, inclusive, of the Public Schools Staff Survey - EEO-5, and if the Job Code, Primary is not 73026 (Registrar), or 52015 or 55052 (PK Teachers), or 51080, 52080, 53080, 54080, 55080 or 59080 (Substitute Teachers), and if the District Number is not 68, then the Personnel Evaluation, Professional and Job Responsibilities Component must be numeric, greater than or equal to zero and less than or equal to 33. For all other employees the Personnel Evaluation, Professional and Job Responsibilities Component must be zero. If Survey Period Code = 2 or 3, then the Personnel Evaluation, Professional and Job Responsibilities Component must be zero.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Job Code or the Personnel Evaluation, Professional or Job Responsibilities Component value and resubmit the record for processing.

### 1T. Personnel Evaluation, Student Performance Component range
If Survey Period Code = 5 and if the employee's Job Code places the employee on lines 09-19 or 21-43, inclusive, of the Public Schools Staff Survey - EEO-5, and if the Job Code is not 73026 (Registrar), or 52015 or 55052 (PK Teachers), or 51080, 52080, 53080, 54080, 55080 or 59080 (Substitute Teachers), and if the District Number is not 68, then the Personnel Evaluation, Student Performance Component must be numeric, greater than or equal to 33 and less than or equal to 67, unless Personnel Evaluation code = H or I, then must be zero. For all other employees the Personnel Evaluation, Student Performance Component must be zero. If Survey Period Code = 2 or 3, then the Personnel Evaluation, Student Performance Component must be zero.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Job Code or the Personnel Evaluation, Student Performance Component value and resubmit the record for processing.

### 1U. Personnel Evaluation, Measures of Student Performance code validity
If Survey Period Code = 5 and if the employee's Job Code places the employee on lines 09-19 or 21-33, inclusive, of the Public Schools Staff Survey - EEO-5, and if the Job Code, Primary is not 73026 (Registrar), or 52015 or 55052 (PK Teachers), or 51080, 52080, 53080, 54080, 55080 or 59080 (Substitute Teachers), and if the District Number is not 68, then Personnel Evaluation, Measures of Student Performance code must be B-G or I-K, unless Personnel Evaluation, Student Performance Component = zero, then Personnel Evaluation, Measures of Student Performance code must be H. For all other employees the Personnel Evaluation, Measures of Student Performance code must be Z. If Survey Period Code = 2 or 3, then the Personnel Evaluation, Measures of Student Performance must be Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Personnel Evaluation, Measures of Student Performance code and resubmit the record for processing.

### 1V. Personnel Evaluation components must total 100 for lines 09-19
If Survey Period Code = 5 and if the employee's Job Code places the employee on lines 09-19, inclusive, of the Public Schools Staff Survey - EEO-5, and if the Job Code is not 73026 (Registrar), and if the District Number is not 68, and if the value reported for this employee for the Personnel Evaluation, Instructional Leadership Component is greater than or equal to 33, then the total of Personnel Evaluation, Instructional Leadership Component; Personnel Evaluation, Professional and Job Responsibilities Component and Personnel Evaluation, Student Performance Component must be 100.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the value for Personnel Evaluation, Instructional Leadership Component; Personnel Evaluation, Professional and Job Responsibilities Component or the Personnel Evaluation, Student Performance Component so that they add up to 100 and resubmit the record for processing.

### 1W. Personnel Evaluation components must total 100 for lines 21-43
If Survey Period Code = 5 and if the employee's Job Code places the employee on lines 21-43, inclusive, of the Public Schools Staff Survey - EEO-5, and if the Job Code is not 52015 or 55052 (PK Teachers) or 51080, 52080, 53080, 54080, 55080 or 59080 (Substitute Teachers), and if the District Number is not 68, and if the value reported for this employee for the Personnel Evaluation, Instructional Practice Component is greater than or equal to 33, then the sum of Personnel Evaluation, Instructional Practice Component; Personnel Evaluation, Professional and Job Responsibilities Component and Personnel Evaluation, Student Performance Component must be 100.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the value for Personnel Evaluation, Instructional Practice Component; Personnel Evaluation, Professional and Job Responsibilities Component or Personnel Evaluation, Student Performance Component so that they add up to 100 and resubmit the record for processing.

### 1#. Personnel Evaluation components required when code is C-G
If Survey Period Code = 5, and the employee's Job Code places the employee on lines 09-19 or 21-43, inclusive, of the Public Schools Staff Survey - EEO-5, and if the Job Code is not 73026 (Registrar), or 52015 or 55052 (PK Teachers), or 51080, 52080, 53080, 54080, 55080 or 59080 (Substitute Teachers), and if the District Number is not 68, and Personnel Evaluation code is C-G then the Personnel Evaluation, Instructional Leadership Component or the Personnel Evaluation, Instructional Practice Component must be greater than or equal to 33 or less than or equal to 67.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Personnel Evaluation, Instructional Practice Component code and resubmit the record for processing.

### 1$. Personnel Evaluation code required for newly assigned instructional employees
If Survey Period Code is 3 and if the employee's Job Code places the employee on lines 21-33, inclusive, of the Public Schools Staff Survey - EEO-5, and if the Job Code is not 52015 or 55052 (PK Teachers), or 51080, 52080, 53080, 54080, 55080 or 59080 (Substitute Teachers), and if Employee Type is RF, RP, CF, CP or TF, and if Employment Date, Current Position is on or after July 1 of the current fiscal year, then the Personnel Evaluation code must be C-I.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Personnel Evaluation code and resubmit the record for processing.

### 20. Separation Date must be zeros for Survey Period 2 or 3
If Survey Period Code is 2 or 3, then Separation Date must be zeros.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the record to show all zeros in the Separation Date field. Resubmit the record for processing.

### 21. Separation Reason must be Z for Survey Period 2 or 3
If Survey Period Code is 2 or 3, then Separation Reason code must be Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must change the Separation Reason code to Z and resubmit the record for processing.

### 23. Record uniqueness
Each Staff Demographic Information record must be unique based on District Number, Social Security Number (or Staff Number Identifier), Survey Period Code, and Fiscal Year.
**Result:** First record accepted, all other duplicate records rejected

**District Responsibility:** If, in fact, the last record should not have been submitted, the district would take no action. The record was rejected. However, if the record should have been submitted but with a different key, the record should be corrected and resubmitted. If the district wishes to update some item in this record, the record should be submitted with a Transaction Code of "C" rather than "A".

### 24. Employee Type code validity
Employee Type code must be RF, RP, TF, TP, CF, CP or ST.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Employee Type codes and resubmit the records for processing.

### 25. Employee Name, Legal: First Name cannot be blank
For the Employee Name, Legal; the First Name cannot be blank. Allowable characters include double or single quotation marks, commas, slashes, periods, hyphens and accent marks. (Z-fill is not allowed.)
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the records by including valid First Names and resubmit the records for processing.

### 26. Employee Name, Legal: Middle/Maiden Name or Initial validity
For the Employee Name, Legal; Middle/Maiden Name or Initial may be blank but may not include nondisplayable characters. Allowable characters include double or single quotation marks, commas, slashes, periods, hyphens and accent marks.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the records by including a valid Middle/Maiden Name or Initial and resubmit the records for processing.

### 27. Degree/Credential Earned code validity
The Degree/Credential Earned code must be C, A, B, M, S, D, or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct Degree/Credential Earned by reporting a valid code and resubmit the records for processing.

### 28. Days Absent, Personal Leave range
If Survey Period Code is 2 or 3, then Days Absent, Personal Leave must be 000. If Survey Period Code is 5, then Days Absent, Personal Leave must be numeric and less than or equal to 180 for Employee Types RF, CF or TF for employees whose job codes place them on lines 9-19 (school administrators) or 21-33 (teachers) of the Public Schools Staff Survey (EEO-5); or it must be 999, unless District Number is 71. All others must be 000.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Days Absent, Personal Leave so that it is in the range 000 to 180 and resubmit the record for processing.

### 29. Days Absent, Sick Leave range
If Survey Period Code is 2 or 3, then Days Absent, Sick Leave must be 000. If Survey Period Code is 5, then Days Absent, Sick Leave must be numeric and less than or equal to 180 for Employee Types RF, CF or TF for employees whose job codes place them on lines 9-19 (school administrators) or 21-33 (teachers) of the Public Schools Staff Survey (EEO-5); or it must be 999, unless District Number is 71. All others must be 000.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Days Absent, Sick Leave so that it is in the range 000 to 180 and resubmit the record for processing.

### 2A. Days Absent, Temporary Duty Elsewhere range
If Survey Period Code is 2 or 3, then Days Absent, Temporary Duty Elsewhere must be 000. If Survey Period Code is 5, then Days Absent, Temporary Duty Elsewhere must be numeric and less than or equal to 180 for Employee Types RF, CF or TF for employees whose job codes place them on lines 9-19 (school administrators) or 21-33 (teachers) of the Public Schools Staff Survey (EEO-5); or it must be 999, unless District Number is 71. All others must be 000.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Days Absent, Temporary Duty Elsewhere so that it is in the range 000 to 180 and resubmit the record for processing.

### 2B. Days Absent, Other range
If Survey Period Code is 2 or 3, then Days Absent, Other must be 000. If Survey Period Code is 5, then Days Absent, Other must be numeric and less than or equal to 180 for Employee Types RF, CF or TF for employees whose job codes place them on lines 9-19 (school administrators) or 21-33 (teachers) of the Public Schools Staff Survey (EEO-5); or it must be 999, unless District Number is 71. All others must be 000.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Days Absent, Other so that it is in the range 000 to 180 and resubmit the record for processing.

### 2C. Days Present range
If Survey Period Code is 2 or 3, then Days Present must be 000. If Survey Period Code is 5, then Days Present must be numeric and greater than zero or less than or equal to 180 for Employee Types RF, CF or TF for employees whose job codes place them on lines 9-19 (school administrators) or 21-33 (teachers) of the Public Schools Staff Survey (EEO-5); or it must be 999, unless District Number is 71. All others may be 000.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Days Present so that it is greater than zero or less than or equal to 180 and resubmit the record for processing.

### 2D. Sum of Days Present and Days Absent range
If Survey Period Code is 2 or 3, then the sum of the number of Days Present; Days Absent, Personal Leave; Days Absent, Sick Leave; Days Absent, Temporary Duty Elsewhere; and Days Absent, Other must be 000. If Survey Period Code is 5, then the sum of the number of Days Present; Days Absent, Personal Leave; Days Absent, Sick Leave; Days Absent, Temporary Duty Elsewhere; and Days Absent, Other must be greater than zero or less than or equal to 180 for Employee Types RF, CF or TF for employees whose job codes place them on lines 9-19 (school administrators) or 21-33 (teachers) of the Public Schools Staff Survey (EEO-5); or all of these must be 999, unless District Number is 71. All others may be 000.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the record so that the sum of the number of days present plus days absent is greater than zero or less than or equal to 180 and resubmit the record for processing.

### 2E. Separation Reason must not be Z when Separation Date falls in Fiscal Year
If Separation Date falls within the Fiscal Year being reported, then Separation Reason code must not be Z.
**Result:** Record rejected

**District Responsibility:** The district should correct the Separation Reason code by changing it to a valid non-Z code or change the Separation Date to zeros if the employee has not separated from the school district or a valid date prior to the Fiscal Year being reported and resubmit the record for processing.

### 2F. Separation Date must be greater than zero when Separation Reason is not Z
If Separation Reason code is not Z, then Separation Date must be greater than zero.
**Result:** Record rejected

**District Responsibility:** The district should correct the Separation Date to be a valid date greater than zero or change the Separation Reason to Z if the employee has not separated from the school district and resubmit the record for processing.

### 2H. Paraprofessional Qualification code validity
Paraprofessional Qualification code must be A, B, C, E, or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Paraprofessional Qualification code and resubmit the records for processing.

### 2I. Paraprofessional Qualification code for Job Codes 51111-51113
Paraprofessional Qualification code must be A, B, C, or E for Job Codes 51111, 51112 and 51113.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the relationship between the Paraprofessional Qualification code and the Job Code and resubmit the record for processing.

### 2J. Paraprofessional Qualification requires Job Code prefix 51-55/59
If Survey Period is 2, 3 or 5 and the Paraprofessional Qualification code is A, B, C, or E then the Job Code must begin with 51, 52, 53, 54, 55 or 59.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the relationship between the Paraprofessional Qualification code and the Job Code and resubmit the record for processing.

### 2K. Paraprofessional Qualification must be Z for EEO-5 lines 21-33
If Survey Period is 2, 3 or 5, then the Paraprofessional Qualification code must be Z for Job Codes that place the employee on lines 21-33 of the Public Schools Staff Survey (EEO-5).
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the relationship between the Paraprofessional Qualification code and the Job Code and resubmit the record for processing.

### 2T. Staff Number Identifier, Local format
The Staff Number Identifier, Local may be any combination of letters, numbers and blanks. All blanks are not allowable. It must be left-justified with trailing blanks.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Staff Number Identifier, Local and resubmit the records.

### 2U. Staff Number Identifier, Local must not equal SSN
The Staff Number Identifier, Local must not be identical to the Social Security Number.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Staff Number Identifier, Local or the Social Security Number and resubmit the record.

### 2V. Employee Type must be RF or RP for Separation Reason A-P
If Separation Reason code is A-P, then Employee type must be RF or RP.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the relationship between the Separation Reason and the Employee Type and resubmit the record for processing.

### 2W. Degree/Credential Earned must be Z for EEO-5 lines 44-54
If the employee's Job Code, Primary places the employee on lines 44-54, inclusive, of the Public Schools Staff Survey - EEO-5, then the Degree/Credential Earned code must be Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Degree/Credential Earned code or the Job Code, Primary and resubmit the records for processing.

### 2X. School Principal Certification Program code validity
If Survey Period Code is 2 or 3, then School Principal Certification Program code must be Z. If Survey Period Code is 5, then School Principal Certification Program must be A, B, C, D or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Principal Certification Program and resubmit the records for processing.

### 2Y. School Principal Certification Program requires EEO-5 lines 1-43
If the School Principal Certification Program is A-D, then the employee's Job Code must place the employee on lines 1-43, inclusive, of the Public Schools Staff Survey - EEO-5.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the School Principal Certification Program code or Job Code, Primary and resubmit the record for processing.

### 2Z. Reading Endorsement code validity
Reading Endorsement codes must be N, Y, R or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Reading Endorsement codes and resubmit the records for processing.

### 3A. Literacy Micro-Credential code validity
Literacy Micro-Credential codes must be E, L, S, A, B, C, D, N or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Literacy Micro-Credential codes and resubmit the records for processing.

### 3B. Literacy Micro-Credential restricted for specified EEO lines *(Updated 04/24/2026)*
If the employee's Job Code places the employee on EEO lines 00, 44, 48, 50, 52, 53, 54; then the Literacy Micro-Credential code cannot be A, B, C, D, E, L, N or S.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Literacy Micro-Credential code and resubmit the records for processing.

### 3C. Youth Mental Health Awareness Training code validity
Youth Mental Health Awareness Training code must be N, T, Y or Z. This edit only applies to Survey 2, 3, and 5.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Youth Mental Health Awareness Training codes and resubmit the records for processing.

### 3D. Teacher Apprenticeship Program Indicator code validity
If Survey Period Code is 2, 3 and 5, then Teacher Apprenticeship Program Indicator must be Y or N.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Teacher Apprenticeship Program Indicator and resubmit the records.

### 3E. Teacher Apprenticeship Program Indicator requires Job Code 59050
If Teacher Apprenticeship Program Indicator is Y, then Job Code must be 59050.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Teacher Apprenticeship Program Indicator and resubmit the records.

---

## State Validation

### 30. Matching payroll or fiscal year format required
If Survey Period Code is 2 or 3, each Staff Demographic Information record must have a matching Staff Payroll record based on District Number, Social Security Number, Survey Period Code and Fiscal Year. If Survey Period Code is 5, each Staff Demographic Information record must have a matching Staff Fiscal Year Salaries, or Staff Fiscal Year Benefits format based on District Number, Social Security number, Survey Period Code, and Fiscal Year.
**Result:** State validation

**District Responsibility:** The district must verify that the Staff Demographic Information record is valid, then submit a matching Staff Payroll record based on District Number, Social Security Number, Survey Period Code and Fiscal Year.

### 31. Fiscal Year Salary threshold for high attendance range
If Survey Period is 5, and the sum of Days Present; Days Absent, Personal Leave; Days Absent, Sick Leave; Days Absent, Temporary Duty Elsewhere; and Days Absent, Other is between 100 and 180 inclusive, then the sum of Fiscal Year Salary on all Staff Fiscal Year Salaries format records for the employee must be greater than $18,000. The following fields should be used in matching the records: District Number, Social Security Number, Survey Period Code and Fiscal Year.
**Result:** State validation

**District Responsibility:** The district must review the information on the Staff Fiscal Year Salaries and Staff Demographic Information records and update the record that is in error to reflect the correct relationship in the edit.

### 32. Job Code, Primary must match Staff Payroll Information
If Survey Period is 2 or 3, Job Code, Primary on the Staff Demographic Information record must match at least one Job Code, Primary on the matching Staff Payroll Information records.
**Result:** State validation

**District Responsibility:** The district must correct the Job Code, Primary on the Staff Demographic Information record or the Staff Payroll Information record so that they are the same and reflect the actual job the employee held.

### 33. Paraprofessional Qualification required when Title I School-Wide is C
If the Title I School-Wide code on any of the matching Staff Fiscal Year Salaries records = C, then the Paraprofessional Qualification code on the Staff Demographic record must be A, B, C or E. The match should be done using the following fields: District Number, Social Security Number, Survey Period Code, and Fiscal Year.
**Result:** State validation

**District Responsibility:** The district must review the information on the two records and correct the Paraprofessional Qualification code or the Title I School-Wide code so that the proper relationship exists between these codes.

### 34. Paraprofessional Qualification required when Job Code is 51111-51113 and Title I Targeted Assistance is C
If the Job Code on any of the matching Staff Fiscal Year Salaries records is 51111, 51112 or 51113 and the Title I Targeted Assistance code is C, then the Paraprofessional Qualification code on the Staff Demographic record must be A, B, C or E. The match should be done using the following fields: District Number, Social Security Number, Survey Period Code, and Fiscal Year.
**Result:** State validation

**District Responsibility:** The district must review the information on the Staff Fiscal Year Salaries and Staff Demographic Information records and update the record that is in error to reflect the correct relationship in the edit.

### 35. Paraprofessional Qualification required when Migrant Regular School Year is C
If the Migrant Regular School Year code on any of the matching Staff Fiscal Year Salaries records = C, then the Paraprofessional Qualification code on the Staff Demographic record must be A, B, C or E. The match should be done using the following fields: District Number, Social Security Number, Survey Period Code, and Fiscal Year.
**Result:** State validation

**District Responsibility:** The district must review the information on the two records and correct the Paraprofessional Qualification code or the Migrant Regular School Year code so that the proper relationship exists between these codes.

### 36. Paraprofessional Qualification required when Migrant Summer is C
If the Migrant Summer code on any of the matching Staff Fiscal Year Salaries records = C, then the Paraprofessional Qualification code on the Staff Demographic record must be A, B, C or E. The match should be done using the following fields: District Number, Social Security Number, Survey Period Code, and Fiscal Year.
**Result:** State validation

**District Responsibility:** The district must review the information on the two records and correct the Paraprofessional Qualification code or the Migrant Summer code so that the proper relationship exists between these codes.

### 38. Staff Experience records required for instructional Job Codes
For Survey Period Code 2 or 3, if the employee's Job Code, Primary on the Staff Demographic Information format places the employee on lines 21-33, inclusive, of the Public Schools Staff Survey - EEO-5, excluding substitute teachers (Job Code, Primary code equal to 51080, 52080, 53080, 54080, 55080 or 59080) and the Employee Type is RF, TF or CF, then the employee must have at least one Staff Experience record with an Experience Type of C, at least one record with an Experience Type of D and at least one record with an Experience Type of F. The following fields should be used in matching the records: District Number, Social Security Number, Survey Period Code and Fiscal Year.
**Result:** State validation

**District Responsibility:** The district must review the staff member's experience and submit an additional Staff Experience record with an Experience Type code of C for this employee.

---

## Aggregate Validation

### 40. Every active school must have at least one Staff Demographic record
For each active school on the Master School Identification (MSID) file for the district, the number of Staff Demographic Information records must be greater than zero.
**Result:** Aggregate validation. An error message will be printed on the validation aggregate report (F70658) for schools that do not meet this edit.

**District Responsibility:** The district must submit Staff Demographic Information records (in addition to other required Staff Reporting formats) for this school.

---

## Exception Reports

### 50. School Number must be 9001 for EEO lines 1-8 at non-charter schools *(Updated 07/01/2026)*
If District Number is 1-68 and Charter School Status is not C or R (located on the Master School Identification File) and if the employee's Job Code places the employee on lines 1-8, inclusive, of the Public Schools Staff Survey - EEO-5, then School Number/Primary Home must be 9001.
**Result:** Exception report

**District Responsibility:** The district should verify the Job Code and the School Number/Primary Home and if in error correct the record.

### 51. Separation Date must not precede employment dates
If Separation Date is not zero then it must be greater than or equal to Employment Date, Current Position; Employment Date, Continuous Employment; and Employment Date, Original Position.
**Result:** Exception report

**District Responsibility:** The district should verify the Separation Date; Employment Date, Current Position; Employment Date, Continuous Employment; and Employment Date, Original Position and correct if in error.

### 52. Employment Date, Current Position must not precede earlier employment dates
If Separation Date is in the current Fiscal Year being reported or is zeroes, then Employment Date, Current Position must be greater than or equal to Employment Date, Continuous Employment and Employment Date, Original Position.
**Result:** Exception report

**District Responsibility:** The district should verify the Employment Date, Current Position; Employment Date, Continuous Employment and Employment Date, Original Position and correct if in error.

### 53. Employment Date, Continuous Employment must not precede Employment Date, Original Position
If Separation Date is in the current Fiscal Year being reported or is zeroes, then Employment Date, Continuous Employment must be greater than or equal to the Employment Date, Original Position.
**Result:** Exception report

**District Responsibility:** The district should verify the Employment Date, Continuous Employment and the Employment Date, Original Position and correct if in error.

### 54. Matching Selected Benefits, Type D record required for RF employees
For Survey Period Code 2 or 3, if Employee Type is RF, then the employee must have a matching Staff Benefits record with a Selected Benefits, Type code of D (Florida Retirement System). For Survey Period Code 5, if Employee Type is RF, then the employee must have a matching Staff Fiscal Year Benefits record with a Selected Benefits, Type/Value code of D. The records should be matched on District Number, Social Security Number, Survey Period Code and Fiscal Year.
**Result:** Exception report

**District Responsibility:** The district must review the Staff Demographic Information record and the Staff Benefits records and update one of the records if there is an error or submit an additional Staff Benefits record with a Selected Benefits, Type code of D.

### 55. Sum of Days Present and Absent must be greater than zero for instructional/administrative staff
If Survey Period is 5, the sum of the number of Days Present; Days Absent, Personal Leave; Days Absent, Sick Leave; Days Absent, Temporary Duty Elsewhere; and Days Absent, Other must be greater than zero for regular full-time (RF), temporary full-time (TF) and contracted full-time (CF) employees whose job codes place them on lines 9-19 (school administrators) or 21-33 (teachers) of the Public Schools Staff Survey (EEO-5) unless they are all 999.
**Result:** Exception report

**District Responsibility:** The district should review the data to verify that this regular full-time teacher did not have days present or absent during the regular 180 day school year. If there is an error in the data on this record, the district should submit an update to the record.

### 56. Degree Earned should not be Z for EEO lines 21-43
If the employee's Job Code places the employee on lines 21-43, inclusive, of the Public Schools Staff Survey - EEO-5, excluding substitute teachers (Job Code, Primary code equal to 51080, 52080, 53080, 54080, 55080 or 59080), vocational technical teachers (53001-53014), adult education teachers (54001) and ROTC teachers (51047, 51048) the Degree Earned code must not be Z.
**Result:** Exception report

**District Responsibility:** The district should verify the Degree Earned code and if in error correct the record.

### 57. Birth Date must reflect age 16-80
Birth Date must be between the age range of 16 and 80 years old, inclusive, in the current calendar year.
**Result:** Exception report

**District Responsibility:** The district should verify the Birth Date and if in error correct the record.

### 59. Matching Selected Benefits, Type A or K record required for RF employees
For Survey Period Code 2 or 3, if Employee Type is RF, then the employee must have a matching Staff Benefits record with a Selected Benefits, Type code of A or K. For Survey Period Code 5, if Employee Type is RF, then the employee must have a matching Staff Fiscal Year Benefits record with a Selected Benefits, Type/Value code of A or K. The records should be matched on District Number, Social Security Number, Survey Period Code and Fiscal Year.
**Result:** Exception report

**District Responsibility:** The district must review the Staff Demographic Information record and the Staff Benefits record and update the record that is in error or submit an additional Staff Benefits record with a Selected Benefits, Type of A or K.
