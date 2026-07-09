# Prior School Status/Student Attendance — Edits and Reject Rules

Source: https://www.fldoe.org/file/20909/2627psssa.pdf
Manual: Student Database 2026-2027

This document covers 66 edits across four categories: Reject Rules (record rejected), State Validation (cross-format matching), Exception Reports (advisory), and Aggregate Exception Reports (school-level counts). Edit numbering is non-sequential; Reject Rules run 1-2, 5-49, 1A, 2A-2G, 4D-4I (gaps at 3-4, and various interior gaps), State Validation runs 50-52, Exception Reports run 71-82, Aggregate Exception Reports run 90-93.

---

## Reject Rules

### 1. District Number, Current Enrollment must be active on Appendix C *(Updated 07/01/2026)*
District Number, Current Enrollment must be numeric, active (A) on the Appendix C: District Name Table and must be correct for the district submitting the data.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct District Number, Current Enrollment and resubmit the records.

### 2. School Number, Current Enrollment numeric range
School Number, Current Enrollment must be numeric in the range 0001 to 9899, excluding 9001 and 7006, or it must be N998 or N999.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct School Number, Current Enrollment and resubmit the records.

### 5. Student Name, Legal cannot be blank
The Student Name, Legal: Must not be blank (Z-fill is NOT allowed). Allowable characters include double or single quotation marks, commas, slashes, periods, parentheses, hyphens, accent marks, and spaces where appropriate.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Student Name, Legal and resubmit the record.

### 6. Sex code validity
Sex code must be M or F.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Sex code and resubmit the records.

### 7. Item 3 filler must be all spaces
Item 3 - Filler on this format in position numbers 7-16 must be all spaces.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must fill the positions noted with all spaces and resubmit the record.

### 8. Birth Date must be numeric, valid, and not in the future
Birth Date must be numeric, a valid date in the format MMDDYYYY, and must be less than or equal to the last day of the Survey Period.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Birth Date and resubmit the records.

### 9. Grade Level code validity
Grade Level code must be PK, KG, or 01-12.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Grade Level and resubmit the records.

### 10. Survey Period Code must be 2, 3, or 5
Survey Period Code must be 2, 3, or 5 and must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the Survey Period Code must be corrected either on the records coming in or the transmission JCL and all the records must be resubmitted.

### 11. School Year correct for submission
School Year must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Year either on the records coming in or the transmission JCL and resubmit all records.

### 12. Entry (Re-entry) Code, PK-12 validity by survey period and term *(Updated 02/06/2026)*
Entry (Re-entry) Code, PK-12 must be E01, E02, E2A, E03, E3A, E04, E4A, E05, E09, E10, E11, E12, E13, R01, R02, R03 or R04 unless Survey Period Code is 3 or 5 and Term is Y, in which case the field should be Z-filled.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Entry (Re-entry) Code, PK-12 and resubmit the record.

### 13. Entry (Re-entry) Date validity by survey period
If Survey Period is 2 or 3, then Entry (Re-entry) Date must be numeric and must be a valid date that is greater than or equal to 07/01/**** and less than or equal to the last day of the survey period. If Survey Period Code is 3 or 5 and Term is Y, then the field should be zero filled. If Survey Period Code is 5, then the Entry (Reentry) Date must be numeric and must be a valid date in the range 7/01/**** to 8/31/****.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Entry (Re-entry) Dates and resubmit the records.

### 14. Prior School/Location: District/County must be active on Appendix C or 99 *(Updated 07/01/2026)*
Prior School/Location: District/County must be numeric and active (A) on the Appendix C: District Name Table or 99.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct Prior School/Location: District/County and resubmit the records.

### 15. Prior School/Location: State/Territory or Commonwealth validity
Prior School/Location: State/Territory or Commonwealth must be a valid code as listed in Appendix H or Appendix Q of the DOE Information Database Requirements Volume I -- Automated Student Information System Manual or ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Prior School/Location: State/Territory or Commonwealth code and resubmit the record.

### 16. Prior School/Location: Country validity
Prior School/Location: Country must be a valid code as listed in Appendix G of the DOE Information Database Requirements Volume I -- Automated Student Information System Manual other than ZZ, unless the Term is Y and Prior School/Location: State/Territory or Commonwealth is ZZ, then Country should be Z-filled.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Prior School/Location: Country codes and/or the Term code and resubmit the records.

### 17. Withdrawal Code, PK-12 validity *(Updated 06/19/2026)*
Withdrawal Code, PK-12 must be DNE, W01, W02, W3A, W3B, W3D, W3E, W3F, W04, W05, W06, W10, W12, W13, W15, W18, W21, W22, W23, W24, W25, W26, WCO, WD1, WEL, WFT, WGA, WGD, WGT, WHP, WMA, WME, WOC, WPC, WPP, WWE, WWT, WWW, WRW, WXL, WXT or WXW. It may also be ZZZ only for survey periods 2 and 3.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Withdrawal Code, PK-12 and resubmit the records.

### 18. Withdrawal Date validity by survey period
If Survey Period = 5, then the Withdrawal Date must be a valid date in the range of 07/01/**** to 08/31/****. If Survey Period = 2 or 3, then the Withdrawal Date must be a valid date and must be less than or equal to the last day of the survey period, or zero-filled if the Withdrawal Code is ZZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Withdrawal Dates and resubmit the records.

### 19. Days Present, Annual by survey period
Days Present, Annual must be zero-filled in Survey 2 and must be numeric for Surveys 3 and 5 unless Term is Y in which case it must be zero-filled.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct Days Present, Annual and resubmit the record.

### 1A. Item 4 filler must be all spaces
Item 4 - Filler on this format in position numbers 17-26 must be all spaces.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must fill the positions noted with all spaces and resubmit the record.

### 20. Days Absent, Annual by survey period
Days Absent, Annual must be zero-filled in Survey 2 and must be numeric in Surveys 3 and 5 unless Term is Y in which case it must be zero-filled.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct Days Absent, Annual and resubmit the record.

### 21. Days Present, Summer Terms by survey period
Days Present, Summer Terms must be zero-filled in surveys 2 and 3 and must be numeric for Survey 5 unless Term is Y in which case it must be zero-filled.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct Days Present, Summer Terms and resubmit the record.

### 22. Days Absent, Summer Terms by survey period
Days Absent, Summer Terms must be zero-filled in surveys 2 and 3 and must be numeric in survey 5 unless Term is Y in which case it must be zero-filled.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct Days Absent, Summer Terms and resubmit the record.

### 23. Withdrawal Date must not precede Entry (Re-entry) Date
For Survey 5, the Withdrawal Date must be greater than or equal to the Entry (Re-entry) Date. For Surveys 2 and 3, the Withdrawal Date must be greater than or equal to the Entry (Re-entry) Date or it must be zero-filled.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Entry (Re-entry) Date and/or the Withdrawal Date and resubmit the record.

### 24. Record uniqueness
Each Prior School Status/Student Attendance record must be unique based on the keys of District Number, Current Enrollment; School Number, Current Enrollment; Florida Education Identifier; Survey Period Code; School Year, and Entry (Re-entry) Date.
**Result:** First record accepted, all other duplicate records rejected

**District Responsibility:** If the records loaded to the database are correct, no action is necessary. However, if the district wishes the rejected records to be loaded to the database, the district must delete any invalid records, correct any rejected records if necessary and resubmit the corrected records.

### 25. School Number, Current Enrollment must be active or N999
School Number, Current Enrollment must exist on the Master School Identification File as a valid active school number for the District Number, Current Enrollment or it must be N999.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Enrollment and resubmit the records.

### 26. Entry Code E01 requires same district and FL/US for Prior School/Location
If the Entry Code is E01, then the Prior School/Location: District must be the same as the District Number, Current Enrollment, the Prior School/Location: State/Territory or Commonwealth must be FL, and the Prior School/Location: Country must be US.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must determine whether the Entry Code and/or the Prior School/Location: District, Prior School/Location: State, Territory or Commonwealth, or Prior School Location: Country is in error, correct it, and resubmit the record.

### 27. Entry Code E02/E2A Prior School/Location District/County requirements
If the Entry Code is E02, then the Prior School/Location: District/County must not be 99 and must not be the same as the District Number, Current Enrollment. If E2A, then the Prior School/Location: District/County must be 99.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must determine whether the Entry Code and/or the Prior School/Location: District/County, Prior School/Location: State/Territory or Commonwealth, or Prior School Location: Country is in error, correct it, and resubmit the record.

### 28. Prior School/Location District 99 with State ZZ cannot have Country US
If the Prior School/Location: District is 99 and the Prior School/Location: State/Territory or Commonwealth is ZZ, the Prior School/Location: Country may not be US and vice versa.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must determine whether the Prior School/Location: District/County, Prior School/Location: State/Territory or Commonwealth, or Prior School Location: Country is in error, correct it, and resubmit the record.

### 29. Re-entry Codes R01-R04 require same district for Prior School/Location *(Updated 02/06/2026)*
If the Entry (Re-Entry) Code is R01, R02, R03, or R04, the Prior School/Location: District must be the same as the District Number, Current Enrollment.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must determine whether the Re-entry Code and/or the Prior School/Location: District/County, Prior School/Location: State/Territory or Commonwealth, or Prior School/Location: Country is in error, correct it, and resubmit the record.

### 2A. Entry Code E03/E3A Prior School/Location District/County requirements
If the Entry Code is E03, then the Prior School/Location: District/County must not be 99. If E3A, then the Prior School/Location: District/County must be 99.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must determine whether the Entry (Re-Entry) Code and/or the Prior School/Location: District/County is in error, correct it, and resubmit the records.

### 2B. Entry Code E04/E4A Prior School/Location District/County requirements
If the Entry Code is E04, then the Prior School/Location: District/County must not be 99. If E4A, then the Prior School/Location: District/County must be 99.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must determine whether the Entry (Re-Entry) Code and/or the Prior School/Location: District/County is in error, correct it, and resubmit the records.

### 2C. Entry Code E09 requires State/Territory or Commonwealth ZZ
If the Entry Code is E09, then the Prior School/Location: State/Territory or Commonwealth must be ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Entry (Re-Entry) Code or the Prior School/Location: State/Territory or Commonwealth code and resubmit the record.

### 2D. Appendix Q territory codes require Country US
If Prior School/Location: State/Territory or Commonwealth is any code listed in Appendix Q, then Prior School/Location: Country code must be US.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Prior School/Location: Country or Prior School/Location: State/Territory or Commonwealth code and resubmit the record.

### 2E. Educational Choice A requires valid District Number, Zoned School
If Educational Choice code = A, then District Number, Zoned School must be 01-67. All other Educational Choice codes must be filled with zeroes.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct District Number, Zoned School and resubmit the record.

### 2F. Educational Choice A requires active School Number, Zoned School
If Educational Choice code = A, then School Number, Zoned School must be an active school for the District Number, Zoned School on the Master School Identification file. All other Educational Choice codes must be filled with zeros.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the error, District Number, Zoned School or School Number, Zoned School and resubmit the record.

### 2G. Educational Choice A requires both District and School Number Zoned School to be nonzero
If Educational Choice code = A, and School Number, Zoned School is greater than 0000, then District Number, Zoned School must be greater than 00. If the District Number, Zoned School is greater than 00, then School Number, Zoned School must be greater than 0000.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct District Number, Zoned School and resubmit the record.

### 30. Term validity by survey period
Term must be Z for survey 2, must be either 3 or Y for survey 3 and must be 3, S or Y for survey 5.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Term codes and resubmit the records.

### 31. Only one ZZZ Withdrawal Code allowed per student per survey
If Survey Period Code is 2 or 3, no more than one record with ZZZ as Withdrawal Code, PK-12 may be loaded to the database, based on School Year; Survey Period Code; District Number, Current Enrollment; FLEID.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Withdrawal Code PK-12 and resubmit the record.

### 32. Transaction Code validity and existence match
The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified then the record must not already exist on the database; if C or D is specified then the record must exist on the database. An original transaction is the first submission of a record during a survey period. After original transmission of records, changes to the record for elements other than the key elements must be done with a "C" as the Transaction Code. To delete a record, the Transaction Code must be a "D". To change key elements in a batch transaction, the record must FIRST be deleted with a "D" and then added with an "A".
**Result:** Record rejected

**District Responsibility:** If the rejected records should have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Transaction Code and resubmit the records.

### 33. Non-US Country requires Entry Code E09 and vice versa, except Term Y
If the Prior School/Location: Country is not US, then the Entry Code must be E09 and vice versa, unless Term is Y.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Entry Code or the Prior School/Location: Country code and resubmit the record.

### 34. Entry Codes E01-E05, E2A, E3A, E4A, E12, R01-R04 require Country US *(Updated 02/06/2026)*
If Entry (Re-Entry) Code equals E01 – E05, E2A, E3A, E4A, E12 or R01 – R04 then Prior School/Location: Country must be US.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must determine whether the Entry (Re-Entry) Code and/or the Prior School/Location: Country is in error, correct it, and resubmit the record.

### 35. Diploma/graduation Withdrawal Codes require Grade Level 9-12 *(Updated 06/19/2026)*
If Withdrawal Code, PK-12 is W06, W10, WCO, WEL, WFT, WRW, WWE, WWT, WWW, WGA, WGD, WGT, WME, WOC, WXL, WXT, WXW, WD1, or WPC; then Grade Level must be 9-12.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct either the Withdrawal Code, PK-12 or Grade Level and resubmit the record.

### 36. Educational Choice code validity *(Updated 07/01/2026)*
Educational Choice must be A, B, C, D, E, F, U or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Educational Choice code and resubmit the record.

### 37. Disaster Affected Student code validity
Disaster Affected Student code must be E, F, O, P, Q, R, V, W, X, Y or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Disaster Affected Student code and resubmit the record.

### 38. Active Appendix C District requires State FL *(Updated 07/01/2026)*
If the Prior School/Location: District/County is active (A) on the Appendix C: District Name Table, then the Prior School/Location: State/Territory or Commonwealth must be FL.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must determine which code (the Prior School/Location: District/County or Prior School/Location: State, Territory or Commonwealth) is in error, correct it, and resubmit the record.

### 39. Student Number Identifier, Local format
The Student Number Identifier, Local may be any combination of letters, numbers and blanks. (All blanks are allowable.) It must be left-justified with trailing blanks.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Student Number Identifier, Local and resubmit the record.

### 40. Florida Education Identifier format
Florida Education Identifier (FLEID) is alphanumeric and must be entered as "FL" in the first 2 positions followed by twelve numeric digits. No blanks, spaces or all zeros for the twelve numeric digits are allowable.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Florida Education Identifier and resubmit the record for processing.

### 41. Student Offender Transfer code validity
Student Offender Transfer must be Y or N.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Student Offender Transfer code and resubmit the record.

### 42. Prior School/Location District 99 cannot have State FL
If the Prior School/Location: District/County is 99, then the Prior School/Location: State/Territory or Commonwealth must not be FL.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must determine which code (the Prior School/Location: District/County or Prior School/Location: State, Territory or Commonwealth) is in error, correct it, and resubmit the record.

### 43. Days Absent, Annual—Unexcused Not Related to Discipline by survey period
Days Absent, Annual—Unexcused Not Related to Discipline must be zero-filled in survey 2 and must be numeric in surveys 3 and 5 unless Term is Y in which case it must be zero-filled.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct Days Absent, Annual—Unexcused Not Related to Discipline and resubmit the record.

### 44. Withdrawal Code DNE requires Term Y for Survey 3 or 5
If Survey Period Code is 3 or 5 and Withdrawal Code is DNE, then Term must be Y.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Term code or the Withdrawal Code and resubmit the record.

### 45. Educational Choice must be Z for specified District/School combinations
The Educational Choice code must be Z for: District Number, Current Enrollment 68, 71-75, or 80-83; School Number, Current Enrollment 3450, 3950, 7001, 7004, 7006, or 7023; School Number, Current Enrollment N998 (Home Education) or N999 (private school); or School Number with School Function Setting equal to V and Charter School Status not equal to Z on the MSID file.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Educational Choice code or the School Number, Current Enrollment and resubmit the record.

### 46. Grade Level PK prohibits Educational Choice C
If Grade Level = PK, Educational Choice must not be C.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Educational Choice code so that it is a code not equal to C and resubmit the record.

### 47. Withdrawal Code W05 requires age 16 or older
If Withdrawal Code, PK-12 = W05 then age must be 16 or greater as of the Withdrawal Date.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Withdrawal Code, PK-12; the Birth Date or the Withdrawal Date and resubmit the record.

### 48. Withdrawal Code W25 requires Grade Level PK or KG
If Withdrawal Code = W25 then Grade Level must be PK or KG.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct either the Withdrawal Code, PK-12 or Grade Level and resubmit the record.

### 49. Withdrawal Code W25 requires age under 6 as of February 1
If Withdrawal Code, PK-12 = W25 then age must be less than 6 years old as of February 1 of the current school year.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Withdrawal Code, PK-12; the Birth Date or the Withdrawal Date and resubmit the record.

### 4D. Prior School/Location State FL requires District not 99; non-FL requires District 99
If the Prior School/Location: State/Territory or Commonwealth is FL, then Prior School Location: District/County must not be 99. If the Prior School/Location: State/Territory or Commonwealth is not FL, then Prior School Location: District/County must be 99.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must determine which code (the Prior School/Location: District/County or Prior School/Location: State/Territory or Commonwealth) is in error, correct it, and resubmit the record.

### 4E. Districts 35/55 specific school combinations require Educational Choice B or Z
If District Number, Current Enrollment is 35 and School Number, Current Enrollment is 0531 or if District Number, Current Enrollment is 55 and School Number, Current Enrollment is 0231; then Educational Choice code must be B or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Educational Choice code and resubmit the record.

### 4F. Charter School enrollment prohibits Educational Choice A
If the School Number, Current Enrollment is a Charter School (Charter School Status on the Master School ID table is any code other than Z), then Educational Choice code must not be A.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Educational Choice code and resubmit the record.

### 4G. Days Present/Absent Summer and Annual relationship by Term
If Survey Period is 5 and Term is S, then Days Present, Summer Terms must be greater than zero and both Days Present, Annual and Days Absent, Annual must be zero. If Survey Period is 5 and Term is 3, then both Days Present, Summer and Days Absent, Summer must be zero.
**Result:** Record rejected

**District Responsibility:** The district should correct the Days Present, Summer Terms or the Term and resubmit the record.

### 4H. District Number, Current Instruction/Service must be active on Appendix C *(Updated 07/01/2026)*
District Number, Current Instruction/Service must be numeric and active (A) on the Appendix C: District Name Table.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the District Number, Current Instruction/Service and resubmit the records.

### 4I. Habitual Truant code validity by survey period
Habitual Truant code must be N, Y or Z. If Survey Period Code is 2 or 3, then Habitual Truant code must be Z. If Survey Period Code is 5, then Habitual Truant code must be N or Y.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Habitual Truant code and resubmit the record.

---

## State Validation

### 50. Matching Student Demographic record required for Survey 5
For Survey Period code 5, each Prior School Status/Student Attendance record must have a matching Student Demographic record based on both the District Number, Current Instruction/Service and District Number, Current Enrollment (Student Demographic) and District Number, Current Enrollment (Prior School Status); Florida Education Identifier; Survey Period Code and School Year.
**Result:** State validation

**District Responsibility:** The district must delete the Prior School Status/Student Attendance record or submit the matching Student Demographic record.

### 51. Withdrawal Code W21 requires Discipline/Resultant Action Code E
If the Withdrawal Code, PK-12 is W21 on the Prior School Status/Student Attendance record, then at least one Discipline/Resultant Action code on the Student Discipline/Resultant Action records must be E. The records should be matched on the following items: District Number, Current Enrollment; Florida Education Identifier; Survey Period Code; and School Year.
**Result:** State validation

**District Responsibility:** The district should verify the Withdrawal Code, PK-12 and the Discipline/Resultant Action Code and correct the code that is in error.

### 52. Re-entry Codes R01-R04 require matching prior entry record with Withdrawal Date *(Updated 02/06/2026)*
If the Entry (Re-Entry) Code, PK-12 is R01, R02, R03, or R04 then there must be a matching Prior School Status/Student Attendance record (based on District Number, Current Enrollment; Florida Education Identifier; Survey Period Code and School Year) with an Entry (Re-Entry) Code, PK-12 of E01-E05, E2A, E3A, E4A, or E09-E13 and a Withdrawal Date less than or equal to the Entry (Re-Entry) Date.
**Result:** State validation

**District Responsibility:** The district must review the Entry (Re-entry), PK-12 code and correct it if necessary or submit a matching record with an Entry (Re-entry) Code, PK-12 of E01-E05, E2A, E3A, E4A, or E09-E13 and a Withdrawal Date less than the Entry (Re-entry) Date on the current record.

---

## Exception Reports

### 71. Days Present, Annual should be in range 0-180 for Survey 3 and 5
For Survey Period Codes 3 and 5, Days Present, Annual must be in the range 0-180.
**Result:** Exception report

**District Responsibility:** The district should verify the Days Present, Annual and correct the record if in error. Otherwise, the district would take no action.

### 72. Days Absent, Annual should be in range 0-180 for Survey 3 and 5
For Survey Period Codes 3 and 5, Days Absent, Annual must be in the range 0-180.
**Result:** Exception report

**District Responsibility:** The district should verify the Days Absent, Annual and correct the record if in error. Otherwise, the district would take no action.

### 73. Days Present, Summer Terms should not exceed 45 for non-District-D schools
For Survey Period Code 5 if School Function/Setting on the MSID file for the School Number, Current Enrollment does not equal D, Days Present, Summer Terms must be in the range 0-45.
**Result:** Exception report

**District Responsibility:** The district should verify the Days Present, Summer Terms and correct the record if in error. Otherwise, the district would take no action.

### 74. Days Absent, Summer Terms should not exceed 45 for non-District-D schools
For Survey Period Code 5 if School Function/Setting on the MSID file for the School Number, Current Enrollment does not equal D, Days Absent, Summer Terms must be in the range 0-45.
**Result:** Exception report

**District Responsibility:** The district should verify the Days Absent, Summer Terms and correct the record if in error. Otherwise, the district would take no action.

### 75. Sum of Days Absent and Present, Annual should not exceed 180
For Survey Period Codes 3 and 5, the sum of Days Absent, Annual and Days Present, Annual must not be greater than 180.
**Result:** Exception report

**District Responsibility:** The district should verify Days Present, Annual and/or Days Absent, Annual and correct the record if in error. Otherwise, the district would take no action.

### 76. Sum of Days Absent and Present, Summer Terms should not exceed 45 for non-District-D schools
For Survey Period Code 5 if School Function/Setting for the School Number, Current Enrollment on the MSID file does not equal D, the sum of Days Absent, Summer Terms and Days Present, Summer Terms must not be greater than 45.
**Result:** Exception report

**District Responsibility:** The district should verify Days Present, Summer Terms and/or Days Absent, Summer Terms and correct the record if it is in error. Otherwise, the district would take no action.

### 77. Entry Code E05 should have Grade Level PK or KG
If Entry Code is E05, grade must be either PK or KG.
**Result:** Exception report

**District Responsibility:** The district should verify the Grade Level and correct the record if it is in error. Otherwise, the district would take no action.

### 78. Days Absent, Annual—Unexcused Not Related to Discipline should be in range 0-180
For Survey Period Code 5, Days Absent, Annual—Unexcused Not Related to Discipline must be in the range 0-180.
**Result:** Exception report

**District Responsibility:** The district should verify the Days Absent, Annual—Unexcused Not Related to Discipline and correct the record if in error. Otherwise, the district would take no action.

### 79. Withdrawal Codes W26 or WGT should require age 16 or older
If Withdrawal Code, PK-12 = W26 or WGT then age must be 16 or greater as of the Withdrawal Date.
**Result:** Exception report

**District Responsibility:** The district must review the record, determine whether all information is accurate and correct the record if necessary.

### 80. Withdrawal Code W02 should have matching R02 re-entry
If Survey Period = 2 or 3 and if the Withdrawal Code is W02, then there must be a matching Prior School Status/Student Attendance record (based on District Number, Current Enrollment; Florida Education Identifier; Survey Period Code and School Year) with an Entry (Re-Entry) Code, PK-12 of R02 and an Entry/Re-entry Date greater than or equal to the Withdrawal Date.
**Result:** Exception report

**District Responsibility:** The district must review the Withdrawal Code and Entry (Re-entry) Code, PK-12 and correct the code(s) that is in error.

### 81. Sum of Days Absent and Present, Summer Terms should not exceed 70 for District-D schools
For Survey Period Code 5 if School Function/Setting on the MSID file for the School Number, Current Enrollment equals D, the sum of Days Absent, Summer Terms and Days Present, Summer Terms must not be greater than 70.
**Result:** Exception report

**District Responsibility:** The district should review the number of days present and number of days absent for accuracy. If the information in the record is correct, no action is necessary. If the information is not correct, the district should correct the Days Present, Summer Terms or Days Absent, Summer Terms or both and submit the record as a batch update.

### 82. Withdrawal Code W21 in Survey 5 should match Student End of Year Status W21
If Survey is 5 and if the Withdrawal Code, PK-12 is W21 on the Prior School Status/Student Attendance record, then the Withdrawal Reason must be W21 on the Student End of Year Status record. The records should be matched on the following items: District Number, Current Enrollment; Florida Education Identifier; Survey Period Code; and School Year.
**Result:** Exception report

**District Responsibility:** The district should verify the Withdrawal Code, PK-12 and the Withdrawal Reason Code, and, correct one of the codes if there is an error.

---

## Aggregate Exception Reports

### 90. Every active school must have at least one Prior School Status record
For Survey Period Codes 2, 3, and 5, for each active school on the Master School Identification (MSID) file for the district, unless it is school 9001 (Superintendent's Office), there must be at least one Prior School Status/Student Attendance record.
**Result:** Aggregate exception edit

**District Responsibility:** The district must verify whether or not Prior School Status/Student Attendance records should be sent for this school and submit these records if necessary.

### 91. Days Absent, Annual must be greater than zero per school for Survey 3 and 5
For Survey Period Codes 3 and 5, for each school on the Prior School Status/Student Attendance table, the number of Days Absent, Annual must be > 0 (Refer to aggregate report F70624).
**Result:** Aggregate exception edit

**District Responsibility:** The district must verify Days Absent, Annual and Days Present, Annual on the Prior School Status/Student Attendance records for this school and correct these fields if in error.

### 92. Days Present percentage should be at least 90 percent for Survey 5
For Survey Period Code 5, for each school on the Prior School Status/Student Attendance table, the percentage of Days Present, Annual (calculated as: Days Present, Annual / sum of Days Present, Annual + Days Absent, Annual × 100) must be equal to or >= 90.
**Result:** Aggregate exception report

**District Responsibility:** The district should verify Days Present, Annual and Days Absent, Annual on the Prior School Status/Student Attendance records for this school and correct these fields if they are in error.

### 93. Days Present, Summer Term percentage should be at least 95 percent for Survey 5
For Survey Period Code 5, for each school on the Prior School Status/Student Attendance table for which Days Present, Summer Term is greater than 0, the percentage of Days Present, Summer Term (calculated as: Days Present, Summer Term / sum of Days Present, Summer Term + Days Absent, Summer Term × 100) must be equal to or greater than 95.
**Result:** Aggregate exception report

**District Responsibility:** The district should verify Days Present, Summer Term and Days Absent, Summer Term on the Prior School Status/Student Attendance records for this school and correct them if they are in error.
