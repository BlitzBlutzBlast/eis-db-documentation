# Student Course Schedule — Edits and Reject Rules

Source: Florida DOE
Manual: Student Database 2026-2027

Student Database 202 6-2027 /  
## Reject Rules

UPDATED 07/01/2026   

### 1. District Number, Current Enrollment must be numeric and active (A) on the Appendix C: District Name 
Table.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected since the District Number, Current Enrollment is  
not in the appropriate range.  
District Number, Current Enrollment  School Number, Current Enrollment  Florida Education Identifier  
01 0021  FL340945895734  
01 0021  FL340945895735  
* 00  0021  FL340945895736  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the District 
Number, Current Enrollment and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
   
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 2. School Number, Current Enrollment must be numeric in the range 0001 to 9899 (excluding 3900, 7006 
and 9001) or it must be N998 or N999.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third and fourth records would be rejected. The third record would be rejected 
because the School Number, Current Enrollment is not in the appropriate numerical range. The fourth 
record would be rejected because the School Number, Current Enrollment is not numeric, N998 or N999. 
The fifth record would be rejected because the School Number, Current Enrollment is excluded from the 
range.  
District Number, Current Enrollment  School Number, Current Enrollment  Florida Education Identifier  
01 0021  FL340945895734  
01 0021  FL340945895735  
* 01  9999  FL340945895736  
* 01  C901  FL340945895737  
* 01  3900  FL123456789500  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the School 
Number, Current Enrollment and resubmit the records.  
 
  
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 4. Survey Period Code must be 1, 2, 3, or 4 and it must be correct for the submission specified by the 
district.  
**Result:** Record rejected
EXAMPLE  
The Survey Period Code as specified in the transmission JCL or in the statements for tape transmission is 
identified as Survey Period Code "2" and records are coded with Survey Period Code "3". All updates, 
adds, or deletes with this inconsistency would be rejected.  

**District Responsibility:** Correct the Survey Period Code either on the records coming in or the transmission JCL and resubmit all 
of the records.  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 5. The Fiscal Year must be correct for the submission specified by the district.  
**Result:** Record rejected
EXAMPLE  
The Fiscal Year on the JCL and the records being submitted for processing must  match. Otherwise, the 
records would be rejected.  

**District Responsibility:** Correct the Fiscal Year either on the transmission JCL or the records being submitted and resubmit all 
records for processing.  
 
  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 6. District Number, Current Instruction/Service must be correct for the district submitting the data.  
**Result:** Record rejected
EXAMPLE  
The District Number, Current Instruction/Service on records being submitted for processing must match 
the District Number, Current Instruction/Service on the JCL. Otherwise, the records would be rejected.  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
District Number, Current Instruction/Service and resubmit the records.  
 
  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 7. If Survey Period Code is 1, then  
• School Number, Current Instruction/Service must be numeric in the range 0001 -9899 or 9996 
(excluding 3450, 3900, 3950, 7001, 7004, 7006, 7023, 9001) and excluding schools where the 
Charter School Status is not Z and School Function/Setting equals V on the Master School  
Identification file, or  
• School Number, Current Instruction/Service must be C901 -C928, U970 -U981, or P001 -P999.  
If Survey Period Code = 2 or 3, then  
• School Number, Current Instruction/Service must be numeric in the range 0001 -9899 (excluding 
3450, 3900, 3950 and 9001), 9996, C901 -C928, U970 -U981, P001 -P999  
If Survey Period Code is 4, then  
• School Number, Current Instruction/Service must be numeric in the range 0001 -9899 (excluding 
3450, 3900, 3950 and 9001), 9996, or  
• School Number, Current Instruction/Service must be C901 -C928, U970 -U981, or P001 -P999.  
**Result:** Record rejected
EXAMPLE  
The records listed below would be rejected because in each case the School Number, Current/Instruction 
Service is not within the valid range.  
District Number, 
Current 
Instruction/Service  School Number, Current 
Instruction/Service  Florida Education 
Identifier  Survey Period  
Code  
* 01  9901  FL340945895734  2 
* 01  C929  FL3409 45895735  2 
*01 U982  FL340945895736  2 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the School 
Number, Current Instruction/Service and resubmit the records.  
 
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 8. If the School Number, Current Instruction/Service is C901 -C928, U970 -U981, P001 -P999, 9996, or N999, 
the District Number, Current Enrollment must be correct for the district submitting the data. If Survey 
Period Code = 2 or 3 and School Number, Current Instruction/Service is a private school number, the 
District Number, Current Enrollment must be correct for the district submitting the data.  
**Result:** Record rejected
NOTE: If School Number, Current Instruction/Service is a private school number, Course Number must 
be 2222222.  
EXAMPLE  
If the district submitting the records is 01, then the first record listed below would be loaded to the 
database assuming no other reject rule would cause its rejection. The second record would be rejected 
because the District Number, Current Enrollment is incorrect for the district submitting the record.  
District Number, 
Current 
Instruction/Service  School Number, Current Instruction/Service  Florida Education Identifier  Survey 
Period 
Code  
01 C901  FL340945895734  2 
* 02  C928 FL340945895735  2 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Student 
Course record or the transmission JCL where the mismatch occurs and resubmit the record.  
 
  
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 9. Course Number must not contain blanks.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other  reject rule 
would cause its rejection. The second record would be rejected because  Course Number contains a 
blank.  
District Number, 
Current 
Instruction/Service  School Number, Current 
Instruction/Service  Florida Education 
Identifier  Course 
Number  
02 0061  FL340945895734  5013010  
* 02  0201  FL340945895735  1008 80  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Course 
Number and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 10. Section Number must not be all blanks. Allowable characters are 0 -9, A-Z, space, hyphen ( -), dollar sign 
($), pound sign  (#), ampersand (&), percent (%), forward slash (/) and colon (:).  
**Result:** Record rejected
Note: Section Number may be submitted with blanks in one to four of the five positions but may not 
be submitted with five blanks.  
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because Section Number is all blanks.  
District Number, 
Current 
Instruction/Service  Florida 
Education 
Identifier  Course Number  Section Number  
02 Fl340945895734  5013010  PP18  
* 02  Fl340945895735  2003340   

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Section 
Number and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 11. Period Number must be numeric and greater than or equal to zero. -record rejected -  
EXAMPLE  
The first and second records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. The third record would be rejected because Period Number is not numeric. 
The fourth record would be rejected because Period Number is blank.  
District Number, 
Current 
Instruction/Service  Florida 
Education 
Identifier  Course Number  Period Number  
02 FL340945895734  5013010  0101  
02 FL340945895735  7910100  0288  
* 02  FL340945895736  2109310  AB80  
* 02  FL340945895737  1300330   

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Period 
Number and resubmit the records.  
 
  
 
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 12. If the School Number Current Instruction/Service does not begin with "P" the  Course Number must not 
be a "local use only transfer" course. If the School Number Current Instruction/Service does not begin 
with "P" then the Course Number must not begin with 00.  
**Result:** Record rejected
Note: Local use only transfer course numbers for Grade Levels 09 -12 are  numeric  course numbers that 
end in 980 or 990. Local use only transfer course numbers for Grade Levels 30 -31 are alphanumeric 
course numbers that begin with one alpha character and end with six zeroes.  
EXAMPLE  
The third record listed below would be loaded to the database assuming no other reject rule would 
cause its rejection. The first and second records would be rejected because the Course Numbers are 
local numbers.  
District Number, 
Current 
Instruction/Service  School Number, 
Current 
Instruction/Service  Florida 
Education 
Identifier  Course Number  
* 01  0201  FL340945895734  2100990  
* 01  0201  FL340945895735  2000990  
01 0201  FL340945895736  1206310  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Course 
Number and resubmit the records.  
 
  
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 13. The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent  
batch/update submissions, if A is specified then the record must not already  exist on the database; if C 
or D is specified then the record must exist on the database.  
**Result:** Record rejected
EXAMPLE  
For all original transmissions, the Transaction Code must be "A". An original transaction is the first 
submission of a record during a survey period. After original transmission of records, changes to the 
record for elements other than the key elements must be done with "C" as the Transaction Code. To 
delete a record, the Transaction Code must be "D". To change key elements in a batch transaction, the 
record must FIRST be deleted with "D" and then added with "A". Records with an incorrect Transaction 
Code would be rejected.  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
Transaction Code and resubmit the records.  
  
 
 
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 14. Each  record must be unique based on Florida Education Identifier; Survey 
Period Code; Fiscal Year; District Number, Current Instruction/Service; School Number, Current 
Instruction/Service; Course Number; Section Number; Period Number; and Term.  
Record having highest weighted FTE accepted, all other duplicate records rejected  
EXAMPLE  
The records that are highlighted are duplicates. The record in each of the pairs which is marked with an 
asterisk would be rejected because it has the lower weighting factor. That is, FEFP Program Number 102 
has a lower weighting factor for funding than does FEFP Program Number 103.  
Florida Education 
Identifier  Svy. 
Pd. 
Code  FY Dist. 
Num.,Curr. 
Inst./Serv.  Schl. 
Num.,Curr. 
Inst./Serv.  Course 
Numer  Section 
Number  Period 
Number  FEFP 
Prog. 
No. Term  
FL340945895734  2 ****  01 0021  2109370  00001  0202  102 1 
FL340945895735  2 ****  01 0021  2109370  00001  0202  102 1 
FL340945895736  2 ****  01 0021  2109370  00001  0202  102 1 
FL340945895737  2 ****  01 0021  2109370  00001  0202  102 1 
FL340945895738  2 ****  01 0021  2109370  00001  0202  102 1 
FL340945895739  2 ****  01 0021  2109370  00001  0202  103 1 
FL340945895730  2 ****  01 0021  2109370  00001  0202  102 1 
*FL340945895731  2 ****  01 0021  2109370  00001  0202  102 1 
FL34094589573 2 2 ****  01 0021  2109370  00001  0202  103 1 
FL34094589573 3 2 ****  01 0021  2109370  00001  0202  103 1 
*FL34094589573 1 2 ****  01 0021  2109370  00001  0202  102 1 
FL34094589573 2 2 ****  01 0021  2109370  00001  0202  103 1 
**** = Valid fiscal year for data submission.  

**District Responsibility:** If the records that were accepted and loaded to the database are the correct ones, no action is required. 
However, if the district wishes the data in the rejected records to be loaded to the database, the district 
must delete any invalid records, correct any rejected records if necessary, and resubmit the corrected 
records.  
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 15. Dual Enrollment Indicator must be A, B, C, E, or Z.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no  other reject rule would 
cause their rejection. The third record would be rejected because the Dual Enrollment Indicator is not 
valid.  
District Number, 
Current 
Instruction/Service  School Number, 
Current 
Instruction/Service  Survey Period 
Code  Florida 
Education 
Identifier  Course 
Number  Dual 
Enrollment 
Indicator  
31 C901 2 FL340945895734  PHY1050  A 
31 0291 2 FL340945895735  1209800  Z 
* 31 0291 2 FL340945895736  PHY1050  D 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Dual 
Enrollment Indicator and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 16. All alphanumeric Course Numbers must either be on the Course Code Directory or on the Statewide 
Course Numbering System file unless School Number, Current Instruction/Service equals N999 or P001 -
P999.  
**Result:** Record rejected
EXAMPLE  
The second and third records listed below would be loaded to the database assuming no other reject 
rule would cause their rejection. The first and fourth records would be rejected because the Course 
Numbers are not on the Course Code Directory or on the Statewide Course Numbering System files.  
Florida Education Identifier  District Number, 
Current 
Instruction/Service  School Number, 
Current 
Instruction/Service  Course 
Number  
*FL340945895734  66 0061  FF10011  
FL340945895735  66 0061  I460103  
FL340945895736  66 0201  B070614  
*FL340945895737  66 0271  ABCDE12  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Course 
Numbers and resubmit the records.  
 
  
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 17. If Course Number is a course number from the Courses That Do Not Generate FTE file (F71424) or School 
Number, Current Enrollment is 3450  or 3950 , then FTE Reported, Course must be 0000 and FEFP 
Program Number must be 999.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because the course is a study hall and the FEFP 
Program Number is not 999. The third record would be rejected because the course is a study hall and 
the FTE Reported, Course is greater than zero.  
Florida 
Education 
Identifier  Survey 
Period Code  FTE Reported, 
Course  Course Number  FEFP Program 
Number  
FL340945895734  2 0000  2200300  999 
FL340945895735  2 0000  2200310  103 
FL340945895736  2 0250  2200320  999 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must appropriately 
correct the element(s) listed in the edit and resubmit the records.  
 
  
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 18. If Course Number equals 0800300 or 8502000, then FEFP Program Number must equal 102, 103, 112, 
113, 254, 255, or 999.  
**Result:** Record rejected
EXAMPLE  
The first and third records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. The second record would be rejected because the proper relationship does 
not exist between FEFP Program Number and the Course Number 8502000.  
Florida 
Education 
Identifier  District Number, Current 
Instruction/Service  School Number, Current 
Instruction/Service  Course 
Number  FEFP 
Program 
Number  
FL340945895734  01 0201  8502000  103 
* 
FL340945895735  01 0201  8502000  300 
FL340945895736  01 0201  8502000  103 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct either the 
FEFP Program Number or the Course Number and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 19. If Course Number equals 2222222, then School Number, Current Instruction/Service must be a private 
school number and vice versa.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected since Course Number is 2222222 and the 
School Number, Current Instruction/Service is not a private school number.  
Florida Education 
Identifier  District Number, 
Current 
Instruction/Service  School Number, 
Current 
Instruction/Service  Course Number  
FL340945895734  01 8034  2222222  
FL340945895734  17 8016  2222222  
* FL340945895734  17 8711  2222222  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct either the 
School Number, Current Instruction/Service or the Course Number and resubmit the record.  
 
 
  
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 1A. Item 3 - Filler on this format in position numbers 7 -16 must be all spaces.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because the data reported is not all spaces.  
District Number, Current Enrollment  School Number, Current Enrollment  Filler Item #3  
01 0151   
* 01  0151  265456789X  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must fill the positions 
noted with all spaces and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 20. FEFP Program Number must be 102, 103, 112, 113 or 999 if Dual Enrollment Indicator code = A, B, C, or  
E.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because the relationship between Dual Enrollment 
Indicator code and FEFP Program Number is not appropriate.  
Florida Education Identifier  Dual Enrollment Indicator  FEFP Program Number  
FL340945895734  A 103 
* FL340945895734  C 251 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct either the 
Dual Enrollment Indicator code or FEFP Program Number and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 21. If Dual Enrollment Indicator equals A, then School Number, Current Instruction/Service must be C901 -
C928, U970 -U981 or P001 -P999.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected since the School Number, Current 
Instruction/Service is not in the appropriate range.  
School Number, 
Current Enrollment  School Number, Current 
Instruction/Service  Dual Enrollment Indicator  
0021  C901  A 
0051  P999  A 
* 0204  0204  A 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the School 
Number, Current Instruction/Service and resubmit the record.  
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 22. Class Minutes, Weekly must be numeric and greater than or equal to zero.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because Class Minutes, Weekly contains a blank. The 
third record would be rejected because Class Minutes, Weekly is not numeric.  
District  Number, Current 
Instruction/Service  Florida Education Identifier  Course Number  Class Minutes, Weekly  
02 FL340945895734  2109370  0050  
* 02  FL340945895735  2109370  075 
* 02   FL340945895736  2109370  W025  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Class 
Minutes, Weekly and resubmit the records.  
 
  
 
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 23. FEFP Program Number must be 101 -103, 111 -113, 130, 254 -255, 300, or 999.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second and third records would be rejected because the FEFP Program Numbers are 
invalid.  
District Number, Current 
Instruction/Service  Florida Education Identifier  Course Number  FEFP Program Number  
02 FL340945895734  2109370  103 
* 02  FL340945895735  2109370  001 
* 02  FL340945895736  2109370  118 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the FEFP 
Program Number and resubmit the records.  
 
  
 
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 24. FTE Reported, Course must be numeric and greater than or equal to zero. If Period Number is 9800, FTE 
Reported, Course must be greater than zero and less than or equal to .1667.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because FTE Reported, Course contains a blank. The 
third record would be rejected because FTE Reported, Course is not numeric.  
District Number, Current 
Instruction/Service  Florida Education Identifier  Course Number  FEFP Program Number  FTE 
02 FL340945895734  2109370  103 0834  
* 02  FL340945895735  2109370  103 0 34  
* 02  FL340945895736  2109370  103 o005  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
records by assigning a value greater than or equal to zero for FTE Reported, Course and resubmit the 
records.  
## Reject Rules

Student Database 202 6-2027 /  

### 25. If Grade Level on the  record is PK, then Reading Intervention Component code 
must be Z. Otherwise, Reading Intervention Component code must be A, B or N.   
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third and fourth records would be rejected because the Reading Intervention 
Component codes are not valid for the Grade Levels.  
District Number, 
Current 
Instruction/Service  Florida Education 
Identifier  Course 
Number  Reading 
Intervention 
Component  Grade Level  
01 FL340945895734  2100010  A 06 
01 FL340945895735  2100010  N 10 
* 01  FL340945895736  2100010  Z 01 
* 01  FL340945895737  5100520  N PK 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
Reading Intervention Component codes and resubmit the records.  
 
  
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 27. If Course Number is 5100520, 5100530, 5100560, 5100570, 5100580, 5100590, 5100600 or 5100610 
Grade Level must be PK.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
it to reject. The second record would be rejected because the student’s Grade Level is not PK.  
Course Number  FEFP Program 
Number  Grade Level  
5100580  999 PK 
* 5100590  999 01 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Grade 
Level or Course Number and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 28. If School Number, Current Instruction/Service equals 9996, then School Number, Current Enrollment 
must be N999.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be rejected because School Number, Current Enrollment is not N999. 
The second record would be loaded to the database assuming no other reject rule would cause it to 
reject.  
Florida 
Education 
Identifier  District Number, 
Current 
Instruction/Service  School Number, Current 
Enrollment  School Number, Current 
Instruction/Service  
* 
FL340945895734  01 0021  9996  
FL340945895735  41 N999  9996  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct either the 
School Number, Current Enrollment or the School Number, Current Instruction/Service and resubmit the 
record.  
 
  
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 29. Grade Level must be PK, KG, or 01 -12.  
**Result:** Record rejected
EXAMPLE  
The third and fourth records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. The first and second records would be rejected because the Grade Level 
codes are not valid.  
Florida Education Identifier  Grade Level  FEFP Program Number  
* FL340945895734  KK 101 
* FL340945895735  1 101 
FL340945895736  01 101 
Fl340945895737  12 103 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Grade 
Level code and resubmit the records.  
 
  
 
 
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 2A. If Dual Enrollment Indicator is A and if School Number, Current Instruction/Service is not P001 -P999 then 
Course Number must start with an alphabetic character.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Course Number is not appropriate 
for the Dual Enrollment Indicator reported.  
District Number, 
Current 
Instruction/Service  School Number, Current 
Instruction/Service  Survey 
Period 
Code  Florida Education 
Identifier  Course 
Number  Dual 
Enrollment 
Indicator  
31 C901  2 FL340945895734  PHY1050  A 
31 U970  2 FL34094589573 4 SOC1022  A 
* 31  U970  2 FL34094589573 4 0701350  A 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Dual 
Enrollment Indicator or the Course Number and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 2B. The Course Grade code must be A+, A, A -, B+, B, B -, C+, C, C -, D+, D, D -, F, I, IP , N, NNN, U, P , S, E, WP , FL, 
NG, W, WF or Z and must be right justified with leading blanks.  
**Result:** Record rejected
EXAMPLE  
In the example below, records two and five would be loaded to the database assuming no other reject 
rule would cause the records to be rejected. Records one and four would be rejected since they contain 
invalid codes. Record three would be rejected since the Course Grade is not right justified with leading 
blanks.  
Course Number  Credit Earned, 
Course  Course 
Grade  
* 1005300  100 OOA  
0900310  050 B+ 
* 0400330  100 C+ 
* 1200350  050 WC 
1200350  050 P 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Course 
Grade and resubmit the records.  
 
  
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

UPDATED 07/01/2026   

### 2C. If Dual Enrollment Indicator = Z and  
• School Number, Current Instruction/Service = 7001, 7004, 7006 or 7023  or District Number, 
Current Instruction/Service = 71.  
• or if School Number, Current Instruction/Service has a Charter School Status is not Z and School 
Function/Setting equals V on the Master School Identification file,  
• or Location of Student equals T; and District Number, Current Instruction is not 71 ; and School 
Number, Current Instruction does not equal 7001, 7004, 7006, or 7023.  
then Course Grade may not equal Z. All other schools must equal Z.  
EXAMPLE  
In the example below, records two and three would be loaded to the database assuming no other reject 
rule would cause the records to be rejected. Record one would be rejected since it contains an invalid 
code.  
District Number, 
Current 
Instruction/Service  School Number, 
Current 
Instruction/Service  Florida 
Education 
Identifier  Course 
Number  Dual 
Enrollment 
Indicator  
* 01  7023  FL340945895734  Z Z 
01 7001  FL340945895735  IP Z 
71 0600  FL340945895736  A- Z 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Course 
Grade and resubmit the record.  
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 2D. If 
• Survey Period Code is 1, 2, 3 or 4;  
• and Course Number is 9504110, 9504120, 9504130, 9504140, 9504150, or 9504160  
• and District Number, Current Instruction/Service and School Number, Current 
Instruction/Service exists on the Non -Fundable Automotive Service Technology file (F71340),  
then FTE Reported, Course must be .0000.  
**Result:** Record rejected
EXAMPLE  
The records listed below would be rejected because in each case District Number, Current 
Instruction/Service and School Number, Current Instruction/Service exists on Non -Fundable Automotive 
Service Technology Program file (F71340).  
District Number, 
Current 
Instruction/Service  School Number, 
Current 
Instruction/Service  Course 
Number  FTE 
Reported 
Course  
* 10  0252  9504110  0035  
* 12  0011  9504130  0024  
* 13  7191  9504140  0005  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct FTE 
Reported, Course and resubmit the records.  
 
  
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 2E. If the School Number, Current Instruction/Service has a School Function /Setting of V and Charter School 
Status not equal to Z on the Master School Identification file, then the Virtual Instruction Provider code 
must be a valid assigned code as specified in Appendix CC.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Virtual Instruction Provider code is 
not valid.  
 records  
District Number, 
Current 
Instruction/Service  School Number, Current 
Instruction/Service  Survey Period 
Code  Florida Education 
Identifier  Virtual 
Instruction 
Provider  
31 0301  2 FL340945895734  308 
31 5001  2 FL340945895735  311 
*  1 0301  2 FL340945895736  989 
 
Master School Identification file records  
District Number  School Number  School 
Function /Setting  Charter 
School 
Status  
31 0301  V R 
31 5001  V R 
*   1 0301  V R 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Virtual 
Instruction Provider code and resubmit the record.  
 
  
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

UPDATED 07/01/2026   

### 2F. If Dual Enrollment Indicator = Z, Course Number does not equal 2222222 and  
• School Number, Current Instruction/Service = 7001, 7004, 7006 or 7023.  
• or District Number, Current Instruction/Service = 71,  
• or if School Number, Current Instruction/Service has a Charter School Status is not Z and 
School Function/Setting equals V on the Master School Identification file,  
• or Location of Student equals T; and District Number, Current Instruction is not 71 ; and 
School Number, Current Instruction does not equal 7001, 7004, 7006, or 7023.  
• and Course Grade is F, I, IP , N, U, WP , FL, NG, W , or WF.  
then FTE Reported, Course must be .0000.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The fourth record would be rejected because FTE Reported, Course is greater than 
zero.  
District Number, 
Current 
Instruction/Service  School Number, 
Current 
Instruction/Service  Course 
Grade  FTE 
Reported 
Course  
02 0012  A 0035  
54 0301  C 0024  
* 63  0021  IP 0025  
* 38  0091  F 0067  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct FTE 
Reported, Course and resubmit the records.  
 
  
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 2G. If the School Number, Current Instruction/Service is 7006, then the Online Course Provider code must be 
a valid code in Appendix GG. If the School Number, Current Instruction/Service is not 7006, then the 
Online Course Provider code must be ZZZ.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Online Course Provider code is not 
valid for the School Number, Current Instruction/Service.  
District Number, 
Current 
Instruction/Service  School Number, Current 
Instruction/Service  Survey 
Period  Florida Education 
Identifier  Course 
Number  Online  
Course  
Provider  
31 7006  2 FL340945895734  1001020  314 
31 7001  2 FL340945895735  1205010  ZZZ 
* 31  7001  2 FL340945895736  1303000  316 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Online 
Course Provider or the School Number, Current Instruction/Service and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

UPDATED 07/01/2026   

### 2H. If Survey Period = 4 and  
• School Number, Current Instruction/Service = 7001, 7004, 7006 or 7023.  
• or if District Number, Current Instruction/Service = 71 and School Number, Current 
Instruction/Service = 0300, 0400 or 0801.  
• or School Number, Current Instruction/Service has a Charter School Status other than Z 
and School Function/Setting equals V on the Master School Identification file,  
• or Location of Student equals T; and District Number, Current Instruction is not 71 ; and 
School Number, Current Instruction does not equal 7001, 7004, 7006, or 7023.  
then Course Grade must not equal IP .  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because Course Grade equals IP .  
District Number, 
Current 
Instruction/Service  School Number, 
Current 
Instruction/Service  Course 
Grade  Survey 
Period Code  
02 7001  A 4 
71 0400  B 4 
* 37  7023  IP 4 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct Course 
Grade and resubmit the record.  
 
  
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

UPDATED 07/01/2026   

### 2I. If  
• School Number, Current Instruction/Service = 7001, 7004, 7006 or 702 3 or District Number, 
Current Instruction/Service = 71.  
• or if School Number, Current Instruction/Service has a Charter School Status other than Z and 
School Function/Setting equals V on the Master School Identification file.  
• or Location of Student equals to T; and District Number, Current Instruction is not 71;  and 
School Number, Current Instruction does not equal 7001, 7004, 7006, nor 7023.  
then Grade Level may not equal PK.  
**Result:** Record rejected
EXAMPLE  
In the example below, records two and three would be loaded to the database assuming no other reject 
rule would cause the records to be rejected. Record one would be rejected since Grade Level = PK.  
District Number, 
Current 
Instruction/Service  School Number, 
Current 
Instruction/Service  Florida 
Education 
Identifier  Grade Level  
* 01  7023  FL340945895734  PK 
01 7001  FL340945895735  06 
71 0600  FL340945895736  12 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Grade 
Level and resubmit the record.  
 
  
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 2L. If on the Master School Identification file the School Function/Setting equals D (DJJ) or J (County 
Jail/State Prison) then Grade Level may not equal PK.  
**Result:** Record rejected
EXAMPLE  
In the example below, records two and three would be loaded to the database assuming no other reject 
rule would cause the records to be rejected. The first record would be rejected since Grade Level = PK.  
District Number, 
Current 
Instruction/Service  School Number, 
Current 
Instruction/Service  Florida 
Education 
Identifier  Grade Level  School 
Function /Setting  
* 01  0021  FL340945895734  PK D 
01 9023  FL340945895734  06 J 
01 0600  FL340945 895734  12 D 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Grade 
Level and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 2M. If Dual Enrollment Indicator Code equals A, B, C or E, then Course Number must not be all numeric.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no  other reject rule would 
cause their rejection. The third record would be rejected because the Dual Enrollment Indicator is not 
valid.  
District Number, 
Current 
Instruction/Service  School Number, 
Current 
Instruction/Service  Survey 
Period 
Code  Florida Education 
Identifier  Course 
Number  Dual 
Enrollment 
Indicator  
31 C901  2 FL340945895734  PHY1050  A 
31 C911  2 FL340945895735  PHY1050  A 
* 31  0291  2 FL340945895736  2003380  E 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Dual 
Enrollment Indicator and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 30. If Survey Period Code = 1 -4 and FEFP Program Number is 999, then FTE Reported, Course must be zero. 
**Result:** Record rejected
Note:  The use of the FEFP Program Number "999" is for individual students who are not eligible for FTE 
funding for reasons other than attendance or program membership. These students would include those 
pre-kindergarten students who are being served in a program for which the student cannot earn FTE.  
EXAMPLE  
The first, second, fifth and sixth records listed below would be loaded to the database assuming no other 
reject rule would cause their rejection. The third and fourth records would be rejected because FTE 
Reported, Course is not zero.  
Florida Education 
Identifier  Grade Level  FEFP 
Program 
Number  FTE 
Reported, 
Course  
FL340945895734  PK 999 0000  
FL340945895735  KG 999 0000  
*FL340945895736  01 999 5000  
*FL34094589573 7 07 999 2500  
FL34094589573 8 01 999 0000  
FL34094589573 9 12 999 0000  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
relationship between FEFP Program Number and FTE Reported, Course and resubmit the records.  
 
  
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 31. In surveys 1 through 4 if the FEFP Program Number is not 999, then there must be a valid association 
between the FEFP Program Number listed below and the student's Grade Level.  
**Result:** Record rejected
FEFP Program 
Numbers  Grade Levels  
101 PK-03 
102 04-08 
103 09-12 
111 PK-03 
112 04-08 
113 09-12 
130 KG-12 
254-255 PK-12 
300 09-12 
EXAMPLE  
The records below without an asterisk would be loaded to the database assuming no other reject rule 
would cause their rejection. The records below which are marked with an asterisk would be rejected 
because of the invalid association between the Grade Level of the student and the FEFP Program 
Number.  
Florida Education Identifier  Dist. Number, 
Current 
Instruction/Service  Sch. Number, 
Current 
Instruction/Service  FEFP 
Program 
Number  Grade 
Level  FTE 
Reported, 
Course  
* FL340945895734  01 0021  102 KG 0834  
* FL340945895735  01 0021  102 12 0834  
FL340945895736  01 0021  102 07 0834  
FL340945895737  01 0021  102 08 0834  
* FL340945895738  01 0021  103 08 0834  
FL340945895739  01 0021  102 07 0834  
* FL340945895730  01 0021  103 07 0834  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the FEFP 
Program Number or the Grade Level so that there is a valid relationship between these two data 
elements and resubmit the records.  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 32. If Survey Period Code is 1 -4, Grade Level is less than 06 and FTE Reported, Course is greater than zero, 
then School Number, Current Instruction/Service must not be a college nor university (C901 -C928, U970 -
U981 nor P001 -P999).  
**Result:** Record rejected
EXAMPLE  
The second and fourth records listed below would be loaded to the database assuming no other reject 
rule would cause their rejection. The first and third records would be rejected because FTE Reported, 
Course is greater than zero and the School Number, Current Instruction/Service is for a college or 
university and the Grade Level is less than 06.  
Florida Education 
Identifier  School Number Current 
Instruction/Service  Section 
Number  Period 
Number  FEFP 
Program 
Number  Grade 
Level  FTE 
Reported, 
Course  
* U974  00001  0202  102 05 0834  
FL340945895734        
*FL340945895735  0021  00001  0202  102 08 0834  
* C901  00001  0202  102 05 0834  
FL340945895736        
FL340945895737  0021  00001  0202  102 07 0834  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
relationship between Grade Level; FTE Reported, Course and School Number Current Instruction/Service 
and resubmit the records.  
 
  
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 33. If Course Number is 5100580 then Survey Period code must be 2 or 3.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the student’s Course Number is 
5100580 and Survey Period Code is 4. The last record would be rejected because the student's Course 
Number is 5100580, and Survey Period Code is 1.  
 
Course Number  Survey Period 
Code  Grade Level  FTE 
Reported, 
Course  
5100580  2 PK 0000  
5100580  3 PK 0000  
* 5100580  4 PK 0000  
* 5100580  1 PK 0000  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Survey 
Period Code or Course Number and resubmit the records.  
 
  
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 34. If the Course Number is 5100590 then the Survey Period Code must be 1 or 4.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the student’s Course Number is 
5100590 and Survey Period Code is 2. The last record would be rejected because the student's Course 
Number is 5100590, and Survey Period Code is 3.  
Course Number  Survey Period 
Code  Grade Level  FTE 
Reported, 
Course  
5100590  1 PK 0000  
5100590  4 PK 0000  
* 5100590  2 PK 0000  
* 5100590  3 PK 0000  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Survey 
Period Code or Course Number and resubmit the records.  
 
  
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 35. Term must be either 1 -9, B-O or S -X.  
**Result:** Record rejected
EXAMPLE  
The records in the first and third examples listed below would be rejected because the Term code is 
invalid. The second record would be rejected because the Term code was left bank.  
Florida Education 
Identifier  Course 
Number  Term  
* FL340945895734  1200310  P 
* FL340945895735  1001310   
* FL340945895736  2000310  A 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Term 
and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 36. English Language Learners: Instructional Model must be E, S, I, C, O, T, or Z.  
**Result:** Record rejected
EXAMPLE  
The first and third records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. The second record would be rejected because English Language Learners: 
Instructional Model is invalid. The fourth record would be rejected because English Language Learners: 
Instructional Model is blank.  
District Number, 
Current 
Instruction/Service  Florida Education 
Identifier  Course 
Number  ELL: 
Instructional 
Model  
01 FL340945895734  5100070  E 
* 01  FL340945895735  5100070  A 
04 FL340945895736  5100070  C 
* 08  FL340945895737  5100070   

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
English Language Learners: Instructional Model and resubmit the records.  
 
  
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 37. Year -Round/Extended School Year FTE Indicator must be A, B or Z.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third and fourth records would be rejected because the Year -Round/Extended 
School Year FTE Indicator codes are not valid.  
District Number, 
Current 
Instruction/Service  Florida Education 
Identifier  Course 
Number  Survey 
Period Code  Year 
Round/Ext ended 
School Year FTE 
Indicator  
01 FL340945895734  5100070  2 A 
01 FL340945895735  5100070  2 Z 
* 01  FL340945895736  5100070  2 E 
* 01  FL340945895737  5100070  2 Y 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Year -
Round/Extended School Year FTE Indicator codes and resubmit the records.  
 
  
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 38. The Student Number Identifier, Local may be any combination of letters, numbers and blanks. (All blanks 
are allowable.) It must be left -justified with trailing blanks.  
**Result:** Record rejected
EXAMPLE  
The first three records listed below would be loaded to the database assuming no other edit would 
cause their rejection. The fourth record would be rejected because the Student Number Identifier, Local 
contains a symbol (@). The fifth record would be rejected because it is right -justified rather than left -
justified.  
District Number, Current 
Instruction/Service  Student Number 
Identifier, Local  
01 0123456789  
01 ABC123DEF9  
01 3001 28K  
* 01  2121@xyz  
* 01  123456  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
Student Number Identifier, Local and resubmit the records.  
 
  
 
 
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

UPDATED 07/01/2026   

### 39. If Survey Period is 2 or 3, and  if Dual Enrollment Indicator is not B nor C, and  
• District Number, Current Instruction/Service = 71 and School Number, Current 
Instruction/Service = 0300, 0400 or 0801; or  
• if School Number, Current Instruction/Service is  
o 7001 (district virtual instruction program – contracted provider), or  
o 7004 (franchise of Florida Virtual School), or  
o 7006 (KG -12 virtual course offerings), or  
o 7023 (district virtual instruction program – district provider), or  
o Location of Student = T; and District Number, Current Instruction is not 71 ; and School Number 
Current Instruction does not equal 7001, 7004, 7006 or 7023,  
then FTE Reported, Course must be 0000.  
 
If Survey Period is 2 or 3 and  
• The School Number, Current Instruction/Service has a School Function /Setting of V on the 
Master School Identification file and  
• The School Number, Current Instruction/Service has a Charter School Status does not equal to Z 
on the Master School Identification file and  
• Dual Enrollment Indicator is not “B” nor “C”, then FTE Reported, Course must be 0000.  
**Result:** Record rejected
EXAMPLE  
The third and fourth records below would be loaded to the database assuming no other reject rule 
would cause their rejection. The first and second records below which are marked with an asterisk would 
be rejected because the FTE Reported, Course is not zero.  
Florida Education 
Identifier  Dist. Number 
Current 
Instruction/Service  Sch. Number 
Current 
Instruction/Service  FEFP 
Program 
Number  Survey 
Period  FTE 
Reported, 
Course  
* FL340945895734  01 7001  101 2 0834  
* FL340945895735  01 7001  103 2 0834  
FL340945895736  01 7001  102 2 0000  
FL340945895737  01 7001  102 2 0000  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the School 
Number, Current Instruction/Service or the FTE Reported, Course and resubmit the records.  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 3A. If Year -Round/Extended School Year FTE Indicator is B, then Survey Period Code must be 1 or 4.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Survey Period Code is not valid for 
the Year -Round/Extended School Year FTE Indicator.  
District Number 
Current 
Instruction/Service  Florida Education 
Identifier  Course 
Number  Survey 
Period 
Code  Year -
Round/Extended 
School Year FTE 
Indicator  
01 FL340945895734  5100070  1 B 
01 FL340945895735  5100070  4 B 
* 01  FL340945895736  5100070  2 B 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Year -
Round/Extended School Year FTE Indicator code and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 3B. If Survey Period Code is 2 or 3, Apprenticeship Sponsor Code must be a valid apprenticeship sponsor 
code listed in Appendix O, or it must be blank. A code is defined as valid if it is on Appendix O and  
Program Status is not ‘cancelled.’ For Surveys 1 and 4 the Apprenticeship Sponsor Code must be blank.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Apprenticeship Sponsor Code is 
not listed on Appendix O.  
District Number 
Current 
Instruction/Service  Florida Education 
Identifier  Survey 
Period 
Code  Apprenticeship  
Sponsorship 
Code  
01 FL340945895734  2 102134  
01 FL340945895 762 3  
*01 FL3409458957 89 2 120041  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Apprenticeship Sponsor Code and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 3C. If Course Number begins with one alphabetic character and ends with R, then the Apprenticeship 
Sponsor Code must be blank.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because the Apprenticeship Sponsor Code is not 
blank.  
Florida Education 
Identifier  Course 
Number  Apprenticeship 
Sponsorship 
Code  
FL340945895734  A46312R   
*FL340945895735  C10020R  102204  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Course 
Number or the Apprenticeship Sponsor Code and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 40. If the School Number, Current Enrollment is not N998 or N999, then it must exist on the Master School 
Identification File as a valid active number in the District Number, Current Enrollment.  
**Result:** Record rejected
EXAMPLE  
The records listed below would be rejected because the School Number, Current Enrollment is not on 
the Master School Identification File as a valid active school number in the District Number, Current 
Enrollment.  
District Number, Current 
Enrollment  School Number, 
Current Enrollment  
* 01 8311   
* 06 0001   
* 09 9999   

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the School 
Number, Current Enrollment and resubmit the records.  
 
  
 
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 41. The Career and Technical Education/Adult General Education Program Code must be a program number 
from the Career and Technical Education/Adult General Education Program Edit file (F61730) or must be 
zero -filled.  
**Result:** Record rejected
Note: For more  information on Vocational/Adult General Education Program Codes refer to  the Career 
and Technical Education Database Handbook Appendices.  
EXAMPLE  
The first and second records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. The third record would be rejected because the Vocational/Adult General 
Education Program Code is not a valid program number.  
Florida Education 
Identifier  Course Number  Career and Technical 
Education/Adult General 
Education Program Code  
FL340945895734  8772010  87720000  
FL340945895735  I480201  I480201  
*FL340945895736  8506310  5806310  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Career 
and Technical Education/Adult General Education Program Code and resubmit the record.  
 
  
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 42. School Number, Current Instruction/Service must exist on the Master School Identification File as a valid 
active number in the District Number, Current Instruction/Service or it must be C901 -C928, U970 -U981, 
P001 -P999, or 9996. If Survey Period Code = 2 or 3, then School Number, Current  Instruction/Service 
may be a private school number anywhere in Florida.  
**Result:** Record rejected
NOTE: If School Number, Current Instruction/Service is a private school number Course Number must be 
2222222.  
EXAMPLE  
The last three records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The first two records would fail this edit because they do not exist on the Master 
School Identification File as a valid and active number for the District Number, Current Instruction. The 
third record would fail this edit because it is not in the valid range for alphanumeric numbers.  
District Number , 
Current 
Instruction/Service  School Number , Current 
Instruction/Service  Survey Period 
Code  Course 
Number  
* 09  8131  2 1001010  
* 13  0021  2 5012000  
* 15  C999  2 SPN2010  
57 0051  2 5012000  
63 0031  2 5012000  
67 C904  2 SPN2010  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the School 
Number, Current Instruction/Service so that it exists as a valid and active number in the District Number, 
Current Instruction/Service or is a valid and active alphanumeric school number and resubmit the 
records.  
 
  
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 43. All numeric Course Numbers must be on the Course Code Directory file, unless School Number, Current 
Instruction/Service begins with P .  
**Result:** Record rejected
EXAMPLE  
The first, fifth and sixth records listed below would be loaded to the database assuming no other reject 
rule would cause their rejection. The second, third and fourth records would be rejected because the 
numeric Course Numbers are not on the Course Code Directory file.  
District Number 
Current Instruc t School  Number , 
Current 
Instruct ion Florida 
Education 
Identifier  Course 
Number  Survey Period 
Code  
01 P021  FL340945895734  1234567  2 
* 01  0021  FL340945895735  0801300  2 
* 01  0021  FL340945895736  0808301  2 
* 01  0021  FL340945895737  1004820  2 
01 0021  FL340945895738  1008320  2 
01 0021  FL340945895739  1200310  2 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Course 
Number and resubmit the records.  
 
  
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 44. If Grade Level equals PK -05, then the Dual Enrollment Indicator must equal Z.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would pass this edit. The second record would be rejected because the 
Grade Level is 5 and the Dual Enrollment Indicator is C.  
Florida Education 
Identifier  Grade 
Level  Dual Enrollment 
Indicator  
FL340945895734  4 Z 
*FL340945895735  5 C 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the  
relationship between the Grade Level and the Dual Enrollment Indicator and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 45. If the Course Number begins with an alpha character and is on the Course  Code Directory file, and the 
School Number, Current Instruction/Service does not begin with P , the FEFP Program Number must be 
102, 103, 112 or 113 , unless School of Enrollment = 3450 or 3950, then FEFP must be 999.   
**Result:** Record rejected
Note: Enrollment of secondary students in postsecondary vocational courses must be reported in the 
Workforce Development Information System. The parallel allowable dual enrollment hours at the high 
school are to be reported under the same postsecondary vocational course number but must be funded 
under the basic program weights of 102, 103, 112 or 113.  
EXAMPLE  
The records listed below would be rejected because the Course Number is for a postsecondary course 
(begins with an alpha character and the School Number, Current Instruction/Service does not begin with 
a P) and the FEFP Program Number is not 102, 103, 112 or 113.  
Florida 
Education 
Identifier  School Number, 
Current 
Instruction/Service  Course 
Number  Section 
Number  Period 
Number  FEFP 
Program 
Number  Grade 
Level  FTE 
Reported 
Course  
* 
FL340945895734  0021  A010304  00100  0202  300 12 0834  
* 
FL340945895735  0021  B070401  00100  0202  300 30 0834  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However,  if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Course 
Number and/or the FEFP Program Number and resubmit the records.  
## Reject Rules

Student Database 202 6-2027 /  

### 46. The first two digits of the Period Number must be 00 -80 while the last two digits must be 00 -80 or 88 
and be greater than or equal to the first two digits. For Survey 4, period 9800 may also be reported.  
**Result:** Record rejected
Note: For more information on Period number refer to the DOE Information Database Requirements: 
Volume I -- Automated Student Information System Manual.  
EXAMPLE  
The first three Student Course records listed below would be loaded to the database assuming no other 
reject rule caused their rejection. The fourth record would be rejected because the Period Number has 
an ending period with a value less than the beginning period. The last record would be rejected because 
the last two digits of Period Number are not in the acceptable range.  
Florida Education 
Identifier  Course 
Number  Section 
Number  Period 
Number  FTE 
Reported 
Course  
FL340945895734  8772030  B0100  0101  0834  
FL34094589573 5 8754500  B0100  0909  0834  
FL34094589573 6 8754500  B0300  0405  1667  
* FL340945895737  8727210  E0100  8070  2000  
* FL340945895738  8727210  E9900  8098  2000  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Period 
Number and resubmit the records.  
 
  
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 47. If Dual Enrollment Indicator code does not equal Z, then Grade Level must equal 06 -12.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would pass this edit. The second record would be rejected because the 
Grade Level is 5 and the Dual Enrollment Indicator is C.  
Florida Education 
Identifier  Grade 
Level  Dual Enrollment 
Indicator  
FL340945895734  12 A 
* FL340945895735  5 C 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
relationship between the Grade Level and the Dual Enrollment Indicator and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 48. If Dual Enrollment Indicator equals E, then School Number, Current Instruction/Service must be C901 -
C928, U970 -U981 or P001 -P999, or a school on the Master School Identification file that has School 
Function /Setting equal to T.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected since the School Number, Current 
Instruction/Service is not in the appropriate range.  
School Number, Current 
Enrollment  School Number 
Current , 
Instruction/Service  Dual Enrollment 
Indicator  
0021  C901  E 
0051  P999  E 
*0204  0204  E 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the School 
Number, Current Instruction/Service or the Dual Enrollment Indicator code and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 49. Days Per Week must be 1 -7. If Period Number is 9800, Days Per Week must equal zero.  
**Result:** Record rejected
EXAMPLE  
The first and third records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. The second record would be rejected because Days Per Week is zero.  
Florida 
Education 
Identifier  Course 
Number  FEFP Program 
Number  Grade 
Level  FTE Reported, 
Course  Class Minutes, 
Weekly  Days Per 
Week  
FL340945895734  1200310  103 12 0834  250 5 
* 
FL340945895734  1200310  103 12 1667  500 0 
FL340945895734  1200310  103 11 2000  300 5 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Days 
Per Week and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 4A. If Course Number = 9900130 -9900135 (GED Prep courses), then School Number, Current 
Instruction/Service must be a valid active school on the Master School Identification (MSID) file with 
School Function/Setting = D (DJJ).  
**Result:** Record rejected
EXAMPLE  
The second  record listed below would be loaded to the database assuming no 
other reject rule would cause its rejection. The first and third records would be rejected because the 
School Function/Setting is not D (DJJ) on the MSID.  
District 
Number 
Current, 
Instruc./Service  School Number 
Current, 
Instruc ./Service  Florida Education 
Identifier  Course 
Number  District 
Number  School 
Number  School 
Function/Setting  
* 49  0201  FL340945895734  9900133  49 0201  Z 
49 9031  * 
FL340945895734  9900132  49 9031  D 
* 49  9013  FL340945895734  9900130  49 9013  M 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Course 
Numbers on the  records or the school type on the Master School Identification 
file and resubmit the records for processing.  
 
  
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 4B. Location of Student must be N, S, T or Z.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no  other reject rule would 
cause their rejection. The third record would be rejected because the Location of Student code is not 
valid.  
District Number 
Current, 
Instruction/Service  School Number Current, 
Instruction/Service  Survey 
Period 
Code  Florida Education 
Identifier  Course 
Number  Location of 
Student  
31 7004  2 FL340945895734  0706320  N 
31 0291  2 FL34094589573 5 1209800  Z 
* 31  7004  2 FL34094589573 6 0706320  P 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Location of Student code and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 4C. Florida Education Identifier (FLEID) is alphanumeric and must be entered as “FL” in the first 2 positions 
followed by twelve numeric digits. No blanks, spaces or all zeros for the twelve numeric digits are 
allowable.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Florida Education Identifier (FLEID) 
is not a valid FLEID.  
District Number, Current Enrollment  Florida Education 
Identifier  
01 FL340945895734  
01 FL004583948567  
* 01  FL00 0000000000  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Florida 
Education Identifier and resubmit the record for processing.  
 
  
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 4D. If Period Number is 9800, Course Number must be 1200310, 2000310, 1206310 or 2100310 and FEFP 
Program Number must be 102 or 103.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Course Number is not valid.  
District Number 
Current, 
Instruction/Service  School Number Current, 
Instruction/Service  Survey 
Period 
Code  Period 
Number  Course 
Number  FEFP Program 
Number  
15 0021  4 9800  1200310  103 
15 0021  4 9800  1206310  103 
* 15  0021  4 9800  1200320  103 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Course 
Number and resubmit the record for processing.  
 
  
 
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 4F. If Period Number is 9800, then all of the following must be N:  
Day of Week Scheduled, Monday,  
Day of Week Scheduled, Tuesday,  
Day of Week Scheduled, Wednesday,  
Day of Week Scheduled, Thursday,  
Day of Week Scheduled, Friday,  
Day of Week Scheduled, Saturday.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Day of Week Scheduled, Monday is 
not valid.  
District Number 
Current, 
Instruction/Service  School Number 
Current, 
Instruction/Service  Survey 
Period 
Code  Period 
Number  Course 
Number  Day of 
Week 
Scheduled, 
Monday  
54 0301  4 9800  1200310  N 
54 0301  4 9800  1206310  N 
* 54  0301  4 9800  2000310  Y 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Day of 
Week Scheduled, Monday and resubmit the record for processing.  
 
  
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 4G. If Period Number is 9800, Day of Week Scheduled, Alternate Date Certain must be Z.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Day of Week Scheduled, Alternate 
Date Certain is not valid.  
District Number 
Current, 
Instruction/Service  School Number Current, 
Instruction/Service  Survey 
Period 
Code  Period 
Number  Course 
Number  Day of Week 
Scheduled, 
Alternate Date 
Certain  
63 0021  4 9800  1200310  Z 
63 0021  4 9800  1206310  Z 
* 63  0021  4 9800  2000310  N 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Day of 
Week Scheduled, Alternate Date Certain and resubmit the record for processing.  
 
  
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 4I. If School Number Current Instruction/Service  
• equals 7001, 7004, 7006, or 7023;  
• or if District Number Current Instruction/Service equals 71;  
• or Charter School Status is not Z and School Function/Setting = V on the Master School 
Identification file, then, Location of Student must be N or S. All other schools must be  T, 
or Z.  
**Result:** Record rejected
EXAMPLE  
The first four records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The fifth record would be rejected because the Location of Student code is not 
valid for the School Number, Current Instruction/Service.  
District Number 
Current, 
Instruction/Service  School Number Current, 
Instruction/Service  Survey 
Period 
Code  Florida Education 
Identifier  Course 
Number  Location of 
Student  
31 7004  2 12345678912X  0706320  S 
71 0500  4 12345679012X  1209800  N 
71 0600  3 12345679123X  1209800  S 
01 0300  3 12345679234X  0706320  Z 
* 31  0021  2 12345679356X  0706320  S 

**District Responsibility:** The district must review the Location of Student code and the School Number and correct the item that 
is in error.  
 
  
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 51. If Survey Period = 1 -4 and the student's Grade Level is 7 -12, Class Minutes, Weekly must be greater than 
zero. If Period Number is 9800, Class Minutes, Weekly must be equal to zero.  
**Result:** Record rejected
EXAMPLE  
The first and fourth records below would be loaded to the database assuming no other reject rule would 
cause their rejection. The second and third records would be rejected because the appropriate 
relationship between Grade Level and Class Minutes, Weekly is not present.  
Florida Education 
Identifier  FEFP Program 
Number  Grade Level  FTE 
Reported, 
Course  Class 
Minutes, 
Weekly  
FL340945895734  102 05 0834  0000  
* FL340945895735  103 12 0834  0000  
* FL340945895736  300 10 1667  0000  
FL340945895737  103 11 2000  0600  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
relationships between Grade Level and Class Minutes, Weekly and resubmit the records.  
 
  
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 52. If the School Number, Current Enrollment is N999 (private school), then Dual Enrollment Indicator must 
be Z.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third and fourth record would be rejected because the Dual Enrollment 
Indicator is not Z for private school students (school of enrollment of N999).  
District Number 
Current, 
Instruction/Service  School Number 
Current, 
Instruction/Service  Survey 
Period 
Code  Florida Education 
Identifier  Dual 
Course 
Number  Enrollment 
Indicator  
31 N999  2 FL340945895734  1007350  Z 
31 N999  2 FL340945895735  1209800  Z 
*31 N999  2 FL340945895736  PHY1050  A 
*31 N999  2 FL340945895737  1007350  A 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Dual 
Enrollment Indicator or the School Number, Current Enrollment and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 53. If Course Number begins with a number; and    
• is a course  number from the  Career and Technical  Education/Adult General Education Program 
Edit file (F61730); other than 0200320, 0200335,  1006300,  1700510,  2000350, 2000360, 
2102360, 2102370, 3027010 or 3027020; or  
• FEFP Program Number is 300 and course number is 0200320, 0200335, 1006300,  1700510,  
2000350,  2000360,  2102360, 2102370, 3027010 or 3027020  
then the Career and Technical Education/Adult General Education Program Code must be a valid 
program number, other than 9900010 or 9900099, for the Course Number submitted, as listed in file 
F61730.  
If Course Number begins with three alphabetic characters followed by a zero in the fourth position, and  
• Is a course  number from the Career and Technical Education/Adult General Education Program 
Edit file (F61730); then the Career and Technical Education/Adult General Education Program 
Code must be a valid program number for the Course Number submitted, as listed in file F61730.  
If Course Number begins with one alphabetic character followed by a numeric digit, and  
• is a course number from the Career and Technical Education/Adult General Education Program 
Edit file (F61730);  
then the Career and Technical Education/Adult General Education Program Code must be the same as 
the Course Number.  
**Result:** Record rejected
EXAMPLE  
Record 1 is rejected because for numeric CTE course numbers, the CTE/AGE Program Code must be a 
valid program number listed in file F61730 and is explicitly prohibited from being 9900010 or 9900099. 
Record 3 is rejected because for courses beginning with three alphabetic characters followed by a zero 
(i.e., ACR0041), the CTE/AGE Program Code must be a valid program number for that specific course as 
listed in file F61730. Record 5 is rejected because for courses beginning with one alphabetic character 
followed by a numeric digit (i.e., C10020R), the CTE/AGE Program Code must be identical to the Course 
Number.  
Florida Education 
Identifier (FLEID)  Course Number  FEFP Program Number  CTE/AGE Program Code  
FL123456789001  8772010  300 9900010  
FL123456789002  8772010  300 8772000  
FL123456789003  ACR0041  300 ZZZZZZZ  
FL123456789004  C10020R  300 C10020R  
FL123456789005  C10020R  300 8772000  
 
  
 
Student Database 202 6-2027 /  

**District Responsibility:** If a record is rejected, the district must verify the correct CTE/AGE Program Code associated with the 
specific Course Number as defined in the F61730 file. The district must then correct the code and 
resubmit the record for processing.  
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

UPDATED 07/01/2 026 

### 54. If the Virtual Instruction Provider code is:  
• 071 (Florida Virtual School) then Grade Level must be KG -12. 
• 302 (K12 Florida, LLC) then Grade Level must be KG -12. 
• 308 (Somerset Academy, Inc.) then Grade Level must be KG -12. 
• 309 (Imagine Learning) then Grade Level must be KG -12. 
• 311 (Mater Virtual Academy) then Grade Level must be KG -12. 
• 313 (District VIP – Florida Connections Academy, LLC) then Grade Level must be KG -12. 
• 320 (Graduation Alliance) then Grade level must be 09 -12. 
• 322 (Accel Online East) then Grade Level must be KG -12. 
• 323 (Optima Academy Online) then Grade Level must be KG -12. 
• 326 (K12 Preparatory Academy) then Grade Level must be 9 -12. 
• 327 (UCP of Central Florida) then Grade Level must be KG -5. 
• 328 (Second Mile Education) then Grade Level must be 7 -12. 
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Grade Level is not valid for the 
Virtual Instruction Provider code.  
District Number 
Current, 
Instruction/Service  School Number 
Current, 
Instruction/Service  Survey 
Period 
Code  Florida  
Education 
Identifier  Grade 
Level  Virtual 
Instruction 
Provider  
31 7001  2 FL340945895734  04 302 
31 7001  2 FL340945895735  09 071 
*31 7001  2 FL340945895736  04 320 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Virtual 
Instruction Provider or the Grade Level and resubmit the record.  
 
  
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

UPDATED 07/01/2026   

### 55. If District Number, Current Instruction is not 71  and  
• School Number, Current Instruction is not 7001, 7004, 7006, or 7023 and 
• if Term equals 4, 5, or S,  
then Survey Period Code must be 1 or 4.  
 
If District Number, Current Instruction is 71 and  
• School Number, Current Instruction equals 0500, 0600 or 0700 and  if Term equals 4, 5, or S,  
then Survey Period Code must be 1, 2, 3 or 4.  
 
If District Number, Current Instruction is 71 and School Number, Current  
Instruction equals = 0300 or 0400 or 0801,  
• or If District Number, Current Instruction is not 71 and  
• if School Number, Current Instruction is 7001, 7004, 7006, or 7023 and  
• if Term equals 4, 5 or S  
  then Survey Period Code must be 4.  
EXAMPLE  
**Result:** Record rejected
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third and fourth records would be rejected because the Term code is not valid 
for the Survey Period Code.  
District Number 
Current, 
Instruction/Service  Florida Education 
Identifier  Course 
Number  Survey 
Period Code  Term  
01 FL340945895734  5100070  1 4 
01 FL340945895735  5100070  4 5 
* 01  FL340945895736  5100070  2 S 
* 01  FL340945895737  5100070  3 S 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Term 
or Survey Period Code and resubmit the records.  
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 56. If Grade Level code is PK and the FEFP Program Number is not 111, 254 or 255, then FEFP Program 
Number must be 101 or 999.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The last record would be rejected because the student's Grade Level code is PK, 
the student is not exceptional and the FEFP Program Number is not 101 or 999.  
Florida Education 
Identifier  FEFP Program 
Number  Grade Level  FTE 
Reported, 
Course  
FL340945895734  254 PK 0834  
FL340945895735  999 PK 0000  
FL340945895736  102 PK 0834  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct either the 
Grade Level or the FEFP Program Number and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 57. If School Number, Current Instruction/Service is 7001, then the Virtual Instruction Provider code must be 
a valid code in Appendix CC.  
All other schools except Virtual Charter Schools (where on the Master School ID file School 
Function /Setting = V and Charter School Status is not equal to Z) must be ZZZ.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Virtual Instruction Provider code is 
not valid for the School Number, Current Instruction/Service.  
District Number 
Current, 
Instruction/Service  School Number 
Current, 
Instruction/Service  Survey 
Period 
Code  Florida 
Education 
Identifier  Course 
Number  Virtual 
Instruction 
Provider  
31 7001  2 FL340945895734  1001020  302 
31 0521  2 FL340945895735  1205010  ZZZ 
*31 7001  2 FL340945895736  1303000  ZZZ 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Virtual 
Instruction Provider or the School Number, Current Instruction/Service and resubmit the record.  
 
 
  
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 59. If Year -Round/Extended School Year FTE Indicator is A then the Year  Round  School code on the Master 
School Identification file must be Y for the reported School Number, Current Instruction/Service. Match 
to the Master School Identification file using District Number, Current Instruction/ Service and School 
Number, Current Instruction/Service.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Year -Round/Extended School Year 
FTE Indicator code is not valid for the School Number, Current Instruction/Service.  
 records  
District Number 
Current 
Instruction/Service  Florida 
Education 
Identifier  School Number 
Current  
Instruction/Service  Survey 
Period Code  Year -
Round/Extended 
School Year FTE 
Indicator  
01 FL340945895734  0021  2 A 
01 FL340945895735  0551  2 A 
* 01 FL340945895736  2031  2 A 
 
Master School Identification file records  
District Number 
Current  School Number  Year Round  
School  
01 0021  Y 
01 0551  Y 
* 01  2031  Z 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Year -
Round/Extended School Year FTE Indicator code or the Year Round School code on the Master School 
Identification file and resubmit the record.  
 
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 5B. If Grade Level = 06 -12 and Course Number contains an alpha character in the first position, then Dual 
Enrollment Indicator must be other than Z.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would pass this edit. The second record would be rejected because the 
Grade Level is 12 and the Course Number contains an alpha character, but the dual Enrollment Indicator 
is Z.  
Florida Education Identifier  Course Number  Grade Level  Dual Enrollment Indicator  
FL340945895734  B070401  12 C 
* FL340945895735  A010304  12 Z 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
relationship between Course Number, Grade Level, and Dual Enrollment Indicator and resubmit the 
record.  
 
  
 
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 5C. If FEFP Program Number is 130, English Language Learners: Instructional Model code must be C, E, I, O, 
S, or T.  
**Result:** Record rejected
EXAMPLE  
The first and second records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. The third record would be rejected because the relationship between the 
FEFP Program Number and the English Language Learners: Instructional Model is not valid.  
Florida Education 
Identifier  School Number 
Current 
Enrollment  FEFP 
Program 
Number  English Language 
Learners: Instructional 
Model  
FL340945895734  0021  130 C 
FL340945895735  3900  130 Z 
FL340945895736  0021  130 Z 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct either the 
FEFP Program Number or the English Language Learners: Instructional Model and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 5D. If Survey Period Code is 2 or 3, then Day of Week Scheduled, Monday must be Y or N.  
**Result:** Record rejected
EXAMPLE  
The first and third records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. The second record would be rejected because Day of Week Scheduled, 
Monday is invalid.  
Florida Education 
Identifier  Course 
Number  Days Per 
Week  Day of Week 
Scheduled, 
Monday  Survey 
Period Code  
FL340945895734  1200310  5 Y 2 
* 
FL340945895735  1200310  0 Z 2 
FL340945895736  1200310  2 N 2 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Day of 
Week Scheduled, Monday and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 5E. If Survey Period Code is 2 or 3, then Day of Week Scheduled, Tuesday must be Y or N.  
**Result:** Record rejected
EXAMPLE  
The first and third records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. The second record would be rejected because Day of Week Scheduled, 
Tuesday is invalid.  
Florida Education 
Identifier  Course Number  Days Per Week  Day of Week Scheduled, Tuesday  Survey Period Code  
FL340945895734  1200310  5 Y 2 
* FL340945895735  1200310  0 Z 2 
FL340945895736  1200310  2 N 2 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Day of 
Week Scheduled, Tuesday and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 5F. If Survey Period Code is 2 or 3, then Day of Week Scheduled, Wednesday must be Y or N.  
**Result:** Record rejected
EXAMPLE  
The first and third records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. The second record would be rejected because Day of Week Scheduled, 
Wednesday is invalid.  
Florida Education 
Identifier  Course 
Number  Days Per 
Week  Day of Week Scheduled, 
Wednesday  Survey Period 
Code  
FL340945895734  1200310  5 Y 2 
* FL340945895735  1200310  0 Z 2 
FL340945895736  1200310  2 N 2 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Day of 
Week Scheduled, Wednesday and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 5G. If Survey Period Code is 2 or 3, then Day of Week Scheduled, Thursday must be Y or N.  
**Result:** Record rejected
EXAMPLE  
The first and third records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. The second record would be rejected because Day of Week Scheduled, 
Thursday is invalid.  
Florida Education 
Identifier  Course Number  Days Per Week  Day of Week Scheduled, Thursday  Survey Period Code  
FL340945895734  1200310  5 Y 2 
* FL340945895735  1200310  0 Z 2 
FL340945895736  1200310  2 N 2 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Day of 
Week Scheduled, Thursday and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 5H. If Survey Period Code is 2 or 3, then Day of Week Scheduled, Friday must be Y or N.  
**Result:** Record rejected
EXAMPLE  
The first and third records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. The second record would be rejected because Day of Week Scheduled, 
Friday is invalid.  
Florida Education 
Identifier  Course Number  Days Per Week  Day of Week Scheduled, Friday  Survey Period Code  
FL340945895734  1200310  5 Y 2 
* FL340945895735  1200310  0 Z 2 
FL340945895736  1200310  2 N 2 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Day of 
Week Scheduled, Friday and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 5I. If Survey Period Code is 2 or 3, then Day of Week Scheduled, Saturday must be Y or N.  
**Result:** Record rejected
EXAMPLE  
The first and third records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. The second record would be rejected because Day of Week Scheduled, 
Saturday is invalid.  
Florida Education 
Identifier  Course Number  Days Per Week  Day of Week Scheduled, Saturday  Survey Period Code  
FL340945895734  1200310  5 Y 2 
* FL340945895735  1200310  0 Z 2 
FL340945895736  1200310  2 N 2 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Day of 
Week Scheduled, Saturday and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 5K. If Survey Period Code is 2 or 3, and  
If the School Number, Current Instruction/Service is not 7001, 7004, 7006 or 7023; or the School 
Number, Current Instruction/Service has a School Function /Setting of V and a Charter School Status not 
equal to Z on the Master School Identification file,   
then at least one of the following must be Y: Day of Week Scheduled, Monday; Day of Week Scheduled, 
Tuesday; Day of Week Scheduled, Wednesday; Day of Week Scheduled, Thursday; Day of Week 
Scheduled, Friday or Day of Week Scheduled, Saturday.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because none of the Day of Week Scheduled 
elements are coded Y .  
Florida 
Education 
Identifier  Sch 
Num 
Curr. 
Enr Days 
Per 
Week  Day of 
Week 
Sched.  
Mon.  Day of 
Week 
Sched.  
Tues.  Day of 
Week 
Sched.  
Wed.  Day of 
Week 
Sched.  
Thurs.  Day of 
Week 
Sched.  
Fri. Day of 
Week 
Sched. 
Sat. Survey 
Period 
Code  
FL340945895734  0411  5 Y Y Y Y Y Y 2 
* 
FL340945895735  0411  3 N  N  N  2 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct at least 
one Day of Week Scheduled and resubmit the record.  
 
  
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 5L. If Survey Period Code is 2 or 3, then Day of Week Scheduled, Alternate Date Certain must be Y , N or Z.  
**Result:** Record rejected
EXAMPLE  
The first and third records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. The second record would be rejected because Day of Week Scheduled, 
Alternate Date Certain is blank.  
Florida Education 
Identifier  Course Number  Days Per 
Week  Day of Week 
Sched uled , 
Alternate 
Date Certain  Survey 
Period Code  
FL340945895734  1200310  5 Y 2 
* FL340945895735  1200310  0  2 
FL340945895736  1200310  2 N 2 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Day of 
Week Scheduled, Alternate Date Certain and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 5M. If Survey Period code is 2 or 3 and Day of Week, Scheduled Friday is Y , then Day of Week Scheduled, 
Alternate Date Certain must be N or Z.  
**Result:** Record rejected
EXAMPLE  
The first, second and fourth records listed below would be loaded to the database assuming no other 
reject rule would cause their rejection. The third record would be rejected because the correct 
relationship between Day of Week Scheduled, Friday and Day of Week Scheduled, Date Certain does not 
exist.  
Note: In the fourth record below, although Day of Week Scheduled, Friday is N, it is not automatically 
assumed that Day of Week Scheduled, Alternate Date Certain is Y unless all of the students in the 
entire school are not scheduled in any core classes (See Appendix S) on Friday.  
Florida Education 
Identifier  Course Number  Days Per 
Week  Day of Week 
Sched uled,  
Friday Day of Week 
Scheduled, 
Alternate 
Date Certain  
FL340945895734  1200310  8 Y N 
* FL340945895735  1200310  2 N Y 
FL340945895736  1200310  2 Y Y 
FL340945895737  1200310  4 N N 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the record 
so that the correct relationship exists between Day of Week Scheduled, Friday and Day of Week 
Scheduled, Alternate Date Certain and resubmit the record.  
 
  
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 5P. If District Number, Current Instruction/Service is equal to 71 and School Number, Current  
Instruction/Service equals 0500, 0600, or 0700 then FEFP Program Number must equal 101, 102, 103, 
111, 112, 113 or 300 , unless School of Enrollment = 3450 or 3950, then FEFP must be 999.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
it rejection. The second record would be rejected because FEFP Program Number does not equal 101, 
102, 103, 111, 112, 113 or 300.  
District 
Number , 
Current  
Enrollment  District Number , 
Current 
Instruction/Service  Florida Education 
Identifier  Course 
Number  FEFP 
Program 
Number  School Number, 
Current 
Instruction /Service  
23 71 FL340945895734  2109370  103 0500  
* 23  71 FL340945895735  2109370  254 0500  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the FEFP 
Program Number and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 5Q. If the School Number, Current Instruction/Service is equal to 7004 and School Number, Current 
Enrollment is not equal to 7004, then FEFP Program Number must be 101, 102, 103, 111, 112, 113, or 
300, unless School of Enrollment = 3450  or 3950,  then FEFP must be 999.  
Record rejecte d 
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because FEFP Program Number does not equal 
to 101, 102, 103, 111, 112, 113 or 300.  
District 
Number, 
Current 
Enrollment  School Number, Current 
Instruction/Service  Florida Education 
Identifier  Course 
Number  FEFP 
Program 
Number  FTE 
Reported , 
Course  
06 7004 FL340945895734  2109370  103 0834  
06 7004 FL340945895735  2109370  101 0834 
* 06  7004  FL340945895736  0200050  130 0834  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the FEFP 
Program Number and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 5S. If Course Number is 5100580 or 5100590 then FEFP Program Number must be 999 and FTE Reported, 
Course must be 0000 and Grade Level must be PK.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the student’s Course Number is 
5100590 and FEFP Program Number is 101. The last record would be rejected because the student's 
Course Number is 5100580, and FTE Reported, Course is 0834.  
Course Number  FEFP 
Program 
Number  Grade Level  FTE Reported, 
Course  
5100580  999 PK 0000  
5100590  999 PK 0000  
* 5100590  101 PK 0000  
* 5100580  999 PK 0834  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the FEFP 
Program Number and the FTE Reported, Course and resubmit the records.  
 
  
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 5U. If Survey Period Code is 2 or 3 and if FEFP Program Number is 130, then the Course Number must be a 
course in Appendix DD.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the FEFP Program Number is 130 and 
the Course Number is not in Appendix DD.  
District Number, 
Current 
Instruction/Service  Florida Education 
Identifier  FEFP 
Program 
Number  Course 
Number  
01 FL340945895734  130 1001040  
01 FL340945895735  130 1002000  
* 01  FL340945895736  130 1301000  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct either the 
Course Number or the FEFP Program Number and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 5V. If Survey Period is 2, 3 or 4 and if English Language Learners: Instructional Model is S or C, then Course 
Number must be a Mathematics, Science, Social Studies or Computer Education course in Appendix DD.  
If Survey Period is 1 and if English Language Learners: Instructional Model is S or C, then Course Number 
must be a Mathematics, Science, Social Studies or Computer Education course in the current or prior 
year in Appendix DD.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected since Course Number 1000010 is not a Science, 
Social Studies, or Computer Literacy course in Appendix DD.  
District Number, 
Current Enrollment  Florida Education 
Identifier  English 
Language 
Learners: 
Instructio
nal 
Model  Course 
Number  
01 FL340945895734  S 2100310  
01 FL340945895735  C 2002480  
* 01  FL340945895736  S 1000010  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct either the 
English Language Learners: Instructional Model code or the Course Number and resubmit the record.  
 
  
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 5W. If Survey Period is 2, 3 or 4 and if English Language Learners: Instructional Model is E or I, then Course 
Number must be a Language Arts Course Number in Appendix DD.  
If Survey Period is 1 and if English Language Learners: Instructional Model is E or I, then Course Number 
must be a Language Arts Course Number in the current or prior year in Appendix DD.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected since Course Number 1204000 is not a 
Language Arts course in Appendix DD.  
District Number, 
Current Enrollment  Florida Education 
Identifier  FEFP 
Program 
Number  Course 
Number  
01 FL340945895734  E 1000000  
01 FL340945895735  I 1000010  
* 01  FL340945895736  E 1204000  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct either the 
English Language Learners: Instructional Model code or the Course Number and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

5Y . 
If School Number, Current Enrollment is not equal to 7001 or 7023 and if School Number, Current 
Instruction/Service is equal to 7001 or 7023, then FEFP Program Number must be 101, 102, 103, 111, 
112, 113, or 300 , unless School of Enrollment = 3450 or 3950, then FEFP must be 999.   
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because FEFP Program Number is not valid for 
the school number reported.  
School  
Number, 
Current 
Enrollment  School Number, 
Current 
Instruction/Service  Florida Education 
Identifier  Course 
Number  FEFP 
Program 
Number  FTE Reported , 
Course  
7001  7001  FL340945895734  2109370  103 0834  
7001  7001  FL340945895734  2109370  111 0834  
* 7001  7001  FL340945895734  0200050  130 0834  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the FEFP 
Program Number or School Number, Current Instruction/Service and resubmit the record.  
 
  
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 5Z. If the School Number, Current Instruction/Service is C901 -C928, U970 -U981 or P001 -P999, then the Dual 
Enrollment Indicator must be other than Z.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Dual Enrollment Indicator is code 
Z.  
School Number, Current 
Enrollment  School Number Current , 
Instruction/Service  Dual Enrollment Indicator  
0021  C901  A 
0051  P999  A 
* 0204  U970  Z 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Dual 
Enrollment Indicator and resubmit the record.  
 
 01 0021  FL123456789003  1001040  
 
Student Demographic Information  
District 
Number, 
Current 
Enrollment  School 
Number, 
Current 
Enrollment  Florida 
Education 
Identifier (FLEID)  
01 0021  FL123456789000  
10 0100  FL123456789001  
05 0030  FL123456789002  
01 0021  FL123456789003  

**District Responsibility:** Student Database 202 6-2027 /  
 
 VALIDATION/NULL EDIT  

### 60. The student's Grade Level on the Student Course record must agree with the  Grade Level on the 
Student Demographic record submitted by the district of instruction unless Year -Round/Extended School 
Year FTE Indicator on the Student Course record = A or if Survey Period Code = 1 or 4.  
State Validation/NULL  
**FTE Reported, Course on all Student Course records set to NULL value for these records at the close of 
the State Records Processing Cycle.**  
EXAMPLE  
The first and third Student Course records listed below would pass this edit. The second and fourth 
records would not pass the edit because the Grade Level codes on the Student Demographic records and 
Student Course records do not agree. (The FTE Reported, Course on the Student Course records would 
be set to a null value at the close of the State Records Processing Cycle.)  
                    Student Demographic Records                                         Student Course Records  
 
District 
Number, 
Current 
Instruc./Service  Florida 
Education 
Identifier  Grade 
Level  
49 FL340945895734  12 
49 FL340945895735  11 
49 FL340945895736  11 
49 FL34094589573 7 12 

**District Responsibility:** The Grade Level codes which do not agree must be corrected. If the Grade Level code on the Student 
Demographic record is correct, then the Grade Level code on the Student Course record must be 
updated so that it agrees. If the Grade Level code on the Student Course record is correct, then the 
Student Demographic record must be updated so that the Grade Level codes agree.  
 
  
 
 
 District 
Number, 
Current 
Instruc./Service  Florida 
Education 
Identifier  Grade 
Level  
49 FL340945895734  12 
*49 FL340945895735  12 
49 FL340945895736  11 
*49 FL340945895737  10 
  
 
Student Database 202 6-2027 /  
 
 VALIDATION/NULL EDIT  

### 61. During Surveys 1 through 4 if FTE Reported, Course is greater than zero and  the student is less than 
3 years old, then Grade Level must be PK and FEFP Program Number must be 101, 111 or 254 -255.  
State Validation/NULL  
**FTE Reported, Course set to NULL after the close of the State Records Processing Cycle**  
EXAMPLE  
If the Birth Date on the matching Student Demographic records for each of the Student Course records 
listed below indicates that the student's age is less than 3, then the record marked with an asterisk 
would fail the edit because the correct relationship between Grade Level code, FEFP Program Number 
and FTE Reported, Course does not exist.  
Florida 
Education 
Identifier  Section 
Number  FEFP Program 
Number  FTE Reported , 
Course  Grade 
Level  
FL340945895734  00100  254 0834  PK 
FL34094589573 4 00200  101 0012  PK 
* 
FL34094589573 4 00500  999 0834  PK 
FL340945895734  A1500  111 0834  PK 

**District Responsibility:** The district must correct the records so that the correct relationship between Grade Level, FEFP Program 
Number and FTE Reported, Course exists.  
 
  
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
 
 VALIDATION/NULL EDIT  
UPDATED 07/01/2026  

### 66. If Period Number is not 9800  
Then each Student Course record must have a matching Teacher Course record based on the key fields of 
District Number, Current Instruction/Service; School Number, Current Instruction/ Service; Survey Period 
Code; Fiscal Year; Course Number; Section Number; Period Number; and Term.  
State Validation/NULL  
**FTE Reported, Course set to NULL following the close of the State Records Processing Cycle**  
EXAMPLE  
The first and second Student Course records listed below would  pass this edit. The  third Student Course 
Schedule would be flagged in error because of the failure to have a matching Teacher Course Schedule 
based on the keys of District Number, Current Instruction/Service; School Number, Current  
Instruction/Service; Survey Period Code; Fiscal Year; Course Number; Section Number; Period Number; 
and Term.  
Student Course Records  
District 
Number, 
Current 
Instruction/
Service  School 
Number, 
Current 
Instructio
n/Service  Florida 
Education 
Identifier  Survey 
Period 
Code  Fiscal 
Year  Course 
Number  Sec. No.  Period 
Number  Term  
01 0421  FL34094589573
4 2 ****  1200330  00200  0404  1 
01 0421  FL34094589573
5 2 ****  1200330  00200  0404  1 
* 01  0421  FL34094589573
6 2 ****  1200330  00100  0303  1 
Teacher Course Records  
District 
Number, 
Current 
Instructi
on/Servi
ce School 
Number, 
Current 
Instruction/
Service  Survey 
Period 
Code  Fiscal 
Year  Course 
Number  Section 
Number  Period 
Number  Term  Social 
Security 
Number  
01 0421  2 ****  1200330  00200  0404   0000291125  
01 0421  2 ****  1200330  00200  0404   0000291125  
**** = Valid fiscal year for data submission.  

**District Responsibility:** Student Database 202 6-2027 /  
 
 If the Student Course record is valid, submit the Matching Teacher Course Schedule record for that class. 
If the Student Course record is invalid, delete the record from the database. If an error has been made in 
one or more of the data elements required to match on either the Student Course record or the Teacher 
Course record, then the record(s) should be corrected so that the two types of records match for each of 
the data elements of District Number, Current Instruction/Service; School Number, Current 
Instruction/Service; Survey Period Code; Fiscal Year; Course Number; Section Number; Period Number; 
and Term.  
 
  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
 
 VALIDATION/NULL EDIT  

### 67. Each  must have a matching Student Demographic record based on District 
Number, Current Enrollment; School Number, Current Enrollment; Florida Education Identifier (FLEID); 
Survey Period Code; Fiscal Year; and District Number, Current Instruction/Service.  
State Validation/NULL  
**FTE Reported, Course set to NULL for ALL  records for this student**  
EXAMPLE  
The  listed below which is marked with an asterisk would fail the edit above 
because it does not have a matching Student Demographic record.  
Student Demographic Records  
District Number, Current 
Instruction/Service  District 
Number, 
Current 
Enrollment  Florida Education 
Identifier  School 
Number, 
Current 
Enrollment  Survey 
Period 
Code  Fiscal 
Year  
01 01 FL340945895734  0021  3 ****  
01 01 FL340945895735  0021  3 ****  
01 01 FL340945895736  0021  3 ****  
 
Student Course Records  
District Number, Current 
Instruction/Service  District 
Number, 
Current 
Enrollment  School 
Number, 
Current 
Enrollment  Florida Education 
Identifier  Survey 
Period 
Code  Fiscal 
Year  
01 01 0021  FL340945895734  3 ****  
01 01 0021  FL340945895735  3 ****  
* 01  01 0321  FL340945895736  3 ****  
      **** = Valid fiscal year for data submission.  

**District Responsibility:** The district must verify the various key comparisons from the Student Course record, correct those in 
error and resubmit the correction. For more detailed explanation of the proper submission of the various 
keys, consult the front pages of both the Student Demographic Information and Student Course 
Schedule formats.  
 
  
  
 
Student Database 202 6-2027 /  
 
 VALIDATION/NULL EDIT  

### 69. If Survey Period Code = 1 -4, each  record with FEFP Program Number equal to 
111-113 or 254 -255 must have a matching Exceptional Student record based on District Number, Current 
Enrollment; School Number, Current Enrollment; Florida Education Identifier (FLEID); Survey Period Code 
and Fiscal Year unless Survey Period Code = 2 or 3 and School Number, Current Instruction/Service is a 
private school number.  
State Validation/NULL  
**FTE Reported, Course set to NULL for all  records for this student**  
EXAMPLE  
The  listed below which is marked with an asterisk would fail the edit above 
because it does not have a matching Exceptional Student record.  
Exceptional Student Records  
District Number, Current 
Enrollment  School 
Number, 
Current 
Enrollment  Florida Education 
Identifier  Survey 
Period 
Code  Fiscal 
Year  
01 0021  FL340945895734  2 ****  
01 0021  FL340945895735  2 ****  
01 0021  FL340945895736  2 ****  
 
Student Course Sche dule Records  
District Number, Current 
Enrollment  School 
Number, 
Current 
Enrollment  Florida Education 
Identifier  Survey 
Period 
Code  Fiscal 
Year  FEFP 
Progr
am 
Num
ber 
01 0021  FL340945895734  2 ****  111 
01 0021  FL340945895735  2 ****  112 
01 0021  FL340945895736  2 ****  113 
* 01  0021  FL340945895737  2 ****  254 
      **** = Valid fiscal year for data submission.  

**District Responsibility:** If the  record is valid, the district must submit the matching Exceptional Student 
record. If the  record is invalid, the district must either delete the record or 
correct the invalid elements.  
 
  
 
Student Database 202 6-2027 /  
 
 VALIDATION/NULL EDIT  

### 72. If FEFP Program Number equals 130, then English Language Learners, PK - 12 on the Student 
Demographic Information record (matched on District Number, Current Enrollment; School Number, 
Current Enrollment; Florida Education Identifier (FLEID); Survey Period Code; Fiscal Year; and District 
Number, Current Instruction/Service) must equal to LY or LP .  
State Validation/NULL  
**FTE Reported, Course set to NULL after the close of the State Records Processing cycle.**  
EXAMPLE  
The second and third records below would pass this edit. The first and fourth records listed below and 
flagged with asterisks would cause error messages to be generated because the English Language 
Learners, PK -12 code does not equal to LY nor LP . If the error is not corrected by the end of the state 
processing period, the FTE Reported, Course will be sent to NULL.  
 Records  
Florida Education 
Identifier  FEFP 
Program 
Number  Course 
Number  
* FL340945895734  130 1200310  
FL340945895735  130 1200310  
FL340945895736  130 1200310  
* FL340945895737  130 1200310  
 
Student Demographic Information  Records  
Florida Education 
Identifier  English Language 
Learners , PK-12 
* FL340945895734  LF 
FL340945895735  LY 
FL340945895736  LP 
* FL340945895737  LN 

**District Responsibility:** The district must review the FEFP Program Number and English Language Learners, PK - 12 codes and 
correct the codes that are in error. If the end of the state processing cycle has occurred and the FTE 
Reported, Course has been changed to a NULL value, then the district must also resubmit the Student 
Course Schedule record with the proper FTE Reported, Course.  
  
 
Student Database 202 6-2027 /  
 
 VALIDATION/NULL EDIT  

### 73. For Surveys 2 and 3;  
• if School Number, Current Enrollment is not N998, nor N999; and  
• if School Number, Current Instruction/Service is not 0500, 0600 nor 0700 within District  Number, 
Current Instruction/Service 71, and  
• if FTE Reported, Course is greater than zero, and  
• if the student has a Withdrawal Code, PK -12 of DNE on a Prior School  Status/Student 
Attendance record, or if there is no matching Prior School Status/Student Attendance record,  
then FTE Reported, Course is set to NULL after the close of the state records processing cycle.  
The match should be made using Year (School and Fiscal), Survey Period Code, District Number, Current 
Enrollment and Florida Education Identifier (FLEID). If the student has more than one Prior School 
Status/Student Attendance record, the match should be made to the record with the most recent Entry 
(Re-entry) Date.  
State Validation/NULL  
EXAMPLE  
In the example below all FTE Reported, Course amounts would be set to null after the end of the state 
processing period except for the FTE Reported in the third record.  records 
should not be submitted for a student with a “Did Not Enter” Withdrawal Code.  
Prior School Status/Student Attendance Records  
School 
Year  Survey 
Period 
Code  District 
Number, 
Current 
Enrollment  Florida Education 
Identifier  Withdrawal 
Code, PK -12 
****  2 03 FL340945895734  DNE  
****  2 03 FL340945895735  DNE  
****  2 03 FL340945895736  ZZZ 
****  2 03 FL340945895737  DNE  
 
 Records  
Fiscal 
Year  Survey 
Period 
Code  Florida Education 
Identifier  Section 
Number  FEFP 
Program 
Number  FTE 
Reported, 
Course  
****  2 *FL340945895734  00100  103 0834  
****  0021  *FL340945895735  00200  101 0012 
****  2 *FL340945895736  00500  102 0834  
  
 
Student Database 202 6-2027 /  
 
 ****  2 *FL340945895737  A1500  111 0834  
                      **** = a valid School or Fiscal Year  

**District Responsibility:** The district must delete the  records if they were submitted in  
error or change the DNE Withdrawal Code if it is incorrect.  
 
  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## State Validation

### 75. If Course Number is 7650030 (Prekindergarten Disabilities: Age 0 -2) then the student must be 0 -2 years 
old. Age is determined using the student’s Birth Date on the Student Demographic Information record 
and the Friday of Survey Week. Match the  record with the Student 
Demographic Information record using the following fields: District Number, Current Enrollment; School 
Number, Current Enrollment; Florida Education Identifier (FLEID); Survey Period Code; Fiscal Year; and 
District Number, Current Instruction/Service.  
## State Validation

EXAMPLE  
The  record listed below which is marked with an asterisk would cause a 
message to be generated because the Course Number is incorrect for the age of the student.  
Student  Course Schedule Records  
District 
Number, 
Current 
Enrollment  Year  Florida Education 
Identifier  Survey 
Period 
Code  Course 
Number  
36 0910 FL340945895734  2 7650030  
* 36  0910 FL340945895735  2 7650030  
36 0910 FL340945895736  2 7650030  
 
Student Demographic Information Records  
District 
Number, 
Current 
Enrollment  Florida Education Identifier  Survey 
Period 
Code  Birth Date  
36 FL340945895734  2 08202009  
36 FL340945895735  2 12152006  
36 FL340945895736  2 06152009  

**District Responsibility:** The district must review both records and correct the record that is in error so that the appropriate 
relationship exists between Course Number and Birth Date.  
 
  
 
  
 
Student Database 202 6-2027 /  
## Exception Reports

### 80. If the School Number, Current Instruction/Service does not begin with "P" and the Course Number is a 
vocational secondary Course Number (begins with 8 or 9) except for Course Number 8502000, then the 
FEFP Program Number must be 300, 102, 103, 112 -113, 130, or 254 -255, unless School of Enrollment = 
3450 or 3950, then FEFP must be 999.   
## Exception Reports

EXAMPLE  
The first record listed below meets the criteria specified in the above edit. The second and third records 
would cause a message to be generated because the FEFP Program Number is not the expected FEFP 
Program Number for the Course Number reported.  
Florida 
Education 
Identifier  Dist. 
Num., 
Curr. 
Inst./Serv.  Sch. Num . 
Curr. 
Inst./Serv.  Svy. 
Per. 
Code  Fiscal 
Year  Course 
Number  Section 
Number  Period 
Number  FEFP 
Prog. 
Num.  
FL340945895734  01 0421  2 ****  8500310  00200  0404  300 
* 
FL340945895734  01 0421  2 ****  8206300  00200  0404  101 
* 
FL340945895734  01 0421  2 ****  8500380  00100  0505  111 
**** = Valid fiscal year for data submission.  

**District Responsibility:** The district should verify the FEFP Program Number and the Course Number and correct if in error.  
 
  
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Exception Reports

### 81. Class Minutes, Weekly must not be greater than 2400.  
## Exception Reports

EXAMPLE  
The first record listed below would pass this edit. The last three records would  cause a message to be 
generated because Class Minutes, Weekly is greater than 2400.  
Florida 
Education 
Identifier  Dist. Num., 
Curr. 
Inst./Serv.  Sch. Num. 
Curr. 
Inst./Serv.  Fiscal 
Year  Course 
Number  Section 
Number  Period 
Number  Class 
Minutes, 
Weekly  
FL340945895734  01 0431 ****  1211300  00100  0401  2400  
* 
FL34094589573 5 01 0431 ****  1211300  00100  0101  2500  
* 
FL34094589573 6 01 0431 ****  1211300  00100  0101  4800  
* 
FL340945895737  01 0431  ****  1211300  00100  0101  2424  
**** = Valid fiscal year for data submission.  

**District Responsibility:** The district should verify the Class Minutes, Weekly and correct if in error.  
 
  
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Exception Reports

### 82. If Course Number is 7650130 then the student must be 3 -5 years old. Age is determined using the 
student’s Birth Date on the Student Demographic Information record and the Friday of Survey Week. 
Match the  record with the Student Demographic Information record using the 
following fields: District Number, Current Enrollment; School Number, Current Enrollment; Florida 
Education Identifier (FLEID); Survey Period Code; Fiscal Year; and District Number, Current 
Instruction/Service.  
## Exception Reports

EXAMPLE  
The  record listed below which is marked with an asterisk would cause a 
message to be generated because the Course Number is inconsistent with the age of the student.  
Student  Course Schedule Records  
District 
Number, 
Current 
Enrollment  Year  Florida Education 
Identifier  Survey 
Period 
Code  Course 
Number  
36 0910  FL340945895734  2 7650 130 
* 36  0910  FL340945895735  2 7650 130 
36 0910  FL340945895736  2 7650 130 
 
Student Demographic Information Records  
District 
Number, 
Current 
Enrollment  Florida Education Identifier  Survey 
Period 
Code  Birth Date  
36 FL340945895734  2 08202009  
36 FL340945895735  2 1215200 8 
36 FL340945895736  2 0605200 5 

**District Responsibility:** The district must review both records and, if the data is incorrect, correct the record that is in error so 
that the appropriate relationship exists between Course Number and Birth Date.  
 
  
  
 
Student Database 202 6-2027 /  
## Exception Reports

### 83. Only one of the FEFP Program Numbers, 111 -113 or 254 -255, may be reported for a student in the same 
survey and Term.  
## Exception Reports

EXAMPLE  
The records listed below would not pass this edit because more than one of the FEFP Program Numbers 
was reported for the same student in the same survey and the same Term.  
Florida Education 
Identifier  Survey Period Code  FEFP 
Program 
Number  Term  
*FL340945895734  2 111 1 
*FL340945895734  2 111 1 
*FL340945895734  2 111 1 
*FL340945895734  2 254 1 
*FL340945895734  2 111 1 
*FL340945895734  2 111 1 

**District Responsibility:** The district should verify the FEFP Program Numbers to determine if they have been reported accurately. 
The records should be corrected if in error. However, if it is determined that the FEFP Program Numbers 
were reported accurately, no action is necessary.  
 
  
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
## Exception Reports

### 84. If the Dual Enrollment Indicator equals to  E on one  record reported for a 
student, then each  record with a postsecondary course number (begins with an 
alphabetic character) for that student must be coded with E in the Dual Enrollment Indicator field. 
Matching  records for a student should be based on District Number, Current 
Instruction/Service; Florida Education Identifier (FLEID); Fiscal Year and Survey Period Code.  
## Exception Reports

EXAMPLE  
The  records listed below marked with an asterisk would fail this edit because 
the Dual Enrollment Indicator does not equal to “E” for all courses for the student.  
Florida Education 
Identifier  Course Number  Dual Enrollment 
Indicator  
FL340945895734  AMH9014  E 
FL340945895734  MAT1201  E 
FL340945895734  PSY1407  E 
FL340945895734  SOC1011  E 
*FL34094589573 5 AMH9001  E 
*FL34094589573 5 MAT1207  A 
*FL340945895735  PSY2011  B 
*FL340945895735  SOC1022  E 

**District Responsibility:** The district should review the status of the student regarding dual enrollment and correct the Dual 
Enrollment Indicator codes on the records that are in error.  
 
  
 
 
 
 
 
  
 
Student Database 202 6-2027 /  
 
 AGGREGATE EXCEPTION REPORTS  
UPDATED 07/01/2026    
AA. 
If Survey Period Code is 1 -4 and District Number, Current Instruction/Service  is not71 , and for any school 
that reported a student where Grade  Level = KG -12, then there must be at least one KG -12 student 
coded A or B on the  Reading Intervention Component element for each School Number, Current 
Instruction in the Master School Identification (MSID) file.  
Aggregate exception report  
EXAMPLE  
School Number 0021 has 973 total  records but all records have a N code on the 
Reading Intervention Component element. An error message is generated for School Number 0021 on 
the exception report indicating that the district failed this exception edit. It is expected that the school 
will have one or more students receiving reading intervention services.  

**District Responsibility:** The district must review the records and correct the Reading Intervention Component element on the 
records that are in error.