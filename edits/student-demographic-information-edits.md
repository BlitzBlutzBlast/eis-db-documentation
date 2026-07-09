# Student Demographic Information — Edits and Reject Rules

Source: Florida DOE
Manual: Student Database 2026-2027

STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 1. District Number, Current Instruction/Service must be correct for the district submitting the data.  
**Result:** Record rejected
EXAMPLE  
If district 01 is submitting records, District Number, Current Instruction/Service must be 01 for all 
records. In the records listed below, the first two records would be loaded to the database assuming no 
other reject rule would cause their rejection. The  third record would be rejected since the District 
Number, Current Instruction/Service is 02 rather than 01 (the number of the district submitting the 
record).  
District Number, Current 
Instruction/Service  School Number, Current 
Enrollment  Florida Education 
Identifier  
01 0021  FL123456789100  
01 0021  FL123456789200  
*02 0021  FL123456789300  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the District 
Number, Current Instruction/Service and resub mit the record.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  
UPDATED 07/01/2026   

### 2. District Number, Current Enrollment must be numeric and active (A) on the Appendix C: District Name 
Table.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be written to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected since the District Number, Current Enrollment is 
not in the appropriate range.  
District Number,  
Current Enrollment  School Number,  
Current Enrollment  Florida Education  
Identifier  
01 0021  FL123456789200  
01 0021  FL123456789300  
* 00  0021  FL123456789000  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the District 
Number, Current Enrollment and resubmit the r ecord.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 3. If Survey Period Code is 1 -4 or 9, School Number, Current Enrollment must be numeric in the range 0001 
to 9899 (excluding 3900, 7006 and 9001) or it must be 9992, 9993, 9997, N998 or N999. If Survey Period 
Code is 5, School Number, Current Enrollment must be numeric in the range 0001 to 9899 (excluding 
3900, 7006 and 9001) or it must be 9992, 9993, 9995, 9997, N998 or N999. If Survey Period Code is 6, 
School Number Current Enrollment must be numeric in the range 0001 to 9899 (excluding 3900, 7006 
and 9001).   
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the School Number, Current 
Enrollment is not in the appropriate numerical range. The fo urth record would be rejected because the 
School Number, Current Enrollment is not numeric, N998 or N999. The fifth record would be rejected 
because the School Number, Current Enrollment is excluded from the range.   
District Number, Current 
Enrollment  School Number, Current 
Enrollment  Florida Education 
Identifier  
01 0021  FL123456789100  
01 0021  FL123456789200  
*01 9999  FL123456789300  
*01 C901  FL123456789400  
*01 3900  FL123456789500  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the School 
Number, Current Enrollment and resubmit the r ecords.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 5. Survey Period Code must be 1, 2, 3, 4, 5, 6 or 9 and must be correct for the submission specified by the 
district.  
**Result:** Record rejected
EXAMPLE   
The Survey Period Code as specified in the transmission Job Control Language (JCL) or in statements for 
tape transmission is identified as Survey Period "2". However, records on the transmission have a Survey 
Period Code "3". All updates, adds or deletes w ith this inconsistency would be rejected.  

**District Responsibility:** The Survey Period Code must be corrected either on the records coming in or the Transmission JCL and 
all records must be resubmitted.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 6. Year must be correct for the submission specified by the district.  
**Result:** Record rejected
EXAMPLE  
The Year as specified in the transmission JCL or in statements for tape transmission is identified as 
"0001". However, records on the transmission have Year coded as "0102". All updates, adds or deletes 
with this inconsistency would be rejected.  

**District Responsibility:** The district must correct the Year either on the records coming in or the Transmission JCL and resubmit 
all the records  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 8. The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent 
batch/update submissions, if A is specified then the record must not already exist on the database; if C 
or D is specified then the record must exist on the database.  
**Result:** Record rejected
EXAMPLE  
For all original transmissions, the Transaction Code must be "A". An original transaction is the first 
submission of a record during a survey period. After original transmission of records, changes to the 
record for elements other than the key elements mus t be done with a "C" as the Transaction Code. To 
delete a record, the Transaction Code must be a "D". To change key elements in a batch transaction, the 
record must FIRST be deleted with a "D" and then added with an "A". Records with an incorrect 
Transacti on Code would be rejected.  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
Transaction Code and resubmit the records.  
 
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  FIRST RECORD ACCEPTED; ALL OTHER DUPLICATE REORDS REJECTED  

### 9. Each Student Demographic record must be unique based on District Number, Current 
Instruction/Service; Florida Education Identifier; Survey Period Code and Year.  
**Result:** Record rejected
EXAMPLE  
The first, third and fourth records listed below would be loaded to the database assuming no other 
reject rule would cause their rejection. The second and fifth records would be rejected since they are 
duplicates (same District Number, Current Instruction/ Service;, Florida Education Identifier; Survey 
Period Code and Year) of the first and fourth records, respectively.  
District Number, Current 
Instruction/Service  Florida Education 
Identifier  Survey Period 
Code  Year  
01 FL123456789100  2 ****  
*01 FL123456789100  2 ****  
01 FL123456789200  2 ****  
01 FL123456789300  2 ****  
*01 FL123456789300  2 ****  
  
**** = Valid fiscal year for data submission.  

**District Responsibility:** If the records that were accepted and loaded to the database are correct ones, no action is required. 
However, if the district wishes the data in the rejected records to be loaded to the database, the district 
must delete any invalid records, correct any r ejected records if necessary, and resubmit the corrected 
records.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 10. The Student Number Identifier, Local may be any combination of letters, numbers and blanks. (All blanks 
are allowable.) It must be left -justified with trailing blanks.  
**Result:** Record rejected
EXAMPLE  
The first three records listed below would be loaded to the database assuming no other edit would 
cause their rejection. The fourth record would be rejected because the Student Number Identifier, Local 
contains a symbol (@). The fifth record would be rejec ted because it is right -justified rather than left -
justified.  
District  Number, Current Enrollment  Student Number Identifier, Local  
01 0123456789  
01 ABC123DEF9  
01 3001 28K  
*01 2121@xyz  
*01 123456  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
Student Number Identifier, Local and resubmit the re cords.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 11. If Survey Period is 5 or 9, Institution Number, Neglected/Delinquent (First); Institution Number, 
Neglected/Delinquent (Second) and Institution Number, Neglected/Delinquent (Third) must be numeric 
in the range 0000 to 9899 or they must be a district assign ed 3 -digit number preceded by an A. If Survey 
Period is not 5 or 9, Institution Number, Neglected/Delinquent must be 0000. (This edit does not apply 
to Survey Period 6.)  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Institution Number, 
Neglected/Delinquent is not in the appropriate numerical range.  The fourth record would be rejected 
because the Survey Period is 2 and the Institution Number, Neglected/Delinquent is not 0000.  
District Number,  
Current  
Enrollment  Survey  
Period  
Code  Institution Number,  
Neglected/  
Delinquent  Florida Education  
Identifier  
01 2 0000  FL340945895734  
01 5 A006  FL004583948567  
*01 9 9999  FL000000000000  
*01 2 A006  FL000000000001  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
Institution Number, Neglected/Delinquent and resubmi t the records.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 12. If the Institution Number, Neglected/Delinquent (First); Institution Number, Neglected/Delinquent 
(Second) or Institution Number, Neglected/Delinquent (Third) is not 0000 then it must be a valid 
institution for neglected/delinquent children in the District  of Enrollment. (This edit does not apply to 
Survey Period 6.)  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule  would 
cause their rejection. The third and fourth records would be rejected because the institution numbers 
are not on the Department of Education’s list of valid institutions for neglected or delinquent children.   
District Number,  
Current  
Enrollment  Survey  
Period  
Code  Institution Number,  
Neglected/  
Delinquent  Florida Education  
Identifier  
01 9 0701  FL123456789000  
01 9 A006  FL123456789001  
*01 9 A352  FL123456789002  
*01 9 9678  FL123456789003  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
Institution Number, Neglected/Delinquent and resubmi t the records or supply correct information about 
the qualifications of these institutions to the designated contact person at the Department of Education 
so that these institutions can be added to the list of valid institutions. Following addition of the 
institutions to the list of valid institutions the district must resubmit the records for processing.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 13. If Institution Number, Neglected/Delinquent (First) is 0000 then Institution Number, 
Neglected/Delinquent (Second) must also be 0000. If Institution Number, Neglected/Delinquent (First) or 
Institution Number, Neglected/Delinquent (Second) is 0000 then Insti tution Number, 
Neglected/Delinquent (Third) must be 0000. (This edit does not apply to Survey Period 6.)   
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Institution Number, 
Neglected/Delinquent (First) is 0000 and Institution Number, Ne glected/Delinquent (Second) and 
Institution Number, Neglected/Delinquent (Third) contain an institution number.  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct Institution 
Number, Neglected/Delinquent (First); Instituti on Number, Neglected/Delinquent (Second) and/or 
Institution Number, Neglected/Delinquent (Third) and resubmit the record.  
  District  
Number,  
Current Enrollment  Institution  
Number,  
Neglected/  
Delinquent  
(First)  Institution  
Number,  
Neglected/  
Delinquent  
(Second)  Institution  
Number,  
Neglected/  
Delinquent  
(Third)  
01 0701  0000  0000  
01 A006  5678  9876  
* 01  0000  3456  5432  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 14. If Survey Period is 2 or 3 and Grade Level is 30 or 31, then School Number, Current Enrollment must be 
9997  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
it rejection. The second record would be rejected because School Number, Current Enrollment is not 
9997 for a student in Grade Level 30.  
District  Number,  
Current  
Enrollment  School Number,  
Current  
Enrollment  Florida Education  
Identifier  Survey Period  
Code  Grade  
Level  
01 9997  FL123456789001  2 30 
* 01  0021  FL123456789002  2 30 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the School 
Number, Current Enrollment or the Grade Level a nd resubmit the record.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  
UPDATED 07/01/2026    

### 15. If Migrant Status Term is B, D, E, S, T, U, V, W or X, then Birth Date must be 0901200 4 through 0831202 7 
inclusive. (This edit does not apply to Survey Period 6).  
**Result:** Record rejected
EXAMPLE  
The first record would be rejected because the Birth Date is not in the acceptable range. The second and 
third records would be loaded to the database assuming no other reject rule would cause their rejection.  
Florida Education  
Identifier  Survey  
Period  
Code  Year  Migrant  
Status  
Term  Birth  
Date  
*FL123456789000  5 ****  D 09141983  
FL123456789001  5 ****  S 0109200 8 
FL123456789002  5 ****  B 101920 12 
**** = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Birth 
Date or the Migrant Status Term and resubmit the  record.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  
UPDATED 07/01/2026   

### 16. If Survey Period Code = 1, 4, 5 or 9, then District Number, Zoned School must be filled with zeroes.  
If Survey Period Code = 2 or 3, then District Number, Zoned School must be 0 1- 67.  
(This edit does not apply to Survey Period 6.)  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be written to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the District Number, Zoned School is 
outside the specified range.  
Survey Period  
Code  District Number,  
Zoned School  School Number,  
Zoned School  
01 00 0000  
02 12 0161  
* 03  69 0114  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
District Number, Zoned School and resubmit the recor ds. 
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 17. If Survey Period Code = 1, 4, 5 or 9, then School Number, Zoned School must be filled with zeroes.  
If Survey Period Code = 2 or 3 and  
• District of Instruction is not 71 and  
• School of Enrollment is in the range 0001 -9899 but not 7001, 7004, 7006, 7023 and  
• School Function/Setting is not D (DJJ) on MSID and  
• Charter School Status is Z (not Charter) on MSID and  
• Grade Level code is KG -12 and  
• Accountability ESE Center is Y or Primary Service Type is B (Alternative Education) on MSID and  
• Neglected, Delinquent Status is not (D) or (N) on MSID  
then School Number, Zoned School must be an active school for the District Number, Zoned School on 
the Master School Identification file unless District of Instruction or District of Enrollment is 68 or 83 in 
which case School Number, Zoned School can also  be zeroes.  
Any other School Number, Zoned School  must be an active school for the District Number, Zoned School 
on the Master School Identification file or  be reported as  all zeros for School Number, Zoned School  
(This edit does not apply to Survey Period 6.)  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be written to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected since the School Number, Zoned School is not 
zero - filled for survey 1. The fourth record woul d be rejected since the School Number, Zoned School is 
not a valid number on the Master School Identification file.  
Survey Period  
Code  District Number,  
Zoned School  School Number,  
Zoned School  
3 00 0000  
2 12 0161  
* 1 00 0345  
* 3 02 9990  

**District Responsibility:** STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the School 
Number, Zoned School and resubmit the records .  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 18. If School Number, Current Enrollment is not 9992, 9993, 9995 or 9997, then there must be a valid 
association between the Grade Level listed below and the student's age. For Survey Periods 1 -4, age will 
be determined as of Date Certain (Friday) of the surve y period. For Survey Period 5, age will be 
determined as of Date Certain of Survey 3. For Survey Period 6, age will be determined as of the Survey 
Due Date. For Survey Period 9, age will be determined as of Date Certain of Survey 2.  
**Result:** Record rejected
Grade Level  Age 
PK not equal to 9+ 
KG not equal to 0-3, 11+ 
1 not equal to 0-4, 12+ 
2 not equal to 0-4, 13+ 
3 not equal to 0-4, 14+ 
4 not equal to 0-4, 15+ 
5 not equal to 0-4, 16 + 
6 not equal to 0-4, 18 + 
7 not equal to 0-4, 19+ 
8 not equal to 0-4, 20 + 
9 not equal to 0-4, 27 + 
10 not equal to 0-4, 28 + 
11 not equal to 0-4, 29 + 
12 not equal to 0-4, 30 + 
EXAMPLE  
The records below without an asterisk would be loaded to the database assuming no other reject rule 
would cause their rejection. The records below which are marked with an asterisk would be rejected 
because of the invalid association between the Grade Leve l of the student and the student’s Birth Date.  
Florida Education Identifier  Year  Survey Period Code  Grade Level  Birth Date  
*FL340945895734  1011  2 02 02021994  
FL004583948567  1011  2 08 05062003  
FL000000000000  1011  2 PK 12022010  
*FL340945895735  1011  2 12 08172014  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Grade 
Level or Birth Date so that there is a valid r elationship between these two data elements and resubmit 
the records.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 19. If Survey Period Code is 1 -4 or 5, and English Language Learners, PK -12 code = LY or LP , and Grade Level 
is not PK, then Date Entered United States School must be numeric and a valid date in the format 
MMDDYYYY . Date Entered United States School may be 000 00000 for all others. For Survey Period 9, 
Date Entered United States School must be 00000000. (This edit does not apply to Survey Period 6.).  
**Result:** Record rejected
EXAMPLE  
Each of the records listed below would be rejected. The first record would be rejected because Date 
Entered United States School is not numeric; the second record would be rejected because Date Entered 
United States School is 00000000 and English Language Learners, PK -12 code = LY; the third record would 
be rejected because Date Entered United States School is an invalid date.  
Florida Education  
Identifier  Survey Period 
Code  Year  English Date Entered United 
States School  Language Learners, 
PK-12 
*FL123456789001  2 ****  ZZZZZZZZ  LF 
*FL123456789002  2 ****  00000000  LY 
*FL123456789003  2 ****  02302005  LP 
 
 **** = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
information for Date Entered United States School or  English Language Learners, PK -12 and resubmit the 
records.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 1A. Ethnicity code must be Y or N. (This edit does not apply to Survey Period 6.)  
**Result:** Record rejected
EXAMPLE  
The records listed below would be rejected. The first record would be rejected because the Ethnicity 
code is not valid. The second record would be rejected because the Ethnicity code was left blank.  
Florida Education  
Identifier  Sex Ethnicity  
*FL123456789000  M Z 
*FL123456789001  F  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
Ethnicity code and resubmit the records.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 1B. Race: American Indian or Alaska Native, Race: Asian, Race: Black or African American, Race: Native 
Hawaiian or Other Pacific Islander, and Race:  
White codes must be Y or N. (This edit does not apply to Survey Period 6.)  
**Result:** Record rejected
EXAMPLE  
The record listed below would be rejected because the first and third examples do not contain valid 
codes for Race: American Indian or Alaska Native and Race: Black or African American; and the fourth 
example contains a blank for Race: Native Hawaiian or O ther Pacific Islander.  
Florida  
Education  
Identifier  Race: American 
Indian or  
Alaska  
Native  Race:  
Asian  Race: Black 
or 
African  
American  Race: Native Hawaiian or 
Other  
Pacific  
Islander  Race:  
White  
*FL123456789001  Z Y Z  N 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Race: 
American Indian or Alaska Native, Race: Black or  African American, and Race: Native Hawaiian or Other 
Pacific Islander codes and resubmit the record.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 1C. At least one Race code (Race: American Indian or Alaska Native, Race: Asian, Race: Black or African 
American, Race: Native Hawaiian or Other Pacific  
Islander, or Race: White) must be Y . (This edit does not apply to Survey Period 6.)  
**Result:** Record rejected
EXAMPLE  
The student record listed below would be rejected because there is not a Y code for any of the Races.  
Florida  
Education  
Identifier  Race: American 
Indian or  
Alaska  
Native  Race:  
Asian  Race: Black 
or 
African  
American  Race: Native Hawaiian or 
Other  
Pacific  
Islander  Race:  
White  
*FL123456789000  N N N N N 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must code at least one 
of the Races with a Y and resubmit the record.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 1E. If School Number, Current Enrollment is 7004 then Grade Level must be KG through 12. (This edit does 
not apply to Survey Period 6.)  
**Result:** Record rejected
EXAMPLE  
The first and third records listed below would be written to the database assuming no other reject rule 
would cause their rejection. The second record would be rejected since the Grade Level is not in the 
appropriate range.  
District Number,  
Current Enrollment  School Number,  
Current Enrollment  Grade  
Level  
04 7004  06 
* 04 7004  PK 
04 7004  10 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Grade 
Level and resubmit the record.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 1F. Item 4 - Filler on this format in position numbers 9 -18 must be all spaces.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because the data reported is not all spaces.  
District Number,  
Current Enrollment  School Number,  
Current Enrollment  Filler,  
Item #4  
01 0151   
* 01  0151  265456789X  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must fill the positions 
noted with all spaces and resubmit the record.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 1G. Item 7 - Filler on this format in position numbers 24 -33 must be all spaces.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because the data reported is not all spaces.  
  
District Number, Current  
Instruction/Service  School Number,  
Current Enrollment  Filler,  
Item #7  
01 0151   
* 01  0151  265456789X  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must fill the positions 
noted with all spaces and resubmit the record.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 20. The Student Name, Legal: Last Name must not be blank (Z -fill is NOT allowed). Allowable characters 
include double or single quotation marks, commas, slashes, periods, parentheses, hyphens and accent 
marks.  
**Result:** Record rejected
EXAMPLE  
The record listed below would be rejected because the Student Name, Legal: Last Name is blank.  
District Number, 
Current Instruction/ 
Identifier  Florida  Education  
Service  Student  
Name, Legal:  
Last Name  Student  
Name, Legal:  
First Name  Name,  Legal:  
Middle/Maiden  Name 
or Initial  
* 01  FL123456789006   Clinton  S 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Student 
Name, Legal: Last Name and resubmit the record .  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 21. The Student Name, Legal: First Name must not be blank (Z -fill is NOT allowed). Allowable characters 
include double or single quotation marks, commas, slashes, periods, hyphens and accent marks. Student 
middle name/appendage may be blank but must not includ e non -displayable characters. Allowable 
characters include double or single quotation marks, commas, slashes, periods, parentheses, hyphens 
and accent marks.  
**Result:** Record rejected
EXAMPLE  
The record listed below would be rejected because the Student Name, Legal: First Name is blank.  
District Number, 
Current Instruction/ 
Identifier  Florida Education 
Service  Student 
Name, Legal: 
Last Name  Student 
Name, Legal: 
First Name  Name, Legal: 
Middle/Maiden Name 
or Initial  
* 01  FL123456789007  Williams   L 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Student 
Name, Legal: First Name and resubmit the recor d. 
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 22. If School Number, Current Enrollment is not 9995, then Birth Date must be numeric and a valid date in 
the format MMDDYYYY .  
**Result:** Record rejected
EXAMPLE  
Each of the records listed below would be rejected. The first record would be rejected because Birth 
Date is not numeric; the second record would be rejected because Birth Date is an invalid date.   
Florida Education  
Identifier  Survey Period  
Code  Year  Birth Date  
* FL123456789005  2 ****  ZZZZZZZZ  
* FL123456789006  2 ****  02301985  
**** = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Birth 
Date and resubmit the records.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 23. Sex code must be M or F.  
**Result:** Record rejected
EXAMPLE  
The records listed below would be rejected. The first record would be rejected because the sex code is 
not M or F. The second record would be rejected because the sex code was left blank.  
Florida Education Identifier  Sex 
*FL123456789006  Z 
*FL123456789007   

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the sex 
code and resubmit the records.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 26. If Survey Period Code = 2 or 3 and School Number, Zoned School is greater than 0000, then District 
Number, Zoned School must be greater than 00. If the District Number, Zoned School is greater than 00, 
then School Number, Zoned School must be greater than 0000. (This edit does not apply to Survey 
Period 6.)  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because District Number, Zoned School is not greater 
than 00 for a School Number, Zoned School that i s greater than zero.  
Survey Period Code  District Number, Zoned School  School Number, Zoned School  
03 01 0602  
* 02  00 0604  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the District 
Number, Zoned School or School Number, Zoned School and resubmit the record.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 27. If Survey Period is 1, 2, 3, 4, 5, or 9, English Language Learners, PK -12 code must be LA, LY , LF, LP , LZ, or 
ZZ. (This edit does not apply to Survey Period  6.)  
**Result:** Record rejected
EXAMPLE  
The records listed below would be rejected. The first record would be rejected because the English 
Language Learners, PK -12 code is not valid. The second record would be rejected because the English 
Language Learners, PK -12 code was left blank.  
Florida Education Identifier  English Language  
Learners, PK -12 Survey Period Code  
* FL123456789001  00 5 
* FL123456789002   5 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
English Language Learners, PK -12 codes and resubmit the records.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 28. If Survey Period Code is 5 or 9 and School Number, Current Enrollment is not  9995, Resident Status, 
State/County code must be 0, A, B, 2, 3, 4, 5, 6 or 7. If Survey Period Code is 1 -4, Grade Level is not 30 or 
31, and School Number, Current Enrollment is not 9995, then Resident Status, State/County code must 
be 0, A, B, 2 or 3. If Survey Period Code is 2 or 3, Grade Level is 30 or 31, and School Number, Current 
Enrollment is not 9995, then Resident Status, State/County code must be 4, 5, 6 or 7. If School Number, 
Current Enrollment = 9995, then Resident Status State/County must be Z. (This edit does not apply to 
Survey Period 6.)  
**Result:** Record rejected
EXAMPLE  
The records listed below would be rejected. The first record would be rejected because the Resident 
Status, State/County code is invalid. The second record would be rejected because the Resident Status, 
State/County code was left blank.  
Florida Education  
Identifier  Resident  
Status, State/County  
*FL123456789001   
*FL123456789002  F 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
Resident Status, State/County codes and resubmit the  records.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 29. If Survey Period Code = 1, 4, 6, or 9, Grade Level code must be PK, KG, or 01 -12. If Survey Period Code = 
9, then Grade Level may also = 30 if Institution Number, Neglected/Delinquent (First) does not = 0000. If 
Survey Period Code = 2, 3 or 5, Grade Level code must be PK, KG, 01 -12, 30 or 31.  
**Result:** Record rejected
EXAMPLE  
The records listed below would be rejected. The first record would be rejected because the Grade Level 
code is invalid. The second record would be rejected because the Grade Level code was left blank.  
Florida Education Identifier  Grade Level  
*FL123456789001   
*FL123456789003  K 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Grade 
Level codes and resubmit the records.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 30. If Survey Period Code is 1 -4, 5 or 9, Student Characteristic, Agency Programs code must be A, C or Z. (This 
edit does not apply to Survey Period 6.)  
**Result:** Record rejected
EXAMPLE  
The records listed below would be rejected.  In each case the Student Characteristic, Agency Programs 
code is not a valid code.  
Florida Education  
Identifier  Student Characteristic,  
Agency Programs  
*FL123456789006  P 
*FL123456789007  0 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
Student Characteristic, Agency Programs codes and re submit the records.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  
31. 
• If Survey Period Code is 1 -5 or 9; and if Grade Level equals 9 – 12; and If School Number, Current 
Enrollment does not equal 9992, 9993, 9995, 9997, N998, N999, 3450, 3950; or If both District 
Number, Current Instruction/Service and District Number, Curren t Enrollment equal 71;  
o then Graduation Option code must be 1, 4, 7, 8, 9, A, B, C, or D.  
• If School Number, Current Enrollment = 9992, 9993, 9995, 9997, N998, N999, 3450, 3950 or if 
District Number, Current Instruction/Service equals 71 and District Number, Current Enrollment 
does not equal 71,  
o then Graduation Option code must be Z.  
• If Grade Level equals PK – 8, 30, or 31,  
o then Graduation Option code must be Z.  
(This edit does not apply to Survey Period 6.)   
**Result:** Record rejected
EXAMPLE  
The first two records would be loaded to the database assuming no other reject rules would cause their 
rejection. The third record would be rejected because Graduation Option does not equal 1 -9. The fourth 
record would be rejected because Graduation Option  does not equal Z.   
District Number,  
Current Enrollment  School Number,  
Current Enrollment  Florida Education  
Identifier  Grade  
Level  Graduation  
Option  
01 0001  FL123456789001  10 1 
01 0001  FL123456789002  07 Z 
* 01  0001  FL123456789003  11 Z 
* 01  3450  FL123456789004  12 1 

**District Responsibility:** If the rejected records should not have been submitted no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Grade 
Level; School Number, Current Enrollment or Gra duation Option so that the proper relationship exists,  
and resubmit the records.   
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 33. Qualifying Arrival Date (QAD) for Migrant Program Eligibility must be numeric and a valid date or must 
be all zeroes. (This edit does not apply to Survey Periods 6.)  
**Result:** Record rejected
EXAMPLE  
The first three records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. The fourth record would be rejected because the Qualifying Arrival Date 
(QAD) for Migrant Program Eligibility is not a valid dat e.     
Florida Education Identifier  Survey Period Code  Year  Qualifying Arrival  
Arrival Date (QAD) for Migrant Program  
Eligibility  
FL123456789001  3 ****  10192009  
FL123456789002  3 ****  01092008  
FL123456789003  3 ****  00000000  
* FL123456789005  3 ****  09312009  
**** = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Qualifying Arrival Date (QAD) for Migrant Program Elig ibility and resubmit the record.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 34. If School Number, Current Enrollment is not 9995, then Residence County code must be 01 -67 or 99. If 
School Number, Current Enrollment is 9995, then Residence County code must be 00. (This edit does not 
apply to Survey Period 6.)  
**Result:** Record rejected
EXAMPLE  
The records listed below would be rejected. The first record would be rejected because the Residence 
County code is invalid. The second record would be rejected because the Residence County code was left 
blank.  
Florida Education Identifier  Residence County  
*FL123456789003   
*FL123456789002  75 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
Residence County codes and resubmit the records.   
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 35. If School Number, Current Enrollment is not 9992, 9993, or 9995, then Lunch Status must be 0, 1, 3, 4, C, 
D, E, F, N or R. If School Number, Current Enrollment is 9992, 9993, or 9995, then Lunch Status must be Z. 
(This edit does not apply to Survey Period 6.)  
**Result:** Record rejected
EXAMPLE  
Both records listed below would be rejected because the Lunch Status codes are invalid.  
District  
Number,  
Current  
Enrollment  Florida  
Education  
Identifier  Survey  
Period  
Code  Lunch  
Status  
* 01  FL123456789200  2 5 
* 01  FL123456789300  2 H 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Lunch 
Status codes and resubmit the records.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 36. Migrant Status Term code must be B, D, E, S, T, U, V, W, X or Z. (This edit does not apply to Survey Period 
6.)  
**Result:** Record rejected
EXAMPLE  
The records listed below would be rejected. The first record would be rejected because the Migrant 
Status Term code is not a valid code for this element. The second record would be rejected because the 
Migrant Status Term code was left blank.  
Florida Education Identifier  Migrant Status Term  
*FL123456789200   
*FL123456789300  L 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
Migrant Status Term code and resubmit the records.   
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 37. If Migrant Status Term is B, D, E, S, T, U, V, W or X, Qualifying Arrival Date (QAD) for Migrant Program 
Eligibility must be numeric and a valid date. If Migrant Status Term equal Z, then QAD must be all zeros. 
(This edit does not apply to Survey Period 6. )  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Qualifying Arrival Date (QAD) for 
Migrant Program Eligibility is not a valid date. The fourth record would be rejected because Qualifying 
Arrival Date (QAD) for Migrant Program Eligibility is all zeroes.  
Florida  
Education  
Identifier  Survey  
Period  
Code  Year  Migrant  
Status  
Term  Qualifying Arrival  
Date (QAD) for  
Migrant Program  
Eligibility  
FL123456789200  5 ****  D 10192006  
FL123456789300  3 ****  S 01092006  
*FL123456789700  5 ****  X 02302006  
*FL123456789400  5 ****  B 00000000  
 
**** = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
Qualifying Arrival Date (QAD) for Migrant Program El igibility and resubmit the records.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  
UPDATED 07/01/2026  

### 38. If Migrant Status Term is B, D, E, S, T, U, V, W or X, then Qualifying Arrival Date (QAD) for Migrant 
Program Eligibility must be greater than or equal to 9/1/202 3 and less than or equal to 08/31/202 7. (This 
edit does not apply to Survey Period 6.)  
**Result:** Record rejected
EXAMPLE  
The first record would be rejected because the Qualifying Arrival Date (QAD) for Migrant Program 
Eligibility is not less than or equal to 8/31/202 6. The second and third records would be loaded to the 
database assuming no other reject rule would cause their rejection.  
Florida  
Education  
Identifier  Survey  
Period  
Code  Year  Migrant  
Status  
Term  Qualifying Arrival  
Date (QAD) for  
Migrant Program  
Eligibility  
*FL123456789100  5 ****  D 09142028  
FL123456789200  5 ****  D 010920 24 
FL123456789300  5 ****  D 101920 25 
 
**** = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Qualifying Arrival Date (QAD) for Migrant Program Elig ibility and resubmit the record.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 39. If Residence County code is 99 and Grade Level is PK -12, then Resident Status, State/County code must 
be 0 or 2. (This edit does not apply to Survey Period 6.)  
**Result:** Record rejected
EXAMPLE  
The first and second records below would be rejected because the Resident Status, State/County code is 
invalid for the Residence County code reported. The third record would be written to the database 
assuming no other reject rule would cause its rejection .  
Florida  
Education  
Identifier  Residence  
County  Resident  
Status,  
State/County  
* FL630123456000  99 5 
* FL630123456001  99 A 
FL630123456002  99 2 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
Residence County codes or the Resident Status, State /County codes and resubmit the records.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 40. If the School Number, Current Enrollment is not 9992, 9993, 9995, N998 , N999 , 3450  or 3950 , then it 
must exist on the Master School Identification File as a valid active school (active in the current school 
year) in the district of enrollment.  
**Result:** Record rejected
EXAMPLE  
The record listed below would be rejected because the School Number, Current Enrollment would not be 
valid and active on the Master School Identification File for the District Number, Current Enrollment.  
     
District Number, Current 
Enrollment  School Number, Current 
Enrollment  Florida Education 
Identifier  
* 01  0001  FL123456789000  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if  the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the School 
Number, Current Enrollment and resubmit the record.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  
UPDATED 07/01/2026  

### 41. If School Number, Current Enrollment is not 9995, then Birth Date must be less than or equal to the 
survey due date. If School Number, Current Enrollment is 9995; Survey Period Code is not 6 and Migrant 
Status Term is Z; then Birth Date must be 00000000. I f School Number, Current Enrollment is  
9995; Survey Period Code is not 6; and Migrant Status Term is not Z, then  
Birth Date must be 0901200 4 through 0831202 7 inclusive.  
**Result:** Record rejected
EXAMPLE  
If the survey week for the records listed below were October 14 -18, 2014, the first record would be 
rejected because the Birth Date is not less than the Survey Date. The second and third records would be 
loaded to the database assuming no other reject rule  would cause their rejection.  
Florida Education  
Identifier  Survey Period  
Code  Year  Birth Date  
* FL123456789000  2 ****  11042014  
FL123456789002  2 ****  03152012  
FL123456789003  2 ****  08112013  
**** = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Birth 
Date and resubmit the record.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 42. If Resident Status, State/County is A, then District Number, Current Enrollment and Residence County 
must not be the same. (This edit does not apply to Survey Period 6.)  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be rejected because District Number, Current Enrollment and 
Residence County are the same. The second record would be written to the database assuming there is 
no other edit that would cause the record to be rejected.  
Florida Education 
Identifier  District Number, Current 
Enrollment  Residence 
County  Resident Status, State/ 
County  
*FL123456789006  12 12 A 
FL123456789008  10 42 A 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the District 
Number, Current Enrollment; Residence County or Resident Status, State/County code and resubmit the 
record.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 43. If School Number, Current Enrollment is not 9992, 9993, or 9995, then Native Language, Student must be 
a valid language code, containing no blanks. If School Number, Current Enrollment is 9992, 9993, or 
9995, then Native Language, Student code must be ZZ. (For additional information on the language 
codes refer to the language codes table, Appendix N of the DOE Information Database Requirements: 
Volume I -- Automated Student Information System Manual.) (This edit does not apply to Survey Period 
6.)  
**Result:** Record rejected
EXAMPLE  
The fourth and fifth record listed below would be loaded to the database assuming no other reject rule 
would cause its rejection. The first three records would be rejected because the Native Language, 
Student codes contain blanks or are invalid codes.  
Florida Education Identifier  Native Language, Student  
* FL123456789001  AY 
* FL123456789002  C 
* FL123456789004  DR 
FL123456789003  BJ 
FL123456789700  CZ 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Native 
Language, Student codes and resubmit the reco rds.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 44. If District Number, Current Enrollment is 01 -67 and if Resident Status,  
State/County is 3, then District Number, Current Enrollment and Residence  
County must be the same. (This edit does not apply to Survey Period 6.)  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be written to the database assuming there is no other edit that would 
cause the record to be rejected. The second record would be rejected because District Number, Current 
Enrollment and Residence Status are not the same .  
Florida  
Education  
Identifier  District  
Number,  
Current  
Enrollment  Residence  
County  Resident  
Status,  
State/  
County  
FL123456789100  12 12 3 
*FL123456789200  10 42 3 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the District 
Number, Current Enrollment, Residence County or Resident Status, State/County code and resubmit the 
record.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 45. If School Number, Current Enrollment is not 9992, 9993, or 9995, then the Primary Language Spoken in 
Home code must be a valid language code as listed in Appendix N of the DOE Information Database 
Requirements: Volume I -- Automated Student Information Sys tem Manual. If School Number, Current 
Enrollment is 9992, 9993, or 9995, then the Primary Language Spoken in  Home code must be ZZ. (This 
edit does not apply to Survey Period 6.)  
**Result:** Record rejected
EXAMPLE  
The third and fourth records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. The first and second records would be rejected because the Primary 
Language Spoken in Home code is invalid.  
Florida Education Identifier  Primary Language Spoken in Home  
* FL123456789400  BB 
* FL123456789001  EZ 
FL123456789300  BR 
FL123456789200  BA 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
Primary Language Spoken in Home codes and resubmit t he records.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 46. If Grade Level = PK -12, 30 or 31, then Country of Birth must be a valid code as listed in Appendix G or 
Appendix Q of the DOE Information Database Requirements: Volume I -- Automated Student Information 
System Manual, including ZZ. (This edit does not appl y to Survey Period 6.)  
**Result:** Record rejected
EXAMPLE  
The first and second records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. The third and fourth records would be rejected because the Country of Birth 
codes are not valid.  
Florida Education Identifier  Country of Birth  
FL123456789003  CU 
FL123456789004  FJ 
*FL123456789001  YI 
* FL123456789002  TX 

**District Responsibility:** If the rejected records should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
Country of Birth codes and resubmit the records.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 47. If Grade Level = 12, Additional School Year Student code must be D, S , or Z. If Grade Level is not 12, then 
Additional School Year Student must be Z. (This edit does not apply to Survey Period 6.)  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because the Grade Level is 08 and the Additional 
School Year Student code is not Z. The third record would be rejected because Grade Level is 12 and 
Additional School Year Student code is blank.  
Florida Education  
Identifier  Grade  
Level  Additional School  
Year Student  
FL123456789100  12 S 
* FL123456789200  08 S 
* FL123456789300  12  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct either the 
Grade Level or the Additional School Year Stu dent code and resubmit the records.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  
UPDATED 07/01/2026   

### 48. If Grade Level = 30 or 31 or if School Number, Current Enrollment is 9992, 9993, 9995, or 9997 then 
English Language Learners: Home Language Survey Date must be zero -filled.  
If School Number, Current Enrollment is not 9992, 9993, 9995, or 9997 and if Grade Level = PK -12, then 
English Language Learners: Home Language Survey Date must be a valid date and must meet the 
following criteria.  
e. If District Number, Current Instruction is numeric and active (A) on the Appendix C: District Name 
Table  or if both District Number, Current Enrollment and District Number, Current Instruction are 71; and 
Survey Period is 1 -3, the date should be less than or equal to the date certain of survey week.  
f. If District Number, Current Enrollment is not 71; District Number, Current Instruction is 71 and Survey 
Period is 1 -3; then the date must be less than or equal to the date certain plus 90 calendar days.  
g. For Survey Period 4, the date should be less than or equal to June 30 of the reporting year.  
h. For Survey Period 5, the date should be less than or equal to August 31 of the reporting year.  
i. For Survey Period 9, the date should be less than January 1 of the reporting year.  
j. (This edit does not apply to Survey Period 6.)  
**Result:** Record rejected
EXAMPLE  
The first and fourth records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. The second and third records would be rejected because the English 
Language Learners: Home Language Survey Date is an inval id date or is inappropriately filled with zeros.  
     
Florida Education 
Identifier  Survey Period 
Code  Year  Grade 
Level  ELL: Home Language Survey 
Date  
FL123456789100  2 1112  12 01152010  
*FL123456789200  2 1112  PK 06319999  
*FL123456789000  2 1112  09 00000000  
*FL123456789006  5 1112  31 00000000  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
English Language Learners: Home Language Survey Date  and resubmit the records.  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /   
## Reject Rules

### 49. If Grade Level is PK -12 and School Number, Current Enrollment is not 9992, 9993, or 9995, then Native 
Language, Student must be other than ZZ. If School Number, Current Enrollment is 9992, 9993, or 9995, 
then Native Language, Student must be ZZ. (This edit  does not apply to Survey Period 6.)  
**Result:** Record rejected
EXAMPLE  
The second record listed below would be loaded to the database assuming no other reject rule would 
cause its rejection. The first record would be rejected because BZ is not a valid Native Language, Student 
code for a student with a Grade Level of PK -12.  
Florida Education Identifier  Grade Level  Native Language, Student  
* FL123456789100  07 BZ 
FL123456789200  03 CZ 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database the district must correct the Native 
Language, Student code and resubmit the record.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 4A. If District Number, Current Enrollment is 71 and School Number equals 0300, 0400 or 0801, then 
Residence County code must not equal 99. This edit does not apply to Survey Period 6.  
**Result:** Record rejected
EXAMPLE  
The second record listed below would be loaded to the database assuming no other reject rule would 
cause its rejection. The first record listed below would be rejected because Residence County equals 99 
for District Number, Current Enrollment 71 and School  Number, Current Enrollment 0300.  
Florida Education  
Identifier  District Number  
Current  
Enrollment  School Number  
Current  
Enrollment  Residence  
County  
*FL123456789100  71 0300  99 
FL123456789200  71 0400  50 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Residence County code or the School Number, Current En rollment and resubmit the record.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  REJECT RULES  

### 4B. Florida Education Identifier (FLEID) is alphanumeric and must be entered as “FL” in the first 2 positions 
followed by twelve numeric digits. No blanks, spaces or all zeros for the twelve numeric digits are 
allowable.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Florida Education Identifier (FLEID) 
is not a valid FLEID.  
District Number, Current Enrollment  Florida Education Identifier  
01 FL340945895734  
01 FL004583948567  
* 01  FL000000000000  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Florida 
Education Identifier and resubmit the record f or processing.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  STATE VALIDATION RULES  

### 52. If Survey Period Code is 2, 3 or 5, and If English Language Learners, PK -12 is LF and if there is a matching 
English Language Learners Information record and if there is a matching Student Course Schedule or 
Student End of Year Status record, then the Engl ish Language Learners:  Basis of Exit (First) must not = Z.  
The match between the  record and the English Language Learners 
Information record should be based on District Number, Current Instruction Service; Florida Education 
Identifier; Survey Period Code and Fiscal/School Year.   
The match between the  record and the Student Course Schedule 
record should be based on District Number, Current Instruction; District Number, Current Enrollment; 
Florida Education Identifier; Survey Period Code; Year/Fiscal Year and District of Instruction is equal to 
District of Enrollment.  
The match between  and Student End of Year Status record should be 
made based on District Number, Current Enrollment; Florida Education Identifier; Survey Period Code; 
and Year/School Year.  
## State Validation

EXAMPLE  
The Student Demographic record listed below marked with an asterisk would cause a message to be 
generated because the English Language Learners: Basis of Exit code is Z for a student with an English 
Language Learners, PK -12 code of LF.  
 records  
District Number, Current 
Instruction/Service  Survey 
Period Code  School 
Year  Florida Education 
Identifier  English Language 
Learners, PK -12 
37 2 1011  FL123456789100  LF 
37 2 1011  FL123456789200  LF 
* 37  2 1011  FL123456789300  LF 
English Language Learners Information records  
District Number, Current 
Instruction/Service  Survey  
Period  
Code  School 
Year  Florida  Education  
Identifier  English  Language  
Learners: Basis  of Exit 
(First)  
37 2 1011  FL123456789001  A 
37 2 1011  FL123456789100  R 
*37 2 1011  FL123456789200  Z 

**District Responsibility:** The district must correct the English Language Learners: Basis of Exit (First) code and/or the English 
Language Learners, PK -12 code so that a valid relationship exists between the elements.    
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  STATE VALIDATION RULES  

### 53. If Survey Period Code is 2, 3 or 5 and if English Language Learners, PK -12 is LY or LF and if Grade Level is 
KG-12 and if there is a matching Student Course Schedule or Student End of Year Status record, then 
there must be a matching English Language Learn ers Information record based on District Number, 
Current Instruction Service;, Florida Education Identifier; Survey Period Code and Year.  
The match between Student Demographic and Student Course should be made based on District 
Number, Current Instruction; District Number, Current Enrollment; Florida Education Identifier; Survey 
Period Code; Year/Fiscal Year and District  Instruction is equal to District of Enrollment. The match 
between Student Demographic and Student End of Year should be made based on District Number,  
Current Enrollment, Florida Education Identifier; Survey Period Code; and Year/School Year. (This edit 
does not apply to Surv ey Period 6.)   
## State Validation

EXAMPLE  
The Student Demographic records listed below which are marked with an asterisk    would cause a 
message to be generated because there are no matching English   Language Learners records.  
Student Demographic records             
District Number, Current 
Instruction/Service  School Number, 
Current 
Enrollment  Survey 
Period 
Code  Year  Florida Education 
Identifier  English 
Language 
Learners, PK -
12 
37 0001  2 1011  FL123456789100  LY 
37 0001  2 1011  FL123456789200  LF 
* 37  0001  2 1011  FL123456789000  LF 
* 37  0002  2 1011  FL123456789300  LY 
        
English Language Learners records  
District Number, Current 
Instruction/Service  School Number, 
Current Enrollment  Survey 
Period Code  Year  Florida Education 
Identifier  
37 0001  2 1011  FL123456789001   
37 0001  2 1011  FL123456789002   
37 0001  2 1011  FL123456789000   
37 0002  2 1011  FL123456789004   

**District Responsibility:** The district must review the Student Demographic records and determine whether the students are 
English Language Learners. The district must either submit an English Language Learners record for each 
student or submit a revision to the English Language Lea rners, PK -12 element to indicate that the 
student is not an English Language Learner.  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  STATE VALIDATION RULES  

### 54. If the English Language Learners code = LF and if Survey Period Code is 2 or 3 and if there is a matching 
Student Course Schedule record, then English Language Learners: Exit Date on the matching English 
Language Learners Information record must be a valid  date.  
The match between the  record and the Student Course Schedule 
record should be based on District Number, Current Instruction; District Number, Current Enrollment; 
Florida Education Identifier; Survey Period Code; Year/Fiscal Year and District Instruction is equal to 
District of Enrollment.  
If the English Language Learners code = LF and if Survey Period Code is 5 and if there is a matching 
Student End of Year Status record and if District Number, Current Enrollment is equal to District Number, 
Current Instruction/Service, then English Languag e Learners: Exit Date on the matching English Language 
Learners Information record must be a valid date.   
The match between the  record and the Student  
End of Year Status record should be based on District Number, Current Enrollment; Florida Education 
Identifier; Survey Period Code; and Fiscal/School Year.   
The match between the  record and the English Language Learners 
Information record should be based on District Number, Instruction/Service; Florida Education Identifier; 
Survey Period Code and Fiscal/School Year.  
## State Validation

EXAMPLE  
An error message would be generated for the student Demographic record marked with an asterisk 
below. This is because the English Language Learners: Exit Date on the matching English Language 
Learners Student Information record is not a valid date.  
 records  
District Number, Current 
Instruction/Service  School Number, 
Current 
Enrollment  Florida Education 
Identifier  Survey 
Period 
Code  English 
Language 
Learners  
01 0021  FL123456789200  2 LF 
* 01  0021  FL123456789300  2 LF 
English Language Learners Student Information records  
District Number, Current 
Instruction/Service  School Number, 
Current 
Enrollment  Florida Education 
Identifier  Survey 
Period 
Code  English 
Language 
Learners  
01 0021  FL123456789600  2 01042010  
01 0021  FL123456789700  2 02302010  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  Student Course Schedule records   
Florida 
Education 
Identifier  District Number, 
Current 
Instruction/Service  School 
Number, 
Current 
Enrollment  Survey 
Period 
Code  Fiscal 
Year  Term  Course 
Number  Section 
Number  Period 
Number  
FL012345675000  01 0021  2 ****  1 1200300  00200  0404  
FL123456789100  01 0021  2 ****  1 1200300  00200  0404  
**** = Valid fiscal year for data submission.  

**District Responsibility:** The district must correct the English Language Learners: Exit Date and/or the English Language Learners 
code so that a valid relationship exists between the elements  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  STATE VALIDATION RULES  

### 55. If Survey = 5 and Diploma Type on the Student End of Year Status record = W07 or W27, then Graduation 
Option code must equal 4 or 7; if Survey = 5 and Diploma Type = W10, WGA or WGD, then Graduation 
Option code must equal 8. (This edit does not apply to Su rvey Period 6.)  
## State Validation

EXAMPLE  
The Student Demographic record listed below which is marked with an asterisk would cause a message 
to be generated because the correct relationship does not exist between Graduation Option and 
Diploma Type.  
Student Demographic records   
District Number, Current 
Instruction/Service  School Number, 
Current 
Enrollment  Survey 
Period 
Code  Florida Education 
Identifier  Grade 
Level  Graduation 
Option  
01 0001  5 FL123456789200  12 7 
01 0001  5 FL123456789000  12 4 
* 01  0001  5 FL123456789600  12 4 
Student End of Year Status records  
District Number, Current 
Instruction/Service  School Number, 
Current 
Enrollment  Survey 
Period 
Code  Florida Education 
Identifier  Grade 
Level  Diploma 
Type  
01 0001  5 FL123456789000  12 W27  
01 0001  5 FL601254693000  12 W07  
01 0001  5 FL014576450000  12 WGA  

**District Responsibility:** The district must correct the Student Demographic record so that the appropriate relationship exists 
between Graduation Option and Diploma Type.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  STATE VALIDATION RULES  

### 56. If Survey Period Code is 2, 3 or 5 and if the English Language Learners, PK12 code is LF and if there is a 
matching Student Course Schedule or Student End of Year Status record then one of the following must 
be true for the English Language Learners Inform ation record:  
• English Language Learners: Reclassification Exit Date is all zeros and the English Language 
Learners: Exit Date is within two years of survey date or  
• English Language Learners: Reclassification Exit Date is greater than zero and is within two years 
of survey date.  
Use the Survey Period 3 survey date for Survey Period 5 editing.  
The match between the Student Demographic record and the English Language Learners record should 
be based on District Number, Current Instruction/Service; Florida Education Identifier; Survey Period 
Code; and Fiscal Year. If no matching English Language Le arners Information record is found, then do not 
generate an error message.  (This edit does not apply to Survey Period 6.)  
The match between the  record and the Student Course Schedule 
record should be based on District Number, Current Instruction; District Number, Current Enrollment; 
Florida Education Identifier; Survey Period Code; Year/Fiscal Year and District Instruction is equal to 
District of Enrollment.    
The match between the  and the Student End of Year Status record 
should be made based on District Number, Current    Enrollment; Florida Education Identifier; Survey 
Period Code; and Year/School    Year.  
## State Validation

EXAMPLE  
An error message will be generated for the    record marked with an 
asterisk below. This is because the English Language Learners: Exit Date on the matching English 
Language Learners Student   Information record is more than two years from the survey date for a 
student with an English Language Learners, PK -12 code of LF.  
 records  
District Number, Current 
Instruction/Service  Florida Education 
Identifier  Survey 
Period Code  Year  English Language 
Learners, PK -12 
01 FL123456789100  2 1011  LF 
01 FL123456789200  2 1011  LF 
*01 FL123456789000  2 1011  LF 
 
English Language Learners Student Information record       
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  District Number, Current 
Instruction/Service  Florida Education 
Identifier  Survey 
Period 
Code  English 
Language 
Learners: Exit 
Date  English Language 
Learners: 
Reclassification Exit 
Date  
01 FL123456789200  2 01042010  00000000  
01 FL019876545000  2 05302007  05302009  
* 01  FL123456789589  2 05302008  00000000  

**District Responsibility:** The district must correct the English Language Learners: Exit Date and/or the English Language Learners, 
PK-12 code so that a valid relationship exists between the elements.    
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  STATE VALIDATION RULES  

### 57. If Survey Period Code is 5 and if Graduation Option code = 4, A or B, and if Prior School Status/Student 
Attendance Term does not equal “Y”, then Exceptionality, Primary or Exceptionality, Other on the 
Exceptional Student record must be reported with a cod e of C, G, H, J, K, O -P , S, V or W and these two 
fields must not contain T or U.  
If Survey Period Code is 2 or 3 and if Graduation Option code = 4, A or B, and if Withdrawal Date on the 
Prior School Status/Student Attendance record is 00000000; then Exceptionality, Primary or 
Exceptionality, Other on the Exceptional Student record must  be reported with a code of C, G, H, J, K, O -
P , S,  
V, or W and these two fields may not contain T or U. (This edit does not apply to Survey Period 6.)  
## State Validation

EXAMPLE  
The third Student Demographic record listed below would cause a message to be generated because the 
correct relationship does not exist between Graduation Option and Exceptionality, Primary. The fourth 
Student Demographic record listed below would cause a message to be generated because the correct 
relationship does not exist between Graduation Option, Exceptionality, Primary; and Exceptionality, 
Other.  
Student Demographic records   
District Number, Current 
Instruction/Service  School Number, 
Current 
Enrollment  Survey 
Period 
Code  Year  Florida Education 
Identifier  Graduation 
Option  
37 0001  3 1314  FL123456789000  4 
37 0001  2 1415  FL123456789200  A 
*37 0001  5 1415  FL601245693000  B 
*37 0001  3 1314  FL123457894560  4 
 
Exceptional Student records  
District Number, 
Current 
Instruction/Service  School 
Number, 
Current 
Enrollment  Survey 
Period 
Code  Year  Florida 
Education 
Identifier  Exceptionality 
Primary  Exceptionality 
Other  
37 0001  3 1314  FL123456789300  W K 
37 0001  2 1415  FL123456789400  G J 
37 0001  5 1415  FL019876545000  T C 
37 0001  3 1314  FL123456789000  I L 
   
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  Prior School Status/Student Attendance records  
District Number, 
Current 
Instruction/Service  School 
Number, 
Current 
Enrollment  Survey 
Period 
Code  Year  Florida Education 
Identifier  Term  Withdrawal 
Date  
37 0001  3 1314  FL123456789700  3 00000000  
37 0001  2 1415  FL601254693000  3 00000000  
37 0001  5 1415  FL123456789200  3 05122004  
37 0001  3 1314  FL123456789300  3 00000000  

**District Responsibility:** The district must correct the Student Demographic, Prior School Status/Student Attendance, or 
Exceptional Student records so that the appropriate relationship exists between Graduation Option; 
Term; Exceptionality, Primary; Exceptionality, Other; and Withd rawal Date.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  STATE VALIDATION RULES  

### 58. If Survey Period Code is 1 or 5 and if Graduation Option code = 7, then Exceptionality, Primary on the 
Exceptional Student record must be C, F -K, M, O -P , S, V, or W.  Exceptionality, Primary may also be L if 
Exceptionality, Other is C, FK, M, O -P , S, V, or  W. 
If Survey Period Code is 2, 3 or 4 and if there is a matching Student Course Schedule record and if 
Graduation Option code = 7, then Exceptionality, Primary on the Exceptional Student record must be C, 
F-K, M, O -P , S, V, or W. Exceptionality, Primary may a lso be L if Exceptionality, Other is C, F -K, M, O -P , S, V, 
or W.   
The match should use District Number, Current Instruction; District Number, Current Enrollment; Florida 
Education Identifier; Survey Period Code; Year/Fiscal Year and District Instruction is equal to District of 
Enrollment. (This edit does not apply to Sur vey Period 6.)  
## State Validation

EXAMPLE  
The third Student Demographic record listed below would cause a message to be generated because the 
correct relationship does not exist between Graduation Option and Exceptionality, Primary. The fourth 
Student Demographic record listed below would cause a message to be generated because the correct 
relationship does not exist between Graduation Option; Exceptionality, Primary; and Exceptionality, 
Other.  
Student Demographic records  
District Number, Current 
Instruction/Service  School Number, 
Current 
Enrollment  Survey 
Period 
Code  Year  Florida Education 
Identifier  Graduation 
Option  
37 0001  3 1011  FL123456789500  7 
37 0001  2 1011  FL123456789600  7 
* 37  0001  5 1011  FL019876545000  7 
* 37  0001  3 1011  FL601254693000  7 
Exceptional Student records   
District Number, 
Current 
Instruction/Service  School 
Number, 
Current 
Enrollment  Survey 
Period 
Code  Year  Florida 
Education 
Identifier  Exceptionality 
Primary  Exceptionality  
Other  
37 0001  3 1011  FL123456789300  W E 
37 0001  2 1011  FL123456789700  F J 
37 0001  5 1011  FL123456789600  T C 
37 0001  3 1011  FL123456789100  L  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  DISTRICT RESPONSIBILITY  
The district must correct the Student Demographic or Exceptional Student records so that the 
appropriate relationship exists between Graduation Option; Exceptionality, Primary; and Exceptionality, 
Other.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  STATE VALIDATION RULES  

### 5A. If Survey Period Code is 2, 3 or 5 and If English Language Learners, PK -12 is LY or LF and if there is a 
matching English Language Learners Information record and if there is a matching Student Course 
Schedule or Student End of Year Status record, then the  English Language Learners: Classification Date 
must not equal zero.    
The match between the  record and the English Language Learners 
Information record should be based on District Number, Current Instruction/Service; Florida Education 
Identifier; Survey Period Code and Fiscal/School Year.   
The match between the  record and the Student Course Schedule 
record should be based on District Number, Current Instruction; District Number, Current Enrollment; 
Florida Education Identifier; Survey Period Code; Year/Fiscal Year and District Instruction is equal to 
District of Enrollment.  
The match between the  and the Student End of Year Status record 
should be made based on District Number, Current    Enrollment; Florida Education Identifier; Survey 
Period Code; and Year/School Year.  
## State Validation

EXAMPLE  
The Student Demographic record listed below marked with an asterisk would cause a message to be 
generated because the English Language Learners:  Classification Date equals zero for a student with an 
English Language Learners, PK -12 code of LF.        
 records       
District Number, Current 
Instruction/Service  
 Survey Period 
Code  
 Year  
 Florida Education 
Identifier  
 Language 
Learners, PK -12 
37 2 1011  FL123456789200  LY 
37 2 1011  FL019876545000  LF 
* 37  2 1011  FL123456789500  LF 
 
English Language Learners Information records  
  
District Number, Current 
Instruction/Service  Survey 
Period 
Code  School 
Year  Florida Education 
Identifier  English Language 
Learners: Classification 
Date  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  37 2 1011  FL123456789600  01042008  
37 2 1011  FL123456789500  02082009  
* 37  2 1011  FL123456789400  00000000  

**District Responsibility:** The district must correct the English Language Learners: Classification Date and/or the English Language 
Learners, PK -12 code so that a valid relationship exists between the elements.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  STATE VALIDATION RULES  

### 5B. If Survey Period Code is 2, 3 or 5 and if English Language Learners, PK -12 is LY or LF and if there is a 
matching English Language Learners Information record and if there is a matching Student Course 
Schedule or Student End of Year Status record, then the  English Language Learners: Basis of Entry code 
on the English Language Learners Information record must not = Z.     
The match between the  record and the English Language Learners 
Information record should be based on District Number, Current Instruction/Service; Florida Education 
Identifier; Survey Period Code and Fiscal/School Year.   
The match between the  record and the Student Course Schedule 
record should be based on District Number, Current Instruction; District Number, Current Enrollment; 
Florida Education Identifier; Survey Period Code; Year/Fiscal Year and District Instruction is equal to 
District of Enrollment.  
The match between  and Student End of Year Status record should be 
made based on District Number, Current Enrollment; Florida Education Identifier; Survey Period Code; 
and Year/School Year.   
## State Validation

EXAMPLE  
The Student Demographic record listed below marked with an asterisk would cause a message to be 
generated because the English Language Learners: Basis of Entry code is Z for a student with an English 
Language Learners, PK -12 code of LF. Student Demographic  Information records  
District Number, Current 
Instruction/Service  Survey 
Period Code  School 
Year  Florida Education 
Identifier  English Language 
Learners: PK -12 
37 2 1011  FL123456789200  LY 
37 2 1011  FL123456789300  LF 
* 37  2 1011  FL123456789600  LF 
English Language Learners Information records  
District Number, Current 
Instruction/Service  Survey 
Period 
Code  School 
Year  Florida Education 
Identifier  English Language 
Learners: Basis of 
Entry  
37 2 1011  FL123456789600  A 
37 2 1011  FL123456789700  R 
* 37  2 1011  FL123456789800  Z 

**District Responsibility:** STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  The district must correct the English Language Learners: Basis of Entry code and/or the English Language 
Learners, PK -12 code so that a valid relationship exists between the elements.    
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  STATE VALIDATION RULES  

### 5C. If Survey Period code is 2 or   3, Grade Level is not equal to PK and if Exceptionality, Primary code = M or 
Exceptionality, Other code = M on the Exceptional Student record, and District of Instruction is not 71, 
then the School     Number, Zoned School m ust be in the range 0001   -9899 but not 7001, 7004, 7006, 
7023. The match between the  record and the Exceptional Student 
record should be based on District Number, Current Enrollment; Florida Education Identifier; Survey 
Period Code and Fiscal Year. (This edit does not apply to Survey Period 6)  
## State Validation

EXAMPLE  
The first and second Student Demographic records listed below would cause a message to be generated 
because the values for School Number, Zoned School are not valid for Exceptional Student records where 
Exceptionality, Primary code = M or the Exceptionalit y, Other code = M.  
Student Demographic records  
District Number, Current 
Instruction/Service  Florida Education 
Identifier  Survey 
Period 
Code  Fiscal 
Year District 
Number, 
Zoned School  School 
Number, 
Zoned School  
* 09  FL123456789700  3 ****  00 0000  
* 09  FL123456789800  2 ****  00 0000  
09 FL123456789678  3 ****  02 0781  
09 FL123456789600  2 ****  01 0345  
Exceptional Student records   
District Number, 
Current 
Instruction/Service  Florida Education 
Identifier  Survey 
Period 
Code  Fiscal 
Year Exceptionality, 
Primary  Exceptionality, 
Other  
09 FL123456789200  3 ****  C M 
09 FL123456789300  2 ****  M Z 
09 FL123456789500  3 ****  K M 
09 FL123456789600  2 ****  M P 
**** = Valid fiscal year for data submission.  

**District Responsibility:** The district must correct the District Number, Zoned School and School Number, Zoned School data on 
the Student Demographic records so that the appropriate relationship exists between School Number, 
Zoned School and the Exceptionality codes on the Exceptio nal Student records.   
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  STATE VALIDATION RULES  

### 5D. If Survey Period Code is 2, 3, or 5, and Immigrant Student = Y on the Federal/State Indicator Status 
record, then Date Entered United States School must be numeric and a valid date in the format 
MMDDYYYY , unless Grade Level = PK then date must be 00000000.  The match for Student Demographic 
and Federal/State Indicator Status records should be based on both District Number, Current Enrollment 
and District Number, Current Instruction/Service (Student Demographic) and District Number, Current 
Enrollment (Federa l/State Indicator Status); Florida Education Identifier; Survey Period Code and Fiscal 
Year. (This edit does not apply to Survey Period 6.).  
## State Validation

EXAMPLE  
Each of the records listed below would cause a message to be generated. The first record because Date 
Entered United States School is not numeric; the second record because Date Entered United States 
School is 00000000 and Grade Level is not PK; and the th ird record because Date Entered United States 
School is an invalid date.  
Federal/State Indicator Status records   
District Number, Current 
Instruction/Service  Florida Education 
Identifier  Survey Period 
Code  Year  Immigrant 
Student  
01 *FL123456789600  2 ****  N 
01 *FL123456789700  2 ****  Y 
01 *FL123456789800  2 ****  Y 
Student Demographic records   
District Number, Current 
Instruction/Service  Florida Education 
Identifier  Survey 
Period 
Code  Year  Data Entered 
United States 
School  Grade 
level  
01 *FL123456789100  2 ****  ZZZZZZZZ  PK 
01 *FL123456789200  2 ****  00000000  03 
01 *FL123456789300  2 ****  02302005  08 
**** = Valid fiscal year for data submission.  

**District Responsibility:** The district must correct the records so that the appropriate relationship exists among Immigrant 
Student, Date Entered United States School and Grade Level.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  STATE VALIDATION RULES  

### 5E. For Survey Periods 2 and 3, if the District Number, Current Enrollment and the District Number, Current 
Instruction/Service are equal and the School Number, Current Enrollment is found on the National 
School Lunch Program (NSLP)  
Reference file - F71447 (provided by the Florida Department of Agriculture and  
Consumer Services), and  
• If the NSLP designated at the school is determined by collection of Free or  
Reduced Priced Lunch Eligibility Applications, then Lunch Status must equal 0, 1, 3, D, E or F.  
• If the NSLP is designated as a school providing Provision 2, then Lunch Status must equal 4 or,  
• If the NSLP is designated as a school providing Community Eligibility Provision (CEP), then Lunch 
Status must equal C, R or N.  
The match should be made using Year; District Number, Current Enrollment; and  
School Number, Current Enrollment.    
## State Validation

EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Lunch Status equals F (eligible for 
free lunch based on eligibility application), b ut in the NSLP Reference File, Lunch Program Type is 
equivalent to CEP .  
Student Demographic records  
District Number, 
Current 
Instruction/Service  District Number, 
Current 
Instruction/Service  Florida Education 
Identifier  School 
Number, 
Current 
Enrollment  Survey 
Period 
Code  Year  Lunch 
Status  
01 01 FL123456789456  0021  3 1415  3 
01 01 FL123456789678  0551  3 1415  4 
* 01  01 FL123456789123  2031  3 1415  F 
 
National School Lunch Program (NSLP) Reference File records  
Year  District Number  School Number  Reference File NSLP - Category  
1415  01 0021  1 
1415  01 0551  2 
1415  01 2031  3 
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /    

**District Responsibility:** The district must correct the Student Demographic record so that the appropriate relationship exists 
between the NSLP Reference File code and Lunch Status code.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  STATE VALIDATION RULES  

### 5F. If Survey Period Code is 2, 3, or 5, and Immigrant Student = Y on the Federal/State Indicator Status 
record, then Country of Birth must not be US or PR (per Appendix G or Appendix Q). The match for 
Student Demographic and Federal/State Indicator Status rec ords should be based on both District 
Number, Current Enrollment and District Number, Current Instruction/Service (Student Demographic) 
and District Number, Current Enrollment (Federal/State Indicator Status); Florida Education Identifier; 
Survey Period Co de and Fiscal Year. (This edit does not apply to Survey Period 6.).  
## State Validation

EXAMPLE  
Each of the records listed below would cause a message to be generated. The first record because 
Country of Birth is not a valid code; the second and third records because Immigrant Student is Y and 
Country of Birth is US and PR, respectively.  
Federal/State Indicator Status records District Number,  Florida  Survey  
Current Education Period Immigrant Enrollment Identifier Code Year Student  
District Number, Current 
Instruction/Service  Florida Education 
Identifier  Survey Period 
Code  Year  Immigrant 
Student  
01 *FL123456789001  2 ****  N 
01 *FL123456789002  2 ****  Y 
01 *FL123456789123  2 ****  Y 
Student Demographic records  
District Number, Current 
Instruction/Service  Florida Education 
Identifier  Survey Period 
Code  Year  Country of 
Birth  
01 * FL123456789200  2 ****  XX 
01 * FL123456789300  2 ****  US 
01 * FL123456789400  2 ****  PR 
**** = Valid fiscal year for data submission.  

**District Responsibility:** The district must correct the records so that the appropriate relationship exists among Immigrant 
Student and Country of Birth.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  STATE VALIDATION  RULES  

### 5G. If Survey = 5 and Migrant Status Term is B, D, E, S, T, U, V or W, then there must be a matching 
Federal/State Compensatory Project Evaluation record based on both District Number, Current 
Enrollment and District Number, Current Instruction/Service (Studen t Demographic) and District 
Number, Current Instruction/Service (Federal/State Compensatory); Florida Education Identifier; Survey 
Period Code and Fiscal Year. (This edit does not apply to Survey Period 6.).  
## State Validation

EXAMPLE  
The second and third Student Demographic records listed below would cause a message to be generated 
because neither has a matching Federal/State Compensatory Project Evaluation record reported based 
on their Migrant Status Terms.  
Student Demographic records  
District Number, Current 
Instruction/Service  Florida Education 
Identifier  Survey Period 
Code  Year  Migrant Status 
Term  
01 FL123456789010  5 ****  B 
* 01  FL123456789020  5 ****  U 
* 01  FL123456789030  5 ****  E 
Federal/State Compensatory Project Evaluation records  
District Number, Current 
Instruction/Service  Florida Education 
Identifier  Survey Period 
Code  Year  
01 FL123456789001  5 ****  
01 FL123456789002  5 ****  
**** = Valid fiscal year for data submission.  

**District Responsibility:** The district must correct the records so that the appropriate relationship exists between the Student 
Demographic record and Federal/State Compensatory Project Evaluation records.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  EXCEPTION REPORT  RULES  

### 60. For Survey Period Codes 2, 3 and 5, if the District Number, Current Instruction/ Service is not equal to 
the District Number, Current Enrollment then all other fields; except Student Number Identifier, Local; 
Resident Status, State/County; Institution Numb er, Neglected/Delinquent (First); Institution Number, 
Neglected/Delinquent (Second) and Institution Number, Neglected/Delinquent (Third), must be exact 
replicas of corresponding fields found on that student's Student Demographic record which was 
submitted by the district of enrollment.  
For Survey Period Codes 2 and 3, if the District Number, Current Instruction/ Service is 71 and District 
Number Current Enrollment is not equal to 71, then all other fields must be exact replicas of 
corresponding fields found on that student’s Student Demo graphic record which was submitted by the 
district of enrollment with the exception of:  
• Student Name, Legal where only the last name must be an exact replica of the corresponding 
field found on that student’s Student Demographic record which was submitted by the district of 
enrollment and  
• District Number, Zoned School; School Number, Zoned School; Student Number identifier, Local; 
Resident Status, State/County; Student Characteristic, Agency Programs; Native Language, Student; 
Primary Language Spoken in Home; Country of Birth; English Lang uage Learners:  
Home Language Survey Date; Qualifying Arrival Date (QAD) for Migrant  
Program Eligibility; Lunch Status; Migrant Status Term; Graduation Option; Institution Number, 
Neglected/Delinquent (First); Institution Number, Neglected/Delinquent (Second) and Institution 
Number, Neglected/Delinquent (Third).  
For Survey Period Codes 1 and 4,  
• if the District Number, Current Instruction/Service is 71 and District Number Current Enrollment 
is not equal to 71,  
• and if there is a matching Student Demographic record in the District  
Number Current Enrollment, then all other fields must be exact replicas of corresponding fields found on 
that student’s Student Demographic record which was submitted by the district of enrollment with the 
exception of:  
• Student Name, Legal where only the last name must be an exact replica of the corresponding 
field found on that student’s Student Demographic record which was submitted by the district of 
enrollment and  
• District Number, Zoned School; School Number, Zoned School; Student Number identifier, Local; 
Resident Status, State/County; Student Characteristic, Agency Programs; Native Language, Student; 
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  Primary Language Spoken in Home; Country of Birth; English Language Learners: Home Language Survey 
Date; Qualifying Arrival Date (QAD) for Migrant  
Program Eligibility; Lunch Status; Migrant Status Term; Graduation Option; Institution Number,  
Neglected/Delinquent (First); Institution   Number, Neglected/Delinquent (Second) and Institution 
Number,  Neglected/Delinquent (Third).    
(This edit does not apply to Survey Period 6.)  
## State Validation

EXAMPLE  
The two records listed below would cause a message to be generated. They are for the same student 
(same, Florida Education Identifier). However, the Grade Levels are different and the English Language 
Learner codes are different.   
District Number, 
Current Enrollment  District Number Current 
Instruction/Service  Florida Education 
Identifier  Grade 
Level  English 
Language 
Learner  
* 42  01 FL123456789100  11 LP 
* 42  42 FL123456789200  12 LY 

**District Responsibility:** The district should verify the data submitted on the Student Demographic records and correct if in error.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  EXCEPTION REPORT  

### 63. If Grade Level is KG -12 and School Number, Current Enrollment is not 9992, 9993, or 9995, the student 
must be at least 5 years old on or before September 1 of the school year being reported.  
Note: Students who transfer to Florida from states with different minimum starting ages are accepted 
into the grade into which they are transferring.  
## Exception Reports

EXAMPLE  
If the record below was submitted in the 2013 -14 school year, then  the record would cause a message to 
be generated because Grade Level is KG and age is less than 5.  
Florida Education  
Identifier  Year  Survey Period  
Code  Grade  
Level  Birth Date  
*FL123456789001  1314  2 KG 02192009  

**District Responsibility:** The district should verify the Birth Date and correct it if it is in error.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  EXCEPTION REPORT  

### 64. If Grade Level is PK -12 and School Number, Enrollment is not 9995; then Resident Status, State/County 
must be 0, A, B, 2 or - 3. If Grade Level is 30 -31, then Resident Status, State/County must be 4, 5, 6 or 7. 
(This edit does not apply to Survey Period 6.)   
## Exception Reports

EXAMPLE  
The records listed below would cause a message to be generated because the relationship between 
Grade Level and Resident Status, State/County is not the expected relationship as stated in the edit.  
Florida Education 
Identifier  Year  Survey Period 
Code  Grade 
Level  Resident Status, 
State/County  
*FL123456789003  ****  2 05 5 
*FL123456789004  ****  2 30 2 
**** = Valid fiscal year for data submission.  

**District Responsibility:** The district should verify the Resident Status, State/County and the Grade Level, and correct if in error.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  EXCEPTION REPORT  
UPDATED  07/01/2026  

### 68. If Survey Period Code = 2, 3 or 5; School Number, Current Enrollment is not 9992, 9993, 9994, 9995 or 
9997; District Number, Current Instruction/Service is not 71; District Number, Current Enrollment equals 
District Number, Current Instruction/Service; Wit hdrawal Code, PK -12 on matching Prior School 
Status/Student Attendance records is not DNE; and Grade Level is not 30 or 31, then each Student 
Demographic record must have a matching Federal/State Indicator Status record and a matching Prior 
School Status/S tudent Attendance  record.  
The Federal/State Indicator Status and the Prior School Status/Student Attendance records must match 
on the District Number, Current Enrollment; Florida Education Identifier; Survey Period Code and Fiscal 
Year with the following  key fields on Student Demog raphic: District Number, Current Instruction/Service; 
Florida Education Identifier; Survey Period Code; and Fiscal Year.  
(This edit does not apply to Survey Period 6.)  
## Exception Reports

EXAMPLE  
The first and third Student Demographic records listed below would pass this edit. The second Student 
Demographic record would not pass the edit because it has no matching Federal/State Indicator Status 
record  and no matching Prior  School Status/Student Attendance record. The fourth Student 
Demographic record would not pass the edit because it has a matching Prior School Status/Student 
Attendance record but not a matching Federal/State Indicator Status record.   The fifth student 
Demographic record would pas s the edit because the District Number, Current Enrollment does not 
equal District Number, Current Instruction/Service.   
Student Demographic records            
District  
Number,  
Current  
Instruction/Service   
District Number,  
Current  
Enrollment  Florida  
Education  
Identifier  Survey  
Period  
Code  Fiscal  
Year  
26 26 FL123456789000  2 ****  
* 26  26 FL123456789100  2 ****  
26 26 FL123456789200  2 ****  
*26 26 FL123456789399  2 ****  
26 45 FL123456789444  2 *** 
 
Federal/State Indicator records  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  District Number,  
Current  
Enrollment  Florida  
Education  
Identifier  Survey  
Period  
Code  Fiscal  
Year  
26 FL123456789000  2 ****  
26 FL123456789200  2 ****  
 
Prior School Status/Student Attendance records  
District  
Number,  
Current  
Enrollment  Florida  
Education  
Identifier  Survey  
Period  
Code  Fiscal  
Year   
Withdrawal 
Code, PK -12  
Grade Level  
26 FL123456789000  2 ****  W3A  11 
26 FL123456789100  2 ****  W3A  11 
26 FL123456789200  2 ****  W3A  11 
 
**** = Valid fiscal year for data submission.  

**District Responsibility:** The district must review the Student Demographic record and determine whether a Federal/State 
Indicator Status record is necessary. If such a record is necessary, the district should submit the record. If 
such a record is not necessary, no action is necess ary.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  EXCEPTION REPORT  
UPDATED 07/01/2026  

### 69. If Survey Period Code is 2, 3, or 5; School Number, Current Enrollment is not 9992, 9993, 9994, 9995, or 
9997; Migrant Status Term is not X; District Number Current Instruction/Service is not 71 and Grade 
Level is not 30 or 31; then each Student Demographi c record must have at least one matching Prior 
School Status/Student Attendance record .  
The match to the Prior School Status/Student Attendance record is performed using the following key 
fields from the Student Demographic format: District Number, Current Instruction/Service, Florida 
Education Identifier, Survey Period Code, and School Year.  These must match on District Number, Current 
Enrollment, Florida Education Identifier, Survey Period Code, and Year on the Prior School Status/Student 
Attendance record.  
(This edit does not apply to Survey Period 6.)  
## Exception Reports

EXAMPLE  
The first record listed below would generate an error message because there is no matching Prior School 
Status/Student Attendance record to accompany it, and Migrant Status Term is not equal to X. The 
second record without a matching Prior School Status/St udent Attendance record would not generate an 
error message because Migrant Status Term is equal to X. The third record would not generate an error 
message because it has a matching Prior School Status/Student Attendance record.  
Student Demographic records   
District Number, Current 
Instruction/Service  Florida Education 
Identifier  Survey Period 
Code  Year  Migrant Status 
Term  
* 02  FL123456789001  3 1011  Z 
02 FL123456789004  3 1011  X 
02 FL123456789005  3 1011  B 
Prior School Status/Student Attendance records  
District Number, Current Enrollment  Florida Education Identifier  Survey Period Code  Year  
02 FL123456789005  3 1011  

**District Responsibility:** The district must review the  record and determine whether a 
matching Prior School Status/Student Attendance record is necessary. If such a record is necessary, the 
district must submit the record. If such a record is not nec essary, then no action is necessary.   
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  AGGREGATE EXCEPTION REPORT  

### 90. For each School Number, Current Enrollment, at least one record must have a Lunch Status code not 
equal to 0 unless the School Number, Current Enrollment is 9996, 9997, N998, or N999. (The student did 
not apply for free or reduced -price lunch). (This edit does not apply to Survey Period 6.)  
Note: The following information will be listed on the exception report for schools that do not meet the 
exception edit above:  
• District Number, Current Enrollment  
• School Number, Current Enrollment  
• Total number of Student Demographic records  
• Number of records with Lunch Status = 0  
## Exception Reports

EXAMPLE  
School 0021 has 56 total Student Demographic records. All of these records have a Lunch Status code of 

### 0. An error message is generated for School 0021 on the exception report indicating that the school 
failed this exception edit.  

**District Responsibility:** The district must review the records to determine whether code 0 was used appropriately. The district 
must correct the Lunch Status on the Student Demographic records that are in error. If no records are in 
error, no action is necessary.  
  
STUDENT DEMOGRAPHIC  
Student Database 202 6-2027 /  AGGREGATE VALIDATION  

### 91. For each School Number, Current Enrollment in the District Number, Current Enrollment either all 
records must have a Lunch Status code of 4 (Provision 2 School) or no records must have a Lunch Status 
code of 4. (This edit does not apply to Survey Period 6. )  
Aggregate Validation  
EXAMPLE  
The records listed below would cause an error message to be printed on the validation report for school 
0012 because one record in the school has a Lunch Status code of 4 and the other record has a Lunch 
Status code of 1.  
District  
Number,  
Current  
Enrollment  School  
Number,  
Current  
Enrollment  Florida  
Education  
Identifier  Survey  
Period  
Code  Lunch  
Status  
* 01  0012  FL123456789002  2 1 
* 01  0012  FL123456789003  2 4 

**District Responsibility:** The district must review the information in the set of records and correct the record that is in error so 
that either all or none of the records in the school have a Lunch Status code of 4.