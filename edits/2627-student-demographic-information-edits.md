# Student Demographic — Edits and Reject Rules

Source: https://www.fldoe.org/file/20909/2627sd.pdf
Manual: Student Database 2026-2027

This document covers edits across four categories: Reject Rules (record rejected), State Validation (cross-format matching), Exception Reports (advisory), and Aggregate Exception/Validation Reports (school- or district-level checks). Edit numbering is non-sequential; gaps and alphanumeric IDs (1A-1G, 4A-4B, 5A-5G) are as published in the source. Many edits note "This edit does not apply to Survey Period 6" — that qualifier is preserved inline where it appears in the source.

---

## Reject Rules

### 1. District Number, Current Instruction/Service correctness
District Number, Current Instruction/Service must be correct for the district submitting the data.
**Result:** Record Rejected

**Example:**
| District Number, Current Instruction/Service | School Number, Current Enrollment | Florida Education Identifier |
|---|---|---|
| 01 | 0021 | FL123456789100 |
| 01 | 0021 | FL123456789200 |
| *02 | 0021 | FL123456789300 |

The first two records would be loaded assuming no other reject rule would cause their rejection. The third record would be rejected since the District Number, Current Instruction/Service is 02 rather than 01 (the district submitting the record).

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number, Current Instruction/Service and resubmit the record.

### 2. District Number, Current Enrollment range and active status *(Updated 07/01/2026)*
District Number, Current Enrollment must be numeric and active (A) on the Appendix C: District Name Table.
**Result:** Record Rejected

**Example:**
| District Number, Current Enrollment | School Number, Current Enrollment | Florida Education Identifier |
|---|---|---|
| 01 | 0021 | FL123456789200 |
| 01 | 0021 | FL123456789300 |
| *00 | 0021 | FL123456789000 |

The first two records would be loaded assuming no other reject rule would cause their rejection. The third record would be rejected since the District Number, Current Enrollment is not in the appropriate range.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number, Current Enrollment and resubmit the record.

### 3. School Number, Current Enrollment range by Survey Period
If Survey Period Code is 1-4 or 9, School Number, Current Enrollment must be numeric in the range 0001 to 9899 (excluding 3900, 7006 and 9001) or it must be 9992, 9993, 9997, N998 or N999. If Survey Period Code is 5, it must additionally allow 9995. If Survey Period Code is 6, School Number Current Enrollment must be numeric in the range 0001 to 9899 (excluding 3900, 7006 and 9001), with no alpha exceptions.
**Result:** Record Rejected

**Example:**
| District Number, Current Enrollment | School Number, Current Enrollment | Florida Education Identifier |
|---|---|---|
| 01 | 0021 | FL123456789100 |
| 01 | 0021 | FL123456789200 |
| *01 | 9999 | FL123456789300 |
| *01 | C901 | FL123456789400 |
| *01 | 3900 | FL123456789500 |

The first two records would be loaded assuming no other reject rule would cause their rejection. The third would be rejected because the School Number, Current Enrollment is not in range; the fourth because it is not numeric, N998 or N999; the fifth because it is excluded from the range.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Current Enrollment and resubmit the records.

### 5. Survey Period Code must be 1, 2, 3, 4, 5, 6 or 9
Survey Period Code must be 1, 2, 3, 4, 5, 6 or 9 and must be correct for the submission specified by the district.
**Result:** Record Rejected

**Example:** The Survey Period Code as specified in the transmission JCL is identified as Survey Period "2". However, records on the transmission have a Survey Period Code "3". All updates, adds or deletes with this inconsistency would be rejected.

**District Responsibility:** The Survey Period Code must be corrected either on the records coming in or the Transmission JCL and all records must be resubmitted.

### 6. Year correctness
Year must be correct for the submission specified by the district.
**Result:** Record Rejected

**Example:** The Year as specified in the transmission JCL is identified as "0001". However, records on the transmission have Year coded as "0102". All updates, adds or deletes with this inconsistency would be rejected.

**District Responsibility:** The district must correct the Year either on the records coming in or the Transmission JCL and resubmit all the records.

### 8. Transaction Code validity
The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified then the record must not already exist on the database; if C or D is specified then the record must exist on the database.
**Result:** Record Rejected

**Example:** For all original transmissions, the Transaction Code must be "A". An original transaction is the first submission of a record during a survey period. After original transmission of records, changes to the record for elements other than the key elements must be done with a "C" as the Transaction Code. To delete a record, the Transaction Code must be a "D". To change key elements in a batch transaction, the record must FIRST be deleted with a "D" and then added with an "A".

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Transaction Code and resubmit the records.

### 9. Record uniqueness
Each Student Demographic record must be unique based on District Number, Current Instruction/Service; Florida Education Identifier; Survey Period Code and Year.
**Result:** Record Rejected (first record accepted, all other duplicate records rejected)

**Example:**
| District Number, Current Instruction/Service | Florida Education Identifier | Survey Period Code | Year |
|---|---|---|---|
| 01 | FL123456789100 | 2 | **** |
| *01 | FL123456789100 | 2 | **** |
| 01 | FL123456789200 | 2 | **** |
| 01 | FL123456789300 | 2 | **** |
| *01 | FL123456789300 | 2 | **** |

**** = Valid fiscal year for data submission. The first, third and fourth records would be loaded assuming no other reject rule would cause their rejection. The second and fifth records would be rejected as duplicates of the first and fourth, respectively.

**District Responsibility:** If the records that were accepted and loaded to the database are correct ones, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must delete any invalid records, correct any rejected records if necessary, and resubmit the corrected records.

### 10. Student Number Identifier, Local format
The Student Number Identifier, Local may be any combination of letters, numbers and blanks. (All blanks are allowable.) It must be left-justified with trailing blanks.
**Result:** Record Rejected

**Example:**
| District Number, Current Enrollment | Student Number Identifier, Local |
|---|---|
| 01 | 0123456789 |
| 01 | ABC123DEF9 |
| 01 | 3001 28K |
| *01 | 2121@xyz |
| *01 | 123456 |

The first three records would be loaded assuming no other edit would cause their rejection. The fourth record would be rejected because it contains a symbol (@). The fifth record would be rejected because it is right-justified rather than left-justified.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Student Number Identifier, Local and resubmit the records.

### 11. Institution Number, Neglected/Delinquent range by Survey Period
If Survey Period is 5 or 9, Institution Number, Neglected/Delinquent (First/Second/Third) must be numeric in the range 0000 to 9899 or a district-assigned 3-digit number preceded by an A. If Survey Period is not 5 or 9, Institution Number, Neglected/Delinquent must be 0000. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:**
| District Number, Current Enrollment | Survey Period Code | Institution Number, Neglected/Delinquent | Florida Education Identifier |
|---|---|---|---|
| 01 | 2 | 0000 | FL340945895734 |
| 01 | 5 | A006 | FL004583948567 |
| *01 | 9 | 9999 | FL000000000000 |
| *01 | 2 | A006 | FL000000000001 |

The first two records would be loaded assuming no other reject rule would cause their rejection. The third would be rejected because the number is not in the appropriate numerical range. The fourth would be rejected because Survey Period is 2 and the number is not 0000.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Institution Number, Neglected/Delinquent and resubmit the records.

### 12. Institution Number, Neglected/Delinquent must be a valid institution
If the Institution Number, Neglected/Delinquent (First/Second/Third) is not 0000 then it must be a valid institution for neglected/delinquent children in the District of Enrollment. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:** Two of four example records would be loaded assuming no other reject rule would cause their rejection. Two records would be rejected because the institution numbers are not on the Department of Education's list of valid institutions for neglected or delinquent children.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Institution Number, Neglected/Delinquent and resubmit the records or supply correct information about the qualifications of these institutions to the designated contact person at the Department of Education so that these institutions can be added to the list of valid institutions.

### 13. Institution Number, Neglected/Delinquent zero-fill cascade
If Institution Number, Neglected/Delinquent (First) is 0000 then Institution Number, Neglected/Delinquent (Second) must also be 0000. If Institution Number, Neglected/Delinquent (First) or (Second) is 0000 then Institution Number, Neglected/Delinquent (Third) must be 0000. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:**
| District Number, Current Enrollment | Institution Number, Neglected/Delinquent (First) | Institution Number, Neglected/Delinquent (Second) | Institution Number, Neglected/Delinquent (Third) |
|---|---|---|---|
| 01 | 0701 | 0000 | 0000 |
| 01 | A006 | 5678 | 9876 |
| *01 | 0000 | 3456 | 5432 |

The first two records would be loaded assuming no other reject rule would cause their rejection. The third record would be rejected because Institution Number (First) is 0000 while (Second) and (Third) contain an institution number.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct Institution Number, Neglected/Delinquent (First), (Second) and/or (Third) and resubmit the record.

### 14. School Number, Current Enrollment 9997 required for Grade 30/31 at Survey 2/3
If Survey Period is 2 or 3 and Grade Level is 30 or 31, then School Number, Current Enrollment must be 9997.
**Result:** Record Rejected

**Example:**
| District Number, Current Enrollment | School Number, Current Enrollment | Florida Education Identifier | Survey Period Code | Grade Level |
|---|---|---|---|---|
| 01 | 9997 | FL123456789001 | 2 | 30 |
| *01 | 0021 | FL123456789002 | 2 | 30 |

The first record would be loaded assuming no other reject rule would cause its rejection. The second record would be rejected because School Number, Current Enrollment is not 9997 for a student in Grade Level 30.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the School Number, Current Enrollment or the Grade Level and resubmit the record.

### 15. Migrant Status Term birth date range *(Updated 07/01/2026)*
If Migrant Status Term is B, D, E, S, T, U, V, W or X, then Birth Date must be 09012004 through 08312027 inclusive. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:**
| Florida Education Identifier | Survey Period Code | Year | Migrant Status Term | Birth Date |
|---|---|---|---|---|
| *FL123456789000 | 5 | **** | D | 09141983 |
| FL123456789001 | 5 | **** | S | 01092008 |
| FL123456789002 | 5 | **** | B | 10192012 |

**** = Valid fiscal year for data submission. The first record would be rejected because the Birth Date is not in the acceptable range. The second and third would be loaded assuming no other reject rule would cause their rejection.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Birth Date or the Migrant Status Term and resubmit the record.

### 16. District Number, Zoned School by Survey Period *(Updated 07/01/2026)*
If Survey Period Code = 1, 4, 5 or 9, then District Number, Zoned School must be filled with zeroes. If Survey Period Code = 2 or 3, then District Number, Zoned School must be 01-67. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:**
| Survey Period Code | District Number, Zoned School | School Number, Zoned School |
|---|---|---|
| 01 | 00 | 0000 |
| 02 | 12 | 0161 |
| *03 | 69 | 0114 |

The first two records would be loaded assuming no other reject rule would cause their rejection. The third record would be rejected because District Number, Zoned School is outside the specified range.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the District Number, Zoned School and resubmit the records.

### 17. School Number, Zoned School validity
If Survey Period Code = 1, 4, 5 or 9, then School Number, Zoned School must be filled with zeroes. If Survey Period Code = 2 or 3 and a specified set of conditions apply (District of Instruction not 71, School of Enrollment in valid range excluding certain virtual codes, School Function/Setting not D on MSID, Charter School Status Z, Grade Level KG-12, Accountability ESE Center Y or Primary Service Type B, and Neglected/Delinquent Status not D or N on MSID), then School Number, Zoned School must be an active school for the District Number, Zoned School on the Master School Identification file, unless District of Instruction or District of Enrollment is 68 or 83 in which case it can also be zeroes. Any other School Number, Zoned School must be an active school on MSID or reported as all zeros. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:**
| Survey Period Code | District Number, Zoned School | School Number, Zoned School |
|---|---|---|
| 3 | 00 | 0000 |
| 2 | 12 | 0161 |
| *1 | 00 | 0345 |
| *3 | 02 | 9990 |

The first two records would be loaded assuming no other reject rule would cause their rejection. The third record would be rejected since the School Number, Zoned School is not zero-filled for survey 1. The fourth record would be rejected since the School Number, Zoned School is not a valid number on MSID.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Zoned School and resubmit the records.

### 18. Grade Level / age association
If School Number, Current Enrollment is not 9992, 9993, 9995 or 9997, then there must be a valid association between Grade Level and the student's age (determined per survey period as specified in the source table: for Surveys 1-4 at Date Certain of the survey period; Survey 5 at Date Certain of Survey 3; Survey 6 at the Survey Due Date; Survey 9 at Date Certain of Survey 2). Valid age ranges per Grade Level run from PK (not equal to 9+) through Grade 12 (not equal to 0-4, 30+).
**Result:** Record Rejected

**Example:**
| Florida Education Identifier | Year | Survey Period Code | Grade Level | Birth Date |
|---|---|---|---|---|
| *FL340945895734 | 1011 | 2 | 02 | 02021994 |
| FL004583948567 | 1011 | 2 | 08 | 05062003 |
| FL000000000000 | 1011 | 2 | PK | 12022010 |
| *FL340945895735 | 1011 | 2 | 12 | 08172014 |

Records without an asterisk would be loaded assuming no other reject rule would cause their rejection. Records marked with an asterisk would be rejected because of the invalid association between Grade Level and Birth Date.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Grade Level or Birth Date so that there is a valid relationship between these two data elements and resubmit the records.

### 19. Date Entered United States School validity
If Survey Period Code is 1-4 or 5, and English Language Learners, PK-12 code = LY or LP, and Grade Level is not PK, then Date Entered United States School must be numeric and a valid date in the format MMDDYYYY. It may be 00000000 for all others. For Survey Period 9, Date Entered United States School must be 00000000. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:** All three example records would be rejected: one because the date is not numeric, one because the date is 00000000 with ELL code LY, and one because the date is invalid.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct Date Entered United States School or English Language Learners, PK-12 and resubmit the records.

### 1A. Ethnicity code validity
Ethnicity code must be Y or N. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:** Two example records would be rejected — one for an invalid code, one for a blank code.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Ethnicity code and resubmit the records.

### 1B. Race codes validity
Race: American Indian or Alaska Native, Race: Asian, Race: Black or African American, Race: Native Hawaiian or Other Pacific Islander, and Race: White codes must be Y or N. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:** A record with invalid or blank codes for multiple Race fields would be rejected.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Race codes and resubmit the record.

### 1C. At least one Race code must be Y
At least one Race code (American Indian or Alaska Native, Asian, Black or African American, Native Hawaiian or Other Pacific Islander, or White) must be Y. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:** A record with N for all five Race codes would be rejected.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must code at least one of the Races with a Y and resubmit the record.

### 1E. School Number 7004 requires Grade Level KG-12
If School Number, Current Enrollment is 7004 then Grade Level must be KG through 12. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:**
| District Number, Current Enrollment | School Number, Current Enrollment | Grade Level |
|---|---|---|
| 04 | 7004 | 06 |
| *04 | 7004 | PK |
| 04 | 7004 | 10 |

The first and third records would be loaded assuming no other reject rule would cause their rejection. The second would be rejected since the Grade Level is not in the appropriate range.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Grade Level and resubmit the record.

### 1F. Item 4 - Filler must be all spaces
Item 4 - Filler on this format in position numbers 9-18 must be all spaces.
**Result:** Record Rejected

**Example:**
| District Number, Current Enrollment | School Number, Current Enrollment | Filler, Item #4 |
|---|---|---|
| 01 | 0151 | |
| *01 | 0151 | 265456789X |

The first record would be loaded assuming no other reject rule would cause its rejection. The second record would be rejected because the data reported is not all spaces.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must fill the positions noted with all spaces and resubmit the record.

### 1G. Item 7 - Filler must be all spaces
Item 7 - Filler on this format in position numbers 24-33 must be all spaces.
**Result:** Record Rejected

**Example:** Same pattern as Item 4 - Filler (Edit 1F), applied to Item 7.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must fill the positions noted with all spaces and resubmit the record.

### 20. Student Name, Legal: Last Name must not be blank
The Student Name, Legal: Last Name must not be blank (Z-fill is NOT allowed). Allowable characters include double or single quotation marks, commas, slashes, periods, parentheses, hyphens and accent marks.
**Result:** Record Rejected

**Example:** A record with a blank Last Name is rejected.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Student Name, Legal: Last Name and resubmit the record.

### 21. Student Name, Legal: First Name must not be blank
The Student Name, Legal: First Name must not be blank (Z-fill is NOT allowed). Allowable characters include double or single quotation marks, commas, slashes, periods, hyphens and accent marks. Middle name/appendage may be blank but must not include non-displayable characters.
**Result:** Record Rejected

**Example:** A record with a blank First Name is rejected.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Student Name, Legal: First Name and resubmit the record.

### 22. Birth Date validity
If School Number, Current Enrollment is not 9995, then Birth Date must be numeric and a valid date in the format MMDDYYYY.
**Result:** Record Rejected

**Example:** Records with a non-numeric or invalid Birth Date are rejected.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Birth Date and resubmit the records.

### 23. Sex code validity
Sex code must be M or F.
**Result:** Record Rejected

**Example:** A record with an invalid code and a record with a blank code are both rejected.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the sex code and resubmit the records.

### 26. Zoned School District/School Number cross-check
If Survey Period Code = 2 or 3 and School Number, Zoned School is greater than 0000, then District Number, Zoned School must be greater than 00. If the District Number, Zoned School is greater than 00, then School Number, Zoned School must be greater than 0000. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:**
| Survey Period Code | District Number, Zoned School | School Number, Zoned School |
|---|---|---|
| 03 | 01 | 0602 |
| *02 | 00 | 0604 |

The first record would be loaded assuming no other reject rule would cause its rejection. The second record would be rejected because District Number, Zoned School is not greater than 00 for a School Number, Zoned School that is greater than zero.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number, Zoned School or School Number, Zoned School and resubmit the record.

### 27. English Language Learners, PK-12 code validity
If Survey Period is 1, 2, 3, 4, 5, or 9, English Language Learners, PK-12 code must be LA, LY, LF, LP, LZ, or ZZ. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:** A record with an invalid code and a record with a blank code are both rejected.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the English Language Learners, PK-12 codes and resubmit the records.

### 28. Resident Status, State/County validity by Survey Period and Grade Level
If Survey Period Code is 5 or 9 and School Number, Current Enrollment is not 9995, code must be 0, A, B, 2, 3, 4, 5, 6 or 7. If Survey Period Code is 1-4, Grade Level is not 30 or 31, and School Number, Current Enrollment is not 9995, code must be 0, A, B, 2 or 3. If Survey Period Code is 2 or 3, Grade Level is 30 or 31, and School Number, Current Enrollment is not 9995, code must be 4, 5, 6 or 7. If School Number, Current Enrollment = 9995, code must be Z. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:** A record with an invalid code and a record with a blank code are both rejected.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Resident Status, State/County codes and resubmit the records.

### 29. Grade Level code validity by Survey Period
If Survey Period Code = 1, 4, 6, or 9, Grade Level code must be PK, KG, or 01-12. If Survey Period Code = 9, Grade Level may also = 30 if Institution Number, Neglected/Delinquent (First) does not = 0000. If Survey Period Code = 2, 3 or 5, Grade Level code must be PK, KG, 01-12, 30 or 31.
**Result:** Record Rejected

**Example:** A record with an invalid code and a record with a blank code are both rejected.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Grade Level codes and resubmit the records.

### 30. Student Characteristic, Agency Programs code validity
If Survey Period Code is 1-4, 5 or 9, Student Characteristic, Agency Programs code must be A, C or Z. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:** Records with invalid codes (e.g., P, 0) are rejected.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Student Characteristic, Agency Programs codes and resubmit the records.

### 31. Graduation Option validity by Grade Level, School, and District
If Survey Period Code is 1-5 or 9; Grade Level equals 9-12; School Number, Current Enrollment does not equal 9992, 9993, 9995, 9997, N998, N999, 3450, 3950; or both District Number, Current Instruction/Service and District Number, Current Enrollment equal 71, then Graduation Option code must be 1, 4, 7, 8, 9, A, B, C, or D. If School Number, Current Enrollment is one of the excluded codes above, or District Number, Current Instruction/Service equals 71 and District Number, Current Enrollment does not equal 71, then Graduation Option code must be Z. If Grade Level equals PK-8, 30, or 31, then Graduation Option code must be Z. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:**
| District Number, Current Enrollment | School Number, Current Enrollment | Florida Education Identifier | Grade Level | Graduation Option |
|---|---|---|---|---|
| 01 | 0001 | FL123456789001 | 10 | 1 |
| 01 | 0001 | FL123456789002 | 07 | Z |
| *01 | 0001 | FL123456789003 | 11 | Z |
| *01 | 3450 | FL123456789004 | 12 | 1 |

The first two records would be loaded assuming no other reject rule would cause their rejection. The third would be rejected because Graduation Option does not equal 1-9. The fourth would be rejected because Graduation Option does not equal Z.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Grade Level, School Number, Current Enrollment, or Graduation Option so that the proper relationship exists, and resubmit the records.

### 33. Qualifying Arrival Date (QAD) validity
Qualifying Arrival Date (QAD) for Migrant Program Eligibility must be numeric and a valid date or must be all zeroes. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:** Three of four example records would be loaded assuming no other reject rule would cause their rejection. One record would be rejected because the QAD is not a valid date.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Qualifying Arrival Date (QAD) for Migrant Program Eligibility and resubmit the record.

### 34. Residence County code validity
If School Number, Current Enrollment is not 9995, then Residence County code must be 01-67 or 99. If School Number, Current Enrollment is 9995, then Residence County code must be 00. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:** A record with an invalid code and a record with a blank code are both rejected.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Residence County codes and resubmit the records.

### 35. Lunch Status validity
If School Number, Current Enrollment is not 9992, 9993, or 9995, then Lunch Status must be 0, 1, 3, 4, C, D, E, F, N or R. If School Number, Current Enrollment is 9992, 9993, or 9995, then Lunch Status must be Z. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:** Two example records with invalid codes are both rejected.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Lunch Status codes and resubmit the records.

### 36. Migrant Status Term code validity
Migrant Status Term code must be B, D, E, S, T, U, V, W, X or Z. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:** A record with a blank code and a record with an invalid code are both rejected.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Migrant Status Term code and resubmit the records.

### 37. QAD requirements by Migrant Status Term
If Migrant Status Term is B, D, E, S, T, U, V, W or X, Qualifying Arrival Date (QAD) for Migrant Program Eligibility must be numeric and a valid date. If Migrant Status Term equals Z, then QAD must be all zeros. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:** Two of four example records would be loaded assuming no other reject rule would cause their rejection. One record would be rejected because QAD is not a valid date; one because QAD is all zeroes with a non-Z Migrant Status Term.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Qualifying Arrival Date (QAD) for Migrant Program Eligibility and resubmit the records.

### 38. QAD date range *(Updated 07/01/2026)*
If Migrant Status Term is B, D, E, S, T, U, V, W or X, then Qualifying Arrival Date (QAD) for Migrant Program Eligibility must be greater than or equal to 9/1/2023 and less than or equal to 08/31/2027. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:** One of three example records would be rejected because the QAD is not less than or equal to 8/31/2026 [as stated in source example]; the other two would be loaded assuming no other reject rule would cause their rejection.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Qualifying Arrival Date (QAD) for Migrant Program Eligibility and resubmit the record.

### 39. Residence County 99 requires Resident Status 0 or 2 for PK-12
If Residence County code is 99 and Grade Level is PK-12, then Resident Status, State/County code must be 0 or 2. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:** Two of three example records would be rejected because the Resident Status code is invalid for the Residence County reported; the third would be loaded assuming no other reject rule would cause its rejection.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Residence County codes or the Resident Status, State/County codes and resubmit the records.

### 40. School Number, Current Enrollment validity against Master School Identification File
If the School Number, Current Enrollment is not 9992, 9993, 9995, N998, N999, 3450 or 3950, then it must exist on the Master School Identification File as a valid active school (active in the current school year) in the district of enrollment.
**Result:** Record Rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the School Number, Current Enrollment and resubmit the record.

### 41. Birth Date range validity by School Number and Migrant Status *(Updated 07/01/2026)*
If School Number, Current Enrollment is not 9995, then Birth Date must be less than or equal to the survey due date. If School Number, Current Enrollment is 9995, Survey Period Code is not 6, and Migrant Status Term is Z, then Birth Date must be 00000000. If School Number, Current Enrollment is 9995, Survey Period Code is not 6, and Migrant Status Term is not Z, then Birth Date must be 09012004 through 08312027 inclusive.
**Result:** Record Rejected

**Example:** One of three example records would be rejected because the Birth Date is not less than the Survey Date; the other two would be loaded assuming no other reject rule would cause their rejection.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Birth Date and resubmit the record.

### 42. Resident Status A prohibits matching District/Residence County
If Resident Status, State/County is A, then District Number, Current Enrollment and Residence County must not be the same. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:** One of two example records would be rejected because District Number, Current Enrollment and Residence County are the same; the other would be loaded assuming no other edit would cause its rejection.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number, Current Enrollment, Residence County, or Resident Status, State/County code and resubmit the record.

### 43. Native Language, Student validity
If School Number, Current Enrollment is not 9992, 9993, or 9995, then Native Language, Student must be a valid language code, containing no blanks. If School Number, Current Enrollment is 9992, 9993, or 9995, then Native Language, Student code must be ZZ. (See Appendix N for language codes.) (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:** Two of five example records would be loaded assuming no other reject rule would cause their rejection. Three records would be rejected because the codes contain blanks or are invalid.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Native Language, Student codes and resubmit the records.

### 44. Resident Status 3 requires matching District/Residence County
If District Number, Current Enrollment is 01-67 and if Resident Status, State/County is 3, then District Number, Current Enrollment and Residence County must be the same. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:** One of two example records would be loaded assuming no other edit would cause its rejection; the other would be rejected because District Number, Current Enrollment and Residence County are not the same.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number, Current Enrollment, Residence County or Resident Status, State/County code and resubmit the record.

### 45. Primary Language Spoken in Home validity
If School Number, Current Enrollment is not 9992, 9993, or 9995, then the Primary Language Spoken in Home code must be a valid language code per Appendix N. If School Number, Current Enrollment is 9992, 9993, or 9995, then the code must be ZZ. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:** Two of four example records would be loaded assuming no other reject rule would cause their rejection. Two records would be rejected because the code is invalid.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Primary Language Spoken in Home codes and resubmit the records.

### 46. Country of Birth validity
If Grade Level = PK-12, 30 or 31, then Country of Birth must be a valid code as listed in Appendix G or Appendix Q, including ZZ. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:** Two of four example records would be loaded assuming no other reject rule would cause their rejection. Two records would be rejected because the codes are not valid.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Country of Birth codes and resubmit the records.

### 47. Additional School Year Student code validity by Grade Level
If Grade Level = 12, Additional School Year Student code must be D, S, or Z. If Grade Level is not 12, then it must be Z. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:**
| Florida Education Identifier | Grade Level | Additional School Year Student |
|---|---|---|
| FL123456789100 | 12 | S |
| *FL123456789200 | 08 | S |
| *FL123456789300 | 12 | |

The first record would be loaded assuming no other reject rule would cause its rejection. The second would be rejected because Grade Level is 08 and the code is not Z. The third would be rejected because Grade Level is 12 and the code is blank.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct either the Grade Level or the Additional School Year Student code and resubmit the records.

### 48. English Language Learners: Home Language Survey Date validity *(Updated 07/01/2026)*
If Grade Level = 30 or 31 or School Number, Current Enrollment is 9992, 9993, 9995, or 9997, then the date must be zero-filled. If School Number, Current Enrollment is not one of those codes and Grade Level = PK-12, then the date must be a valid date meeting survey-period-specific criteria: at or before date certain of survey week for Surveys 1-3 (with a 90-day extension for District of Instruction 71 mismatches); on or before June 30 for Survey 4; on or before August 31 for Survey 5; before January 1 for Survey 9. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:** Two of four example records would be loaded assuming no other reject rule would cause their rejection. Two records would be rejected because the date is invalid or inappropriately filled with zeros.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the English Language Learners: Home Language Survey Date and resubmit the records.

### 49. Native Language, Student non-ZZ requirement for PK-12
If Grade Level is PK-12 and School Number, Current Enrollment is not 9992, 9993, or 9995, then Native Language, Student must be other than ZZ. If School Number, Current Enrollment is 9992, 9993, or 9995, then it must be ZZ. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:** One of two example records would be loaded assuming no other reject rule would cause its rejection; the other would be rejected because the code is not valid for a Grade Level of PK-12.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Native Language, Student code and resubmit the record.

### 4A. Residence County must not equal 99 for District 71, School 0300/0400/0801
If District Number, Current Enrollment is 71 and School Number equals 0300, 0400 or 0801, then Residence County code must not equal 99. (This edit does not apply to Survey Period 6.)
**Result:** Record Rejected

**Example:** One of two example records would be loaded assuming no other reject rule would cause its rejection; the other would be rejected because Residence County equals 99 for District 71, School 0300.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Residence County code or the School Number, Current Enrollment and resubmit the record.

### 4B. Florida Education Identifier (FLEID) format
Florida Education Identifier (FLEID) is alphanumeric and must be entered as "FL" in the first 2 positions followed by twelve numeric digits. No blanks, spaces or all zeros for the twelve numeric digits are allowable.
**Result:** Record Rejected

**Example:**
| District Number, Current Enrollment | Florida Education Identifier |
|---|---|
| 01 | FL340945895734 |
| 01 | FL004583948567 |
| *01 | FL000000000000 |

The first two records would be loaded assuming no other reject rule would cause their rejection. The third record would be rejected because the FLEID is not valid.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Florida Education Identifier and resubmit the record for processing.

---

## State Validation

### 52. English Language Learners: Basis of Exit required for LF status
If Survey Period Code is 2, 3 or 5, English Language Learners, PK-12 is LF, there is a matching English Language Learners Information record, and there is a matching Student Course Schedule or Student End of Year Status record, then English Language Learners: Basis of Exit (First) must not = Z.
**Result:** State Validation

**District Responsibility:** The district must correct the English Language Learners: Basis of Exit (First) code and/or the English Language Learners, PK-12 code so that a valid relationship exists between the elements.

### 53. Matching English Language Learners record required for LY/LF, Grade KG-12
If Survey Period Code is 2, 3 or 5, English Language Learners, PK-12 is LY or LF, Grade Level is KG-12, and there is a matching Student Course Schedule or Student End of Year Status record, then there must be a matching English Language Learners Information record. (This edit does not apply to Survey Period 6.)
**Result:** State Validation

**District Responsibility:** The district must review the Student Demographic records and determine whether the students are English Language Learners. The district must either submit an English Language Learners record for each student or submit a revision to the English Language Learners, PK-12 element to indicate that the student is not an English Language Learner.

### 54. English Language Learners: Exit Date validity for LF status
If the English Language Learners code = LF, Survey Period Code is 2 or 3, and there is a matching Student Course Schedule record, then English Language Learners: Exit Date on the matching English Language Learners Information record must be a valid date. If the code = LF, Survey Period Code is 5, there is a matching Student End of Year Status record, and District Number, Current Enrollment equals District Number, Current Instruction/Service, the same requirement applies.
**Result:** State Validation

**District Responsibility:** The district must correct the English Language Learners: Exit Date and/or the English Language Learners code so that a valid relationship exists between the elements.

### 55. Graduation Option / Diploma Type relationship
If Survey = 5 and Diploma Type on the Student End of Year Status record = W07 or W27, then Graduation Option code must equal 4 or 7. If Survey = 5 and Diploma Type = W10, WGA or WGD, then Graduation Option code must equal 8. (This edit does not apply to Survey Period 6.)
**Result:** State Validation

**District Responsibility:** The district must correct the Student Demographic record so that the appropriate relationship exists between Graduation Option and Diploma Type.

### 56. English Language Learners: Reclassification/Exit Date recency check
If Survey Period Code is 2, 3 or 5 and the English Language Learners, PK-12 code is LF and there is a matching Student Course Schedule or Student End of Year Status record, then either the Reclassification Exit Date must be all zeros with the Exit Date within two years of the survey date, or the Reclassification Exit Date must be greater than zero and within two years of the survey date. Use the Survey Period 3 survey date for Survey Period 5 editing. If no matching English Language Learners Information record is found, no error is generated. (This edit does not apply to Survey Period 6.)
**Result:** State Validation

**District Responsibility:** The district must correct the English Language Learners: Exit Date and/or the English Language Learners, PK-12 code so that a valid relationship exists between the elements.

### 57. Exceptionality code requirements for Graduation Option 4/A/B
If Survey Period Code is 5, Graduation Option code = 4, A or B, and Prior School Status/Student Attendance Term does not equal "Y", then Exceptionality, Primary or Exceptionality, Other on the Exceptional Student record must be C, G, H, J, K, O-P, S, V or W (not T or U). If Survey Period Code is 2 or 3, Graduation Option = 4, A or B, and Withdrawal Date on the matching Prior School Status/Student Attendance record is 00000000, the same requirement applies. (This edit does not apply to Survey Period 6.)
**Result:** State Validation

**District Responsibility:** The district must correct the Student Demographic, Prior School Status/Student Attendance, or Exceptional Student records so that the appropriate relationship exists between Graduation Option; Term; Exceptionality, Primary; Exceptionality, Other; and Withdrawal Date.

### 58. Exceptionality code requirements for Graduation Option 7
If Survey Period Code is 1 or 5 and Graduation Option code = 7, then Exceptionality, Primary on the Exceptional Student record must be C, F-K, M, O-P, S, V, or W (or L if Exceptionality, Other is one of those codes). If Survey Period Code is 2, 3 or 4, there is a matching Student Course Schedule record, and Graduation Option = 7, the same requirement applies. (This edit does not apply to Survey Period 6.)
**Result:** State Validation

**District Responsibility:** The district must correct the Student Demographic or Exceptional Student records so that the appropriate relationship exists between Graduation Option; Exceptionality, Primary; and Exceptionality, Other.

### 5A. English Language Learners: Classification Date required
If Survey Period Code is 2, 3 or 5 and English Language Learners, PK-12 is LY or LF, and there is a matching English Language Learners Information record and a matching Student Course Schedule or Student End of Year Status record, then English Language Learners: Classification Date must not equal zero.
**Result:** State Validation

**District Responsibility:** The district must correct the English Language Learners: Classification Date and/or the English Language Learners, PK-12 code so that a valid relationship exists between the elements.

### 5B. English Language Learners: Basis of Entry required
If Survey Period Code is 2, 3 or 5 and English Language Learners, PK-12 is LY or LF, and there is a matching English Language Learners Information record and a matching Student Course Schedule or Student End of Year Status record, then the English Language Learners: Basis of Entry code must not = Z.
**Result:** State Validation

**District Responsibility:** The district must correct the English Language Learners: Basis of Entry code and/or the English Language Learners, PK-12 code so that a valid relationship exists between the elements.

### 5C. School Number, Zoned School restrictions for Exceptionality M
If Survey Period code is 2 or 3, Grade Level is not PK, Exceptionality Primary or Other = M on the Exceptional Student record, and District of Instruction is not 71, then School Number, Zoned School must be in the range 0001-9899 but not 7001, 7004, 7006, 7023. (This edit does not apply to Survey Period 6.)
**Result:** State Validation

**District Responsibility:** The district must correct the District Number, Zoned School and School Number, Zoned School data on the Student Demographic records so that the appropriate relationship exists with the Exceptionality codes on the Exceptional Student records.

### 5D. Date Entered United States School required for Immigrant Students
If Survey Period Code is 2, 3, or 5 and Immigrant Student = Y on the Federal/State Indicator Status record, then Date Entered United States School must be numeric and a valid date, unless Grade Level = PK, in which case it must be 00000000. (This edit does not apply to Survey Period 6.)
**Result:** State Validation

**District Responsibility:** The district must correct the records so that the appropriate relationship exists among Immigrant Student, Date Entered United States School and Grade Level.

### 5E. Lunch Status must match NSLP Reference File designation
For Survey Periods 2 and 3, if District Number, Current Enrollment equals District Number, Current Instruction/Service and the School Number, Current Enrollment is found on the National School Lunch Program (NSLP) Reference file (F71447), Lunch Status must match the school's NSLP designation type: eligibility-application schools require 0, 1, 3, D, E or F; Provision 2 schools require 4; Community Eligibility Provision (CEP) schools require C, R or N.
**Result:** State Validation

**District Responsibility:** The district must correct the Student Demographic record so that the appropriate relationship exists between the NSLP Reference File code and Lunch Status code.

### 5F. Country of Birth must not be US/PR for Immigrant Students
If Survey Period Code is 2, 3, or 5, and Immigrant Student = Y on the Federal/State Indicator Status record, then Country of Birth must not be US or PR (per Appendix G or Q). (This edit does not apply to Survey Period 6.)
**Result:** State Validation

**District Responsibility:** The district must correct the records so that the appropriate relationship exists among Immigrant Student and Country of Birth.

### 5G. Matching Federal/State Compensatory record required for Migrant Status
If Survey = 5 and Migrant Status Term is B, D, E, S, T, U, V or W, then there must be a matching Federal/State Compensatory Project Evaluation record. (This edit does not apply to Survey Period 6.)
**Result:** State Validation

**District Responsibility:** The district must correct the records so that the appropriate relationship exists between the Student Demographic record and Federal/State Compensatory Project Evaluation records.

---

## Exception Reports

### 60. Field replication requirements between instruction and enrollment districts
For Survey Period Codes 2, 3 and 5, if District Number, Current Instruction/Service does not equal District Number, Current Enrollment, most fields must be exact replicas of the corresponding fields on the enrollment district's Student Demographic record, with specific exceptions (Student Number Identifier Local, Resident Status, and Institution Numbers) always excluded, and additional exceptions applying when District Number, Current Instruction/Service = 71. (This edit does not apply to Survey Period 6.)
**Result:** State Validation / Exception (source labels this "State Validation" in the result line but files it under exception-style advisory reporting)

**District Responsibility:** The district should verify the data submitted on the Student Demographic records and correct if in error.

### 63. Minimum age for KG-12 enrollment
If Grade Level is KG-12 and School Number, Current Enrollment is not 9992, 9993, or 9995, the student must be at least 5 years old on or before September 1 of the school year being reported. Students who transfer to Florida from states with different minimum starting ages are accepted into the grade into which they are transferring.
**Result:** Exception Report

**District Responsibility:** The district should verify the Birth Date and correct it if it is in error.

### 64. Resident Status / Grade Level relationship
If Grade Level is PK-12 and School Number, Current Enrollment is not 9995, then Resident Status, State/County must be 0, A, B, 2 or 3. If Grade Level is 30-31, then it must be 4, 5, 6 or 7. (This edit does not apply to Survey Period 6.)
**Result:** Exception Report

**District Responsibility:** The district should verify the Resident Status, State/County and the Grade Level, and correct if in error.

### 68. Matching Federal/State Indicator Status and Prior School Status records required *(Updated 07/01/2026)*
If Survey Period Code = 2, 3 or 5; School Number, Current Enrollment is not 9992, 9993, 9994, 9995 or 9997; District Number, Current Instruction/Service is not 71; District Number, Current Enrollment equals District Number, Current Instruction/Service; Withdrawal Code, PK-12 on matching Prior School Status/Student Attendance records is not DNE; and Grade Level is not 30 or 31, then each Student Demographic record must have a matching Federal/State Indicator Status record and a matching Prior School Status/Student Attendance record. (This edit does not apply to Survey Period 6.)
**Result:** Exception Report

**District Responsibility:** The district must review the Student Demographic record and determine whether a Federal/State Indicator Status record is necessary. If such a record is necessary, the district should submit the record. If not, no action is necessary.

### 69. Matching Prior School Status/Student Attendance record required *(Updated 07/01/2026)*
If Survey Period Code is 2, 3, or 5; School Number, Current Enrollment is not 9992, 9993, 9994, 9995, or 9997; Migrant Status Term is not X; District Number, Current Instruction/Service is not 71; and Grade Level is not 30 or 31, then each Student Demographic record must have at least one matching Prior School Status/Student Attendance record. (This edit does not apply to Survey Period 6.)
**Result:** Exception Report

**Example:**
| District Number, Current Instruction/Service | Florida Education Identifier | Survey Period Code | Year | Migrant Status Term |
|---|---|---|---|---|
| *02 | FL123456789001 | 3 | 1011 | Z |
| 02 | FL123456789004 | 3 | 1011 | X |
| 02 | FL123456789005 | 3 | 1011 | B |

The first record would generate an error message because there is no matching Prior School Status/Student Attendance record and Migrant Status Term is not X. The second, without a matching record, would not generate an error because Migrant Status Term equals X. The third would not generate an error because it has a matching record.

**District Responsibility:** The district must review the Student Demographic Information record and determine whether a matching Prior School Status/Student Attendance record is necessary. If necessary, the district must submit the record. If not, no action is necessary.

---

## Aggregate Exception / Validation Reports

### 90. At least one non-zero Lunch Status per school (Aggregate Exception Report)
For each School Number, Current Enrollment, at least one record must have a Lunch Status code not equal to 0, unless the School Number, Current Enrollment is 9996, 9997, N998, or N999. (This edit does not apply to Survey Period 6.)

The exception report lists, for schools that fail this edit: District Number, Current Enrollment; School Number, Current Enrollment; total number of Student Demographic records; and number of records with Lunch Status = 0.
**Result:** Exception Report (aggregate, school-level)

**District Responsibility:** The district must review the records to determine whether code 0 was used appropriately and correct the Lunch Status on records that are in error. If no records are in error, no action is necessary.

### 91. Consistent Provision 2 Lunch Status within a school (Aggregate Validation)
For each School Number, Current Enrollment in the District Number, Current Enrollment, either all records must have a Lunch Status code of 4 (Provision 2 School) or no records must have a Lunch Status code of 4. (This edit does not apply to Survey Period 6.)
**Result:** Aggregate Validation

**Example:**
| District Number, Current Enrollment | School Number, Current Enrollment | Florida Education Identifier | Survey Period Code | Lunch Status |
|---|---|---|---|---|
| *01 | 0012 | FL123456789002 | 2 | 1 |
| *01 | 0012 | FL123456789003 | 2 | 4 |

These records would cause an error message to be printed on the validation report for school 0012 because one record has a Lunch Status code of 4 and the other has a Lunch Status code of 1.

**District Responsibility:** The district must review the information in the set of records and correct the record that is in error so that either all or none of the records in the school have a Lunch Status code of 4.
