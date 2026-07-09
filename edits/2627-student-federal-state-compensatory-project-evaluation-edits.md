# Federal/State Compensatory Project Evaluation — Edits and Reject Rules

Source: https://www.fldoe.org/file/20909/2627fscp.pdf
Manual: Student Database 2026-2027

This document covers 36 edits across two categories: Reject Rules (record rejected) and State Validation (cross-format matching). Edit numbering is non-sequential; Reject Rules run 1-2, 4-29, 1A, 2A-2P, 30 (gaps at 3), State Validation is 31. No Exception Reports section exists in this document.

---

## Reject Rules

### 1. District Number, Current Instruction/Service must match submitting district *(Updated 07/01/2026)*
District Number, Current Instruction/Service must be numeric and active (A) on the Appendix C: District Name Table and must be correct for the district submitting the data.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number, Current Instruction/Service and resubmit the record.

### 2. School Number, Current Instruction/Service numeric range
School Number, Current Instruction/Service must be numeric in the range 0001 to 9899, excluding 9001, or it may be 9992, 9993, 9995, 9996 or 9997.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Instruction/Service and resubmit the records.

### 4. Survey Period Code must be 5
Survey Period Code must be 5 and correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** The district must correct the Survey Period Code either on the records being submitted or the transmission JCL and resubmit.

### 5. School Year correct for submission
School Year must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** Correct the School Year either on the records being submitted or the transmission JCL and resubmit all records in a batch transaction or add them on-line.

### 6. Federal/State Project Type code validity
Federal/State Project Type must be 1, 2, 5 or 8.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Federal/State Project Type code and resubmit the record.

### 7. Federal/State Subject Area required when Term S and Project Type 2 or 5 with no Support Service
If Term = S and Federal/State Project Type is 2 or 5, and Federal/State Project - Support Service = Z, then Federal/State Subject Area may not equal 0 (zero).
**Result:** Record rejected

**District Responsibility:** The district should verify that the elements, Term, Federal/State Project Type and Federal/State Subject Area have been accurately reported. If there is an error, the record should be corrected and resubmitted for processing. Otherwise, no further action is necessary.

### 8. Migrant Priority for Services code validity
Migrant Priority for Services must be Y, N or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Migrant Priority for Services codes and resubmit the records.

### 9. Migrant Priority for Services must not be Z for Project Type 2 or 5
If Federal/State Project Type is 2 or 5 then the Migrant Priority for Services code must not equal Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Migrant Priority for Services code and resubmit the record.

### 10. Immigrant Student Services Code L validity
Immigrant Student Services Code L must be L or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Immigrant Student Services codes and resubmit the records.

### 11. Immigrant Student Services Code D validity
Immigrant Student Services Code D must be D or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Immigrant Student Services codes and resubmit the records.

### 12. Immigrant Student Services Code F validity
Immigrant Student Services Code F must be F or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Immigrant Student Services codes and resubmit the records.

### 13. Immigrant Student Services Code A validity
Immigrant Student Services Code A must be A or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Immigrant Student Services codes and resubmit the records.

### 14. Immigrant Student Services Code B validity
Immigrant Student Services Code B must be B or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Immigrant Student Services codes and resubmit the records.

### 15. Immigrant Student Services Code C validity
Immigrant Student Services Code C must be C or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Immigrant Student Services codes and resubmit the records.

### 16. Immigrant Student Services Code M validity
Immigrant Student Services Code M must be M or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Immigrant Student Services codes and resubmit the records.

### 17. Transaction Code validity and existence match
The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified then the record must not already exist on the database; if C or D is specified then the record must exist on the database. An original transaction is the first submission of a record during a survey period. After original transmission of records, changes to the record for elements other than the key elements must be done with a "C" as the Transaction Code. To delete a record, the Transaction Code must be a "D." To change key elements in a batch transaction, the record must FIRST be deleted with a "D" and then added with an "A."
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Transaction Code and resubmit the records.

### 18. Record uniqueness
Each Federal/State Compensatory Project Evaluation record must be unique based on the keys of District Number, Current Instruction/Service; School Number, Current Instruction/Service; Florida Education Identifier; Survey Period Code; School Year; Federal/State Project Type, Term and Federal/State Model.
**Result:** First record accepted; all other duplicate records rejected

**District Responsibility:** If the records that were accepted and loaded to the database are the correct ones, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must delete any invalid records, correct any rejected records if necessary, and resubmit the corrected records.

### 19. Immigrant Student Services Code O validity
Immigrant Student Services Code O must be O or Z.
**Result:** Records rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Immigrant Student Services codes and resubmit the records.

### 1A. Item 3 filler must be all spaces
Item 3 - Filler on this format in position numbers 7-16 must be all spaces.
**Result:** Records rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must fill the positions noted with all spaces and resubmit the record.

### 20. Term validity
Term must be 3 or S.
**Result:** Records rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Term code and resubmit the records.

### 21. Immigrant Student Services Code R validity
Immigrant Student Services Code R must be R or Z.
**Result:** Records rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Immigrant Student Services codes and resubmit the records.

### 22. Immigrant Student Services Code S validity
Immigrant Student Services Code S must be S or Z.
**Result:** Records rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Immigrant Student Services codes and resubmit the records.

### 23. Immigrant Student Services Code T validity
Immigrant Student Services Code T must be T or Z.
**Result:** Records rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Immigrant Student Services codes and resubmit the records.

### 24. Federal/State Project Support Service code validity
Federal/State Project - Support Service must be A, D, H, N, O, R, S, T, X, or Z.
**Result:** Records rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Federal/State Project - Support Service code and resubmit the records.

### 25. Migrant Referred Services code validity
Migrant Referred Services must be Y, N or Z.
**Result:** Records rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Migrant Referred Services codes and resubmit the records.

### 26. Migrant Referred Services must not be Z for Project Type 2 or 5
If Federal/State Project Type is 2 or 5 then the Migrant Referred Services code must not equal Z.
**Result:** Records rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Migrant Referred Services code and resubmit the record.

### 27. Student Number Identifier, Local format
The Student Number Identifier, Local may be any combination of letters, numbers and blanks. (All blanks are allowable.) It must be left-justified with trailing blanks.
**Result:** Records rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Student Number Identifier, Local and resubmit the record.

### 28. Federal/State Migrant Service Provider requires Project Type 2 or 5 and Subject Area 1 or 2
If Federal/State Project Type is 2 or 5 and Federal/State Subject Area is 1 or 2, then Federal/State Migrant Service Provider code must be T or Z. For all other Federal/State Types and Federal/State Subject Areas, the Federal/State Migrant Service Provider code must be Z.
**Result:** Records rejected

**District Responsibility:** If the rejected record should not have been submitted, then no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Federal/State Project Type or Federal/State Subject Area and resubmit the record.

### 29. Federal/State Model cannot be 00 when Project Type is 1
If Federal/State Project Type is 1, then Federal/State Model code cannot be 00.
**Result:** Records rejected

**District Responsibility:** If the rejected record should not have been submitted, then no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Federal/State Project Type or Federal/State Subject Area and resubmit the record.

### 2A. Migrant Continuation of Services code validity
Migrant Continuation of Services must be A, B, C or Z.
**Result:** Records rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Migrant Continuation of Services codes and resubmit the records.

### 2B. Florida Education Identifier format
Florida Education Identifier (FLEID) is alphanumeric and must be entered as "FL" in the first 2 positions followed by twelve numeric digits. No blanks, spaces or all zeros for the twelve numeric digits are allowable.
**Result:** Records rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Florida Education Identifier and resubmit the record for processing.

### 2C. Federal/State Model code validity
Federal/State Model must equal 00, 01, 09, 10, 11, 12, 13, 14.
**Result:** Records rejected

**District Responsibility:** If the rejected record should not have been submitted, then no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Federal/State Model and resubmit the record.

### 2D. Federal/State Migrant Service Provider code validity
Federal/State Migrant Service Provider must be T or Z.
**Result:** Records rejected

**District Responsibility:** If the rejected record should not have been submitted, then no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Federal/State Migrant Service Provider and resubmit the record.

### 2E. Project Type 8 requires Federal/State Model 14
If Federal/State Project Type equals 8, then Federal/State Model must equal 14.
**Result:** Records rejected

**District Responsibility:** If the rejected record should not have been submitted, then no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Federal/State Project Type or Federal/State Model and resubmit the record.

### 2F. Federal/State Model 12 or 13 allows Migrant Service Provider T or Z; all others must be Z
If Federal/State Model equals 12 or 13, then Federal/State Migrant Service Provider code must be T or Z. For all other Federal/State Models the Federal/State Migrant Service Provider must be Z.
**Result:** Records rejected

**District Responsibility:** If the rejected record should not have been submitted, then no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Federal/State Model and resubmit the record.

### 2G. Federal/State Subject Area — Other code validity
Federal/State Subject Area - Other must be 0 or Z.
**Result:** Records rejected

**District Responsibility:** If the rejected record should not have been submitted, then no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Federal/State Subject Area code and resubmit the record.

### 2H. Federal/State Subject Area — Reading/Language Arts code validity
Federal/State Subject Area – Reading/Language Arts must be 1 or Z.
**Result:** Records rejected

**District Responsibility:** If the rejected record should not have been submitted, then no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Federal/State Subject Area code and resubmit the record.

### 2I. Federal/State Subject Area — Math code validity
Federal/State Subject Area – Math must be 2 or Z.
**Result:** Records rejected

**District Responsibility:** If the rejected record should not have been submitted, then no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Federal/State Subject Area code and resubmit the record.

### 2J. Federal/State Subject Area — ESOL code validity
Federal/State Subject Area – ESOL must be 4 or Z.
**Result:** Records rejected

**District Responsibility:** If the rejected record should not have been submitted, then no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Federal/State Subject Area code and resubmit the record.

### 2K. Federal/State Subject Area — Multidisciplinary Studies/Tutoring/Extended Learning code validity
Federal/State Subject Area – Multidisciplinary Studies/Tutoring/Extended Learning Opportunities must be 5 or Z.
**Result:** Records rejected

**District Responsibility:** If the rejected record should not have been submitted, then no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Federal/State Subject Area code and resubmit the record.

### 2L. Federal/State Subject Area — Readiness Skills code validity
Federal/State Subject Area – Readiness Skills must be 6 or Z.
**Result:** Records rejected

**District Responsibility:** If the rejected record should not have been submitted, then no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Federal/State Subject Area code and resubmit the record.

### 2M. Federal/State Subject Area — Transition Skills code validity
Federal/State Subject Area – Transition Skills must be 7 or Z.
**Result:** Records rejected

**District Responsibility:** If the rejected record should not have been submitted, then no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Federal/State Subject Area code and resubmit the record.

### 2N. Federal/State Subject Area — Science code validity
Federal/State Subject Area – Science must be 8 or Z.
**Result:** Records rejected

**District Responsibility:** If the rejected record should not have been submitted, then no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Federal/State Subject Area code and resubmit the record.

### 2O. Federal/State Subject Area — Social Studies code validity
Federal/State Subject Area – Social Studies must be 9 or Z.
**Result:** Records rejected

**District Responsibility:** If the rejected record should not have been submitted, then no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Federal/State Subject Area code and resubmit the record.

### 2P. Federal/State Subject Area — Career and Technical Education/Career Prep code validity
Federal/State Subject Area – Career and Technical Education/Career Prep must be A or Z.
**Result:** Records rejected

**District Responsibility:** If the rejected record should not have been submitted, then no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Federal/State Subject Area code and resubmit the record.

### 30. School Number, Current Instruction/Service must be active except reserved codes
If the School Number, Current Instruction/Service is not 9992, 9993, 9995 or 9996, then it must exist on the Master School Identification File as a valid active school in the district of instruction.
**Result:** Records rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the School Number, Current Instruction/Service and resubmit the record.

---

## State Validation

### 31. Matching Student Demographic record required
Each Federal/State Compensatory Project Evaluation record must have a matching Student Demographic record based on District Number, Current Instruction/Service; Florida Education Identifier; Survey Period Code and School Year.
**Result:** State validation

**District Responsibility:** The district must delete the Federal/State Compensatory Project Evaluation record if it was submitted in error. Otherwise, submit the matching demographic record if it should have been submitted with the original transmission.
