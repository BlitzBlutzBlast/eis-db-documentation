# Federal/State Indicator Status — Edits and Reject Rules

Source: https://www.fldoe.org/file/20909/2627fsis.pdf
Manual: Student Database 2026-2027

This document covers 38 edits across four categories: Reject Rules (record rejected), State Validation (cross-format matching), Exception Reports (advisory), and an Aggregate Exception Report (district-level count). Edit numbering is non-sequential; Reject Rules run 1-2, 4-16, 20-22, 25-26, 31, 39-44, 46, 48-49, 4A-4C (gap at 3, 13, 17-19, 23-24, 27-30, 32-38, 45, 47), State Validation runs 50-52, 59-61, 63-64, 66-67, Exception Reports are 81-82, Aggregate Exception Report is 91.

---

## Reject Rules

### 1. District Number, Current Enrollment must be active on Appendix C *(Updated 07/01/2026)*
District Number, Current Enrollment must be numeric and active (A) on the Appendix C: District Name Table and must be correct for the district submitting the data.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the District Number, Current Enrollment and resubmit the records.

### 2. School Number, Current Enrollment numeric range
If Survey Period Code is 2, 3 or 5, School Number, Current Enrollment must be numeric in the range 0001 to 9899, excluding 9001 and 7006, or it must be N998 or N999.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Enrollment and resubmit the records.

### 4. Survey Period Code must be 2, 3 or 5
Survey Period Code must be 2, 3 or 5 and must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** The Survey Period Code must be corrected either on the records coming in or the transmission JCL and all records must be resubmitted.

### 5. Fiscal Year correct for submission
Fiscal Year must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** The district must correct the Fiscal Year either on the records coming in or the transmission JCL and resubmit all records.

### 6. Transaction Code validity and existence match
The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified then the record must not already exist on the database; if C or D is specified then the record must exist on the database. An original transaction is the first submission of a record during a survey period. After original transmission of records, changes to the record for elements other than the key elements must be done with a "C" as the Transaction Code. To delete a record, the Transaction Code must be a "D". To change key elements in a batch transaction, the record must FIRST be deleted with a "D" and then added with an "A".
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Transaction Code and resubmit the records.

### 7. Record uniqueness
Each Federal/State Indicator record must be unique based on the keys of District Number, Current Enrollment; Florida Education Identifier; Survey Period Code; and Fiscal Year.
**Result:** First record accepted, all other duplicate records rejected

**District Responsibility:** If the records that were accepted and loaded to the database are the correct ones, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must delete any invalid records, correct any rejected records if necessary, and resubmit the corrected records.

### 8. Federally Connected Student Indicator code validity by survey period
For Survey Period Code 3, Federally Connected Student Indicator code must be A, B, C or Z. For Survey Period Codes 2 and 5 Federally Connected Student Indicator code must be Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Federally Connected Student Indicator code or the Survey Period Code and resubmit the records.

### 9. Medical Complexity Exemption code validity
Medical Complexity Exemption code must be A, B, C, D, E or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Medical Complexity Exemption code and resubmit the record.

### 10. Bullied or Harassed — Religion code validity
Bullied or Harassed - Religion code must be Y, N or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Bullied or Harassed - Religion code and resubmit the record.

### 11. Bullied or Harassed — Sexual Orientation code validity
Bullied or Harassed – Sexual Orientation code must be Y, N or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Bullied or Harassed – Sexual Orientation code and resubmit the record.

### 12. Immigrant Student code validity
Immigrant Student code must be Y or N.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Immigrant Student code and resubmit the record.

### 14. Dropout Prevention/Juvenile Justice Programs code validity by survey period
For Survey Period Codes 2 and 3, Dropout Prevention/Juvenile Justice Programs must be A, D, E, J, N, P, R, S, T, U, W or Z. For Survey Period Code 5, Dropout Prevention/Juvenile Justice Programs must be Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Dropout Prevention/Juvenile Justice Programs codes and resubmit the records.

### 15. Student Number Identifier, Local format
The Student Number Identifier, Local may be any combination of letters, numbers and blanks. (All blanks are allowable.) It must be left-justified with trailing blanks.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Student Number Identifier, Local and resubmit the record.

### 16. Item 3 filler must be all spaces
Item 3 - Filler on this format in position numbers 7-16 must be all spaces.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must fill the positions noted with all spaces and resubmit the record.

### 20. Test Accommodations code validity
Test Accommodations code must be A, C, D, I, L, M, P, Q, R, S, T, U, V, X, Y or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes data in the rejected record to be loaded to the database, the district must correct the Test Accommodations code and resubmit the record.

### 21. Immunization Status code validity
For Survey Period Codes 2, 3 and 5, Immunization Status must be 0, 1, 2, 3, 4, 8, U, V, W, X or Y.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct Immunization Status codes and resubmit the records.

### 22. Career and Professional Academy Participant code validity
Career and Professional Academy Participant code must be Y or N.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Career and Professional Academy Participant codes and resubmit the records.

### 25. Homelessness Cause code validity
If Survey Period Code is 2, 3 or 5, Homelessness Cause code must be D, E, F, H, M, N, P, S, T, U, W or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Homelessness Cause code and resubmit the record.

### 26. Homelessness Cause must align with Homeless Student PK-12 code
If Homeless Student, PK-12 code is A, B, D or E, Homelessness Cause must be D, E, F, H, M, N, P, S, T, U or W. If Homeless Student, PK-12 code is N, Homelessness Cause must be Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Homelessness Cause code or the Homeless Student, PK-12 code and resubmit the record.

### 31. School-Related Arrests code validity
School-Related Arrests code must be Y or N.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the School-Related Arrests code and resubmit the record.

### 39. Section 504 Eligible code validity
For Survey Period Codes 2, 3 and 5, the Section 504 Eligible code must be Y, N, I or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Section 504 Eligible codes and resubmit the records.

### 40. School Number, Current Enrollment must be active except reserved codes
If the School Number, Current Enrollment is not N998 or N999, then it must exist on the Master School Identification File as a valid active school number in the district of enrollment.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the School Number, Current Enrollment and resubmit the record.

### 41. Homeless Student, PK-12 code validity
For Survey Period Codes 2, 3 and 5, the Homeless Student, PK-12 code must be A, B, D, E or N.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Homeless Student, PK-12 code and resubmit the record.

### 42. Homeless Unaccompanied Youth code validity
For Survey Period Codes 2, 3 and 5, Homeless Unaccompanied Youth code must be N, C, U or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Homeless Unaccompanied Youth code and resubmit the record.

### 43. Unaccompanied Youth must align with Homeless Student PK-12 code
If Homeless Student, PK-12 code is A, B, D or E, then Unaccompanied Youth must be C, U or N. If Homeless Student, PK-12 code is N, then Unaccompanied Youth must be Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the appropriate field and resubmit the record.

### 44. Fund Source code validity by survey period
For Survey Period Code 5, Fund Source code must be I or Z. For Survey Period Codes 2 or 3, Fund Source code must be Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Fund Source and resubmit the record.

### 46. Military Family Student code validity
Military Family Student code must be Y, N or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Military Family Student codes and resubmit the records.

### 48. Physical Education Waiver code validity
If Survey Period Code is 2, 3 or 5, then the Physical Education Waiver code must be Y, N or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes data in the rejected records to be loaded to the database, the district must correct the Physical Education Waiver code and resubmit the records.

### 49. Bullied or Harassed — Disability code validity
Bullied or Harassed - Disability code must be Y, N or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Bullied or Harassed - Disability code and resubmit the record.

### 4A. Bullied or Harassed — Race code validity
Bullied or Harassed - Race code must be Y, N or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Bullied or Harassed - Race code and resubmit the record.

### 4B. Bullied or Harassed — Sex code validity
Bullied or Harassed - Sex code must be Y, N or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Bullied or Harassed - Sex code and resubmit the record.

### 4C. Florida Education Identifier format
Florida Education Identifier (FLEID) is alphanumeric and must be entered as "FL" in the first 2 positions followed by twelve numeric digits. No blanks, spaces or all zeros for the twelve numeric digits are allowable.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Florida Education Identifier and resubmit the record for processing.

---

## State Validation

### 50. Matching Student Demographic record required
Each Federal/State Indicator Status record must have a matching Student Demographic record based on both District Number, Current Enrollment and District Number, Current Instruction/Service (Student Demographic) and District Number, Current Enrollment (Federal/State Indicator Status); Florida Education Identifier; Survey Period Code and Fiscal Year.
**Result:** State validation

**District Responsibility:** The district must delete the Federal/State Indicator Status record or add a Student Demographic record to match the above key fields.

### 51. Immunization Status restricted for Grade KG students with Course Schedule record
If Survey Period Code is 2 or 3 and Grade Level is KG on the matching Student Demographic Information record and if there is at least one matching Student Course Schedule record for the student, then the Immunization Status code must be 0, 1, 2, 3, 4, U, V, W, X or Y. The Student Demographic Information and Student Course Schedule matches are based on both District Number, Current Enrollment and District Number, Current Instruction/Service (Student Demographic and Student Course Schedule) and District Number, Current Enrollment (Federal/State Indicator Status); Florida Education Identifier; Survey Period Code and Fiscal Year.
**Result:** State validation

**District Responsibility:** The district must correct the records so that the appropriate relationship exists between Grade Level and Immunization Status.

### 52. Career and Professional Academy Participant requires Grade Level 06-12
If Career and Professional Academy Participant is not N then Grade Level on the matching Student Demographic Information record must be 06-12. The match is based on both District Number, Current Enrollment and District Number, Current Instruction/Service (Student Demographic) and District Number, Current Enrollment (Federal/State Indicator Status); Florida Education Identifier; Survey Period Code and Fiscal Year.
**Result:** State validation

**District Responsibility:** The district must correct the record so that the appropriate relationship exists between Career and Professional Academy Participant and Grade Level.

### 59. Dropout Prevention codes D or T require Grade Level not PK or KG
If Dropout Prevention/Juvenile Justice Programs code is D or T, then Grade Level on the matching Student Demographic Information record must not equal PK or KG. The match is based on both District Number, Current Enrollment and District Number, Current Instruction/Service (Student Demographic) and District Number, Current Enrollment (Federal/State Indicator Status); Florida Education Identifier; Survey Period Code and Fiscal Year.
**Result:** State validation

**District Responsibility:** The district must correct the records so that the appropriate relationship exists between Dropout Prevention/Juvenile Justice Programs and Grade Level.

### 60. Military Family Student must be Z for Grade PK
If Grade Level on the Student Demographic Information record is PK, then Military Family Student code must be Z. The records should be matched using the following elements: District Number, Current Enrollment (Federal/State Indicator Status) and both District Number, Current Instruction/Service and District Number, Current Enrollment (Student Demographic Information); Fiscal Year/Year; Survey Period Code and Florida Education Identifier.
**Result:** State validation

**District Responsibility:** The district must review the records and correct the record that is in error so that the appropriate relationship exists between Military Family Student and Grade Level.

### 61. Immunization Status restricted for Grade 07 students with Course Schedule record
If Survey Period Code is 2 or 3 and Grade Level is 07 on the matching Student Demographic Information record and if there is at least one matching Student Course Schedule record for the student, then Immunization Status code must be 0, 2, 3, 4, 8, U, V, W, X or Y. The Student Demographic Information and Student Course Schedule matches are based on both District Number, Current Enrollment and District Number, Current Instruction/Service (Student Demographic and Student Course Schedule) and District Number, Current Enrollment (Federal/State Indicator Status); Florida Education Identifier; Survey Period Code and Fiscal Year.
**Result:** State validation

**District Responsibility:** The district must review both records and correct the record that is in error so that the appropriate relationship exists between Grade Level and Immunization Status.

### 63. Physical Education Waiver must align with Grade Level
If Grade Level equals PK or 9-12 on the matching Student Demographic Information record, then the Physical Education Waiver code must be Z. If Survey Period Code is 2, 3 or 5 and if Grade Level equals KG-8 on the matching Student Demographic Information record, then the Physical Education Waiver code must be Y or N. The match should be made using the following elements: District Number, Current Enrollment (Federal/State Indicator Status) and both District Number, Current Enrollment and District Number, Current Instruction/Service (Student Demographic Information); Survey Period Code; Year and Florida Education Identifier.
**Result:** State validation

**District Responsibility:** The district should review the Grade Levels and Physical Education Waiver codes and correct the ones that are in error.

### 64. Immigrant Student Y requires non-US/PR Country of Birth
If the Immigrant Student = Y, then the Country of Birth on the Student Demographic record must not be US or PR. The records should be matched on the following elements: District Number, Current Enrollment (Federal/State Indicator Status) and both District Number, Current Enrollment and District Number, Current Instruction/Service (Student Demographic); Florida Education Identifier; Survey Period Code and Fiscal Year.
**Result:** State validation

**District Responsibility:** The district must correct the records so that the appropriate relationship exists between Immigrant Student and Country of Birth.

### 66. Dropout Prevention code P requires Grade Level not KG-04
If Dropout Prevention/Juvenile Justice Programs code is P, then Grade Level on the matching Student Demographic Information record must not be KG-04. The match is based on both District Number, Current Enrollment and District Number, Current Instruction/Service (Student Demographic) and District Number, Current Enrollment (Federal/State Indicator Status); Florida Education Identifier; Survey Period Code and Fiscal Year.
**Result:** State validation

**District Responsibility:** The district must correct the records so that the appropriate relationship exists between Dropout Prevention/Juvenile Justice code and Grade Level.

### 67. Section 504 Eligible Y requires no ESE exceptionality other than L/Z during Survey 2 or 3
If Survey Period Code is 2 or 3 and there is a matching Exceptional Student record with an Exceptionality, Primary or Exceptionality, Other code other than L and Z; then the Section 504 Eligible code must be Z. The match is based on District Number, Current Enrollment; Florida Education Identifier; Survey Period Code and Fiscal Year/Year.
**Result:** State validation

**District Responsibility:** The district must correct the records so that the appropriate relationship exists between Section 504 Eligible and Exceptionality, Primary on the Exceptional Student record.

---

## Exception Reports

### 81. Dropout Prevention code P should not apply to Grade 05 or 06
If Dropout Prevention/Juvenile Justice Programs code is P, then Grade Level on the matching Student Demographic Information record must not be 05 or 06. The match is based on both District Number, Current Enrollment and District Number, Current Instruction/Service (Student Demographic) and District Number, Current Enrollment (Federal/State Indicator Status); Florida Education Identifier; Survey Period Code and Fiscal Year.
**Result:** Exception report

**District Responsibility:** The district must review the Dropout Prevention/Juvenile Justice code and Grade Level and correct one of the records if there is an error.

### 82. Section 504 Eligible Y during Survey 5 should not coexist with non-L/Z exceptionality
If Survey Period Code is 5 and there is a matching Exceptional Student record with an Exceptionality, Primary or Exceptionality, Other code other than L and Z; then the Section 504 Eligible code must be Z. The match is based on District Number, Current Enrollment; Florida Education Identifier; Survey Period Code and Fiscal Year/Year.
**Result:** Exception report

**District Responsibility:** The district must review the records and, if a code is in error, correct the record so that the expected relationship exists between Section 504 Eligible and Exceptionality, Primary on the Exceptional Student record. If the data are correct as reported no action is necessary.

---

## Aggregate Exception Reports

### 91. Each district 01-67 must have at least one Homeless Student PK-12 code A, B, D or E
If Survey Period Code is 2, 3 or 5, for each school district in the range of 01-67 there must be at least one student coded A, B, D or E on the Homeless Student, PK-12 element.
**Result:** Aggregate exception report

**District Responsibility:** The district must review the records and correct the Homeless Student, PK-12 element on the records that are in error.
