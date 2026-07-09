# English Language Learners Information — Edits and Reject Rules

Source: https://www.fldoe.org/file/20909/2627ell.pdf
Manual: Student Database 2026-2027

This document covers 74 edits across three categories: Reject Rules (record rejected), State Validation (cross-format matching), and Exception Reports (advisory, does not reject). Edit numbering is non-sequential; Reject Rules run 1-2, 4-49, 1A, 2C, 2H-2M, 2O, 59, 62-65 (with a duplicate 62), State Validation runs 75-77, 79-80, 82-83, 85-86, Exception Reports run 91-94 (with a duplicate 93).

---

## Reject Rules

### 1. District Number, Current Instruction/Service must match submitting district *(Updated 07/01/2026)*
District Number, Current Instruction/Service must be numeric and active (A) on the Appendix C: District Name Table and must be correct for the district submitting the data.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the District Number, Current Instruction/Service and resubmit the records.

### 2. School Number, Current Enrollment range for Survey Periods 2, 3, 5
If Survey Period Code is 2, 3 or 5, School Number, Current Enrollment must be numeric in the range 0001 to 9899 (excluding 9001 and 7006), N998 or N999.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Enrollment and resubmit the records.

### 4. Survey Period Code must be 2, 3 or 5
Survey Period Code must be 2, 3 or 5, and must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the Survey Period Code should be corrected either on the records coming in or the transmission JCL and all records should be resubmitted.

### 5. School Year correct for submission
School Year must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Year either on the records coming in or the transmission JCL and resubmit all records.

### 6. ELL Entry Date validity by survey period
If Survey Period Code is 2 or 3, English Language Learners: Entry Date must be numeric and a valid date less than or equal to the survey date unless zero filled. If Survey Period Code is 5, English Language Learners: Entry Date must be numeric and a valid date less than or equal to June 30th unless zero filled.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the English Language Learners: Entry Date and resubmit the records.

### 7. ELL Basis of Entry code validity
If Survey Period Code is 2, 3 or 5, English Language Learners: Basis of Entry code must be A, R, L, or T.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the English Language Learners: Basis of Entry and resubmit the record.

### 8. Student Plan Date must be a valid date or zeros
Student Plan Date must be a valid date or zeros.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the English Language Learners: Student Plan Date and resubmit the records.

### 9. ELL Classification Date validity by survey period
If Survey Period is 2 or 3, English Language Learners Classification Date must be numeric and a valid date less than or equal to the survey date unless zero filled. If Survey Period is 5, English Language Learners Classification Date must be numeric and a valid date less than or equal to June 30th unless zero filled.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the English Language Learners: Classification Date and resubmit the records.

### 10. ELL Exit Date validity by survey period
If Survey Period Code is 2 or 3, English Language Learners: Exit Date must be numeric and a valid date less than or equal to the survey date, unless zero-filled. If Survey Period Code is 5, English Language Learners: Exit Date must be numeric and a valid date less than or equal to June 30th unless zero filled.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the ELL: Exit Date and resubmit the record.

### 11. ELL Reevaluation Date validity by survey period
If Survey Period Code is 2 or 3, English Language Learners: Reevaluation Date must be numeric and a valid date less than or equal to the survey date unless zero filled. If Survey Period Code is 5, English Language Learners: Reevaluation Date must be numeric and a valid date less than or equal to June 30th unless zero filled.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the District Number, Current Instruction/Service and resubmit the records.

### 12. ELL Extension of Instruction code validity
If Survey Period Code is 2, 3 or 5, English Language Learners: Extension of Instruction must be Y or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the English Language Learners: Extension of Instruction and resubmit the record.

### 13. ELL Reclassification Date validity by survey period
If Survey Period Code is 2 or 3, the English Language Learners: Reclassification Date must be numeric and a valid date less than or equal to the survey date unless zero filled. If Survey Period Code is 5, English Language Learners: Reclassification Date must be numeric and a valid date less than or equal to June 30th unless zero filled.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the English Language Learners: Reclassification Date and resubmit the records.

### 14. Test Date Listening validity by survey period
If Survey Period is 2 or 3, Test Date Listening must be numeric and a valid date, less than or equal to the survey date, unless zero filled. If Survey Period is 5, Test Date Listening must be numeric and a valid date less than or equal to June 30th, unless zero-filled.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Date and resubmit the record.

### 15. ELL Basis of Exit (First) code validity
If Survey Period Code is 2, 3 or 5, English Language Learners: Basis of Exit (First) code must be H, I, J, L or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the English Language Learners: Basis of Exit (First) and resubmit the record.

### 16. Fund Source code validity
Fund Source code must be E or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Fund Source and resubmit the record.

### 17. Item 3 filler must be all spaces
Item 3 - Filler on this format in position numbers 7-16 must be all spaces.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must fill the positions noted with all spaces and resubmit the record.

### 18. Student Plan Date must not precede Entry Date
The English Language Learners: Student Plan Date must be greater than or equal to the English Language Learners: Entry Date.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the English Language Learners: Student Plan Date and resubmit the record.

### 19. ELL Program Participation code validity
English Language Learners: Program Participation code must be E, H, L, N or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the English Language Learners: Program Participation code and resubmit the record.

### 1A. ELL Tier Placement code validity by survey period
If Survey Period Code is 2, English Language Learners: Tier Placement code must be A, B, C, D, O or Z. If Survey Period Code is 3 or 5, then English Language Learners: Tier Placement code must be Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the English Language Learners: Tier Placement code and resubmit the record.

### 20. Reclassification Date must not precede Exit Date
If there is a valid English Language Learners: Reclassification Date, then the English Language Learners: Reclassification Date must be greater than or equal to a valid English Language Learners: Exit Date.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the English Language Learners: Reclassification Date and resubmit the record.

### 21. Record uniqueness
Each English Language Learners Student Information record must be unique based on the keys of District Number, Current Instruction/Service; Florida Education Identifier; Survey Period Code; and School Year.
**Result:** First record accepted, all duplicate records rejected

**District Responsibility:** If the records loaded to the database are correct, no action is necessary. However, if the district wishes the rejected records to be loaded to the database, the district must delete any invalid records, correct any rejected records if necessary, and resubmit the corrected records.

### 22. Test Name Listening validity when Entry Date valid
If English Language Learners: Entry Date is a valid date, then Test Name Listening must be a valid test on the Test Name Table in Appendix I with an indicator code of L (Listening) or Test Name Listening may be ZZZ. If District Number, Current Enrollment is 68, then Test Name Listening may be X__.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Name and resubmit the record.

### 23. Test Subject Content Listening validity
The Test Subject Content Listening must be a valid code specified in Appendix L of the DOE Information Database Requirements Volume I-Automated Student Information System manual, or it may be ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must the correct the Test Subject Content code and resubmit the records.

### 24. Transaction Code validity and existence match
The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified then the record must not already exist on the database; if C or D is specified then the record must exist on the database. An original transaction is the first submission of a record during a survey period. After original transmission of records, changes to the record for elements other than the key elements must be done with a "C" as the Transaction Code. To delete a record, the Transaction Code must be a "D". To change key elements in a batch transaction, the record must FIRST be deleted with a "D" and then added with an "A".
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Transaction Code and resubmit the records.

### 25. School Number, Current Enrollment must be active except reserved codes
The School Number, Current Enrollment must exist on the Master School Identification File as a valid active school in the district of enrollment, unless School Number, Current Enrollment is equal to N998 or N999.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Enrollment and resubmit the records.

### 26. Test Name Listening required when Test Date valid
If the Test Date Listening is a valid date, then the Test Name Listening must be a valid code other than ZZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Name and resubmit the record.

### 27. Test Score Type Listening validity
Test Score Type Listening must be RS, SS, NP, AL or ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Score and resubmit the record.

### 28. Test Score Listening format
Test Score Listening must be numeric and right justified with leading zeros.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Score and resubmit the records.

### 29. Listening test fields must be zero-filled when Test Date is zero
If Test Date Listening is equal to zero, then Test Name Listening must be ZZZ, the Test Score Type Listening must be ZZ, the Test Subject Content Listening must be ZZ, and the Test Score Listening must be zero.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the appropriate fields and resubmit the records.

### 2C. Exit Date required when Basis of Exit (First) not Z
If Survey Period Code is 2, 3 or 5 and if English Language Learners: Basis of Exit (First) is not Z, then English Language Learners: Exit Date must be greater than 0.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the English Language Learners: Exit Date or the English Language Learners: Basis of Exit (First) and resubmit the record.

### 2H. Listening/Speaking Test Names required for Basis of Entry A with open Exit Date
If English Language Learners: Basis of Entry is code A and If English Language Learners: Exit Date is 00000000 then the Test Name: Listening and Test Name: Speaking must be other than ZZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Name information of the ELL, Basis of Entry an resubmit the record.

### 2I. Reading/Writing Test Names required for Basis of Entry R with open Exit Date
If English Language Learners: Basis of Entry is code R and If English Language Learners: Exit Date is 00000000 then the Test Name: Reading and Test Name: Writing must be other than ZZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Name or the ELL: Basis of Entry code and resubmit the record.

### 2J. Test Form must not be blank
If Survey Period Code is 2, 3 or 5, then Test Form must not be blank.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Form and resubmit the record.

### 2K. Test Level must not be blank
If Survey Period Code is not 2, 3 or 5, then Test Level must not be blank.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Level and resubmit the record.

### 2L. Exit Date must postdate April 6, 2012 for Basis of Exit H/I/J
If Survey Period Code is 2, 3 or 5 and if either English Language Learners: Basis of Exit (First) or English Language Learners: Basis of Exit (Second) is code H, I or J, then English Language Learners: Exit Date must be after April 6, 2012.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the English Language Learners: Exit Date or the English Language Learners: Basis of Exit (First) and resubmit the record.

### 2M. District Number, Current Enrollment must be active on Appendix C *(Updated 07/01/2026)*
District Number, Current Enrollment must be numeric and active (A) on the Appendix C: District Name Table.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number, Current Enrollment and resubmit the record.

### 2O. Florida Education Identifier format
Florida Education Identifier (FLEID) is alphanumeric and must be entered as "FL" in the first 2 positions followed by twelve numeric digits. No blanks, spaces or all zeros for the twelve numeric digits are allowable.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Florida Education Identifier and resubmit the records for processing.

### 30. Test Score Type Listening required when Test Date greater than zero
If Test Date Listening is greater than zero, then Test Score Type Listening must be a valid code other than ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Score Type and resubmit the records.

### 31. Test Subject Content Listening required when Test Date greater than zero
If Test Date Listening is greater than zero, then Test Subject Content Listening must be a valid code other than ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Subject Content and resubmit the records.

### 32. Test Date Speaking validity by survey period
If Survey Period is 2 or 3 Test Date Speaking must be numeric and a valid date, less than or equal to the survey date, unless zero filled. If Survey Period is 5, Test Date Speaking must be numeric and a valid date, less than or equal to June 30th, unless zero filled.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Date and resubmit the record.

### 33. Test Name Speaking validity when Entry Date valid
If English Language Learners: Entry Date is a valid date, then Test Name Speaking must be a valid test on the Test Name Table in Appendix I with an indicator code of S (Speaking) or Test Name Speaking may be ZZZ. If District Number, Current Enrollment is 68, then Test Name Speaking may be X__.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Name and resubmit the record.

### 34. Test Score Type Speaking validity
Test Score Type Speaking must be RS, SS, NP, AL or ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Score Type and resubmit the record.

### 35. Test Subject Content Speaking validity
The Test Subject Content Speaking must be a valid code specified in Appendix L of the DOE Information Database Requirements: Volume I--Automated Student Information System manual or it may be ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Subject Content code and resubmit the records.

### 36. Test Score Speaking format
Test Score Speaking must be numeric and right justified with leading zeros.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Score and resubmit the records.

### 37. Speaking test fields must be zero-filled when Test Date is zero
If Test Date Speaking is equal to zero, then Test Name Speaking must be ZZZ, the Test Score Type Speaking must be ZZ, the Test Subject Content Speaking must be ZZ, and the Test Score Speaking must be zero.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the appropriate fields and resubmit the records.

### 38. Test Name Speaking required when Test Date valid
If the Test Date Speaking is a valid date, then the Test Name Speaking must be a valid code other than ZZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Name and resubmit the record.

### 39. Test Score Type Speaking required when Test Date greater than zero
If Test Date Speaking is greater than zero, then Test Score Type Speaking must be a valid code other than ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Score Type and resubmit the records.

### 40. Test Subject Content Speaking required when Test Date greater than zero
If Test Date Speaking is greater than zero, then Test Subject Content Speaking must be a valid code other than ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Subject Content and resubmit the records.

### 41. Test Date Reading validity by survey period
If Survey Period is 2 or 3, Test Date Reading must be numeric and a valid date less than or equal to the survey date, unless zero filled. If Survey Period is 5, Test Date Reading must be numeric and a valid date, less than or equal to June 30th, unless zero filled.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Date and resubmit the record.

### 42. Test Name Reading validity when Entry Date valid
If English Language Learners: Entry Date is a valid date, then Test Name Reading must be an approved test listed on the Test Name Table in Appendix I with an indicator code of R (Reading) or Test Name Reading may be ZZZ. If District Number, Current Enrollment is 68, then Test Name Reading may be X__.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Name and resubmit the record.

### 43. Test Score Type Reading validity
Test Score Type Reading must be RS, SS, NP, AL or ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Score Type and resubmit the record.

### 44. Test Subject Content Reading validity
The Test Subject Content Reading must be a valid code specified in Appendix L of the DOE Information Database Requirements: Volume I-Automated Student Information System manual or it may be ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Date and resubmit the records.

### 45. Test Score Reading format
Test Score Reading must be numeric and right justified with leading zeros.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Score and resubmit the records.

### 46. Reading test fields must be zero-filled when Test Date is zero
If Test Date Reading is equal to zero, then Test Name Reading must be ZZZ, the Test Score Type Reading must be ZZ, the Test Subject Content Reading must be ZZ, and the Test Score Reading must be zero.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Score Type and resubmit the records.

### 47. Test Name Reading required when Test Date valid
If the Test Date Reading is a valid date, then the Test Name Reading must be a valid code other than ZZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Name and resubmit the record.

### 48. Test Score Type Reading required when Test Date greater than zero
If Test Date Reading is greater than zero, then Test Score Type Reading must be a valid code other than ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Score Type and resubmit the records.

### 49. Test Subject Content Reading required when Test Date greater than zero
If Test Date Reading is greater than zero, then Test Subject Content Reading must be a valid code other than ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Subject Content and resubmit the records.

### 50. Test Date Writing validity by survey period
If Survey Period is 2 or 3, Test Date Writing must be numeric and a valid date, less than or equal to the survey date, unless zero filled. If Survey Period is 5, Test Date Writing must be numeric and a valid date less than or equal to June 30th, unless zero filled.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Date and resubmit the record.

### 51. Test Name Writing validity when Entry Date valid
If English Language Learners: Entry Date is a valid date, then Test Name Writing must be an approved test listed on the Test Name Table in Appendix I with an indicator code of W (Writing) or Test Name Writing may be ZZZ. If District Number is 68, then Test Name Writing may be X__.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Name and resubmit the record.

### 52. Test Score Type Writing validity
Test Score Type Writing must be RS, SS, NP, AL or ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Score Type and resubmit the record.

### 53. Test Subject Content Writing validity
The Test Subject Content Writing must be a valid code specified in Appendix L of the DOE Information Database Requirements: Volume I-Automated Student Information System manual or it may be ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Subject Content code and resubmit the records.

### 54. Test Score Writing format
Test Score Writing must be numeric and right justified with leading zeros.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Score and resubmit the records.

### 55. Writing test fields must be zero-filled when Test Date is zero
If Test Date Writing is equal to zero, then Test Name Writing must be ZZZ, the Test Score Type Writing must be ZZ, the Test Subject Content Writing must be ZZ, and the Test Score Writing must be zero.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the appropriate fields and resubmit the records.

### 56. Test Name Writing required when Test Date valid
If the Test Date Writing is a valid date, then the Test Name Writing must be other than ZZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Test Name and resubmit the record.

### 57. Test Score Type Writing required when Test Date greater than zero
If Test Date Writing is greater than zero, then Test Score Type Writing must be a valid code other than ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Score Type and resubmit the records.

### 58. Test Subject Content Writing required when Test Date greater than zero
If Test Date Writing is greater than zero, then Test Subject Content Writing must be a valid code other than ZZ.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Test Subject Content and resubmit the records.

### 59. Student Number Identifier, Local format
The Student Number Identifier, Local may be any combination of letters, numbers and blanks. (All blanks are allowable.) It must be left-justified with trailing blanks.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Student Number Identifier, Local and resubmit the record.

### 62. ELL Reclassification Exit Date validity *(duplicate edit number in source)*
If Survey Period Code is 2, 3 or 5, then English Language Learners: Reclassification Exit Date must be numeric and a valid date, unless zero-filled.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the ELL: Reclassification Exit Date and resubmit the record.

<!-- Note: duplicate edit number in source -->
### 62. ELL Reclassification Exit Date validity (duplicate)
If Survey Period Code is 2, 3 or 5, then English Language Learners: Reclassification Exit Date must be numeric and a valid date, unless zero-filled.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the ELL: Reclassification Exit Date and resubmit the record.

### 63. Reclassification Exit Date must not precede Reclassification Date
If the English Language Learners: Reclassification Exit Date is greater than zero, then the English Language Learners: Reclassification Exit Date must be equal to or greater than the English Language Learners: Reclassification Date.
**Result:** Record rejected (result type not explicitly labeled in source; treated as reject rule per surrounding context)

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the English Language Learners: Reclassification Exit Date and resubmit the record.

### 64. ELL Basis of Exit (Second) code validity
If Survey Period Code is 2, 3 or 5, English Language Learners: Basis of Exit (Second) code must be L or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the English Language Learners: Basis of Exit (Second) and resubmit the record.

### 65. Basis of Exit (First) must not be Z when Basis of Exit (Second) is not Z
If Survey Period Code is 2, 3 or 5 and English Language Learners: Basis of Exit (Second) code is not Z, then English Language Learners: Basis of Exit (First) code must not be Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the English Language Learners: Basis of Exit (First) or the English Language Learners: Basis of Exit (Second) and resubmit the record.

---

## State Validation

### 75. Matching Student Demographic record required for ELL codes LY, LP, LF
Each English Language Learners Student Information record must have a matching Student Demographic record based on District Number, Current Instruction/Service (Student Demographic) and District Number, Current Instruction/Service (English Language Learners Student Information); Florida Education Identifier; Survey Period Code and School Year and with the English Language Learners code = LY, LP or LF.
**Result:** State validation

**District Responsibility:** The district must delete the English Language Learners Student Information record or add a Student Demographic record to match the above key fields.

### 76. ELL code must be LF when Exit Date is valid unless Reclassification Date is set
If the English Language Learners: Exit Date is greater than zero, then the English Language Learners code must be LF, unless the English Language Learners: Reclassification Date is greater than zero.
**Result:** State validation

**District Responsibility:** The district must correct the English Language Learners: Exit Dates and/or the English Language Learners codes so that the valid relationship exists between the elements.

### 77. ELL PK-12 code must be LP or LY when both Basis of Exit codes are Z
If Survey Period Code is 2, 3 or 5; and if the English Language Learners: Basis of Exit (First) code is Z; and if the English Language Learners: Basis of Exit (Second) code is Z, then the English Language Learners, PK-12 code (on the Student Demographic Information record) must be LP or LY. The records should be matched on the following elements: District Number, Current Instruction/Service (Student Demographic) and District Number, Current Instruction/Service (English Language Learners Student Information); Florida Education Identifier; Survey Period Code and School Year.
**Result:** State validation

**District Responsibility:** The district must correct the English Language Learners, PK-12 code and/or the English Language Learners: Basis of Exit code so that a valid relationship exists between the elements.

### 79. ELL code must be LF when Reclassification Exit Date is valid
If the English Language Learners: Reclassification Exit Date is a valid date, then the English Language Learners code must be LF.
**Result:** State validation

**District Responsibility:** The district must correct the English Language Learners: Reclassification Exit Dates and/or the English Language Learners codes so that the valid relationship exists between the elements.

### 80. Tier Placement code required for LY students in Grade 1-12 during Survey 2
If Survey Period Code = 2 and if English Language Learners, PK-12 on the Student Demographic Information record is LY and Grade Level = 1-12, then English Language Learners: Tier Placement code must be A, B, C, D or O. The match between the two records should be done by matching the District Number, Current Instruction/Service (Student Demographic Information) and District Number, Current Instruction/Service (English Language Learners Information); Florida Education Identifier; Survey Period Code and School Year.
**Result:** State validation

**District Responsibility:** The district must correct the English Language Learners: Tier Placement code, the English Language Learners, PK-12 code or Grade Level so that a valid relationship exists among the elements.

### 82. Classification Date must not precede Home Language Survey Date
English Language Learners: Classification Date must be greater than or equal to the English Language Learners: Home Language Survey Date, unless the ELL: Classification Date is zero filled.
**Result:** State validation

**District Responsibility:** The district must correct the ELL: Classification Date and/or the ELL: Home Language Date so that a valid relationship exists between these elements.

### 83. Entry Date required when PK-12 code is LY or LF
If English Language Learners, PK-12 on the Student Demographic Information record is LY or LF, then English Language Learners: Entry Date cannot be zero. The match between the two records should be done by matching the District Number, Current Instruction/Service (Student Demographic) and District Number, Current Instruction/Service (English Language Learners Student Information); Florida Education Identifier; Survey Period Code and School Year.
**Result:** State validation

**District Responsibility:** The district must correct the English Language Learners: Entry Dates and/or the English Language Learners, PK-12 codes so that a valid relationship exists between the elements.

### 85. Grade Level must be K-12 when matching Student Demographic record exists
If there is a matching Student Demographic record, then the Grade Level must be K-12. The records should be matched using the District Number, Current Instruction/Service (Student Demographic) and District Number, Current Instruction/Service (English Language Learners Student Information); Florida Education Identifier; Survey Period Code and School Year.
**Result:** State validation

**District Responsibility:** The district must delete the English Language Learners Student Information record or change the Grade Level on the matching Student Demographic record.

### 86. At least one Test Name required for LY students with Basis of Entry A, R, or T
If Survey Period Code is 2, 3 or 5 and if English Language Learners, PK-12 code is LY and if the English Language Learners: Basis of Entry code is A, R or T, then at least one of the following must be other than ZZZ: Test Name: Listening; Test Name: Reading; Test Name: Writing; or Test Name: Speaking.
**Result:** State validation

**District Responsibility:** The district must correct the English Language Learners: PK-12 code and/or an English Language Learners: Basis of Entry code or submit the appropriate Test Name so that a valid relationship exists between the elements.

---

## Exception Reports

### 91. Entry Date should be within six years of Survey Date unless ELL code is LF
If English Language Learners, PK-12 on the Student Demographic Information record is not code LF and if English Language Learners: Entry Date is not zero, then it must be within six years of the Survey Date for Survey Period Codes 2 or 3 or August 31 of the start of the next school year for Survey Period Code 5. The match between the two records should be done using the District Number, Current Instruction/Service (Student Demographic) and District Number, Current Instruction/Service (English Language Learners Student Information); Florida Education Identifier; Survey Period Code and School Year.
**Result:** Exception report

**District Responsibility:** The district should verify the English Language Learners: Entry Date on the English Language Learners Information format and the English Language Learners, PK-12 code on the Student Demographic Information format and correct the date or code if it is in error.

### 92. Exit Date should be within two years of Survey Date unless Reclassification Date set
If Survey Period is 2 or 3, English Language Learners: Exit Date must be greater than or equal to two years prior to the Survey Date, unless zero filled or unless English Language Learners: Reclassification Date is greater than zero. If Survey Period is 5, English Language Learners: Exit Date must be greater than or equal to two years prior to August 15th of the year in which the survey 5 data are due to the Department, unless zero filled or unless English Language Learners Reclassification Date is greater than zero. Purpose: to ensure that LF code in the English Language Learners, PK-12 data element is changed to LA after two years.
**Result:** Exception rules (Exception report)

**District Responsibility:** The district should verify the English Language Learners: Exit Date and correct the date if it is in error.

### 93. Reclassification Exit Date should be within two years of Survey Date *(duplicate edit number in source)*
If Survey Period is 2 or 3, English Language Learners: Reclassification Exit Date must be greater than or equal to two years prior to the Survey Date, unless zero filled. If Survey Period is 5, the English Language Learners Reclassification Exit Date must be greater than or equal to two years prior to August 15th of the year in which the survey 5 data is due to the Department, unless zero filled. Purpose: to ensure that an LF code in the English Language Learners, PK-12 data element is changed to LA after two years.
**Result:** Exception rules (Exception report)

**District Responsibility:** The district should verify the English Language Learners: Exit Date and correct the date if it is in error.

<!-- Note: duplicate edit number in source -->
### 93. Reclassification Exit Date should be within two years of Survey Date (duplicate)
If Survey Period is 2 or 3, English Language Learners: Reclassification Exit Date must be greater than or equal to two years prior to the Survey Date, unless zero filled. If Survey Period is 5, the English Language Learners Reclassification Exit Date must be greater than or equal to two years prior to August 15th of the year in which the survey 5 data is due to the Department, unless zero filled.
**Result:** Exception report

**District Responsibility:** The district should verify the English Language Learners: Reclassification Exit Date and correct it if it is in error.

### 94. FEFP Program Number 130 not allowed once six-year LY funding window exceeded
If Survey Period is 2 or 3 and English Language Learners, PK-12 code on the Student Demographic Information record = LY, and if Survey Date is greater than the English Language Learners: Entry Date on the English Language Learners Information record in excess of six years, then FEFP Program Number on the Student Course Schedule record must not be 130. Match the Student Demographic record to the Student Course Schedule record based on District Number, Current Instruction/Service; Florida Education Identifier; Survey Period Code and Year.
**Result:** Exception reports (Exception report)

**District Responsibility:** The district must correct the FEFP Program Number for the English Language Learners student based on the English Language Learners: Entry Date because the maximum of six years of funding has been met based on the data reported.
