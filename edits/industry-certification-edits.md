# Industry Certification — Edits and Reject Rules

Source: [FLDOE Student Database Reject Rules — Industry Certification](https://www.fldoe.org/file/20844/2526ic.pdf)
Manual: Student Database 2025-2026

This document is organized into three edit categories: Reject Rules (record-level, causes rejection), State Validation (cross-format matching, causes rejection if unmatched), and Exception Reports (flags for review, does not reject).

---

## Reject Rules

### 1. District Number, Current Enrollment range
District Number, Current Enrollment must be numeric and in the range 01-68 or 71-75 or 80-83.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. If the district wants the data loaded, correct the District Number, Current Enrollment and resubmit.

### 2. School Number, Current Enrollment range *(Updated 07/01/2025)*
School Number, Current Enrollment must be numeric in the range 0001 to 9899, excluding 9001 and 7006, or it must be N998 or N999.
**Result:** Record rejected

**District Responsibility:** Correct the School Number, Current Enrollment and resubmit.

### 4. Survey Period Code must match submission
Survey Period Code must be 5 and must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** Correct the Survey Period Code either on the transmission JCL or on the records and resubmit.

### 5. School Year – Record Submission must match submission
School Year – Record Submission must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** Correct the School Year - Record Submission either on the records or the transmission JCL and resubmit all records.

### 6. District Number, Current Instruction/Service range and match
District Number, Current Instruction/Service must be numeric in the range 01-68 or 71-75 or 80-83 and must be correct for the district submitting the data.
**Result:** Record rejected

**District Responsibility:** Correct the District Number, Current Instruction/Service and resubmit.

### 7. School Number, Current Instruction/Service range
The School Number, Current Instruction/Service must be numeric in the range 0001-9899, excluding 9001, or it must be C901-C928, U970-U981, or P001-P999.
**Result:** Record rejected

**District Responsibility:** Correct the School Number, Current Instruction/Service and resubmit.

### 8. Industry Certification Identifier must exist on Appendix Z
Industry Certification Identifier must exist on Appendix Z of the FDOE Information Database Requirements: Volume I -- Automated Student Information System Manual.
**Result:** Record rejected

**District Responsibility:** Correct the Industry Certification Identifier and resubmit.

### 9. Industry Certification Outcome must be P or F
Industry Certification Outcome must be P or F.
**Result:** Record rejected

**District Responsibility:** Correct the Industry Certification Outcome code and resubmit.

### 10. Course Number validity *(Updated 06/05/2026)*
Course Number must not contain blanks. If School Number, Current Instruction/Service does not begin with C, P or U, then:
- If Grade Level is KG-05, the Course Number must be 0000000; or
- If Grade Level is 06-08 and position 6 of the Industry Certification Identifier is not 8, the Course Number must be a valid Course Number in the Course Code Directory for the School Year - Course Taken; or
- If Grade Level is 09-12, the Course Number must be a valid Course Number in the Course Code Directory for the School Year - Course Taken.

If School Number, Current Instruction/Service begins with C or U, then the Course Number must be on the Statewide Course Numbering System file for the School Year - Course Taken.
**Result:** Record rejected

**District Responsibility:** Correct the Course Number and resubmit.

### 11. Career and Technical Education/Adult General Education Program Code validity
If Course Number equals 0000000 and Grade Level is KG-08, then the Career and Technical Education/Adult General Education Program Code must be zero.

If Course Number begins with a number and is a course number from the Career and Technical Education/Adult General Education Program Edit file (F61730), other than 0000000, 0200320, 0200335, 1700510, 2000350, 2000360, 2102360, 2102370, 3027010, or 3027020, then the Career and Technical Education/Adult General Education Program Code must be a valid program number (Supplemental Indicator at position 20 not equal 'A') for the Course Number submitted, as listed in file F61730 for School Year - Course Taken.

If the Course Number begins with three alphabetic characters followed by a zero in the fourth position, and is a course number from F61730, then the Program Code must be a valid program number for the Course Number submitted, as listed in F61730 for School Year - Course Taken.

If Course Number begins with one alphabetic character followed by a numeric digit, and is a course number from F61730, then the Program Code (Supplemental Indicator at position 20 not equal 'A') must be the same as the Course Number for School Year - Course Taken.
**Result:** Record rejected

**District Responsibility:** Correct the Career and Technical/Adult General Education Program Code and resubmit.

### 12. School Year – Course Taken validity
The School Year – Course Taken must be a valid school year greater than or equal to 0708 and less than or equal to the current school year.
**Result:** Record rejected

**District Responsibility:** Correct the School Year – Course Taken field and resubmit.

### 13. Grade Level restriction for Type 3 certifications *(Updated 06/05/2026)*
If position 6 of Industry Certification Identifier is 8 (Type = 3 on Appendix Z), then Grade Level must be KG-05.
**Result:** Record rejected

**District Responsibility:** Correct the Grade Level and resubmit.

### 14. School Year match for Type 3 certifications
If position 6 of the Industry Certification Identifier is 8 (Type = 3 on Appendix Z) then the School Year - Course Taken must be equal to the School Year - Record Submission.
**Result:** Record rejected

**District Responsibility:** Correct the School Year - Course Taken or School Year – Record Submission and resubmit.

### 15. Student Number Identifier, Local format
The Student Number Identifier, Local may be any combination of letters, numbers and blanks (all blanks are allowable). It must be left-justified with trailing blanks.
**Result:** Record rejected

**District Responsibility:** Correct the Student Number Identifier, Local and resubmit.

### 16. Grade Level must be KG-12
Grade Level must be KG-12.
**Result:** Record rejected

**District Responsibility:** Correct the Grade Level and resubmit.

### 17. Transaction Code validity
The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified the record must not already exist on the database; if C or D is specified the record must exist on the database. To change key elements in a batch transaction, the record must first be deleted with a "D" and then added with an "A".
**Result:** Record rejected

**District Responsibility:** Correct the Transaction Code and resubmit.

### 18. Record uniqueness
Each record must be unique based on Florida Education Identifier; School Year - Record Submission; District Number, Current Instruction/Service; School Number, Current Instruction/Service; Course Number; Industry Certification Identifier; Industry Certification Outcome; and Survey Period Code.
**Result:** First record accepted, all other duplicate records rejected

**District Responsibility:** Delete any invalid records, correct rejected records if necessary, and resubmit.

### 19. School Number, Current Enrollment must be active on Master School ID File
If the School Number, Current Enrollment is not N998 or N999, then it must exist on the Master School Identification File as a valid active number in the District Number, Current Enrollment.
**Result:** Record rejected

**District Responsibility:** Correct the School Number, Current Enrollment and resubmit.

### 1A. Filler must be spaces
Item 3 - Filler on this format in position numbers 7-16 must be all spaces.
**Result:** Record rejected

**District Responsibility:** Fill the noted positions with all spaces and resubmit.

### 20. School Number, Current Instruction/Service must be active on Master School ID File
If the School Number, Current Instruction/Service is not C901-C928, U970-U981, or P001-P999, then it must exist as a valid active number in the District Number, Current Instruction/Service on the Master School Identification File.
**Result:** Record rejected

**District Responsibility:** Correct the School Number, Current Instruction/Service and resubmit.

### 21. Grade Level restriction for CAPE / CAPE Acceleration certifications
If the Industry Certification Identifier on Appendix Z is indicated to be a CAPE Industry Certification (Type = 1) or CAPE Acceleration Industry Certification (Type = 2), then Grade Level must be 06-12.
**Result:** Record rejected

**District Responsibility:** Correct the Industry Certification Identifier or Grade Level and resubmit.

### 22. Course Number validity for CAPE / CAPE Acceleration certifications
If the Industry Certification Identifier on Appendix Z is indicated to be a CAPE Industry Certification (Type = 1) or CAPE Acceleration Industry Certification (Type = 2), then Course Number must be a valid number on the Course Code Directory or the Statewide Course Numbering System file for the School Year - Course Taken, unless School Number, Current Instruction/Service equals P001-P999.
**Result:** Record rejected

**District Responsibility:** Correct the Course Number and resubmit.

### 24. Career and Technical Education/Adult General Education Program Code validity (general)
The Career and Technical Education/Adult General Education Program Code must be a program number from the Career and Technical Education/Adult General Education Program Edit file (F61730) for School Year – Course Taken or must be zero-filled.
**Result:** Record rejected

**District Responsibility:** Correct the Career and Technical Education/Adult General Education Program Code and resubmit.

### 25. Florida Education Identifier (FLEID) format
FLEID is alphanumeric and must be entered as "FL" in the first 2 positions followed by twelve numeric digits. No blanks, spaces, or all zeros for the twelve numeric digits are allowable.
**Result:** Record rejected

**District Responsibility:** Correct the FLEID and resubmit.

### 27. Dual Enrollment Institution Type validity
Dual Enrollment Institution Type must be A, B, C, D or Z.
**Result:** Record rejected

**District Responsibility:** Correct the Dual Enrollment Institution Type and resubmit.

### 28. Dual Enrollment Institution Type for alphabetic Course Numbers
If Course Number begins with an alphabetic character then Dual Enrollment Institution Type must be A, B, C or D.
**Result:** Record rejected

**District Responsibility:** Correct the Dual Enrollment Institution Type and resubmit.

### 29. Industry Certification Date Earned validity
If Industry Certification Outcome = P, then the Industry Certification Date Earned must be numeric and a valid date in the format MMDDYYYY; for all other Industry Certification Outcomes, the Industry Certification Date Earned must be zero filled.
**Result:** Record rejected

**District Responsibility:** Correct the Industry Certification Outcome code or the Industry Certification Date Earned and resubmit.

---

## State Validation

### 40. Matching Student Demographic Information record required
Each Industry Certification record must have a matching Student Demographic Information record based on District Number, Current Instruction; Florida Education Identifier; Survey Period Code; and Year.
**Result:** State validation

**District Responsibility:** Delete the Industry Certification records if submitted in error, or submit matching Student Demographic Information records.

### 41. Matching CTE Student Course Schedule record required
If Course Number begins with a number and School Year - Course Taken = School Year - Record Submitted; and is a course number from the Career and Technical Education/Adult General Education Program Edit file (F61730) for the School Year – Course Taken; and is not 0000000, 0200320, 0200335, 1700510, 2000350, 2000360, 2102360, 2102370, 3027010, or 3027020; then there must be a matching record on the Career and Technical Education Student Course Schedule format based on Florida Education Identifier; District Number, Current Instruction; School Number, Current Instruction; Survey Period Code; Career and Technical Education/Adult General Education Program Code; Course Number; School Year - Record Submitted.
**Result:** State validation

**District Responsibility:** Delete the Industry Certification records if submitted in error, or submit matching Career and Technical Education Student Course Schedule records.

---

## Exception Reports

### 60. Grade Level agreement with Student Demographic record
The student's Grade Level code on the Industry Certification record must agree with the Grade Level code on the Student Demographic record submitted by the district of instruction. Matched based on District Number, Current Instruction; Florida Education Identifier; Survey Period Code; and Year.
**Result:** Exception report (does not reject; generates a message)

**District Responsibility:** Verify the student's Grade Level to confirm whether the Grade Level at the time the course was taken is legitimately different from the student's Grade Level at the end of the school year. Correct if it should match; no action needed if the discrepancy is correct.
