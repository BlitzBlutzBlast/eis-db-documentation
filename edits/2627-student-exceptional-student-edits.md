# Exceptional Student — Edits and Reject Rules

Source: https://www.fldoe.org/file/20909/2627exst.pdf
Manual: Student Database 2026-2027

This document covers 41 edits across four categories: Reject Rules (record rejected), State Validation (cross-format matching, including one State Validation/NULL edit), Exception Reports (advisory, does not reject), and an Aggregate Exception Report (school-level count). Edit numbering is non-sequential; Reject Rules run 1-2, 4-24, 26, 28-29, and 2A-2M, State Validation runs 30-35, 38-39, and 3A-3D, Exception Reports run 41-44, and the Aggregate Exception Report is 80.

---

## Reject Rules

### 1. District Number, Current Enrollment must match submitting district
District Number, Current Enrollment must be numeric and active (A) on the Appendix C: District Name Table and must be correct for the district submitting the data.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct District Number, Current Enrollment and resubmit the record.

### 2. School Number, Current Enrollment range
If Survey Period Code is 1-4 or 5, School Number, Current Enrollment must be numeric in the range 0001 to 9899, excluding 9001 and 7006, or it must be N998 or N999.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct School Number, Current Enrollment and resubmit the records.

### 4. Survey Period Code must be 1-5
Survey Period Code must be 1, 2, 3, 4 or 5 and must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** The district must correct the Survey Period Code either on the records coming in or the transmission JCL, and all records should be resubmitted.

### 5. Year correct for submission
Year must be correct for the submission specified by the district. For Survey Periods 1-4, Year is Fiscal Year. For Survey Period 5, Year is School Year.
**Result:** Record rejected

**District Responsibility:** The district must correct the Year either on the JCL or the records being submitted and resubmit all records for processing.

### 6. Transaction Code validity and existence match
The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified the record must not already exist on the database; if C or D is specified then the record must exist on the database. An original transaction is the first submission of a record during a survey period. After the original transmission of records, changes to the record for elements other than the key elements must be done with a "C" as the Transaction Code. To delete a record, the Transaction Code must be a "D". To change key elements in a batch transaction, the record must FIRST be deleted with a "D" and then added with an "A".
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Transaction Code and resubmit the records.

### 7. Record uniqueness
Each Exceptional Student record must be unique based on the keys of District Number, Current Enrollment; Florida Education Identifier; Survey Period Code; and Year.
**Result:** First record accepted, all other duplicate records rejected

**District Responsibility:** If the records accepted and loaded to the database are the correct ones no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must delete any invalid records, correct any rejected records if necessary, and resubmit the corrected records.

### 8. Exceptionality, Other code validity
Exceptionality, Other must be C-M, O, P, S-Y, or Z. Nine possible codes may be selected. If less than nine codes are selected, Z-fill the remaining fields.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Exceptionality, Other code and resubmit the records.

### 9. Exceptional Student Plan Date validity by exceptionality and survey period
If Survey Period Code = 1, 2, 3 or 4, and if Exceptionality, Primary is not L, then the Exceptional Student Plan Date must be a valid date within the current or previous fiscal year. If Survey Period Code = 1, 2, 3 or 4, and if Exceptionality, Primary is L, then the Exceptional Student Plan Date must be a valid date within the current or four previous fiscal years. If Survey Period Code = 5, Exceptional Student Plan Date may either be zeroes or a valid date.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct Exceptional Student Plan Date and resubmit the records.

### 10. Exceptionality, Primary code validity
Exceptionality, Primary must be C, F-M, O-P, S-W, or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Exceptionality, Primary code and resubmit the records.

### 11. Time, Total School Week validity for Survey 2
If Survey Period Code = 2, Time, Total School Week must be numeric and must be greater than zero unless Exceptionality, Primary code is L and Exceptionality, Other is Z-filled, in which case Time, Total School Week may be zero. If survey does not equal 2, then Time, Total School Week must be 0000.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Time, Total School Week and resubmit the records.

### 12. Time With Non-Disabled Peers validity for Survey 2
If Survey Period Code = 2 and there is a code other than L in either Exceptionality, Primary or Exceptionality, Other; then Time With Non-Disabled Peers must be numeric and must be greater than or equal to zero. If Survey Period Code is not 2 or if Exceptionality, Primary code is L and Exceptionality, Other is Z-filled; then Time With Non-Disabled Peers must be 0000.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Time With Non-Disabled Peers value and resubmit the record.

### 13. Student Number Identifier, Local format
The Student Number Identifier, Local may be any combination of letters, numbers and blanks. (All blanks are allowable.) It must be left-justified with trailing blanks.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Student Number Identifier, Local and resubmit the record.

### 14. Exceptionality, Other must be fully Z-filled if first character is Z
If the first character in the field for Exceptionality, Other is a Z, then all codes for the remaining eight fields must be Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Exceptionality, Other code and resubmit the record.

### 15. Time With Non-Disabled Peers must not exceed Time, Total School Week
If Survey Period Code = 2, Time With Non-Disabled Peers must be less than or equal to Time, Total School Week.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must determine if the Time With Non-Disabled Peers or the Time, Total School Week is in error, correct the record, then resubmit it.

### 16. Exceptionality, Other may not repeat Exceptionality, Primary
If Exceptionality, Primary is not Z; then Exceptionality, Other codes may not include the Exceptionality, Primary code.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must determine which exceptionality code is in error, correct the record, then resubmit it.

### 17. Exceptionality, Other codes must be left-justified
If any Exceptionality, Other codes C-M, O, P or S-Y are reported, the codes must be left-justified and the remaining fields Z-filled.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Exceptionality, Other codes and resubmit the records.

### 18. IDEA Educational Environments code validity for Survey 2
For Survey Period Code = 2, Exceptional Student, IDEA Educational Environments must be A, B, C, D, F, H, J, K, L, M, P, S, or Z. For all other surveys this code must be Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Exceptional Student, IDEA Educational Environments code and resubmit the record.

### 19. IDEA Educational Environments must be Z for Exceptionality L with no Other codes
If the Exceptionality, Primary code = L, and the Exceptionality, Other code is Z-filled, then the Exceptional Student, IDEA Educational Environments code must be Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Exceptional Student, IDEA Educational Environments code and resubmit the record.

### 20. School Number, Current Enrollment must be active except reserved codes
If School Number, Current Enrollment is not N998 or N999, then the School Number, Current Enrollment must exist on the Master School Identification File as a valid active school number in the district of enrollment.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct School Number, Current Enrollment and resubmit the record.

### 21. Dismissal Date validity
If Survey Period Code is 1-4 or 5, Exceptional Student, Dismissal Date must be numeric and must be a valid date or zeroes.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Exceptional Student, Dismissal Date and resubmit the record.

### 22. Alternate Assessment Administered code validity
If Survey Period Code = 2 or 3, Alternate Assessment Administered must be D, P or Z. For all other Survey Periods the Alternate Assessment Administered code must be Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Alternate Assessment Administered code and resubmit the record.

### 23. Alternate Assessment Administered must be Z for Exceptionality L with no Other codes
For Survey Period Code = 2 or 3, if the Exceptionality, Primary code = L, and the Exceptionality, Other code is Z-filled, then the Alternate Assessment Administered code must be Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Alternate Assessment Administered code and resubmit the record.

### 24. Item 3 filler must be all spaces
Item 3 - Filler on this format in position numbers 7-16 must be all spaces.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must fill the positions noted with all spaces and resubmit the record.

### 26. Gifted Eligibility code validity
If Survey Period Code is 1-5 then Gifted Eligibility code must be A, B, or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Gifted Eligibility code and resubmit the record.

### 28. Gifted Eligibility A/B requires Exceptionality L
If Gifted Eligibility = A or B; then Exceptionality, Primary or Exceptionality, Other must = L.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Gifted Eligibility code; the Exceptionality, Primary; or the Exceptionality, Other code and resubmit the record.

### 29. IDEA Educational Environments must be Z when Exceptionality is U
If the Exceptionality, Primary code or the Exceptionality, Other code equals U, then the Exceptional Student, IDEA Educational Environments code must be Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Exceptional Student, IDEA Educational Environments code or the Exceptionality, Primary code and resubmit the record.

### 2A. Exceptionality, Other must be unique other than Z
Exceptionality, Other must be unique other than Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Exceptionality, Other codes and resubmit the records.

### 2B. Exceptional Student Placement Date validity by survey period and placement status
For Survey Periods 2 and 3, if School Number, Current Enrollment is not N999, then Exceptional Student Placement Date must be a valid numeric date and less than or equal to the survey date. For Survey Period 4, if School Number, Current Enrollment is not N999, then Exceptional Student Placement Date must be a valid numeric date and less than or equal to June 30 of the current school year. For Survey 5, if Exceptional Student Placement Status = P or T and School Number, Current Enrollment is not N999, then Exceptional Student Placement Date must be a valid numeric date less than August 31 following the 180 day school year. For Survey 5, if Exceptional Student Placement Status = R, E, I, or N, Exceptional Student Placement Date must be zero-filled. If School Number, Current Enrollment is N999 or if Survey = 1 then the Exceptional Student Placement Date must either follow the rules above or it must be zero-filled.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Exceptional Student Placement Date and resubmit the records.

### 2C. Exceptional Student Eligibility Determination Date validity
Exceptional Student Eligibility Determination Date must be numeric and either a valid date or all zeros. If Exceptional Student Placement Status = T, then Exceptional Student Eligibility Determination Date must be a valid date that is less than or equal to the survey date or it must be zero-filled (for Survey 5, use August 31 to represent the survey date). If Survey Period is 1 and Exceptional Student Placement Status = P, then Exceptional Student Eligibility Determination Date must be less than or equal to the survey date or zero-filled. If Survey Period is 2, 3 or 4 and Exceptional Student Placement Status = P, then Exceptional Student Eligibility Determination Date must be less than or equal to the survey date. If Survey Period = 5 and if Exceptional Student Placement Status = R or E then the Exceptional Student Eligibility Determination Date must be zero-filled. If Survey Period = 5 and if Exceptional Student Placement Status = I, N or P, then the Exceptional Student Eligibility Determination Date must be a valid date less than or equal to August 31.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Exceptional Student Eligibility Determination Date and resubmit the records.

### 2D. Exceptional Student Placement Status code validity by survey period
If Survey Period Code is 1, 2, 3 or 4, then Exceptional Student Placement Status must be P or T. In Survey Period 5, Exceptional Student Placement Status must be R, E, P, I, N, or T.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Exceptional Student Placement Status and resubmit the record.

### 2E. Exceptionality, Primary must be Z for specified Survey 5 Placement Statuses
If Survey Period is 5 and if Exceptional Student Placement Status is R, E, I or N, then Exceptionality, Primary must be Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct Exceptionality, Primary and resubmit the record.

### 2F. Evaluation Completion Date validity by placement status and survey period
Evaluation Completion Date must be numeric. If Exceptional Student Placement Status = E, P, I or N and Survey Period does not equal 1, then Evaluation Completion Date must be a valid date and less than or equal to the survey date (for survey periods 2, 3 and 4) or less than August 31 following the 180 day school year (for survey period 5). If Exceptional Student Placement Status = E, P, I or N and Survey Period is 1, then Evaluation Completion Date must be a valid date and less than or equal to the survey date or it must be zero-filled. If Exceptional Student Placement Status = R, then Evaluation Completion Date must be zero-filled. If Exceptional Student Placement Status = T, then Evaluation Completion Date must be zero-filled or a valid date that is less than or equal to the survey date (for survey periods 1, 2, 3 and 4) or less than August 31 following the 180 day school year (for survey period 5).
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct Evaluation Completion Date and resubmit the record.

### 2G. Evaluation Consent Date validity
Evaluation Consent Date must be a valid date and less than August 31 at the start of the next school year or it must be zero filled.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Evaluation Consent Date and resubmit the record.

### 2H. Exceptional Student Referral Reason code validity by survey period
If Survey Period Code is 5, Exceptional Student Referral Reason must be D, G, M or Z. If Survey Period Code is 1, 2, 3 or 4, Exceptional Student Referral Reason must be Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct Exceptional Student Referral Reason and resubmit the record.

### 2I. 60-Day Exception/Extension code validity
Exceptional Student, 60-Day Exception/Extension must be N, P, T or Y.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct Exceptional Student, 60-Day Exception/Extension and resubmit the records.

### 2J. Placement Status required when Exceptionality Primary is Z during Survey 5
If Exceptionality, Primary is Z and Survey Period is 5, then Exceptional Student Placement Status must be R, E, I or N.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Exceptionality, Primary or the Exceptional Student Placement Status and resubmit the record.

### 2K. Florida Education Identifier format
Florida Education Identifier (FLEID) is alphanumeric and must be entered as "FL" in the first 2 positions followed by twelve numeric digits. No blanks, spaces or all zeros for the twelve numeric digits are allowable.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Florida Education Identifier and resubmit the record for processing.

### 2L. Exceptionality, Primary must not be Z for Survey Periods 1-4
If Survey Period is 1, 2, 3, or 4, then Exceptionality, Primary must not be Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct Exceptionality, Primary and resubmit the record.

### 2M. Exceptionality, Other must be fully Z when Primary is Z
If Exceptionality, Primary equals Z then Exceptionality, Other cannot contain anything other than Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must determine which exceptionality code is in error, correct the record, then resubmit it.

---

## State Validation

### 30. Matching Student Demographic record required
For Survey Periods 1 - 4, each Exceptional Student record must have a matching Student Demographic record based on District Number, Current Enrollment; School Number, Current Enrollment; Florida Education Identifier; Survey Period Code and Year. For Survey Period 5, each Exceptional Student record must have a matching Student Demographic record based on District Number, Current Enrollment; Florida Education Identifier; Survey Period Code and Year.
**Result:** State validation

**District Responsibility:** The district must delete the Exceptional Student record or add a Student Demographic record to match the key fields on the Exceptional Student record.

### 31. IDEA Educational Environments code for age 3-5, Grade PK
For Survey Period Code = 2, if the student is age 3-5 and if Grade Level = PK and if Exceptionality, Primary or Exceptionality, Other contains a code other than L or Z, then the Exceptional Student, IDEA Educational Environments code must be A, B, J, K, L, M or S. If Survey Period Code is 2 and if the student is age 3-5 and if Grade Level = PK and if Exceptionality, Primary equals L and Exceptionality, Other is all Z's, then Exceptional Student, IDEA Educational Environments code must be Z. Age is determined using the student's Birth Date on the Student Demographic Information record and the Friday of Survey Week.
**Result:** State validation

**District Responsibility:** The district must review both records and correct the record that is in error so that the appropriate relationship exists between Exceptional Student, IDEA Educational Environments code and Birth Date.

### 32. IDEA Educational Environments code for age 5 non-PK or age 6-21
For Survey Period Code = 2, if the student is age 5 and Grade Level is not equal to PK or is age 6-21 then the Exceptional Student, IDEA Educational Environments code must be C, D, F, H, P or Z.
**Result:** State validation

**District Responsibility:** The district must correct the record so that the appropriate relationship exists between Exceptional Student, IDEA Educational Environments and Birth Date.

### 33. IDEA Educational Environments must be Z for age 0-2
For Survey Period Code = 2, if the student is age 0-2, the Exceptional Student, IDEA Educational Environments code must be Z.
**Result:** State validation

**District Responsibility:** The district must correct the record so that the appropriate relationship exists between Exceptional Student, IDEA Educational Environments and Birth Date.

### 34. Exceptionality L not allowed for Grade PK
If Grade Level = PK on the Student Demographic Information format, then neither Exceptionality, Primary nor Exceptionality, Other may equal L.
**Result:** State validation

**District Responsibility:** The district must correct the records so that the appropriate relationship exists between Exceptionality, Primary or Exceptionality, Other and Grade Level.

### 35. Exceptionality restrictions for specified IDEA Educational Environments codes
If the Exceptional Student, IDEA Educational Environments code equals C, D, F, H, or P then the Exceptionality, Primary code and the Exceptionality, Other codes must not equal U, or must not equal T unless the student's age is less than ten as of the first day of the survey week and the Grade Level is KG, 1, or 2.
**Result:** State validation

**District Responsibility:** The district must correct the records so that the appropriate relationship exists between Exceptionality, Primary or Exceptionality, Other and Exceptional Student, IDEA Educational Environments.

### 38. Exceptionality U requires age under three unless extended FTE
If Survey Period Code = 1-4 and if either Exceptionality, Primary is U or Exceptionality, Other is U, age must be less than three as of the first day of survey week; unless Year-Round/Extended School Year FTE Indicator = A or B.
**Result:** State validation/NULL

**District Responsibility:** The district must correct the Birth Date or Exceptionality, Primary so that the proper relationship exists. If the FTE, Earned has been nulled, the district must also correct the FTE, Earned amount.

### 39. Exceptionality T requires age under ten unless extended FTE *(Updated 07/01/2026)*
If Survey Period Code = 1-4 and if either Exceptionality, Primary is T or Exceptionality, Other is T, age must be less than ten (10) as of the last day of survey week; unless Year-Round/Extended School Year FTE Indicator = A or B.
**Result:** State validation

**District Responsibility:** The district must correct the Birth Date or Exceptionality, Primary so that the proper relationship exists. If FTE, Earned has been nulled, the district must also correct the FTE, Earned amount.

### 3A. Placement Date must postdate Birth Date
If Exceptional Student Placement Date is not zeros, then Exceptional Student Placement Date must be greater than Birth Date on the Student Demographic Information record. For Survey Periods 1 - 4, the records should be matched to the Student Demographic Information record based on District Number, Current Enrollment; School Number, Current Enrollment; Florida Education Identifier; Survey Period Code and Year. For Survey Period 5, the records should be matched to the Student Demographic Information record based on District Number, Current Enrollment; Florida Education Identifier; Survey Period Code and Year.
**Result:** State validation

**District Responsibility:** The district must correct either the Exceptional Student Placement Date or the Birth Date so that the proper relationship exists.

### 3B. Eligibility Determination Date must postdate Birth Date
If Exceptional Student Placement Status = P and if Exceptional Student Eligibility Determination Date is not zero-filled, Exceptional Student Eligibility Determination Date must be greater than Birth Date. For Survey Periods 1 - 4, the records should be matched to the Student Demographic Information record based on District Number, Current Enrollment; School Number, Current Enrollment; Florida Education Identifier; Survey Period Code and Year. For Survey Period 5, the records should be matched to the Student Demographic Information record based on District Number, Current Enrollment; Florida Education Identifier; Survey Period Code and Year.
**Result:** State validation

**District Responsibility:** The district must correct either the Exceptional Student Eligibility Determination Date or the Birth Date and resubmit the record.

### 3C. Evaluation Completion Date must postdate Birth Date
If Exceptional Student Placement Status = P and Evaluation Completion Date is not zero-filled, then Evaluation Completion Date must be greater than Birth Date. For Survey Periods 1 - 4, the records should be matched to the Student Demographic Information record based on District Number, Current Enrollment; School Number, Current Enrollment; Florida Education Identifier; Survey Period Code and Year. For Survey Period 5, the records should be matched to the Student Demographic Information record based on District Number, Current Enrollment; Florida Education Identifier; Survey Period Code and Year.
**Result:** State validation

**District Responsibility:** The district must correct either the Evaluation Completion Date or the Birth Date so that the proper relationship exists.

### 3D. Access Course required for specified exceptionalities
If Survey Period Code = 2 or 3, and Exceptionality, Primary does not equal L or Z, or if Exceptionality, Primary = L and Exceptionality, Other is not L, D, E, U, X, Y or Z, and Alternate Assessment Administered is not Z, then at least one Course Number on the Student Course Schedule must be one of the Access Courses on Reference File - F71538. The match between the Exceptional Student record and the Student Course Schedule record should be based on District Number, Current Enrollment, Florida Education Identifier (FLEID), Survey Period Code and Fiscal Year.
**Result:** State validation

**District Responsibility:** The district must review both records and correct the record that is in error so that the appropriate relationship exists.

---

## Exception Reports

### 41. Placement Date must not precede Eligibility Determination Date
If Exceptional Student Placement Date is not zeros then Exceptional Student Placement Date must be greater than or equal to Exceptional Student Eligibility Determination Date.
**Result:** Exception report

**District Responsibility:** The district should verify the Exceptional Student Placement Date and the Exceptional Student Eligibility Determination Date and correct if in error.

### 42. Evaluation Completion Date should not follow Eligibility Determination Date
If Exceptional Student Placement Status = P, Evaluation Completion Date must be prior to (less than) or equal to Exceptional Student Eligibility Determination Date.
**Result:** Exception report

**District Responsibility:** The district should verify the Evaluation Completion Date and the Exceptional Student Eligibility Determination Date and correct if in error.

### 43. Evaluation Consent Date should not follow Evaluation Completion Date
If Exceptional Student Placement Status = P and Evaluation Consent Date is not zero-filled, then Evaluation Consent Date must be prior to (less than) or equal to Evaluation Completion Date.
**Result:** Exception report

**District Responsibility:** The district should verify the Evaluation Consent Date and the Evaluation Completion Date and correct if in error.

### 44. Dismissal Date should fall within expected range
If Exceptional Student, Dismissal Date is a valid date, then it must be in the range 07/01/**** to 08/16/****.
**Result:** Exception report

**District Responsibility:** The district should verify the Exceptional Student, Dismissal Date and correct the record if in error.

---

## Aggregate Exception Reports

### 80. At least one Placement Status "I" record expected per school in Survey 5
For Survey Period 5, for each school that submits an Exceptional Student, there must be at least one student record with Exceptional Student Placement Status equal to code "I". An error message will be printed on the exception report for schools that do not meet this aggregate exception edit.
**Result:** Aggregate exception report

**District Responsibility:** The district must verify whether or not the records should include the Exceptional Student Placement Status code of "I" and submit corrected records as necessary.
