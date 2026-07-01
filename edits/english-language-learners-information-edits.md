# English Language Learners Information — Edits and Reject Rules

Source: [FLDOE Student Database — English Language Learners Information Edits](https://origin.fldoe.org/file/20909/2627ell.pdf)
Manual: Student Database 2026-2027

This document covers edits across three categories: Reject Rules (record rejected), State Validation (cross-format matching), and Exception Reports (advisory, does not reject). Edit numbering is non-sequential and includes alphanumeric IDs (1A, 2C, 2H, 2I, 2J, 2K, 2L, 2M, 2O). Two edits are numbered 62 and two are numbered 93 in the source document — these duplications are preserved as published.

---

## Reject Rules

### 1. District Number, Current Instruction/Service must be active and match submitter *(Updated 07/01/2026)*
District Number, Current Instruction/Service must be numeric and active (A) on the Appendix C: District Name Table and must be correct for the district submitting the data.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the District Number, Current Instruction/Service and resubmit the records.

### 2. School Number, Current Enrollment range
If Survey Period Code is 2, 3 or 5, School Number, Current Enrollment must be numeric in the range 0001 to 9899 (excluding 9001 and 7006), N998 or N999.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Enrollment and resubmit the records.

### 4. Survey Period Code must be 2, 3 or 5
Survey Period Code must be 2, 3 or 5, and must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the Survey Period Code should be corrected either on the records coming in or the transmission JCL and all records should be resubmitted.

### 5. School Year must match submission
School Year must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Year either on the records coming in or the transmission JCL and resubmit all records.

### 6. English Language Learners: Entry Date validity
If Survey Period Code is 2 or 3, English Language Learners: Entry Date must be numeric and a valid date less than or equal to the survey date unless zero filled. If Survey Period Code is 5, English Language Learners: Entry Date must be numeric and a valid date less than or equal to June 30th unless zero filled.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the English Language Learners: Entry Date and resubmit the records.

### 7. English Language Learners: Basis of Entry must be valid code
If Survey Period Code is 2, 3 or 5, English Language Learners: Basis of Entry code must be A, R, L, or T.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the English Language Learners: Basis of Entry and resubmit the record.

### 8. Student Plan Date must be valid date or zeros
Student Plan Date must be a valid date or zeros.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the English Language Learners: Student Plan Date and resubmit the records.

### 9. English Language Learners: Classification Date validity
If Survey Period is 2 or 3, English Language Learners Classification Date must be numeric and a valid date less than or equal to the survey date unless zero filled. If Survey Period is 5, English Language Learners Classification Date must be numeric and a valid date less than or equal to June 30th unless zero filled.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the English Language Learners: Classification Date and resubmit the records.

### 10. English Language Learners: Exit Date validity
If Survey Period Code is 2 or 3, English Language Learners: Exit Date must be numeric and a valid date less than or equal to the survey date, unless zero-filled. If Survey Period Code is 5, English Language Learners: Exit Date must be numeric and a valid date less than or equal to June 30th unless zero filled.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the ELL: Exit Date and resubmit the record.

### 11. English Language Learners: Reevaluation Date validity
If Survey Period Code is 2 or 3, English Language Learners: Reevaluation Date must be numeric and a valid date less than or equal to the survey date unless zero filled. If Survey Period Code is 5, English Language Learners: Reevaluation Date must be numeric and a valid date less than or equal to June 30th unless zero filled.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the District Number, Current Instruction/Service and resubmit the records.

### 12. English Language Learners: Extension of Instruction must be Y or Z
If Survey Period Code is 2, 3 or 5, English Language Learners: Extension of Instruction must be Y or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the English Language Learners: Extension of Instruction and resubmit the record.

### 13. English Language Learners: Reclassification Date validity
If Survey Period Code is 2 or 3, The English Language Learners: Reclassification Date must be numeric and a valid date less than or equal to the survey date unless zero filled. If Survey Period Code is 5, English Language Learners: Reclassification Date must be numeric and a valid date less than or equal to June 30th unless zero filled.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the English Language Learners: Reclassification Date and resubmit the records.

### 14. Test Date Listening validity
If Survey Period is 2 or 3, Test Date Listening must be numeric and a valid date, less than or equal to the survey date, unless zero filled. If Survey Period is 5, Test Date Listening must be numeric and a valid date less than or equal to June 30th, unless zero-filled.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Date and resubmit the record.

### 15. English Language Learners: Basis of Exit (First) must be valid code
If Survey Period Code is 2, 3 or 5, English Language Learners: Basis of Exit (First) code must be H, I, J, L or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the English Language Learners: Basis of Exit (First) and resubmit the record.

### 16. Fund Source code must be E or Z
Fund Source code must be E or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Fund Source and resubmit the record.

### 17. Filler positions 7-16 must be all spaces
Item 3 - Filler on this format in position numbers 7-16 must be all spaces.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must fill the positions noted with all spaces and resubmit the record.

### 18. Student Plan Date must be on or after Entry Date
The English Language Learners: Student Plan Date must be greater than or equal to the English Language Learners: Entry Date.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the English Language Learners: Student Plan Date and resubmit the record.

### 19. English Language Learners: Program Participation must be valid code
English Language Learners: Program Participation code must be E, H, L, N or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the English Language Learners: Program Participation code and resubmit the record.

### 1A. English Language Learners: Tier Placement must be valid code per survey period
If Survey Period Code is 2, English Language Learners: Tier Placement code must be A, B, C, D, O or Z. If Survey Period Code is 3 or 5, then English Language Learners: Tier Placement code must be Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the English Language Learners: Tier Placement code and resubmit the record.

### 20. Reclassification Date must be on or after Exit Date
If there is a valid English Language Learners: Reclassification Date, then the English Language Learners: Reclassification Date must be greater than or equal to a valid English Language Learners: Exit Date.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the English Language Learners: Reclassification Date and resubmit the record.

### 21. Record uniqueness
Each English Language Learners Student Information record must be unique based on the keys of District Number, Current Instruction/Service; Florida Education Identifier; Survey Period Code; and School Year.
**Result:** First record accepted, all duplicate records rejected

**District Responsibility:** If the records loaded to the database are correct, no action is necessary. However, if the district wishes the rejected records to be loaded to the database, the district must delete any invalid records, correct any rejected records if necessary, and resubmit the corrected records.

### 22. Test Name Listening must be valid when Entry Date is present
If English Language Learners: Entry Date is a valid date, then Test Name Listening must be a valid test on the Test Name Table in Appendix I with an indicator code of L (Listening) or Test Name Listening may be ZZZ. If District Number, Current Enrollment is 68, then Test Name Listening may be X__.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Name and resubmit the record.

### 23. Test Subject Content Listening must be valid code
The Test Subject Content Listening must be a valid code specified in Appendix L of the DOE Information Database Requirements Volume I-Automated Student Information System manual, or it may be ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Subject Content code and resubmit the records.

### 24. Transaction Code validity
The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified then the record must not already exist on the database; if C or D is specified then the record must exist on the database.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Transaction Code and resubmit the records.

### 25. School Number, Current Enrollment must be active on Master School ID File
The School Number, Current Enrollment must exist on the Master School Identification File as a valid active school in the district of enrollment, unless School Number, Current Enrollment is equal to N998 or N999.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Enrollment and resubmit the records.

### 26. Test Name Listening required when Test Date Listening is a valid date
If the Test Date Listening is a valid date, then the Test Name Listening must be a valid code other than ZZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Name and resubmit the record.

### 27. Test Score Type Listening must be valid code
Test Score Type Listening must be RS, SS, NP, AL or ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Score and resubmit the record.

### 28. Test Score Listening must be numeric and right-justified with leading zeros
Test Score Listening must be numeric and right justified with leading zeros.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Score and resubmit the records.

### 29. All Listening test fields must be zero/ZZZ/ZZ when Test Date Listening is zero
If Test Date Listening is equal to zero, then Test Name Listening must be ZZZ, the Test Score Type Listening must be ZZ, the Test Subject Content Listening must be ZZ, and the Test Score Listening must be zero.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the appropriate fields and resubmit the records.

### 2C. Exit Date must be greater than 0 when Basis of Exit (First) is not Z
If Survey Period Code is 2, 3 or 5 and if English Language Learners: Basis of Exit (First) is not Z, then English Language Learners: Exit Date must be greater than 0.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the English Language Learners: Exit Date or the English Language Learners: Basis of Exit (First) and resubmit the record.

### 2H. Test Name Listening and Speaking required when Basis of Entry is A and Exit Date is zero
If English Language Learners: Basis of Entry is code A and if English Language Learners: Exit Date is 00000000 then the Test Name: Listening and Test Name: Speaking must be other than ZZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Name information of the ELL, Basis of Entry and resubmit the record.

### 2I. Test Name Reading and Writing required when Basis of Entry is R and Exit Date is zero
If English Language Learners: Basis of Entry is code R and if English Language Learners: Exit Date is 00000000 then the Test Name: Reading and Test Name: Writing must be other than ZZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Name or the ELL: Basis of Entry code and resubmit the record.

### 2J. Test Form must not be blank for Surveys 2, 3 or 5
If Survey Period Code is 2, 3 or 5, then Test Form must not be blank.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Form and resubmit the record.

### 2K. Test Level must not be blank for surveys other than 2, 3 or 5
If Survey Period Code is not 2, 3 or 5, then Test Level must not be blank.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Level and resubmit the record.

### 2L. Exit Date must be after April 6, 2012 for Basis of Exit codes H, I or J
If Survey Period Code is 2, 3 or 5 and if either English Language Learners: Basis of Exit (First) or English Language Learners: Basis of Exit (Second) is code H, I or J, then English Language Learners: Exit Date must be after April 6, 2012.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the English Language Learners: Exit Date or the English Language Learners: Basis of Exit (First) and resubmit the record.

### 2M. District Number, Current Enrollment must be active on Appendix C *(Updated 07/01/2026)*
District Number, Current Enrollment must be numeric and active (A) on the Appendix C: District Name Table.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number, Current Enrollment and resubmit the record.

### 2O. Florida Education Identifier (FLEID) format
Florida Education Identifier (FLEID) is alphanumeric and must be entered as "FL" in the first 2 positions followed by twelve numeric digits. No blanks, spaces or all zeros for the twelve numeric digits are allowable.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Florida Education Identifier and resubmit the records for processing.

### 30. Test Score Type Listening must be valid non-ZZ code when Test Date Listening is present
If Test Date Listening is greater than zero, then Test Score Type Listening must be a valid code other than ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Score Type and resubmit the records.

### 31. Test Subject Content Listening must be valid non-ZZ code when Test Date Listening is present
If Test Date Listening is greater than zero, then Test Subject Content Listening must be a valid code other than ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Subject Content and resubmit the records.

### 32. Test Date Speaking validity
If Survey Period is 2 or 3 Test Date Speaking must be numeric and a valid date, less than or equal to the survey date, unless zero filled. If Survey Period is 5, Test Date Speaking must be numeric and a valid date, less than or equal to June 30th, unless zero filled.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Date and resubmit the record.

### 33. Test Name Speaking must be valid when Entry Date is present
If English Language Learners: Entry Date is a valid date, then Test Name Speaking must be a valid test on the Test Name Table in Appendix I with an indicator code of S (Speaking) or Test Name Speaking may be ZZZ. If District Number, Current Enrollment is 68, then Test Name Speaking may be X__.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Name and resubmit the record.

### 34. Test Score Type Speaking must be valid code
Test Score Type Speaking must be RS, SS, NP, AL or ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Score Type and resubmit the record.

### 35. Test Subject Content Speaking must be valid code
The Test Subject Content Speaking must be a valid code specified in Appendix L of the DOE Information Database Requirements: Volume I--Automated Student Information System manual or it may be ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Subject Content code and resubmit the records.

### 36. Test Score Speaking must be numeric and right-justified with leading zeros
Test Score Speaking must be numeric and right justified with leading zeros.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Score and resubmit the records.

### 37. All Speaking test fields must be zero/ZZZ/ZZ when Test Date Speaking is zero
If Test Date Speaking is equal to zero, then Test Name Speaking must be ZZZ, the Test Score Type Speaking must be ZZ, the Test Subject Content Speaking must be ZZ, and the Test Score Speaking must be zero.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the appropriate fields and resubmit the records.

### 38. Test Name Speaking required when Test Date Speaking is a valid date
If the Test Date Speaking is a valid date, then the Test Name Speaking must be a valid code other than ZZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Name and resubmit the record.

### 39. Test Score Type Speaking must be valid non-ZZ code when Test Date Speaking is present
If Test Date Speaking is greater than zero, then Test Score Type Speaking must be a valid code other than ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Score Type and resubmit the records.

### 40. Test Subject Content Speaking must be valid non-ZZ code when Test Date Speaking is present
If Test Date Speaking is greater than zero, then Test Subject Content Speaking must be a valid code other than ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Subject Content and resubmit the records.

### 41. Test Date Reading validity
If Survey Period is 2 or 3, Test Date Reading must be numeric and a valid date less than or equal to the survey date, unless zero filled. If Survey Period is 5, Test Date Reading must be numeric and a valid date, less than or equal to June 30th, unless zero filled.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Date and resubmit the record.

### 42. Test Name Reading must be valid when Entry Date is present
If English Language Learners: Entry Date is a valid date, then Test Name Reading must be an approved test listed on the Test Name Table in Appendix I with an indicator code of R (Reading) or Test Name Reading may be ZZZ. If District Number, Current Enrollment is 68, then Test Name Reading may be X__.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Name and resubmit the record.

### 43. Test Score Type Reading must be valid code
Test Score Type Reading must be RS, SS, NP, AL or ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Score Type and resubmit the record.

### 44. Test Subject Content Reading must be valid code
The Test Subject Content Reading must be a valid code specified in Appendix L of the DOE Information Database Requirements: Volume I-Automated Student Information System manual or it may be ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Date and resubmit the records.

### 45. Test Score Reading must be numeric and right-justified with leading zeros
Test Score Reading must be numeric and right justified with leading zeros.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Score and resubmit the records.

### 46. All Reading test fields must be zero/ZZZ/ZZ when Test Date Reading is zero
If Test Date Reading is equal to zero, then Test Name Reading must be ZZZ, the Test Score Type Reading must be ZZ, the Test Subject Content Reading must be ZZ, and the Test Score Reading must be zero.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Score Type and resubmit the records.

### 47. Test Name Reading required when Test Date Reading is a valid date
If the Test Date Reading is a valid date, then the Test Name Reading must be a valid code other than ZZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Name and resubmit the record.

### 48. Test Score Type Reading must be valid non-ZZ code when Test Date Reading is present
If Test Date Reading is greater than zero, then Test Score Type Reading must be a valid code other than ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Score Type and resubmit the records.

### 49. Test Subject Content Reading must be valid non-ZZ code when Test Date Reading is present
If Test Date Reading is greater than zero, then Test Subject Content Reading must be a valid code other than ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Subject Content and resubmit the records.

### 50. Test Date Writing validity
If Survey Period is 2 or 3, Test Date Writing must be numeric and a valid date, less than or equal to the survey date, unless zero filled. If Survey Period is 5, Test Date Writing must be numeric and a valid date less than or equal to June 30th, unless zero filled.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Date and resubmit the record.

### 51. Test Name Writing must be valid when Entry Date is present
If English Language Learners: Entry Date is a valid date, then Test Name Writing must be an approved test listed on the Test Name Table in Appendix I with an indicator code of W (Writing) or Test Name Writing may be ZZZ. If District Number is 68, then Test Name Writing may be X__.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Name and resubmit the record.

### 52. Test Score Type Writing must be valid code
Test Score Type Writing must be RS, SS, NP, AL or ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Score Type and resubmit the record.

### 53. Test Subject Content Writing must be valid code
The Test Subject Content Writing must be a valid code specified in Appendix L of the DOE Information Database Requirements: Volume I-Automated Student Information System manual or it may be ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Subject Content code and resubmit the records.

### 54. Test Score Writing must be numeric and right-justified with leading zeros
Test Score Writing must be numeric and right justified with leading zeros.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Score and resubmit the records.

### 55. All Writing test fields must be zero/ZZZ/ZZ when Test Date Writing is zero
If Test Date Writing is equal to zero, then Test Name Writing must be ZZZ, the Test Score Type Writing must be ZZ, the Test Subject Content Writing must be ZZ, and the Test Score Writing must be zero.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the appropriate fields and resubmit the records.

### 56. Test Name Writing required when Test Date Writing is a valid date
If the Test Date Writing is a valid date, then the Test Name Writing must be other than ZZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Name and resubmit the record.

### 57. Test Score Type Writing must be valid non-ZZ code when Test Date Writing is present
If Test Date Writing is greater than zero, then Test Score Type Writing must be a valid code other than ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Score Type and resubmit the records.

### 58. Test Subject Content Writing must be valid non-ZZ code when Test Date Writing is present
If Test Date Writing is greater than zero, then Test Subject Content Writing must be a valid code other than ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Subject Content and resubmit the records.

### 59. Student Number Identifier, Local format
The Student Number Identifier, Local may be any combination of letters, numbers and blanks. (All blanks are allowable.) It must be left-justified with trailing blanks.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Student Number Identifier, Local and resubmit the record.

### 62. English Language Learners: Reclassification Exit Date must be valid date <!-- Note: duplicate edit number 62 in source -->
If Survey Period Code is 2, 3 or 5, then English Language Learners: Reclassification Exit Date must be numeric and a valid date, unless zero-filled.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the ELL: Reclassification Exit Date and resubmit the record.

### 63. Reclassification Exit Date must be on or after Reclassification Date
If the English Language Learners: Reclassification Exit Date is greater than zero, then the English Language Learners: Reclassification Exit Date must be equal to or greater than the English Language Learners: Reclassification Date.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the English Language Learners: Reclassification Exit Date and resubmit the record.

### 64. English Language Learners: Basis of Exit (Second) must be L or Z
If Survey Period Code is 2, 3 or 5, English Language Learners: Basis of Exit (Second) code must be L or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the English Language Learners: Basis of Exit (Second) and resubmit the record.

### 65. Basis of Exit (First) must not be Z when Basis of Exit (Second) is not Z
If Survey Period Code is 2, 3 or 5 and English Language Learners: Basis of Exit (Second) code is not Z, then English Language Learners: Basis of Exit (First) code must not be Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the English Language Learners: Basis of Exit (First) or the English Language Learners: Basis of Exit (Second) and resubmit the record.

---

## State Validation

### 75. Matching Student Demographic record required with ELL code LY, LP or LF
Each English Language Learners Student Information record must have a matching Student Demographic record based on District Number, Current Instruction/Service (Student Demographic) and District Number, Current Instruction/Service (English Language Learners Student Information); Florida Education Identifier; Survey Period Code and School Year and with the English Language Learners code = LY, LP or LF.
**Result:** State validation

**District Responsibility:** The district must delete the English Language Learners Student Information record or add a Student Demographic record to match the above key fields.

### 76. ELL code must be LF when Exit Date is present, unless Reclassification Date is present
If the English Language Learners: Exit Date is greater than zero, then the English Language Learners code must be LF, unless the English Language Learners: Reclassification Date is greater than zero.
**Result:** State validation

**District Responsibility:** The district must correct the English Language Learners: Exit Dates and/or the English Language Learners codes so that the valid relationship exists between the elements.

### 77. ELL PK-12 code must be LP or LY when both Basis of Exit codes are Z
If Survey Period Code is 2, 3 or 5; and if the English Language Learners: Basis of Exit (First) code is Z; and if the English Language Learners: Basis of Exit (Second) code is Z, then the English Language Learners, PK-12 code (on the Student Demographic Information record) must be LP or LY. The records should be matched on the following elements: District Number, Current Instruction/Service (Student Demographic) and District Number, Current Instruction/Service (English Language Learners Student Information); Florida Education Identifier; Survey Period Code and School Year.
**Result:** State validation

**District Responsibility:** The district must correct the English Language Learners, PK-12 code and/or the English Language Learners: Basis of Exit code so that a valid relationship exists between the elements.

### 79. ELL code must be LF when Reclassification Exit Date is present
If the English Language Learners: Reclassification Exit Date is a valid date, then the English Language Learners code must be LF.
**Result:** State validation

**District Responsibility:** The district must correct the English Language Learners: Reclassification Exit Dates and/or the English Language Learners codes so that the valid relationship exists between the elements.

### 80. Tier Placement must be A, B, C, D or O for LY students in grades 1-12 in Survey 2
If Survey Period Code = 2 and if English Language Learners, PK-12 on the Student Demographic Information record is LY and Grade Level = 1-12, then English Language Learners: Tier Placement code must be A, B, C, D or O. The match between the two records should be done by matching the District Number, Current Instruction/Service (Student Demographic Information) and District Number, Current Instruction/Service (English Language Learners Information); Florida Education Identifier; Survey Period Code and School Year.
**Result:** State validation

**District Responsibility:** The district must correct the English Language Learners: Tier Placement code, the English Language Learners, PK-12 code or Grade Level so that a valid relationship exists among the elements.

### 82. Classification Date must be on or after Home Language Survey Date
English Language Learners: Classification Date must be greater than or equal to the English Language Learners: Home Language Survey Date, unless the ELL: Classification Date is zero filled.
**Result:** State validation

**District Responsibility:** The district must correct the ELL: Classification Date and/or the ELL: Home Language Date so that a valid relationship exists between these elements.

### 83. Entry Date cannot be zero when ELL PK-12 code is LY or LF
If English Language Learners, PK-12 on the Student Demographic Information record is LY or LF, then English Language Learners: Entry Date cannot be zero. The match between the two records should be done by matching the District Number, Current Instruction/Service (Student Demographic) and District Number, Current Instruction/Service (English Language Learners Student Information); Florida Education Identifier; Survey Period Code and School Year.
**Result:** State validation

**District Responsibility:** The district must correct the English Language Learners: Entry Dates and/or the English Language Learners, PK-12 codes so that a valid relationship exists between the elements.

### 85. Grade Level must be K-12 on matching Student Demographic record
If there is a matching Student Demographic record, then the Grade Level must be K-12. The records should be matched using the District Number, Current Instruction/Service (Student Demographic) and District Number, Current Instruction/Service (English Language Learners Student Information); Florida Education Identifier; Survey Period Code and School Year.
**Result:** State validation

**District Responsibility:** The district must delete the English Language Learners Student Information record or change the Grade Level on the matching Student Demographic record.

### 86. At least one Test Name must be non-ZZZ for LY students with Basis of Entry A, R or T
If Survey Period Code is 2, 3 or 5 and if English Language Learners, PK-12 code is LY and if the English Language Learners: Basis of Entry code is A, R or T, then at least one of the following must be other than ZZZ: Test Name: Listening; Test Name: Reading; Test Name: Writing; or Test Name: Speaking.
**Result:** State validation

**District Responsibility:** The district must correct the English Language Learners: PK-12 code and/or an English Language Learners: Basis of Entry code or submit the appropriate Test Name so that a valid relationship exists between the elements.

---

## Exception Reports

### 91. Entry Date must be within six years of Survey Date for non-LF students
If English Language Learners, PK-12 on the Student Demographic Information record is not code LF and if English Language Learners: Entry Date is not zero, then it must be within six years of the Survey Date for Survey Period Codes 2 or 3 or August 31 of the start of the next school year for Survey Period Code 5. The match between the two records should be done using the District Number, Current Instruction/Service (Student Demographic) and District Number, Current Instruction/Service (English Language Learners Student Information); Florida Education Identifier; Survey Period Code and School Year.
**Result:** Exception report

**District Responsibility:** The district should verify the English Language Learners: Entry Date on the English Language Learners Information format and the English Language Learners, PK-12 code on the Student Demographic Information format and correct the date or code if it is in error.

### 92. Exit Date must be within two years of Survey Date <!-- Note: labeled "Exception rules" in source -->
If Survey Period is 2 or 3, English Language Learners: Exit Date must be greater than or equal to two years prior to the Survey Date*, unless zero filled or unless English Language Learners: Reclassification Date is greater than zero. If Survey Period is 5, English Language Learners: Exit Date must be greater than or equal to two years prior to August 15th of the year in which the survey 5 data are due to the Department, unless zero filled or unless English Language Learners Reclassification Date is greater than zero.

*Note: The Survey Date is the date of the Friday during Survey Week for the Survey Period reported.

Purpose: The purpose of this edit is to ensure that LF code in the English Language Learners, PK-12 data element is changed to LA after two years.
**Result:** Exception report

**District Responsibility:** The district should verify the English Language Learners: Exit Date and correct the date if it is in error.

### 93. Reclassification Exit Date must be within two years of Survey Date <!-- Note: duplicate edit number 93 in source -->
If Survey Period is 2 or 3, English Language Learners: Reclassification Exit Date must be greater than or equal to two years prior to the Survey Date*, unless zero filled. If Survey Period is 5, the English Language Learners Reclassification Exit Date must be greater than or equal to two years prior to August 15th of the year in which the survey 5 data is due to the Department, unless zero filled.

*Note: The Survey Date is the date of the Friday during Survey Week for the Survey Period reported.

Purpose: The purpose of this edit is to ensure that an LF code in the English Language Learners, PK-12 data element is changed to LA after two years.
**Result:** Exception report

**District Responsibility:** The district should verify the English Language Learners: Reclassification Exit Date and correct it if it is in error.

### 94. FEFP Program Number 130 restriction for LY students past six-year entry date threshold
If Survey Period is 2 or 3 and English Language Learners, PK-12 code on the Student Demographic Information record = LY, and if Survey Date is greater than the English Language Learners: Entry Date on the English Language Learners Information record in excess of six years, then FEFP Program Number on the Student Course Schedule record must not be 130. Match the Student Demographic record to the Student Course Schedule record based on District Number, Current Instruction/Service; Florida Education Identifier; Survey Period Code and Year.
**Result:** Exception report

**District Responsibility:** The district must correct the FEFP Program Number for the English Language Learners student based on the English Language Learners: Entry Date because the maximum of six years of funding has been met based on the data reported.
