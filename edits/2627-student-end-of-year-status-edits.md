# Student End of Year Status — Edits and Reject Rules

Source: https://www.fldoe.org/file/20909/2627seoy.pdf
Manual: Student Database 2026-2027

This document covers 47 edits across four categories: Reject Rules (record rejected), State Validation (cross-format matching), Exception Reports (advisory), and an Aggregate Exception Report (school-level count). Edit numbering is non-sequential; Reject Rules run 1-2, 4-9, 12-18, 20-26, 28, 32, 34, 37, 2A-2D, 2P, 3C-3D, 3I-3L, 3Q-3Z (note: Edit 3U is marked DELETED 07/01/25 and Edit 3V is UPDATED 06/04/2026), State Validation runs 41-45, 47, 49, 4A-4B, 4D, 4H-4O, Exception Reports are 50 and 5A, and the Aggregate Exception Report is 80.

---

## Reject Rules

### 1. District Number, Current Enrollment must be active on Appendix C *(Updated 07/01/2026)*
District Number, Current Enrollment must be numeric and active (A) on the Appendix C: District Name Table and must be correct for the district submitting the data.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number, Current Enrollment and resubmit the record.

### 2. School Number, Current Enrollment numeric range
School Number, Current Enrollment must be numeric in the range 0001 to 9899, excluding 9001 and 7006, or it must be N998 or N999.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Enrollment and resubmit the records.

### 4. Survey Period Code must be 5
Survey Period Code must be 5 and must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** The district must correct Survey Period Code either on the records coming in or the transmission JCL and all records must be resubmitted.

### 5. School Year correct for submission
School Year must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** The district must correct School Year either on the records coming in or the transmission JCL and all records must be resubmitted.

### 6. Transaction Code validity and existence match
The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified then the record must not already exist on the database; if C or D is specified then the record must exist on the database. An original transaction is the first submission of a record during a survey period. After original transmission of records, changes to the record for elements other than the key elements must be done with a "C" as the Transaction Code. To delete a record, the Transaction Code must be a "D". To change key elements in a batch transaction, the record must FIRST be deleted with a "D" and then added with an "A".
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Transaction Code and resubmit the records.

### 7. Record uniqueness
Each Student End of Year Status record must be unique based on the keys of District Number, Current Enrollment; Florida Education Identifier; Survey Period Code; School Year; and Grade Level. If more than one Student End of Year Status record is submitted, only one record with Grade Level = PK-12 will be accepted and only one record with Grade Level = 30 or 31 will be accepted.
**Result:** First record accepted, all other duplicate records rejected

**District Responsibility:** If the record that was accepted and loaded to the database is the correct one, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must delete an invalid record, correct any rejected record if necessary, and resubmit the corrected record.

### 8. Grade Promotion Status code validity
Grade Promotion Status must be A, D, P, R, N or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Grade Promotion Status and resubmit the record.

### 9. Diploma Type code validity
Diploma Type must be W06, W10, WCO, WD1, WEL, WFT, WGD, WGA, WME, WOC, WRW, WWE, WWT, WWW, WXL, WXT, WXW, W43, W45, W52, W54, W55, W58, W59, W61, W62, W63 or ZZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Diploma Type and resubmit the records.

### 12. Item 3 filler must be all spaces
Item 3 - Filler on this format in position numbers 7-16 must be all spaces.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must fill the positions noted with all spaces and resubmit the record.

### 13. Student Number Identifier, Local format
The Student Number Identifier, Local may be any combination of letters, numbers and blanks. (All blanks are allowable.) It must be left-justified with trailing blanks.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Student Number Identifier, Local and resubmit the records.

### 14. Year Entered Ninth Grade required for Grade Levels 09-12, must be zeros for PK-08
If Grade Level is PK-08 then Year Entered Ninth Grade, Graduation Requirements Determination must be 00000000. If Grade Level is 09, 10, 11 or 12 then Year Entered Ninth Grade, Graduation Requirements Determination must be greater than zero.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district should correct the Year Entered Ninth Grade, Graduation Requirements Determination or the Grade Level and resubmit the records.

### 15. Grade Promotion Status must not be Z for Grade Levels K-12
If Grade Level equals K-12, then Grade Promotion Status must not equal Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct either the Grade Promotion Status code or Grade Level and resubmit the record.

### 16. Withdrawal Reason code validity
Withdrawal Reason code must be DNE, W01, W02, W05, W3A, W3B, W3D, W3E, W3F, W04, W12, W13, W15, W18, W21-W26, WAG, WGT, WHP, WMA, WPC, WPP or ZZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Withdrawal Reason code and resubmit the records.

### 17. Grade Level code validity
Grade Level code must be PK, KG, 01-12, 30 or 31.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Grade Level and resubmit the records.

### 18. School Number restriction for District 71
If District Number, Current Enrollment equals 71, School Number, Current Enrollment must not equal 0500, 0600, or 0700.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Enrollment and resubmit the records.

### 20. School Number, Current Enrollment must exist on Master School Identification File
The School Number, Current Enrollment must exist on the Master School Identification File as a valid school number in the district of enrollment.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the School Number, Current Enrollment and resubmit the record.

### 21. Dropout Prevention Performance-Based Exit Option Test Results requires Grade Level 10+
If Dropout Prevention Performance-Based Exit Option Test Results is P or F, then Grade Level must be 10 or higher.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct either the Dropout Prevention Performance-Based Exit Option Test Results or the Grade Level and resubmit the record.

### 22. Grade Promotion Status restriction for Withdrawal Reason DNE
If Withdrawal Reason is DNE, then Grade Promotion Status must not be A, D, P, or R.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct either the Withdrawal Reason or the Grade Promotion Status and resubmit the record.

### 23. Diploma Biliteracy Seal Designation code validity
Diploma Biliteracy Seal Designation must be B, G, S or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Diploma Biliteracy Seal Designation and resubmit the record.

### 24. Diploma Florida Seal of Fine Arts Designation code validity
Diploma Florida Seal of Fine Arts Designation must be Y or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Diploma Biliteracy Seal Designation and resubmit the record.

### 25. Grade Point Average State, Cumulative numeric range
Grade Point Average State, Cumulative must be numeric and greater than or equal to zero but must not exceed 4.0000 or it may be 99999. Note: Four decimal places assumed.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Grade Point Average State, Cumulative and resubmit the records.

### 26. Withdrawal Date date range
If District Number, Current Enrollment is not 71, or if District Number, Current Enrollment is 71 and School Number, Current Enrollment is 0300, 0400 or 0801, then Withdrawal Date must be a valid date in the range of 07/01/**** to 08/31/****.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Withdrawal Date and resubmit the records.

### 28. Florida Education Identifier format
Florida Education Identifier (FLEID) is alphanumeric and must be entered as "FL" in the first 2 positions followed by twelve numeric digits. No blanks, spaces or all zeros for the twelve numeric digits are allowable.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Florida Education Identifier and resubmit the record for processing.

### 2A. Job Attainment Skills code validity *(New 07/01/2026)*
The Job Attainment Skills code must be Y or Z; and if Grade Level is PK, KG, or 01-08, then the Job Attainment Skills code must be Z. This code is only valid in Survey Period Code 5.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Job Attainment Skills code, the Grade Level, or the Survey Period Code and resubmit the record.

### 2B. Employability Skills and Resiliency in the Workplace code validity *(New 07/01/2026)*
The Employability Skills and Resiliency in the Workplace must be Y or Z; and if Grade Level is PK, KG, or 01-08, then the Employability Skills and Resiliency in the Workplace code must be Z. This code is only valid in Survey Period Code 5.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Employability Skills and Resiliency in the Workplace code, the Grade Level, or the Survey Period Code and resubmit the record.

### 2C. Workplace Safety code validity *(New 07/01/2026)*
The Workplace Safety code must be Y or Z; and if Grade Level is PK, KG, or 01-08, then the Workplace Safety code must be Z. This code is only valid in Survey Period Code 5.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Workplace Safety code, the Grade Level, or the Survey Period Code and resubmit the record.

### 2D. Self-Advocacy and Career Planning code validity *(New 07/01/2026)*
The Self-Advocacy and Career Planning code must be Y or Z; and if Grade Level is PK, KG, or 01-08, then the Self-Advocacy and Career Planning code must be Z. This code is only valid in Survey Period Code 5.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Self-Advocacy and Career Planning code, the Grade Level, or the Survey Period Code and resubmit the record.

### 2P. Year Entered Ninth Grade format and validity
Year Entered Ninth Grade, Graduation Requirements Determination must be numeric, contain no blanks and be a valid two-consecutive-years combination not in the future or it must be all zeros.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district should correct the Year Entered Ninth Grade, Graduation Requirements Determination and resubmit the records.

### 32. Diploma Type grade level requirements for standard diploma types
If Diploma Type is W06, WCO, WD1, WEL, WFT, WGA, WGD, WOC, WRW, WWE, WWT, WWW, WXL, WXT or WXW, Grade Level must be one of the grades 9-12. If Diploma Type is W10, Grade Level must be one of the grades 10-12.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Diploma Type or the Grade Level so that they are in the proper relationship and resubmit the record.

### 34. At least one of Diploma Type or Withdrawal Reason must not be ZZZ
Of the two data elements, Diploma Type and Withdrawal Reason, one must be other than ZZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Diploma Type or Withdrawal Reason and resubmit the records.

### 37. Single Parent and Single Pregnant Woman code validity
Single Parent and Single Pregnant Woman code must be S, W, B or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Vocational, Single Parent and Single Pregnant Woman codes and resubmit the records.

### 3C. Diploma Types W43-W63 require Grade Level 30 or 31
If Diploma Type is W43, W45, W52, W54, W55, W58, W59, W61, W62 or W63, Grade Level must be 30 or 31.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Diploma Type or the Grade Level so that they are in the proper relationship and resubmit the record.

### 3D. Dropout Prevention Performance-Based Exit Option Test Results and Diploma Type relationship
The Dropout Prevention Performance-Based Exit Option Test Results code must be P, F, or Z. If the Performance-Based Exit Option Test Results code is P, then Diploma Type must either be W10, WGD or WGA. If the Diploma Type code is W10, WGD or WGA then the Dropout Prevention Performance-Based Exit Option Test Results code must be P.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct either the Dropout Prevention Performance-Based Exit Option Test Results code or the Diploma Type and resubmit the records.

### 3I. Grade Promotion Status: Good Cause Exemption code validity
Grade Promotion Status: Good Cause Exemption must be 0 (zero), 1, 2, 3, 4, 5 or 7.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct Grade Promotion Status: Good Cause Exemption and resubmit the record.

### 3J. Good Cause Exemption relationship with Grade Level 3 and Grade Promotion Status
If Grade Promotion Status equals A and Grade Level equals 3, Grade Promotion Status: Good Cause Exemption must not be 0 (zero). If Grade Promotion Status: Good Cause Exemption is greater than 0, then Grade Level must equal 3 and Grade Promotion Status must equal A.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the records so that the appropriate relationship exists between Grade Promotion Status, Grade Level and Grade Promotion Status: Good Cause Exemption and resubmit the records.

### 3K. Diploma Type required when Grade Level 12 and Grade Promotion Status P
If Grade Level equals 12 and Grade Promotion Status equals P, Diploma Type must not equal ZZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Diploma Type so that they correctly correspond to the Grade Level and Promotion Status code and resubmit the record.

### 3L. Diploma Type must be ZZZ when Grade Promotion Status is R, N or Z for PK-12
If Grade Level equals PK-12 and Grade Promotion Status = R, N or Z, then Diploma Type must equal ZZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct either the Grade Promotion Status code or Diploma Type and resubmit the records.

### 3Q. Grade Promotion Status must be Z for Grade Levels 30 or 31
If Grade Level equals 30 or 31, then Grade Promotion Status must equal Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct either the Grade Promotion Status code or Grade Level and resubmit the record.

### 3R. Grade Promotion Status and Grade Level must have valid association
There must be a valid association between the Grade Promotion Status listed below and the student's Grade Level.

| Grade Promotion Status | Valid Grade Levels |
|---|---|
| A | KG-11 |
| D | 12 |
| P | PK-12 |
| R | PK-12 |
| N | KG-12 |
| Z | PK, 30-31 |

**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Grade Promotion Status or the Grade Level so that there is a valid relationship between these two data elements and resubmit the records.

### 3S. Diploma Type not ZZZ requires Grade Promotion Status P
For Grade Levels PK-12, if Diploma Type is not equal to ZZZ, then Grade Promotion Status must be P. If Diploma Type equals WD1, then Grade Promotion Status must be P or D.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Grade Promotion Status.

### 3T. Withdrawal Reason W05 or W26 requires Grade Level 06 or above *(Updated 07/01/2025)*
If Withdrawal Reason is W05 or W26, Grade Level must not be PK-05.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the record so that the appropriate relationship exists between Withdrawal Reason and Grade Level and resubmit the record.

### 3U. *(DELETED 07/01/2025)*
Edit 3U (Withdrawal Reason W26 restriction for Grade PK-5) was deleted effective 07/01/2025. Its logic is now incorporated into Edit 3T.

### 3V. Grade Promotion Status D requires Grade Level 12 and valid Withdrawal Reason or WD1 Diploma *(Updated 06/04/2026)*
If Grade Promotion Status = D, then Grade Level must equal 12 and Withdrawal Reason must be W01, W02 or W3A, or Diploma Type must equal WD1.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Grade Level or the Withdrawal Reason so that it correctly corresponds to the Grade Promotion Status, and resubmit the record.

### 3W. Withdrawal Reason W25 requires Grade Level PK or KG
If Withdrawal Reason is W25, Grade Level must be PK or KG.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the record so that the appropriate relationship exists between Withdrawal Reason and Grade Level and resubmit the record.

### 3X. Diploma Designation code validity
Diploma Designation must be S, I, B or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Diploma Designation and resubmit the record.

### 3Y. Virtual Instruction Provider code requires valid Grade Level *(Updated 07/01/2026)*
If the Virtual Instruction Provider code is 071 (FLVS) then Grade Level must be KG-12; 302 (K12 Florida, LLC) then KG-12; 308 (Somerset Academy) then KG-12; 309 (Imagine Learning) then KG-12; 311 (Mater Virtual Academy) then KG-12; 313 (Florida Connections Academy) then KG-12; 320 (Graduation Alliance) then 09-12; 322 (Accel Online East) then KG-12; 323 (Optima Academy Online) then KG-12; 326 (K12 Preparatory Academy) then 9-12; 327 (UCP of Central Florida) then KG-5; 328 (Second Mile Education) then 7-12.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Virtual Instruction Provider or the Grade Level and resubmit the record.

### 3Z. School Number 7001 requires valid Virtual Instruction Provider code
If the School Number, Current Enrollment is 7001, then the Virtual Instruction Provider code must be a valid code in Appendix CC.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Virtual Instruction Provider or the School Number, Current Enrollment and resubmit the record.

---

## State Validation

### 41. Matching Student Demographic record required
Each Student End of Year Status record must have a matching Student Demographic record based on both District Number, Current Enrollment and District Number, Current Instruction/Service (Student Demographic); District Number, Current Enrollment (Student End of Year Status); Florida Education Identifier; Survey Period Code; and School Year.
**Result:** State validation

**District Responsibility:** The district must delete the Student End of Year Status record or add a Student Demographic record to match the above key fields.

### 42. Good Cause Exemption 1 requires US School Entry within two years of Withdrawal Date
If Grade Promotion Status: Good Cause Exemption equals 1, then there must be a matching Student Demographic record where Date Entered United States School is less than two years from the Withdrawal Date. The records should match based on both District Number, Current Enrollment and District Number, Current Instruction/Service (Student Demographic); District Number Current Enrollment (End of Year Status) Florida Education Identifier; Survey Period, and School Year.
**Result:** State validation

**District Responsibility:** The district must correct the Student End of Year Status record (Grade Promotion Status: Good Cause Exemption element) or the Student Demographic record (Date Entered United States School element) so the appropriate relationship exists.

### 43. Grade Promotion Status D not allowed when Exceptionality Primary is L only
If Exceptionality, Primary is L and Exceptionality, Other is Z-filled, then the Grade Promotion Status must not be D. The records should match based on District Number, Current Enrollment; School Number, Current Enrollment; Florida Education Identifier, Survey, and Year.
**Result:** State validation

**District Responsibility:** The district must correct the record so that the appropriate relationship exists between Grade Promotion Status, Exceptionality, Primary and Exceptionality, Other.

### 44. Diploma Types WRW/WXW require non-L exceptionality
If a Student End of Year Status record does not have a matching Exceptional Student record, or if Exceptionality, Primary is L and Exceptionality, Other is Z-filled, then the Diploma Type must not be WRW or WXW.
**Result:** State validation

**District Responsibility:** The district must correct the applicable Student End of Year Status record so that the appropriate relationship exists between Diploma Type; Exceptionality, Primary and Exceptionality, Other, or delete the record and submit a matching Exceptional Student record.

### 45. Good Cause Exemption 2 requires non-L, non-Z exceptionality
If Grade Promotion Status: Good Cause Exemption equals 2, then there must be a matching Exceptional Student record where one of the two elements Exceptionality, Primary or Exceptionality, Other does not equal L or Z. The records should match based on District Number, Current Enrollment; School Number, Current Enrollment; Florida Education Identifier; Survey, and Year.
**Result:** State validation

**District Responsibility:** The district must correct the Student End of Year Status record or the Exceptional Student record so that the appropriate relationship exists between Grade Promotion Status: Good Cause Exemption and Exceptionality, Primary or Exceptionality, Other.

### 47. Year Entered Ninth Grade 20142015 or later prohibits Graduation Option 4
If Year Entered Ninth Grade, Graduation Requirements Determination is 20142015 or later, then Graduation Option on the Student Demographic record may not equal 4. The records should match based on both District Number, Current Enrollment and District Number, Current Instruction/Service (Student Demographic); District Number, Current Enrollment (End of Year Status), Florida Education Identifier; Survey Period Code, and Year.
**Result:** State validation

**District Responsibility:** The district must correct the Student End of Year Status record (Year Entered Ninth Grade, Graduation Requirements Determination) or the Student Demographic record (Graduation Option) so the appropriate relationship exists.

### 49. Good Cause Exemption 5 requires Section 504 or non-L/Z exceptionality
If Grade Promotion Status Good Cause Exemption equals 5, then there must either be a matching Federal/State Indicator record with Section 504 Eligible equal to "Y", or there must be a matching Exceptional Student record with one of the two elements Exceptionality, Primary or Exceptionality, Other not equal to L or Z. The records should match based on District Number, Current Enrollment; School Number, Current Enrollment; Florida Education Identifier; Survey, and Year.
**Result:** State validation

**District Responsibility:** The district must correct the Student End of Year Status record (Grade Promotion Status: Good Cause Exemption element), the Federal/State Indicator Status record (Section 504 Indicator element) or the Exceptional Student record (Exceptionality, Primary or Exceptionality, Other elements) so that the appropriate relationship exists between Grade Promotion Status: Good Cause Exemption and one of these three elements.

### 4A. Additional School Year Student S/F requires Grade Promotion Status P, D, or N
If Additional School Year Student (on the Student Demographic Information record) = S or F, then Grade Promotion Status must be P, D, or N. The records should match based on both District Number, Current Enrollment and District Number, Current Instruction/Service (Student Demographic); District Number Current Enrollment (Student End of Year Status); Florida Education Identifier; Survey Period Code and School Year.
**Result:** State validation

**District Responsibility:** The district should review the data and correct the record that is in error so that the appropriate relationship exists between Additional School Year Student and Grade Promotion Status.

### 4B. Withdrawal Reason W25 requires student age under 6 as of Withdrawal Date
If Withdrawal Reason = W25 then age must be less than 6 as of the Withdrawal Date. The records should match based on both District Number, Current Enrollment and District Number, Current Instruction/Service (Student Demographic); District Number Current Enrollment (Student End of Year Status); Florida Education Identifier; School Year and Survey Period Code.
**Result:** State validation

**District Responsibility:** The district must review the Withdrawal Reason on the Student End of Year format and the Birth Date on the Student Demographic Information record, correct the one that is wrong and resubmit the record as a change to the database.

### 4D. Withdrawal Reason W21 requires matching Prior School Status record with W21
If Withdrawal Reason is W21 on the Student End of Year Status record, then there must be a matching Prior School Status/Student Attendance record with a Withdrawal Code, PK-12 of W21. The records should be matched on District Number, Current Enrollment; Florida Education Identifier; School Year and Survey Period Code.
**Result:** State validation

**District Responsibility:** The district should review the Withdrawal Reason code and the Withdrawal Code, PK-12 and correct the record that is in error.

### 4H. Performance-Based Exit Option Test Results P/F requires Graduation Option 8
If the Dropout Prevention: Performance-Based Exit Option Test Results code is F or P, then the Graduation Option on Student Demographic must equal 8. The Student Demographic Information record is found by matching on both District Number, Current Enrollment and District Number, Current Instruction/Service; Florida Education Identifier; Survey Period Code and School Year.
**Result:** State validation

**District Responsibility:** The district must correct the Student End of Year Status record (Dropout Prevention Performance-Based Exit Option Test Results) or the Student Demographic record (Graduation Option) so that the appropriate relationship exists between Performance-Based Exit Option Test Results and Graduation Option.

### 4I. Diploma Types W10/WGA/WGD require Graduation Option 8
If the Diploma Type is W10, WGA or WGD (on the Student End of Year Status record), then Graduation Option on Student Demographic Information record must = 8. The Student Demographic Information record is found by matching on both District Number, Current Enrollment and District Number, Current Instruction/Service; Florida Education Identifier; Survey Period Code and School Year.
**Result:** State validation

**District Responsibility:** The district must correct the Student End of Year Status record (Diploma Type) or the Student Demographic record (Graduation Option) so that the appropriate relationship exists between Diploma Type and Graduation Option.

### 4J. Diploma Type WEL requires ELL PK-12 code LP or LY
If the Diploma Type is WEL (on the Student End of Year Status record), then English Language Learners, PK-12 code on Student Demographic Information record must = LP or LY. The Student Demographic Information record is found by matching on both District Number, Current Enrollment and District Number, Current Instruction/Service; Florida Education Identifier; Survey Period Code and School Year.
**Result:** State validation

**District Responsibility:** The district must correct the Student End of Year Status record (Diploma Type) or the Student Demographic record (English Language Learners, PK-12) so that the appropriate relationship exists between Diploma Type and English Language Learners, PK-12.

### 4K. Withdrawal Reason WMA requires Exceptionality Primary from valid list
If Withdrawal Reason is WMA on the Student End of Year Status record, then there must be a matching Exceptional Student record where Exceptionality, Primary on the Exceptional Student record must be C, F, G, H, I, J, K, M, O, P, S, T, U, V, or W. The records should be matched on District Number, Current Enrollment; School Number, Current Enrollment; Florida Education Identifier; Survey Period Code; and School Year.
**Result:** State validation

**District Responsibility:** The district must correct the record so that the appropriate relationship exists between Exceptionality, Primary and Student End of Year Status Record.

### 4L. Withdrawal Reason WMA requires student age 22 or older as of June 30
If Withdrawal Reason is WMA on the Student End of Year Status record, then there must be a matching Student Demographic record where the student's age cannot be less than 22 as of June 30th of the reporting year in Survey 5. The match should be made using the following elements: District Number, Current Enrollment; School Number, Current Enrollment; Florida Education Identifier; Survey Period Code; and School Year.
**Result:** State validation

**District Responsibility:** The district must review the Withdrawal Reason on the Student End of Year format and the Birth Date on the Student Demographic Information record, correct the one that is wrong and resubmit the record as a change to the database.

### 4M. Third Grade Retention — Level 1 FAST PM3 Reading requires Grade Promotion Status A, N, or R
If Grade Level = 3 and the student exists on the table of students who scored at Level 1 in Reading on the 3rd Grade Florida Assessment of Student Thinking (FAST) Progress Monitoring 3 Test (matched on District Number, Current Enrollment and Florida Education Identifier), then Grade Promotion Status must = A, N or R. Note: The Level 1 table is refreshed during summer while Survey 5 is ongoing; districts may initially receive validation errors for students who subsequently achieve a passing score during summer.
**Result:** State validation

**District Responsibility:** The district must review the Grade Promotion Status code on the Student End of Year Status record so that the appropriate relationship exists.

### 4N. Workforce Badge Y requires valid Exceptionality Primary or Other *(New 07/01/2026)*
If any of the Workforce Badges (Employability Skills and Resiliency in the Workplace, Job Attainment Skills, Self-Advocacy or Workplace Safety) is reported as Y, then Exceptionality, Primary must be C, F, G, H, I, J, K, O, P, S, V, or W, or Exceptionality, Other must contain at least one of the following codes: C, F, G, H, I, J, K, O, P, S, V, or W.
**Result:** State validation

**District Responsibility:** The district must verify the Workforce Badge indicators and the student's exceptionality codes. If the student earned a badge, the district must ensure they are reported with a valid ESE record containing at least one of the required exceptionality codes. If the badge was reported in error, it must be corrected; otherwise, the matching Exceptional Student record must be submitted or corrected to include an allowed code.

### 4O. Workforce Badge Y for Grade 09-12 requires matching Exceptional Student record *(New 07/01/2026)*
If code Y is reported for any of the Workforce Badges (Employability Skills and Resiliency in the Workplace, Job Attainment Skills, Self-Advocacy or Workplace Safety) and the Grade Level is 09-12, then there must be a matching Exceptional Student record based on District Number, Current Enrollment; Florida Education Identifier; Survey Period Code; and Year.
**Result:** State validation

**District Responsibility:** The district must delete the Student End of Year Status records if they were submitted in error or submit Exceptional Student records that match on the indicated fields with at least one acceptable exceptionality code reported in Exceptionality, Primary or Exceptionality, Other.

---

## Exception Reports

### 50. Grade Point Average State, Cumulative should not be zero for Grade 9-12
If District Number, Current Enrollment is not 71 and Grade Level = 9-12, then Grade Point Average State, Cumulative must not equal 00000.
**Result:** Exception report

**District Responsibility:** The district should verify the Grade Level and the Grade Point Average State, Cumulative and correct if in error.

### 5A. Withdrawal Reason W21 should have matching Discipline record with Action Code E
If Withdrawal Reason is W21 on the Student End of Year Status record, then there must be a matching Student Discipline/Resultant Action record with a Disciplinary/Referral Action code of E. The records should be matched on District Number, Current Enrollment; Florida Education Identifier; School Year and Survey Period Code.
**Result:** Exception report

**District Responsibility:** The district should review the Withdrawal Reason code and the Disciplinary/Referral Action Code and correct one of the records if there is an error.

---

## Aggregate Exception Reports

### 80. Grade 9-12 GPA 99999 should not exceed 20 percent of school's records
If District Number, Current Enrollment is not 71 and Grade Level = 9-12, then less than 20 percent of records should be reported with Grade Point Average State, Cumulative equal to 99999. An error message will be printed on the exception report for schools that fail the aggregate exception edit.
**Result:** Aggregate exception report

**District Responsibility:** The district must verify Grade Point Average State, Cumulative on the Student End of Year Status records for this school and correct these fields if they are in error.
