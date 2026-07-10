# Student Transportation — Edits and Reject Rules

Source: https://www.fldoe.org/file/20909/2627st.pdf
Manual: Student Database 2026-2027

This document covers edits across three categories: Reject Rules (record rejected), State Validation (cross-format matching), and one Aggregate Exception Report (bus-level check). Edit numbering is non-sequential; gaps (edits 3, 20) are as published in the source.

---

## Reject Rules

### 1. District Number, Current Instruction/Service range and active status *(Updated 07/01/2026)*
District Number, Current Instruction/Service must be numeric and active (A) on the Appendix C: District Name Table.
**Result:** Record rejected

**Example:**
| District Number, Current Instruction/Service | Florida Education Identifier |
|---|---|
| 01 | FL123456789100 |
| 01 | FL123456789200 |
| *00 | FL123456789300 |

The first two records would be loaded assuming no other reject rule would cause their rejection. The third record would be rejected since the District Number, Current Instruction/Service is not in the appropriate range.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number, Current Instruction/Service and resubmit the record.

### 2. District Number, Current Instruction/Service correctness
District Number, Current Instruction/Service must be correct for the district submitting the data.
**Result:** Record rejected

**Example:** If district 01 is submitting records, District Number, Current Instruction/Service must be 01 for all records. A record with District Number 02 submitted by district 01 would be rejected.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number, Current Instruction/Service and resubmit the record.

### 4. Survey Period Code must be 1-4
Survey Period Code must be 1, 2, 3, or 4 and must be correct for the submission specified by the district.
**Result:** Record rejected

**Example:** The Survey Period Code as specified in the transmission JCL or in the statements for tape transmission is identified as Survey Period Code "2" and records are coded with Survey Period Code "3". All updates, adds, or deletes with this inconsistency are rejected.

**District Responsibility:** Correct the Survey Period Code either on the records coming in or the transmission JCL and resubmit all of the records.

### 5. Transaction Code validity
The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified then the record must not already exist on the database; if C or D is specified then the record must exist on the database.
**Result:** Record rejected

**Example:** For all original transmissions, the Transaction Code must be "A". An original transaction is the first submission of a record during a survey period. After original transmission of records, changes to the record for elements other than the key elements must be done with a "C" as the Transaction Code. To delete a record, the Transaction Code must be a "D". To change key elements in a batch transaction, the record must FIRST be deleted with a "D" and then added with an "A".

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be applied to the database, the district must correct the Transaction Code and resubmit the records.

### 6. Fiscal Year correctness
Fiscal Year must be correct for the submission specified by the district.
**Result:** Record rejected

**Example:** The Fiscal Year as specified in the Transmission JCL or in the statements for tape transmission is identified as the valid year for data submission but records being submitted have the previous Fiscal Year coded. All updates, adds or deletes with this inconsistency are rejected.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Fiscal Year and resubmit the records.

### 7. Days in Term (for FTE Purposes) must be numeric
Days in Term (for FTE Purposes) must be numeric, greater than zero and less than 100.
**Result:** Record rejected

**Example:**
| District Number, Current Instruction/Service | Florida Education Identifier | Survey Period Code | Days in Term (for FTE Purposes) |
|---|---|---|---|
| 01 | F123456789200 | 2 | 090 |
| *01 | F123456729200 | 2 | A90 |
| *01 | F123456189200 | 3 | 90 |

The first record would be loaded assuming no other reject rule would cause its rejection. The second and third records would be rejected because Days in Term (for FTE Purposes) is not numeric or contains blanks.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct Days in Term (for FTE Purposes) and resubmit the records.

### 8. Year-Round/Extended School Year FTE Indicator validity
Year-Round/Extended School Year FTE Indicator must be A or Z.
**Result:** Record rejected

**Example:**
| District Number, Current Instruction/Service | Florida Education Identifier | Survey Period Code | Year-Round/Extended School Year FTE Indicator |
|---|---|---|---|
| 01 | FL123456789100 | 2 | A |
| 01 | FL123456789200 | 2 | Z |
| *01 | FL123456789300 | 2 | B |

The first two records would be loaded assuming no other reject rule would cause their rejection. The third record would be rejected because the code is not valid on this format.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Year-Round/Extended School Year FTE Indicator code and resubmit the record.

### 9. Bus Number must not be all blanks
Bus Number must not contain all spaces (blanks).
**Result:** Record rejected

**Example:**
| District Number, Current Instruction/Service | Florida Education Identifier | Bus Number |
|---|---|---|
| 01 | F123456789100 | 123456789 |
| 01 | F123456789200 | 1234567ABC |
| *01 | F123456789300 | |

The first two records would be loaded assuming no other reject rule would cause their rejection. The third record would be rejected because the number contains all blanks.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Bus Number and resubmit the record.

### 10. Bus Route Number must not be all blanks
Bus Route Number must not contain all spaces (blanks).
**Result:** Record rejected

**Example:**
| District Number, Current Instruction/Service | Florida Education Identifier | Bus Route Number |
|---|---|---|
| 01 | FL123456789100 | 12345678 |
| 01 | FL123456789200 | 65432ABC |
| *01 | FL123456789300 | |

The first two records would be loaded assuming no other reject rule would cause their rejection. The third record would be rejected because the Bus Route Number contains all blanks.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Bus Route Number and resubmit the record.

### 11. Vehicle Category validity
Vehicle Category must be B, E, P, or G.
**Result:** Record rejected

**Example:**
| District Number, Current Instruction/Service | Florida Education Identifier | Vehicle Category |
|---|---|---|
| 01 | FL123456789100 | B |
| 01 | FL123456789200 | G |
| *01 | FL123456789300 | H |

The first two records would be loaded assuming no other reject rule would cause their rejection. The third record would be rejected because the Vehicle Category code is not valid.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Vehicle Category code and resubmit the record.

### 12. Transportation Membership Category validity
Transportation Membership Category must be F, G, L, M, or N.
**Result:** Record rejected

**Example:**
| District Number, Current Instruction/Service | Florida Education Identifier | Transportation Membership Category |
|---|---|---|
| 01 | FL123456789100 | L |
| 01 | FL123456789200 | M |
| *01 | FL123456789300 | D |

The first two records would be loaded assuming no other reject rule would cause their rejection. The third record would be rejected because the code is not valid.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Transportation Membership Category code and resubmit the record.

### 13. Record uniqueness
Each Student Transportation record must be unique based on District Number, Current Instruction/Service; Florida Education Identifier; Survey Period Code, Fiscal Year and Year-Round/Extended School Year FTE Indicator.
**Result:** First record accepted, all other duplicate records rejected

**Example:**
| District Number, Current Instruction/Service | Florida Education Identifier | Survey Period Code | Fiscal Year | Year-Round/Extended School Year FTE Indicator |
|---|---|---|---|---|
| 01 | FL123456789100 | 2 | **** | A |
| *01 | FL123456789100 | 2 | **** | A |
| 01 | FL123456789200 | 2 | **** | A |
| 01 | FL123456789400 | 2 | **** | A |
| *01 | FL123456789400 | 2 | **** | A |

**** = Valid fiscal year for data transmission. The first, third and fourth records would be loaded assuming no other reject rule would cause their rejection. The second and fifth records would be rejected as duplicates of the first and fourth, respectively.

**District Responsibility:** If the records that were accepted and loaded to the database are correct ones, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must delete any invalid records, correct any rejected records if necessary, and resubmit the corrected records.

### 14. Bus Number must not be all Zs for Vehicle Category B
If Vehicle Category equals B, then Bus Number must not be all Zs.
**Result:** Record rejected

**Example:**
| District Number, Current Instruction/Service | Vehicle Category | Bus Number |
|---|---|---|
| 01 | B | 12345678 |
| 01 | B | 65432ABC |
| *01 | B | ZZZZZZZZZZZZZZZ |

The first two records would be loaded assuming no other reject rule would cause their rejection. The third record would be rejected because the Bus Number contains all Zs.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Bus Number and resubmit the record.

### 15. Bus Route Number must not be all Zs for Vehicle Category B
If Vehicle Category equals B, then Bus Route Number must not be all Zs.
**Result:** Record rejected

**Example:** Same pattern as Edit 14, applied to Bus Route Number.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Bus Route Number and resubmit the record.

### 16. District Number, Current Enrollment range and active status *(Updated 07/01/2026)*
District Number, Current Enrollment must be numeric and active (A) on the Appendix C: District Name Table.
**Result:** Record rejected

**Example:**
| District Number, Current Enrollment | District Number, Current Instruction/Service | Florida Education Identifier |
|---|---|---|
| 01 | 01 | FL123456789100 |
| 01 | 42 | FL123456789200 |
| *00 | 01 | FL123456789300 |

The first two records would be loaded assuming no other reject rule would cause their rejection. The third record would be rejected because the District Number, Current Enrollment is not in the appropriate range.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number, Current Enrollment and resubmit the record.

### 17. Student Number Identifier, Local format
The Student Number Identifier, Local may be any combination of letters, numbers and blanks. (All blanks are allowable.) It must be left-justified with trailing blanks.
**Result:** Record rejected

**Example:**
| District Number, Current Enrollment | Student Number Identifier, Local |
|---|---|
| 01 | 0123456789 |
| 01 | ABC123DEF9 |
| 01 | 3001 28K |
| *01 | 2121@xyz |
| *01 | 123456 |

The first three records would be loaded assuming no other edit would cause their rejection. The fourth record would be rejected because the Student Number Identifier, Local contains a symbol (@). The fifth record would be rejected because it is right-justified rather than left-justified.

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Student Number Identifier, Local and resubmit the records.

### 18. Item 2 - Filler must be all spaces
Item 2 - Filler on this format in position numbers 3-12 must be all spaces.
**Result:** Record rejected

**Example:**
| District Number, Current Instruction/Service | Filler Item #2 |
|---|---|
| 01 | |
| *01 | 265456789X |

The first record would be loaded assuming no other reject rule would cause its rejection. The second record would be rejected because the data reported is not all spaces.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must fill the positions noted with all spaces and resubmit the record.

### 19. Hazardous Walking Code by Transportation Membership Category
If Transportation Membership Category is G then Hazardous Walking Code must be 111111, otherwise it must be 000000 for all other Transportation Membership Categories (F, L, M, N).
**Result:** Record rejected

**Example:**
| District Number, Current Instruction/Service | Florida Education Identifier | Transportation Membership Category | Hazardous Walking Code |
|---|---|---|---|
| 01 | FL123456789100 | G | 111111 |
| 01 | FL123456789200 | L | 000000 |
| *01 | FL123456789200 | G | 000000 |

The first two records would be loaded assuming no other reject rule would cause their rejection. The third record would be rejected because Transportation Membership Category code is G and Hazardous Walking Code is not 111111.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Transportation Membership Category code or Hazardous Walking Code and resubmit the record.

### 21. Florida Education Identifier (FLEID) format
Florida Education Identifier (FLEID) is alphanumeric and must be entered as "FL" in the first 2 positions followed by twelve numeric digits. No blanks, spaces or all zeros for the twelve numeric digits are allowable.
**Result:** Record rejected

**Example:**
| District Number, Current Enrollment | Florida Education Identifier |
|---|---|
| 01 | FL340945895734 |
| 01 | FL004583948567 |
| *01 | FL000000000000 |

The first two records would be loaded assuming no other reject rule would cause their rejection. The third record would be rejected because the Florida Education Identifier (FLEID) is not a valid FLEID.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Florida Education Identifier and resubmit the record for processing.

### 22. Days in Term must not exceed Less than 180 Days Regular School Year table
If Survey Period is 2 or 3 and the District Number, Current Enrollment exists on the Less than 180 Days Regular School Year table, then Days in Term (for FTE Purposes) should not exceed the days in the survey reported on that table. Match by Year and District Number, Current Enrollment.
**Result:** Record rejected

Note: Less than 180 Days Regular School Year table can be found at DPS.DISTRICT.GQ.F71497.Yyyyy.

**Example:**
| District Number, Current Enrollment | Florida Education Identifier | Survey Period Code | Days in Term (for FTE Purposes) |
|---|---|---|---|
| 24 | FL123456789100 | 2 | 85 |
| 24 | FL123456789200 | 2 | 82 |
| *24 | FL123456789300 | 3 | 88 |

The first and second records would be loaded assuming no other reject rule would cause their rejection. The third record would be rejected because the district previously informed the department that the Days in Term for Survey 3 is 86.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the rejected record to be loaded to the database, the district must correct the Days in Term field on the Student Transportation format and resubmit the record.

### 23. Vehicle Category B required for Transportation Membership Category L or N
If Transportation Membership Category is L or N, then Vehicle Category must be B.
**Result:** Record rejected

**Example:**
| District Number, Current Instruction/Services | Florida Education Identifier | Vehicle Category | Membership Category |
|---|---|---|---|
| 01 | FL123456789100 | B | N |
| 01 | FL123456789200 | B | L |
| *01 | FL123456789300 | E | N |

The first two records would be loaded assuming no other reject rule would cause their rejection. The third record would be rejected because the Vehicle Category code is not valid.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Vehicle Category code and resubmit the record.

### 24. Transportation Membership Category N required for Districts 68/83
If District Number, Current Enrollment is 68 or 83, then Transportation Membership Category must be N.
**Result:** Record rejected

**Example:**
| District Number, Current Enrollment | Florida Education Identifier | Transportation Membership Category |
|---|---|---|
| 68 | FL123456789100 | N |
| 68 | FL123456789200 | N |
| *68 | FL123456789300 | G |

The first two records would be loaded assuming no other reject rule would cause their rejection. The third record would be rejected because the Transportation Membership Category code is not valid.

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Transportation Membership Category and resubmit the record.

---

## State Validation

### 50. Matching Student Demographic record required
Each Student Transportation record must have a matching Student Demographic record based on District Number, Current Enrollment; Florida Education Identifier; Survey Period Code; and Fiscal Year.
**Result:** State validation

Note: Students transported and reported by one district (District Number, Current Instruction/Service) but officially enrolled in another district (District Number, Current Enrollment) should have a matching Student Demographic Information record sent by the district in which the student is officially enrolled, not by the district providing the transportation. For a list of Student Transportation records that do not have a matching Student Demographic Information record, refer to district-level transportation report F71026.

**Example:**

Student Transportation records:
| District Number, Current Instruction/Service | District Number, Current Enrollment | Florida Education Identifier | Survey Period Code | Fiscal Year |
|---|---|---|---|---|
| *01 | 01 | FL123456789100 | 2 | **** |
| 01 | 01 | FL123456789200 | 2 | **** |
| 01 | 42 | FL123456789300 | 2 | **** |

Student Demographic Information records:
| District Number, Current Instruction/Service | District Number, Current Enrollment | Florida Education Identifier | Survey Period Code | Fiscal Year |
|---|---|---|---|---|
| 01 | 01 | FL123456789100 | 2 | **** |
| 42 | 42 | FL123456789200 | 2 | **** |

**** = Valid fiscal year for data submission. The Student Transportation record marked with an asterisk would cause a message to be generated because it does not have a matching Student Demographic record.

**District Responsibility:** The district must delete the Student Transportation record or add a Student Demographic record to match the key fields on the Student Transportation record.

### 51. Matching Exceptional Student record required for Transportation Membership Category L
If Transportation Membership Category = L, then there must be a matching Exceptional Student record where Exceptionality, Primary code is not L, based on District Number, Current Enrollment; Florida Education Identifier; Year and Survey Period Code.
**Result:** State validation

Note: Students reported under Transportation Membership Category "M" can be Exceptional or non-Exceptional. Those exceptional students reported with code "M" must have a matching Exceptional Student record based on District Number, Current Enrollment; Florida Education Identifier; Year and Survey Period Code.

**District Responsibility:** The district must correct the Transportation Membership Category code on the Student Transportation record or submit a matching Exceptional Student record.

### 52. Grade Level PK-12 required for Transportation Membership Category L or M
If Transportation Membership Category = L, or M, then Grade Level on the matching Student Demographic Information record must be PK-12. Match on District Number, Current Enrollment; Florida Education Identifier; Survey Period Code; and Year.
**Result:** State validation

**District Responsibility:** The district must correct the Transportation Membership Category code on the Student Transportation record or the Grade Level on the Student Demographic Information record.

### 53. Hazardous Walking Code must be zero for Grade Level 07-12
If Grade Level on the Demographic Information record is 07-12 then the Hazardous Walking Code must be 000000. Match on District Number, Current Enrollment; Florida Education Identifier; Survey Period Code; and Fiscal Year.
**Result:** State validation

**District Responsibility:** The district must review the records and correct the Hazardous Walking Code on the Student Transportation record or the Grade Level on the Student Demographic Information record.

---

## Aggregate Exception Report

### 90. Minimum student count per school bus *(Updated 07/01/25)*
The number of students for each school bus (Vehicle Category = B) must be greater than 5.

The exception report lists, for buses that fail this edit: District Number, Current Instruction/Service; Bus Number; and Total Student Count.
**Result:** Aggregate exception (bus-level)

**District Responsibility:** The district must verify the data for the affected Bus Number on the Student Transportation records and correct this field if it is in error on one or more records.
