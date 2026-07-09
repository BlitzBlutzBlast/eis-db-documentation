# Industry Certification — Edits and Reject Rules

Source: https://www.fldoe.org/file/20909/2627ic.pdf
Manual: Student Database 2026-2027

This document covers 30 edits across three categories: Reject Rules (record rejected), State Validation (cross-format matching), and Exception Reports (advisory). Edit numbering is non-sequential; Reject Rules run 1-2, 4-22, 24-29, 1A (gaps at 3, 23), State Validation runs 40-41, Exception Reports is 60.

---

## Reject Rules

### 1. District Number, Current Enrollment must be active on Appendix C *(Updated 07/01/2026)*
District Number, Current Enrollment must be numeric and active (A) on the Appendix C: District Name Table.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number, Current Enrollment and resubmit the record.

### 2. School Number, Current Enrollment numeric range
School Number, Current Enrollment must be numeric in the range 0001 to 9899, excluding 9001 and 7006, or it must be N998 or N999.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Enrollment and resubmit the records.

### 4. Survey Period Code must be 5
Survey Period Code must be 5 and must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** The District must correct the Survey Period Code either on the transmission JCL or on the records and resubmit the records.

### 5. School Year correct for submission
School Year – Record Submission must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** Correct the School Year - Record Submission either on the records coming in or the transmission JCL and resubmit all records.

### 6. District Number, Current Instruction/Service must match submitting district *(Updated 07/01/2026)*
District Number, Current Instruction/Service must be numeric and active (A) on the Appendix C: District Name Table and must be correct for the district submitting the data.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number, Current Instruction/Service and resubmit the record.

### 7. School Number, Current Instruction/Service numeric range
The School Number, Current Instruction/Service must be numeric in the range 0001-9899, excluding 9001, or it must be C901-C928, U970-U981, or P001-P999.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Instruction/Service and resubmit the records.

### 8. Industry Certification Identifier must be on Appendix Z
Industry Certification Identifier must exist on Appendix Z of the FDOE Information Database Requirements: Volume I -- Automated Student Information System Manual.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Industry Certification Identifier codes and resubmit the records.

### 9. Industry Certification Outcome code validity
Industry Certification Outcome must be P or F.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Industry Certification Outcome code and resubmit the record.

### 10. Course Number validity by Grade Level and School Number *(Updated 07/01/2026)*
Course Number must not contain blanks. If School Number, Current Instruction/Service does not begin with C, P or U: (a) If Grade Level is KG-05, the Course Number must be 0000000; (b) If Grade Level is 06-08 and position 6 of the Industry Certification Identifier is 8, the Course Number must be 0000000 or a valid Course Number in the Course Code Directory for the School Year - Course Taken; (c) If Grade Level is 06-08 and position 6 of the Industry Certification Identifier is not 8, the Course Number must be a valid Course Number in the Course Code Directory for the School Year - Course Taken; (d) If Grade Level is 09-12, the Course Number must be a valid Course Number in the Course Code Directory for the School Year - Course Taken. If School Number, Current Instruction/Service begins with C or U, then the Course Number must be on the Statewide Course Numbering System file for the School Year - Course Taken.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Course Number and resubmit the records.

### 11. Career and Technical Education/Adult General Education Program Code validity
If Course Number equals 0000000 and Grade Level is KG-08, then the Career and Technical Education/Adult General Education Program Code must be zero. If Course Number begins with a number and is a CTE/Adult GE course from file F61730 (other than specified exemptions), then the Career and Technical Education/Adult General Education Program Code must be a valid program number (Supplemental Indicator at position 20 not equal 'A') for the Course Number submitted, as listed in file F61730 for School Year - Course Taken. If the Course Number begins with three alphabetic characters followed by a zero in the fourth position and is from F61730, then the Program Code must be valid for the Course Number in F61730. If the Course Number begins with one alphabetic character followed by a numeric digit and is from F61730, then the Program Code (Supplemental Indicator at position 20 not equal 'A') must be the same as the Course Number.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Career and Technical/Adult General Education Program Code and resubmit the record.

### 12. School Year — Course Taken must be valid and at least 0708
The School Year – Course Taken must be a valid school year greater than or equal to 0708 and less than or equal to the current school year.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Year – Course Taken fields and resubmit the records.

### 13. Type 3 Industry Certifications require Grade Level KG-08 *(Updated 07/01/2026)*
If position 6 of Industry Certification Identifier is 8 (Type = 3 on Appendix Z), then Grade Level must be KG-08.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Grade Level and resubmit the records.

### 14. Type 3 Industry Certifications require School Year — Course Taken to equal School Year — Record Submission
If position 6 of the Industry Certification Identifier is 8 (Type = 3 on Appendix Z) then the School Year - Course Taken must be equal to the School Year - Record Submission.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Year - Course Taken or School Year – Record Submission and resubmit the records.

### 15. Student Number Identifier, Local format
The Student Number Identifier, Local may be any combination of letters, numbers and blanks. (All blanks are allowable.) It must be left-justified with trailing blanks.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Student Number Identifier, Local and resubmit the record.

### 16. Grade Level must be KG-12
Grade Level must be KG-12.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Grade Level and resubmit the records.

### 17. Transaction Code validity and existence match
The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified then the record must not already exist on the database; if C or D is specified then the record must exist on the database. An original transaction is the first submission of a record during a survey period. After original transmission of records, changes to the record for elements other than the key elements must be done with a "C" as the Transaction Code. To delete a record, the Transaction Code must be a "D". To change key elements in a batch transaction, the record must FIRST be deleted with a "D" and then added with an "A".
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Transaction Code and resubmit the records.

### 18. Record uniqueness
Each record must be unique based on Florida Education Identifier; School Year - Record Submission; District Number, Current Instruction/Service; School Number, Current Instruction/Service; Course Number; Industry Certification Identifier; Industry Certification Outcome and Survey Period Code.
**Result:** First record accepted, all other duplicate records rejected

**District Responsibility:** If the records that were accepted and loaded to the database are the correct ones, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must delete any invalid records, correct any rejected records if necessary, and resubmit the corrected records.

### 19. School Number, Current Enrollment must be active except reserved codes
If the School Number, Current Enrollment is not N998 or N999, then it must exist on the Master School Identification File as a valid active number in the District Number, Current Enrollment.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Enrollment and resubmit the records.

### 1A. Item 3 filler must be all spaces
Item 3 - Filler on this format in position numbers 7-16 must be all spaces.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must fill the positions noted with all spaces and resubmit the record.

### 20. School Number, Current Instruction/Service must be active except postsecondary codes
If the School Number, Current Instruction/Service is not C901-C928, U970-U981, or P001-P999, then it must exist as a valid active number in the District Number, Current Instruction/Service on the Master School Identification File.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Instruction/Service and resubmit the records.

### 21. CAPE Industry Certification or Acceleration type requires Grade Level 06-12
If the Industry Certification Identifier on Appendix Z is indicated to be a CAPE Industry Certification (Type = 1) or CAPE Acceleration Industry Certification (Type = 2), then Grade Level must be 06-12.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Industry Certification Identifier or Grade Level and resubmit the records.

### 22. CAPE Industry Certification or Acceleration type requires valid Course Number
If the Industry Certification Identifier on Appendix Z is indicated to be a CAPE Industry Certification (Type = 1) or CAPE Acceleration Industry Certification (Type = 2), then Course Number must be a valid number on the Course Code Directory or the Statewide Course Numbering System file for the School Year - Course Taken, unless School Number, Current Instruction/Service equals P001-P999.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Course Number and resubmit the records.

### 24. Career and Technical Education/Adult General Education Program Code must be on F61730 or zero-filled
The Career and Technical Education/Adult General Education Program Code must be a program number from the Career and Technical Education/Adult General Education Program Edit file (F61730) for School Year – Course Taken or must be zero-filled.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Career and Technical Education/Adult General Education Program Code and resubmit the record.

### 25. Florida Education Identifier format
Florida Education Identifier (FLEID) is alphanumeric and must be entered as "FL" in the first 2 positions followed by twelve numeric digits. No blanks, spaces or all zeros for the twelve numeric digits are allowable.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Florida Education Identifier and resubmit the record for processing.

### 27. Dual Enrollment Institution Type code validity
Dual Enrollment Institution Type must be A, B, C, D or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Dual Enrollment Institution Type and resubmit the records.

### 28. Dual Enrollment Institution Type requires A, B, C, or D when Course Number begins with alphabetic character
If Course Number begins with an alphabetic character then Dual Enrollment Institution Type must be A, B, C or D.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Dual Enrollment Institution Type and resubmit the records.

### 29. Industry Certification Date Earned required for Outcome P; must be zero-filled otherwise
If Industry Certification Outcome = P, then the Industry Certification Date Earned must be numeric and a valid date in the format of MMDDYYYY; for all other Industry Certification Outcomes, the Industry Certification Date Earned must be zero filled.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Industry Certification Outcome code or the Industry Certification Date Earned and resubmit the record.

---

## State Validation

### 40. Matching Student Demographic record required
Each Industry Certification record must have a matching Student Demographic Information record based on District Number, Current Instruction; Florida Education Identifier; Survey Period Code; and Year.
**Result:** State validation

**District Responsibility:** The district must delete the Industry Certification records if they were submitted in error or submit Student Demographic Information records that match on the indicated fields.

### 41. Matching CTE Student Course Schedule record required for numeric CTE course numbers
If Course Number begins with a number and School Year - Course Taken equals School Year - Record Submitted, and the Course Number is from the Career and Technical Education/Adult General Education Program Edit file (F61730) for the School Year – Course Taken, and is not one of the specified exempt course numbers; then there must be a matching record on the Career and Technical Education Student Course Schedule format based on Florida Education Identifier; District Number, Current Instruction; School Number, Current Instruction; Survey Period Code; Career and Technical Education/Adult General Education Program Code; Course Number; School Year - Record Submitted.
**Result:** State validation

**District Responsibility:** The district must delete the Industry Certification records if they were submitted in error or submit Career and Technical Education Student Course Schedule records that match on the indicated fields.

---

## Exception Reports

### 60. Grade Level must agree with Student Demographic record
The student's Grade Level code on the Industry Certification record must agree with the Grade Level code on the Student Demographic record submitted by the district of instruction. Matched based on District Number, Current Instruction; Florida Education Identifier; Survey Period Code; and Year.
**Result:** Exception report

**District Responsibility:** The district should verify the student's Grade Level to assure that the Grade Level at the time the course was taken is actually different than the student's Grade Level at the end of the school year. If the Grade Level should be the same, correct the Grade Level. If the reported Grade Level is correct, no action is necessary.
