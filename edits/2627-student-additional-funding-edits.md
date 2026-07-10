# Student Additional Funding — Edits and Reject Rules

Source: https://www.fldoe.org/file/20909/2627saf.pdf
Manual: Student Database 2026-2027

This document covers 30 edits across three categories: Reject Rules (record rejected), State Validation (cross-format matching), and Exception Reports (advisory, does not reject). Edit numbering is non-sequential; gaps (edit 3, 23) and deleted edits are as published in the source.

---

## Reject Rules

### 1. District Number, Current Instruction/Service range and active status *(Updated 07/01/2026)*
District Number, Current Instruction/Service must be numeric and active (A) on the Appendix C: District Name Table and must be correct for the district submitting the data.
**Result:** Record Rejected

**Example:**
| District Number, Current Instruction/Service | School Number, Current Instruction/Service | Florida Education Identifier |
|---|---|---|
| 01 | 0021 | FL340945895734 |
| 01 | 0021 | FL340945895735 |
| *00 | 0021 | FL340945895736 |

The third record would be rejected since the District Number, Current Instruction/Service is not active (A) on the Appendix C: District Name Table.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number, Current Instruction/Service and resubmit the record.

### 2. School Number, Current Instruction/Service range
School Number, Current Instruction/Service must be numeric in the range 0001 to 9899 (excluding 9001), C901-C928, U970-U981, P001-P999, or it must be N998 or N999.
**Result:** Record Rejected

**Example:**
| District Number, Current Instruction/Service | School Number, Current Instruction/Service | Florida Education Identifier |
|---|---|---|
| 01 | 0021 | FL340945895734 |
| 01 | 0021 | FL340945895735 |
| *01 | 9999 | FL340945895736 |

The third record would be rejected because the School Number, Current Instruction/Service is not in the appropriate numerical range.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the School Number, Current Instruction/Service and resubmit the record.

### 4. Survey Period Code must be 5
Survey Period Code must be 5 and must be correct for the submission specified by the district.
**Result:** Record Rejected

**Example:** The Survey Period Code as specified in the transmission JCL or in statements for tape transmission is identified as Survey Period "5". However, records on the transmission have a Survey Period Code "3". All updates, adds or deletes with this inconsistency would be rejected.

**District Responsibility:** The district must correct Survey Period Code either on the records coming in or the transmission JCL and all records must be resubmitted.

### 5. School Year correctness
School Year must be correct for the submission specified by the district.
**Result:** Record Rejected

**Example:** The School Year as specified in the transmission JCL or in statements for tape transmission is identified as the valid year for data submission. However, records on the transmission have the previous School Year coded. All updates, adds or deletes with this inconsistency will be rejected.

**District Responsibility:** The district must correct School Year either on the records coming in or the transmission JCL and all records must be resubmitted.

### 6. Transaction Code validity
The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified then the record must not already exist on the database; if C or D is specified then the record must exist on the database.
**Result:** Record Rejected

**Example:** For all original transmissions, the Transaction Code must be "A". An original transaction is the first submission of a record during a survey period. After original transmission of records, changes to the record for elements other than the key elements must be done with a "C" as the Transaction Code. To delete a record, the Transaction Code must be a "D". To change key elements in a batch transaction, the record must FIRST be deleted with a "D" and then added with an "A". Records with an incorrect Transaction Code would be rejected.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Transaction Code and resubmit the records.

### 7. Value Earned, CEEB Advanced Placement Test validity *(Updated 07/01/25)*
Value Earned, College Entrance Examination Board (CEEB) Advanced Placement Test must be numeric and must equal 0.00, 0.16, 0.32, 0.48, 0.64, 0.80, 0.96, 1.12, 1.28, 1.44, 1.60, 1.76, 1.92, 2.08, 2.24 or 2.40.
**Result:** Record Rejected

Note: Two decimal places assumed.

**Example:**
| District Number, Current Instruction/Service | Florida Education Identifier | Value Earned, CEEB Advanced Placement Test |
|---|---|---|
| 30 | FL340945895734 | 032 |
| *30 | FL340945895735 | ZZZ |
| *30 | FL340945895736 | 480 |
| 30 | FL340945895737 | 000 |

The first and fourth records would be loaded assuming no other reject rule would cause their rejection. The second record would be rejected because Value Earned, CEEB Advanced Placement Test is not numeric. The third record would be rejected because it is not valid.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Value Earned, CEEB Advanced Placement Test and resubmit the records.

### 8. Student Number Identifier, Local format
The Student Number Identifier, Local may be any combination of letters, numbers and blanks. (All blanks are allowable.) It must be left-justified with trailing blanks.
**Result:** Record Rejected

**Example:**
| District Number, Current Instruction/Service | Student Number Identifier, Local |
|---|---|
| 01 | 0123456789 |
| 01 | ABC123DEF9 |
| 01 | 3001 28K |
| *01 | 2121@xyz |
| *01 | 123456 |

The first three records would be loaded assuming no other edit would cause their rejection. The fourth record would be rejected because the Student Number Identifier, Local contains a symbol (@). The fifth record would be rejected because it is right-justified rather than left-justified.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Student Number Identifier, Local and resubmit the records.

### 9. Value Earned, International Baccalaureate Diploma validity *(Updated 07/01/25)*
Value Earned, International Baccalaureate Diploma must be 0.00 or 0.30.
**Result:** Record Rejected

Note: Two decimal places assumed.

**Example:**
| District Number, Current Instruction/Service | Florida Education Identifier | Value Earned, International Baccalaureate Diploma |
|---|---|---|
| 35 | FL340945895734 | 030 |
| 35 | FL340945895735 | 000 |
| *35 | FL340945895736 | 050 |

The first two records would be loaded assuming no other reject rule would cause their rejection. The last record would be rejected because Value Earned, International Baccalaureate Diploma is not 0.00 or 0.30.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Value Earned, International Baccalaureate Diploma and resubmit the record.

### 10. Value Earned, International Baccalaureate Score validity *(Updated 07/01/25)*
Value Earned, International Baccalaureate Score must be numeric and must equal 0.00, 0.16, 0.32, 0.48, 0.64, 0.80, 0.96, or 1.12.
**Result:** Record Rejected

Note: Two decimal places assumed.

**Example:**
| District Number, Current Instruction/Service | Florida Education Identifier | Value Earned, International Baccalaureate Score |
|---|---|---|
| 35 | FL340945895734 | 112 |
| 35 | FL340945895735 | 000 |
| *35 | FL340945895736 | 320 |

The first two records would be loaded assuming no other reject rule would cause their rejection. The last record would be rejected because Value Earned, International Baccalaureate Score is not valid.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Value Earned, International Baccalaureate Score and resubmit the record.

### 11. School Number, Current Instruction/Service validity against Master School Identification File
The School Number, Current Instruction/Service must exist on the Master School Identification File as a valid school number in the district of Instruction/Service, or it must be C901-C928, U970-U981 or P001-P999.
**Result:** Record Rejected

**Example:**
| District Number, Current Instruction/Service | School Number, Current Instruction/Service | Florida Education Identifier |
|---|---|---|
| *01 | 0351 | FL340945895734 |

The record would be rejected because the School Number, Current Instruction/Service is not valid on the Master School Identification File for the District Number, Current Instruction/Service.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the School Number, Current Instruction/Service and resubmit the record.

### 12. Value Earned, Advanced International Certificate of Education Diploma validity *(Updated 07/01/25)*
Value Earned, Advance International Certificate of Education Diploma must be 0.00 or 0.30.
**Result:** Record Rejected

Note: Two decimal places assumed.

**Example:**
| District Number, Current Instruction/Service | Florida Education Identifier | Value Earned, Advanced International Certificate of Education Diploma |
|---|---|---|
| 35 | FL340945895734 | 030 |
| 35 | FL340945895735 | 000 |
| *35 | FL340945895736 | 050 |

The first two records would be loaded assuming no other reject rule would cause their rejection. The last record would be rejected because Value Earned, Advance International Certificate of Education Diploma is not 0.00 or 0.30.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Value Earned, Advance International Certificate of Education Diploma and resubmit the record.

### 13. Value Earned, Advanced International Certificate of Education Score validity *(Updated 07/01/25)*
Value Earned, Advanced International Certificate of Education Score must be 0.00, 0.08, 0.16, 0.24, 0.32, 0.40, 0.48, 0.56, 0.64, 0.72, 0.80, 0.88, 0.96, 1.04, or 1.12.
**Result:** Record Rejected

Note: Two decimal places assumed.

**Example:**
| District Number, Current Instruction/Service | Florida Education Identifier | Value Earned, Advanced International Certificate of Education Score |
|---|---|---|
| 35 | FL340945895734 | 104 |
| 35 | FL340945895735 | 000 |
| *35 | FL340945895736 | 122 |

The first two records would be loaded assuming no other reject rule would cause their rejection. The last record would be rejected because Value Earned, Advance International Certificate of Education Score is not valid.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Value Earned, Advance International Certificate of Education Score and resubmit the record.

### 14. Item 4 - Filler must be all spaces
Item 4 - Filler on this format in position numbers 9-18 must be all spaces.
**Result:** Record Rejected

**Example:**
| District Number, Current Instruction/Service | School Number, Current Instruction/Service | Filler, Item #4 |
|---|---|---|
| 01 | 0151 | |
| *01 | 0151 | 265456789X |

The first record would be loaded assuming no other reject rule would cause its rejection. The second record would be rejected because the data reported is not all spaces.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must fill the positions noted with all spaces and resubmit the record.

### 15. Value Earned, Early Graduates validity *(Updated 07/01/25)*
Value Earned, Early Graduates must be numeric and must be equal to 0.0000, 0.2500, or 0.5000.
**Result:** Record Rejected

Note: Four decimal places assumed.

**Example:**
| District Number, Current Instruction/Service | Florida Education Identifier | Value Earned, Early Graduates |
|---|---|---|
| 30 | FL340945895734 | 02500 |
| 30 | FL340945895735 | 00000 |
| *30 | FL340945895736 | ZZZZZ |
| *30 | FL340945895737 | 33333 |

The first and second records would be loaded assuming no other reject rule would cause their rejection. The third record would be rejected because Value Earned, Early Graduates is not numeric. The fourth record would be rejected because it is not equal to 0.0000, 0.2500, or 0.5000.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Value Earned, Early Graduates and resubmit the records.

### 16. Florida Education Identifier (FLEID) format
Florida Education Identifier (FLEID) is alphanumeric and must be entered as "FL" in the first 2 positions followed by twelve numeric digits. No blanks, spaces or all zeros for the twelve numeric digits are allowable.
**Result:** Record Rejected

**Example:**
| District Number, Current Enrollment | Florida Education Identifier |
|---|---|
| 01 | FL340945895734 |
| 01 | FL004583948567 |
| *01 | FL000000000000 |

The first two records would be loaded assuming no other reject rule would cause their rejection. The third record would be rejected because the Florida Education Identifier (FLEID) is not a valid FLEID.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Florida Education Identifier and resubmit the record for processing.

### 17. District Number, Current Enrollment range and active status *(Updated 07/01/2026)*
District Number, Current Enrollment must be numeric and active (A) on the Appendix C: District Name Table.
**Result:** Record Rejected

**Example:**
| District Number, Current Enrollment | Florida Education Identifier |
|---|---|
| 01 | FL340945895734 |
| 01 | FL340945895735 |
| *00 | FL340945895736 |

The third record would be rejected since the District Number, Current Enrollment is active (A) on the Appendix C: District Name Table.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number, Current Enrollment and resubmit the record.

### 18. Record uniqueness
Each Student Additional Funding record must be unique based on District Number, Current Instruction/Service; School Number, Current Instruction/Service; Florida Education Identifier; Survey Period Code and School Year.
**Result:** Record Rejected

**Example:**
| District Number, Current Instruction/Service | School Number, Current Instruction/Service | Florida Education Identifier | Survey Period Code | School Year |
|---|---|---|---|---|
| 01 | 0381 | FL340945895734 | 5 | **** |
| *01 | 0381 | FL340945895734 | 5 | **** |
| 01 | 0250 | FL340945895736 | 5 | **** |

**** = Valid fiscal year for data submission. The first and third records would be loaded assuming no other reject rule would cause their rejection. The second record would be rejected because it is a duplicate (same District Number, Current Instruction/Service; Florida Education Identifier; Survey Period Code and School Year) of the first record.

**District Responsibility:** If the records accepted and loaded to the database are the correct ones no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the rejected record and resubmit the record. The district must delete any invalid records.

### 19. Early Graduates value requires matching District Number, Current Enrollment *(Updated 07/01/25)*
If Value Earned, Early Graduates is greater than zero, then District Number, Current Enrollment must match District Number, Current Instruction/Service.
**Result:** Record Rejected

**Example:**
| District Number, Current Instruction/Service | District Number, Current Enrollment | Value Earned, Early Graduates |
|---|---|---|
| 01 | 01 | 0.2500 |
| *02 | 01 | 0.2500 |

The first record would be loaded assuming no other reject rule would cause its rejection. The second record would be rejected since the District Number, Current Instruction/Service and District Number, Current Enrollment does not match.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the rejected record and resubmit the record.

### 20. Value Earned, College Board Advanced Placement Capstone Diploma validity *(Updated 07/01/25)*
Value Earned, College Board Advanced Placement Capstone Diploma must be numeric and must equal 0.00 or 0.30.
**Result:** Record Rejected

Note: Two decimal places assumed.

**Example:**
| District Number, Current Instruction/Service | Florida Education Identifier | Value Earned, College Board Advanced Placement Capstone Diploma |
|---|---|---|
| 35 | FL340945895734 | 030 |
| 35 | FL340945895742 | 000 |
| *35 | FL340945895739 | 050 |

The first two records would be loaded assuming no other reject rule would cause their rejection. The last record would be rejected because Value Earned, College Board Advanced Placement Capstone Diploma is not 0.00 or 0.30.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Value Earned, College Board Advanced Placement Capstone Diploma and resubmit the record.

### 21. FTE Earned, Dual Enrollment Course validity *(Deleted 07/01/25)*
FTE Earned, Dual Enrollment Course must be numeric and must equal 0.00, 0.08, 0.16, 0.24, 0.32, 0.40, 0.48, 0.56, 0.64, 0.72, 0.80, 0.88, 0.96, 1.04, 1.12, 1.28, 1.44, 1.60, 1.76, or 1.92.
**Result:** Record Rejected

Note: Two decimal places assumed.

**Example:**
| District Number, Current Instruction/Service | Florida Education Identifier | FTE Earned, Dual Enrollment Course |
|---|---|---|
| 30 | FL340945895734 | 016 |
| *30 | FL340945895751 | ZZZ |
| *30 | FL340945895726 | 480 |
| 30 | FL340945895744 | 000 |

The first and fourth records would be loaded assuming no other reject rule would cause their rejection. The second record would be rejected because FTE Earned, Dual Enrollment Course is not numeric. The third record would be rejected because it is not valid.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the FTE Earned, Dual Enrollment Course and resubmit the records.

### 22. Value Earned, Academic Dual Enrollment Associate Degree validity *(Updated 07/01/25)*
Value Earned, Academic Dual Enrollment Associate Degree must be numeric and must equal 0.00 or 0.30.
**Result:** Record Rejected

Note: Two decimal places assumed.

**Example:**
| District Number, Current Instruction/Service | Florida Education Identifier | Value Earned, Academic Dual Enrollment Associate Degree |
|---|---|---|
| 30 | FL340945895734 | 030 |
| *30 | FL340945895751 | ZZZ |
| *30 | FL340945895726 | 480 |
| 30 | FL340945895744 | 000 |

The first and fourth records would be loaded assuming no other reject rule would cause their rejection. The second record would be rejected because Value Earned, Academic Dual Enrollment Associate Degree is not numeric. The third record would be rejected because it is not valid.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Value Earned, Academic Dual Enrollment Associate Degree and resubmit the records.

### 24. Value Earned, Career Dual Enrollment Course validity *(Updated 06/05/26)*
Value Earned, Career Dual Enrollment Course must be numeric and must equal 0.00, 0.08, 0.16, 0.24, 0.32, 0.40, 0.48, 0.56, 0.64, 0.72, 0.80, 0.88, 0.96, 1.04, 1.12, 1.20, 1.28, 1.36, 1.44, 1.52, 1.60.
**Result:** Record Rejected

Note: Two decimal places assumed.

**Example:**
| District Number, Current Instruction/Service | Florida Education Identifier | Value Earned, Career Dual Enrollment Course |
|---|---|---|
| 35 | FL340945895737 | 008 |
| 35 | FL340945895738 | 000 |
| *35 | FL340945895739 | 050 |

The first two records would be loaded assuming no other reject rule would cause their rejection. The last record would be rejected because Value Earned, Career Dual Enrollment Course is not 0.00 or 0.08.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Value Earned, Career Dual Enrollment Course and resubmit the record.

### 25. Value Earned, CAPE Pathway Completer validity *(New 07/01/25)*
Value Earned, CAPE Pathway Completer must be numeric: 0.00 or 0.30.
**Result:** Record Rejected

Note: Two decimal places assumed.

**Example:**
| District Number, Current Instruction/Service | Florida Education Identifier | Value Earned, CAPE Pathway Completer |
|---|---|---|
| 35 | FL340945895737 | 030 |
| 35 | FL340945895738 | 000 |
| *35 | FL340945895739 | 050 |

The first two records would be loaded assuming no other reject rule would cause their rejection. The last record would be rejected because Value Earned, CAPE Pathway Completer is not 0.00 or 0.30.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Value Earned, CAPE Pathway Completer and resubmit the record.

### 26. Value Earned, Early College Program Dual Enrollment validity *(Updated 06/05/26)*
Value Earned, Early College Program Dual Enrollment must be numeric and must equal 0.00, 0.16, 0.32, 0.48, 0.64, 0.80, 0.96, 1.12, 1.28, 1.44, 1.60, 1.76, 1.92, 2.08, 2.24, 2.40, 2.56, 2.72, 2.88, 3.04; 3.20.
**Result:** Record Rejected

Note: Two decimal places assumed.

**Example:**
| District Number, Current Instruction/Service | Florida Education Identifier | Value Earned, Early College Program Dual Enrollment |
|---|---|---|
| 35 | FL340945895737 | 016 |
| 35 | FL340945895738 | 000 |
| *35 | FL340945895739 | 050 |

The first two records would be loaded assuming no other reject rule would cause their rejection. The last record would be rejected because Value Earned, Early College Program Dual Enrollment is not 0.00 or 0.16.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Value Earned, Early College Program Dual Enrollment and resubmit the record.

### 27. Value Earned, Non Early College Program Dual Enrollment validity *(Updated 06/05/26)*
Value Earned, Non Early College Program Dual Enrollment must be numeric and must equal 0.00, 0.08, 0.16, 0.24, 0.32, 0.40, 0.48, 0.56, 0.64, 0.72, 0.80, 0.88, 0.96, 1.04, 1.12, 1.20, 1.28, 1.36, 1.44, 1.52, 1.60.
**Result:** Record Rejected

Note: Two decimal places assumed.

**Example:**
| District Number, Current Instruction/Service | Florida Education Identifier | Value Earned, Non Early College Program Dual Enrollment |
|---|---|---|
| 35 | FL340945895737 | 008 |
| 35 | FL340945895738 | 000 |
| *35 | FL340945895739 | 050 |

The first two records would be loaded assuming no other reject rule would cause their rejection. The last record would be rejected because Value Earned, Non Early College Program Dual Enrollment is not 0.00 or 0.08.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Value Earned, Non Early College Program Dual Enrollment and resubmit the record.

---

## State Validation

### 40. Early Graduates value requires matching End of Year diploma type *(Updated 07/01/25)*
If Value Earned, Early graduates is greater than zero, then a Student End of Year Status record must exist and the Diploma Type on the Student End of Year Status record must be W06, WFT, or WRW. The records should match based on District Number, Current Enrollment; Florida Education Identifier; Survey Period, and Year.
**Result:** State Validation

**Example:**

Student End of Year Status records:
| District Number, Current Enrollment | Florida Education Identifier | Diploma Type |
|---|---|---|
| 36 | FL340945895734 | W06 |
| *36 | FL340945895735 | W6A |
| *36 | FL340945895736 | ZZZ |

Student Additional Funding records:
| District Number, Current Enrollment | Florida Education Identifier | Value Earned, Early Graduates |
|---|---|---|
| 36 | FL340945895734 | 0.2500 |
| *36 | FL340945895735 | 0.2500 |
| *36 | FL340945895736 | 0.2500 |

The second and third records would cause a message to be generated because the Value Earned, Early Graduates is greater than zero and the Diploma Type codes are not W06, WFT or WRW.

**District Responsibility:** The district must review the Diploma Type codes and the Value Earned, Early Graduates amounts and correct the items that are in error. The district must then resubmit the records.

### 41. Matching Student Demographic record required
Each Student Additional Funding record must have a matching Student Demographic record based on District Number, Current Instruction/Service; Florida Education Identifier; Survey Period Code and School Year.
**Result:** State Validation

**Example:**

Student Additional Funding records:
| District Number, Current Instruction/Service | Florida Education Identifier | Survey Period Code | Year |
|---|---|---|---|
| 01 | FL340945895734 | 5 | **** |
| *01 | FL340945895735 | 5 | **** |
| 01 | FL340945895736 | 5 | **** |

Student Demographic records:
| District Number, Current Instruction/Service | Florida Education Identifier | Survey Period Code | Year |
|---|---|---|---|
| 01 | FL340945895734 | 5 | **** |
| 01 | FL340945895735 | 5 | **** |

**** = Valid fiscal year for data submission. The Student Additional Funding record marked with an asterisk would cause a message to be generated because it does not have a matching Student Demographic record.

**District Responsibility:** The district must delete the Student Additional Funding record or add a Student Demographic record to match the above key fields.

---

## Exception Reports

### 60. AICE value requires matching AICE course *(Updated 07/01/25)*
If the FTE amount is greater than zero for either of the following data elements:
- Value Earned: Advanced International Certificate of Education Diploma
- Value Earned: Advanced International Certificate of Education Score

then the student must have a Student Course Schedule record with a course number that matches a course identified in the Course Code Directory (AICE_) as an Advanced International Certificate of Education (AICE) course in Surveys 2 or 3 of the current school year. The District Number, Current Instruction/Service, School Number, Current Instruction/Service, Year and Florida Education Identifier (FLEID) on the Student Additional Funding format must match the Student Course Schedule format for Survey 2 or 3 records only.
**Result:** Exception Report

**Example:**

Student Additional Funding records:
| District Number, Current Instruction/Service | Florida Education Identifier | Survey Period Code | Year | Value Earned: AICE Score |
|---|---|---|---|---|
| 36 | FL340945895734 | 5 | **** | 0.12 |
| *36 | FL340945895735 | 5 | **** | 0.12 |

Student Course Schedule record:
| District Number, Current Instruction/Service | Florida Education Identifier | Survey Period Code | Year | Course Number |
|---|---|---|---|---|
| 36 | FL340945895734 | 3 | **** | 1202360 |

**** = Valid fiscal year for data submission. The first record would pass this edit. The second record would not pass because the Value Earned: Advanced International Certificate of Education Score is greater than zero and the student does not have a Student Course Schedule record with a course number identified in the Course Code Directory for AICE courses in Surveys 2 or 3 of the current school year.

**District Responsibility:** The district must verify that the student took an Advanced International Certificate of Education (AICE) course. If the student did not take an AICE course, then the district must correct the Value Earned: Advanced International Certificate of Education Score on the Student Additional Funding record.

### 61. IB value requires matching IB course *(Updated 07/01/25)*
If the FTE amount is greater than zero for either of the following data elements:
- Value Earned: International Baccalaureate Diploma
- Value Earned: International Baccalaureate Score

then the student must have a Student Course Schedule record with a course number that matches a course identified in the Course Code Directory (IB_) as an International Baccalaureate (IB) course in Surveys 2 or 3 of the current school year. The District Number, Current Instruction/Service, School Number, Current Instruction/Service, Year, and Florida Education Identifier (FLEID) on the Student Additional Funding format must match the Student Course Schedule format for Survey 2 or 3 records only.
**Result:** Exception Report

**Example:**

Student Additional Funding records:
| District Number, Current Instruction/Service | Florida Education Identifier | Survey Period Code | Year | Value Earned: IB Diploma |
|---|---|---|---|---|
| 36 | FL340945895734 | 5 | **** | 0.30 |
| *36 | FL340945895735 | 5 | **** | 0.30 |

Student Course Schedule record:
| District Number, Current Instruction/Service | Florida Education Identifier | Survey Period Code | Year | Course Number |
|---|---|---|---|---|
| 36 | FL340945895734 | 3 | **** | 0114860 |

**** = Valid fiscal year for data submission. The first record would pass this edit. The second record would not pass because the Value Earned: International Baccalaureate Diploma is greater than zero and the student does not have a Student Course Schedule record with a course number identified in the Course Code Directory for IB courses in Surveys 2 or 3 of the current school year.

**District Responsibility:** The district must verify that the student took an International Baccalaureate (IB) course. If the student did not take an IB course, then the district must correct the Value Earned: International Baccalaureate Diploma on the Student Additional Funding record.

### 62. AP value requires matching AP course, with district/school-specific survey windows *(Updated 07/01/2026)*
If Value Earned, College Entrance Examination Board Advanced Placement Test or Value Earned, College Board Advanced Placement Capstone Diploma is greater than zero, and:
- If District Number, Current Instruction/Service does not equal 71, then the student must have a Student Course Schedule record with a course number that matches a course identified in the Course Code Directory (AP_) as an Advanced Placement (AP) course in Surveys 2 or 3 of the current school year, or
- If District Number, Current Instruction/Service equals 71 and School Number, Current Instruction Service equals 0300 or 0400 or 0801, then the student must have a Student Course Schedule record with a course number that matches a course identified in the Course Code Directory (AP_) as an Advanced Placement (AP) course in Surveys 2, 3 or 4 of the current school year, or
- If District Number, Current Instruction is equal to 71 and School Number, Current Instruction/Service equal 0500, 0600, or 0700 then the student must have a Student Course Schedule record with a course number that matches a course identified in the Course Code Directory (AP_) as an Advanced Placement (AP) course in Surveys 1, 2, 3, or 4 of the current school year.
- The District Number, Current Instruction/Service, School Number, Current Instruction/Service, Year, and Florida Education Identifier (FLEID) on the Student Additional Funding format must match the Student Course Schedule format record.
**Result:** Exception Report

**Example:**

Student Additional Funding records:
| District Number, Current Instruction/Service | Florida Education Identifier | Survey Period Code | Year | Value Earned: CEEB AP Test |
|---|---|---|---|---|
| 36 | FL340945895734 | 5 | **** | 0.24 |
| *36 | FL340945895735 | 5 | **** | 0.24 |

Student Course Schedule record:
| District Number, Current Instruction/Service | Florida Education Identifier | Survey Period Code | Year | Course Number |
|---|---|---|---|---|
| 36 | FL340945895734 | 3 | **** | 0708400 |

**** = Valid fiscal year for data submission. The first record would pass this edit. The second record would not pass because the Value Earned: College Entrance Examination Board (CEEB) Advanced Placement Test is greater than zero and the student does not have a Student Course Schedule record with a course number identified in the Course Code Directory for AP course in Surveys 2 or 3 of the current school year.

**District Responsibility:** The district must verify that the student took an Advanced Placement (AP) course. If the student did not take an AP course, then the district must correct the Value Earned: College Entrance Examination Board Advanced Placement Test or Value Earned, College Board Advanced Placement Capstone Diploma amount on the Student Additional Funding record.

### 63. FTE Earned, Dual Enrollment Course requires matching Dual Enrollment Indicator *(Deleted 07/01/25)*
If FTE Earned, Dual Enrollment Course is greater than zero: then the student must have a Student Course Schedule record with a Dual Enrollment Indicator = "A", "B", "C", or "E" in Surveys 2 or 3 of the current school year. The Year, District Number, Current Instruction/Service and the Florida Education Identifier on the Student Additional Funding format must match the Student Course Schedule format for Survey 2 or 3 records only.
**Result:** Exception Report

**Example:**

Student Additional Funding records:
| District Number, Current Instruction/Service | Florida Education Identifier | Survey Period Code | Year | FTE Earned, Dual Enrollment Course |
|---|---|---|---|---|
| 36 | FL340945895734 | 5 | **** | 016 |
| *36 | FL340945895735 | 5 | **** | 008 |

Student Course Schedule record:
| District Number, Current Instruction/Service | Florida Education Identifier | Survey Period Code | Year | Dual Enrollment Indicator |
|---|---|---|---|---|
| 36 | FL340945895734 | 3 | **** | E |
| 36 | FL340945895735 | 2 | **** | Z |

**** = Valid fiscal year for data submission. The first record would pass this edit. The second record would not pass because the FTE Earned, Dual Enrollment Course is equal to 008 and the student does not have a Student Course Schedule record with a Dual Enrollment Indicator equal to "A", "B", "C", or "E" in Surveys 2 or 3 of the current school year.

**District Responsibility:** The district must verify that the student took a dual enrollment course where the Dual Enrollment Indicator equals "A", "B", "C", or "E". If the student did not take a dual enrollment course, then the district must correct the FTE Earned, Dual Enrollment Course on the Student Additional Funding record.

### 64. Academic Dual Enrollment Associate Degree value requires matching Dual Enrollment Indicator *(Updated 07/01/25)*
If Value Earned, Academic Dual Enrollment Associate Degree equals 030: then the student must have a Student Course Schedule record with a Dual Enrollment Indicator = "A" or "E" in Surveys 2 or 3 of the current school year. The Year, District Number, Current Instruction/Service and the Florida Education Identifier on the Student Additional Funding format must match the Student Course Schedule format for Survey 2 or 3 records only.
**Result:** Exception Report

**Example:**

Student Additional Funding records:
| District Number, Current Instruction/Service | Florida Education Identifier | Survey Period Code | Year | FTE Earned, Academic Dual Enrollment Course |
|---|---|---|---|---|
| 36 | FL340945895734 | 5 | **** | 030 |
| *36 | FL340945895735 | 5 | **** | 030 |

Student Course Schedule record:
| District Number, Current Instruction/Service | Florida Education Identifier | Survey Period Code | Year | Dual Enrollment Indicator |
|---|---|---|---|---|
| 36 | FL340945895734 | 3 | **** | E |
| 36 | FL340945895735 | 2 | **** | Z |

**** = Valid fiscal year for data submission. The first record would pass this edit. The second record would not pass because the Value Earned, Academic Dual Enrollment Associate Degree is equal to 030 and the student does not have a Student Course Schedule record with a Dual Enrollment Indicator equal to "A" or "E" in Surveys 2 or 3 of the current school year.

**District Responsibility:** The district must verify that the student took an academic dual enrollment course where the Dual Enrollment Indicator equal to "A" or "E". If the student did not take an academic dual enrollment course, then the district must correct the FTE Earned, Academic Dual Enrollment Associate Degree on the Student Additional Funding record.
