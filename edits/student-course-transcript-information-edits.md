# Student Course Transcript Information — Edits and Reject Rules

Source: Florida DOE
Manual: Student Database 2026-2027

Student Database 202 6-2027 /  REJECT RULES  

### 1. Survey Period Code must be 5 and must be correct for the submission specified by the district.  
**Result:** Record rejected
EXAMPLE  
The Survey Period Code as specified in the transmission JCL or in statements for tape transmission is 
identified as Survey Period "5". However, if records on the transmission have a Survey Period Code "3", 
all records updated, added, or deleted with this i nconsistency would be rejected.  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the Survey Period Code must be 
corrected either on the records coming in or the tran smission JCL and all records must be resubmitted in 
a batch transaction or added on -line.  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
  
  
 
Student Database 202 6-2027 /  REJECT RULES  
UPDATED 07/01/2026  

### 2. District Number, Current Enrollment must be numeric and active (A) on the Appendix C: District Name 
Table  and must be correct for the district submitting the data.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no  other reject rule would 
cause their rejection. The third record (indicated by an asterisk) would be rejected since the District 
Number, Current Enrollment is not active (A) on the Appendix C: District Name Table . 
District Number , Current 
Enrollment  School Number, Current 
Enrollment  Florida Education Identifier  
01 0021  FL123456789100  
01 0021  FL12345 6789200  
* 00  0021  FL123456789300  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the District 
Number, Current Enrollment and resubmit the r ecord.  
 
 
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  REJECT RULES  

### 3. School Number, Current Enrollment must be numeric in the range 0001 to 9899, excluding 9001 and 
7006.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause the records to be rejected. The two records indicated with asterisks would be rejected. The first of 
these would be rejected because the School Num ber, Current Enrollment is not in the appropriate  
numerical range. The second of these two records would be rejected because the School Number, 
Current Enrollment is not numeric.  
District Number, Current 
Enrollment  School Number, Current 
Enrollment  Florida Education Identifier  
01 0021  FL123456789100  
01 0021  FL123456789200  
* 01 9999  FL123456789300  
* 01  C901  FL123456789 000 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the School 
Number, Current Enrollment and resubmit the r ecords.  
## Reject Rules

Student Database 202 6-2027 /  REJECT RULES  
UPDATED 07/01/2026  

### 5. The District Number, Where Credit Earned must be active (A) on the Appendix C: District Name Table  for 
Florida public school districts, 99 for credit earned in Florida non -public schools, alpha codes AK -WY for 
credit earned out -of-state, or  AA-ZB for credit earned out -of-country, or AQ to WQ for credit earned at 
United States Commonwealth and Territories. (See Appendices G, H and Q of the DOE  Information 
Database Requirements: Volume I --Automated Student Information System Manual for valid Foreign 
Country, State codes and United States Commonwealth and Territories.)  
**Result:** Record rejected
EXAMPLE  
The first and third records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. The second record would be rejected since the District Number, Where  
Credit Earned is not active (A) on the Appendix C: District Name Table . 
District Number, 
Where Credit Earned  School Number, Current 
Enrollment  School Year  Term  
01 0151  0203  2 
* 70  7542  0203  1 
99 9999  0203  4 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the District 
Number, Where Credit Earned entries and res ubmit the records.  
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  REJECT RULES  

### 6. The School Number, Where Credit Earned must be alphanumeric in the range of 0001 -9899 for Florida 
public school district sites, N999 or in the range of 0001 -9899 for credit earned in Florida PK -12 non -
public schools, 9900 for credit earned in out -of-state schools, N998 for credit earned in home  education, 
N997 for credit earned in an American school abroad, C901 -C928 for Florida public  community colleges, 
U970 -U981 for Florida public state universities, or P001 -P999 for eligible  postsecondary nonpublic 
institutions.  
**Result:** Record rejected
EXAMPLE  
The second and fourth records listed below would be loaded to the database  assuming no other reject 
rule would cause their rejection. The first record would be rejected since the School Number, Where 
Credit Earned contains a blank. The third record would be rejected since the School Number, Where 
Credit Earned has an invalid code . 
District Number, 
Where Credit Earned  School Number, Current 
Enrollment  School Year  Term  
* 01 151 ****  2 
64 6881  ****  1 
* 99 M999 ****  4 
ID N999  ****  2 
**** = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the School 
Number, Where Credit Earned and resubmit the records.  
 
 
 
 
 
 
 
  
  
 
Student Database 202 6-2027 /  REJECT RULES  

### 7. School Year – Course Taken must be a valid school year, numeric, and less than or equal to the current 
school year.  
**Result:** Record rejected
EXAMPLE  
The first, fourth and fifth records listed below would be loaded to the database  assuming no other reject 
rule would cause their rejection. The second and third records would be rejected since the school year is 
invalid.  
District Number, Where 
Credit Earned  School Number, Current 
Enrollment  School Year  Course 
Taken  
01 0021  0203  
* 01  0021  9597  
* 01  0021  9492  
01 0021  9899  
01 0021  0910  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the School 
Year – Course Taken and resubmit the records.  
 
 
 
 
 
 
 
 
 
 
 
  
  
 
Student Database 202 6-2027 /  REJECT RULES  

### 8. Grade Level must be 01 -12 or 30.  
**Result:** Record rejected
EXAMPLE  
The second and third records listed below would be loaded to the database  assuming no other reject rule 
would cause their rejection. The first record would be rejected because the Grade Level does not contain 
two characters as required. The fourth record would be rejected since the Grade Level is not a valid 
grade.  
School Year  Grade Level  Term  
* 0001 8 1 
0001  10 2 
0203  11 1 
* 0203  40 2 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Grade 
Level and resubmit the records.  
 
 
 
 
 
 
 
 
 
 
 
  
  
 
Student Database 202 6-2027 /  REJECT RULES  

### 9. Term must be 1 -9, B-O, or S -X.  
**Result:** Record rejected
EXAMPLE  
The second and third records listed below would be loaded to the database  assuming no other reject rule 
would cause their rejection. The first record would be rejected because Term was left blank. The fourth 
record would be rejected since the Term code is not valid.  
School Year  Grade Level  Term  
* 0001  8  
0001  10 2 
0203  11 1 
* 0203  12 A 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Term 
codes and resubmit the records.  
 
 
 
 
 
 
 
 
 
 
 
  
  
 
Student Database 202 6-2027 /  REJECT RULES  

### 10. Course Number must be alphanumeric and contain no blanks.  
**Result:** Record rejected
EXAMPLE  
The second, third, fourth, fifth, and sixth records listed below would be loaded to the database assuming 
no other reject rule would cause their rejection. The first and seventh records would be rejected since 
the Course Number contains blanks.  
Florida Education 
Identifier  School Year  Course Number  Course Sequence 
Number  
FL123456789100  ****  1  5300  1234A  
FL123456789200  ****  0900310  1234A  
FL123456789100  ****  A010203  12345  
FL123456789100  ****  1200330  3456C  
FL123456789100  ****  V200302  1234A  
FL123456789100  ****  2109310  ABCDE  
* FL123456789100  ****  1005  21234  
**** = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district should correct the 
Course Number and resubmit the record.  
 
 
 
 
 
 
 
 
 
  
  
 
Student Database 202 6-2027 /  REJECT RULES  

### 11. The Course Sequence Number must be alphanumeric and contain no blanks. Allowable characters are 0 -
9, A-Z, hyphen, dollar sign, pound sign, and colon.  
**Result:** Record rejected
EXAMPLE  
The second, third, fourth, fifth, and sixth records listed below would be loaded to the database assuming 
no other reject rule would cause their rejection. The first and seventh records would be rejected since 
the Course Sequence Number contains blanks.  
Florida Education 
Identifier  School Year  Course Number  Course Sequence 
Number  
* FL123456789100  ****  1005300  1  34A 
FL123456789200  ****  0900310  1234A  
FL123456789100  ****  0400330  12345  
FL123456789100  ****  1200330  3456C  
FL123456789100  ****  1302340  1234A  
FL123456789100  ****  2109310  ABCDE  
* FL123456789100  ****  1005 300 2   4 
**** = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Course 
Sequence Number and resubmit the records.  
 
 
 
 
 
 
 
 
 
  
  
 
Student Database 202 6-2027 /  REJECT RULES  

### 12. All alphanumeric Course Numbers must either be on the Course Code Directory or on the Statewide 
Course Numbering System file unless School Number, Where Credit Earned equals P001 -P999.  
**Result:** Record rejected
EXAMPLE  
The second and third records listed below would be loaded to the database  assuming no other reject rule 
would cause their rejection. The first and fourth records would be rejected because the Course Numbers 
are not on the Course Code Directory or on the Statewide Course Numbering System files.  
Florida Education 
Identifier  District Number, 
Where Credit 
Earned  School Number, Where 
Credit Earned  Course Number  
* FL123456789100  66 0061 FF10011  
FL123456789200  66 0061 I460103  
FL123456789300  66 0201 B070614  
* FL123456789000  66 C901 ABCDE12  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Course 
Numbers and resubmit the records.  
 
 
 
 
 
 
 
 
 
 
  
  
 
Student Database 202 6-2027 /  REJECT RULES  
UPDATED 07/01/25  

### 13. If School Year -Course Taken = School Year -Record Submission, then  Course, State Subject Area 
Requirements must equal A1, AG, AH, BI, CT, EC, EL, EN, EQ, FE,  GE, MA, NC, PE, PF, PL, or WH.  
**Result:** Record rejected
EXAMPLE  
In the example below, records number two, five, six, and seven would be loaded to the database 
assuming no other reject rule would cause the records to be rejected. Records one, three and four would 
be rejected since the Course, State Subject Area Requirem ents codes are invalid.  
Course Number  Course Sequence Number  Course, State Subject  Area 
Requirements  
* 1005300  1234A  E 
0900310  2345B  EL 
* 0400330  1235B  FP 
* 1200330  3456C  MS 
1302340  45678  PF 
2109310  ABCDE  WH 
1005320  123AB EN 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
Course, State Subject Area Requirements and resubmit  the records.  
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  REJECT RULES  

### 14. If School Year -Course Taken = School Year -Record Submission, then Course Flag must be 7, 9, G -I, N, P, T, 
W, X, * or blank.  
**Result:** Record rejected
EXAMPLE  
In the example below, records one and three would be loaded to the database  assuming no other reject 
rules would cause the records to be rejected. Record two would be rejected since the Course Flag 
contains invalid characters.  
Course Number  Course Flag  
 HT 
* 0900310  9S5 
1302340   

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Course 
Flag entry and resubmit the record.  
 
 
 
 
 
 
 
 
 
 
 
  
  
 
Student Database 202 6-2027 /  REJECT RULES  

### 15. For each  record, no Course Flag, except blanks, may be repeated.  
**Result:** Record rejected
EXAMPLE  
In the example below, records two and three would be loaded to the database  assuming no other reject 
rule would cause the records to be rejected. The first record would be rejected since the Course Flag 
contains two H codes.  
Course Number  Course Flag  
* 1005300  RHH  
0900310  9 
1302340   

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Course 
Flag and resubmit the record.  
 
 
 
 
 
 
 
 
 
 
 
 
  
  
 
Student Database 202 6-2027 /  REJECT RULES  

### 16. Credit Attempted, Course must be numeric.  
**Result:** Record rejected
NOTE: Two decimal places assumed.  
EXAMPLE  
In the example below, records two, five, six, and seven would be loaded to the database assuming no 
other reject rule would cause the records to be rejected. Records one, three, and four would be rejected 
since the Credit Attempted, Course is not numeric.  
Course Number  Credit Attempted, 
Course  Credit Earned , 
Course  
* 1005300  edk 100 
0900310  050 050 
* 0400330  05a 100 
* 1200350  Ooo  050 
1302340  100 100 
2109310  100 050 
1005320  050 050 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Credit 
Attempted, Course and resubmit the records.  
 
 
 
 
 
 
 
 
 
  
  
 
Student Database 202 6-2027 /  REJECT RULES  

### 17. Credit Earned, Course must be numeric.  
**Result:** Record rejected
NOTE: Two decimal places assumed.  
EXAMPLE  
In the example below, records two, five, six, and seven would be loaded to the database assuming no 
other reject rule would cause the records to be rejected. Records one, three, and four would be rejected 
since the Credit Earned, Course is not numeric.  
Course Number  Credit Attempted, 
Course  Credit Earned, 
Course  
* 1005300  100 edk 
0900310  050 050 
* 0400330  100 Ooo  
* 1200350  050 5x5 
1302340  100 100 
2109310  100 050 
1005320  050 050 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Credit 
Earned, Course and resubmit the records.  
 
 
 
 
 
 
 
 
 
  
  
 
Student Database 202 6-2027 /  REJECT RULES  

### 18. The Course Grade code must be A+, A, A -, B+, B, B -, C+, C, C -, D+, D, D -, F, I, N, NNN, U, P, S, SB, T, E, WP, 
FL, NG, W or WF and must be right justified with leading blanks.  
**Result:** Record rejected
EXAMPLE  
In the example below, records two and five would be loaded to the database  assuming no other reject 
rule would cause the records to be rejected. Records one and four would be rejected since they contain 
invalid codes. Record three would be rejected since the Course Grade is not right justified with leading 
blanks.  
Course Number  Credit Attempted, 
Course  Credit Earned, 
Course  
* 1005300  100 OOA  
0900310  050 B+ 
* 0400330  100 C+ 
* 1200350  050 WC 
1200350  050 P 

**District Responsibility:** If the rejected records should not have been submitted, no action is required.  
However, if the district wishes the data in the rejected records to be loaded to the  
database, the district must correct the Course Grade and resubmit the records.  
 
 
 
 
 
 
 
 
 
  
  
 
Student Database 202 6-2027 /  REJECT RULES  

### 19. The Transaction Code must be A, C or D. For the original transmission, only  A is valid. For subsequent 
batch/update submissions, if A is specified then the record must not already exist on the database; if C or 
D is specified then the record must exist on the database.  
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
 
 
 
 
 
 
 
 
 
 
 
 
  
  
 
Student Database 202 6-2027 /  REJECT RULES  

### 20. Each  record must be unique based on Survey Period Code; District 
Number, Current Enrollment; School Number, Current Enrollment; Florida Education Identifier; School 
Year – Record Submission; School Year – Course Taken;  Grade Level; Term; Course Number; and Course 
Sequence Number.  
**Result:** First record accepted, all other duplicate records rejected
EXAMPLE  
The first, third, fourth, sixth, and seventh records listed below would be loaded to the database assuming 
no other reject rule would cause the records to be rejected. The second and fifth records would be 
rejected since they are duplicates of the first an d fourth records, respectively.  
Survey 
Period 
Code  District 
Number, 
Current 
Enrollment  School 
Number, 
Current 
Enrollment  Florida 
Education 
Identifier  School 
Year -
Course 
Taken  Grade 
Level  Term  Course 
Number  Course 
Sequence 
Number  
5 01 0021  FL123456789100  1011  12 2 1200310  1234A  
*5 01 0021  FL123456789100  1011  12 2 1200310  1234A  
5 01 0021  FL123456789200  1011  12 3 1001370  1234D  
5 01 0021  FL123456789300  1011  12 3 1001370  1234D  
*5 01 0021  FL123456789300  1011  12 3 1001370  1234D  
5 01 0021  FL123456789000  1011  11 1 2001370  1234D  
5 01 0021  FL123456789000  1011  11 2 2001370  1234D  

**District Responsibility:** If the records loaded to the database are correct, no action is necessary. However, if the district wishes 
the rejected records to be loaded to the database, the district must delete any invalid records, correct 
any rejected records if necessary, and resub mit the corrected records.  
 
 
 
 
 
 
 
  
  
 
Student Database 202 6-2027 /  REJECT RULES  

### 21. School Number, Current Enrollment must exist on the Master School Identification File as a valid active 
school number for the District Number, Current Enrollment.  
**Result:** Record rejected
EXAMPLE  
The fourth and fifth records listed below would be loaded to the database assuming no other reject rule 
would cause the records to be rejected. Records one, two, and three would be rejected because the 
School Number, Current Enrollment does not exist on th e Master School Identification File as a valid 
active school number for the District Number, Current Enrollment . 
District Number, Current Enrollment  School Number, Current Enrollment  
* 09  8131  
* 13  0021  
* 15  C999  
57 0051  
63 0031  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the School 
Number, Current Enrollment and resubmit the r ecords.  
 
 
 
 
 
 
 
 
 
 
  
  
 
Student Database 202 6-2027 /  REJECT RULES  

### 22. Item 5 - Filler on this format in position numbers 22 -31 must be all spaces.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because the data reported is not all spaces.  
District Number, Current 
Enrollment  School Number, Current 
Enrollment  Filler, Item #5 
01 0151   
* 01  0151  265456789X  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must fill the positions 
noted with all spaces and resubmit the record.  
 
 
 
 
 
 
 
 
 
 
 
 
  
  
 
Student Database 202 6-2027 /  REJECT RULES  

### 23. The Student Number Identifier, Local may be any combination of letters, numbers and blanks. (All blanks 
are allowable.) It must be left -justified with trailing blanks.  
**Result:** Record rejected
EXAMPLE  
The first three records listed below would be loaded to the database assuming no other edit would cause 
their rejection. The fourth record would be rejected because the Student Number Identifier, Local  
contains a symbol (@). The fifth record would be rejected because it is right -justified rather than left -
justified.  
District Number, Current Enrollment  School Number Identifier, Local  
01 0123456789  
01 ABC123DEF9  
01 3001  28K  
* 01  2121@XYZ  
* 01  123456  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
Student Number Identifier, Local and resubmit the re cords.  
 
 
 
 
 
 
 
 
 
  
  
 
Student Database 202 6-2027 /  REJECT RULES  

### 24. If School Number, Where Credit Earned equals C901 -C928, U970 -U981, or P001 -P999, then District 
Number, Where Credit Earned must equal 99.  
Record reject ed 
EXAMPLE  
The first record listed below would pass the edit. The second record would be rejected because the 
School Number, Where Credit Earned is not correct for the District Number, Where Credit Earned.  
District Number, Where Credit 
Earned  School Number, Where Credit 
Earned  Florida Education Identifier  
99 U970  FL123456789100  
* 16  C901  FL123456789200  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the District 
Number, Where Credit Earned or the School Num ber, Where Credit Earned and resubmit the record.  
 
 
 
 
 
 
 
 
 
 
 
 
  
  
 
Student Database 202 6-2027 /  REJECT RULES  

### 25. If the Course Grade code equals W, then the School Number, Where Credit Earned must be U970 -U981, 
C901 -C928, P001 -P999, 9900 or N999.  
**Result:** Record rejected
EXAMPLE  
In the examples below, records two and four would be loaded to the database  assuming no other reject 
rule would cause the records to be rejected. Records one and three would be rejected because the 
Course Grade is not valid for the reported School Number, Where Credit Earned.  
Course Number  School Number, Where Credit 
Earned  Course Grade  
* 1005300  0021  W 
Z001010  C901  W 
* 04 00330  7851  W 
PSY2012  U970  W 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Course 
Grade or the School Number, Where Credit Earn ed and resubmit the records.  
 
 
 
 
 
 
 
 
 
 
 
  
  
 
Student Database 202 6-2027 /  REJECT RULES  

### 26. Course Number, Substituted must be a course in the Course Code Directory or it must be blank.  
**Result:** Record rejected
EXAMPLE  
The second record listed below would be loaded to the database assuming no other reject rule would 
cause its rejection. The first and third records would be rejected because the Course Numbers,  
Substituted are not in the Course Code Directory.  
Florida Education 
Identifier  District Number, Where 
Credit Earned  School Number, Where 
Credit Earned  Course Number 
Substituted  
* FL123456789100  66 0101  FF10011  
FL123456789200  66 0101  0800300  
* FL123456789300  66 C917  ABCDE12  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Course 
Number, Substituted fields and resubmit the r ecords.  
 
 
 
 
 
 
 
 
 
 
 
 
  
  
 
Student Database 202 6-2027 /  REJECT RULES  

### 27. If the Course Number, Substituted is not blank, then at least one Course Flag must be “*”.  
**Result:** Record rejected
EXAMPLE  
The first and third records listed below would be loaded to the database assuming  no other reject rule 
would cause their rejection. The second record would be rejected because there is no asterisk (*) Course 
Flag.  
Florida Education 
Identifier  Course Number  Course Number 
Substituted  Grade Level  Course Flag  
FL123456789100  1802300  0800300  09 * 
* FL123456789200  1802300  0800300  10  
FL123456789300  1802300  0800300  11 * 

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Course 
Number, Substituted or the Course Flag field and resubmit the record.  
 
 
 
 
 
 
 
 
 
 
 
 
  
  
 
Student Database 202 6-2027 /  REJECT RULES  

### 28. If any of the four Course Flags are “*”, then the Course Number, Substituted must not be blank.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Course Number, Substituted must 
not be blank when there is a Course Flag of ‘*’.  
Florida Education 
Identifier  Course Number  Course Number 
Substituted  Grade Level  Course Flag  
FL123456789100  1802300  0800300  09 * 
* FL123456789200  1802300  0800300  10 * 
FL123456789300  1802300   11 * 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Course 
Number, Substituted or the Course Flag field an d resubmit the record.  
 
 
 
 
 
 
 
 
 
 
 
  
  
 
Student Database 202 6-2027 /  REJECT RULES  
UPDATED 07/01/25  

### 29. If School Year -Course Taken = School Year -Record Submission, then Course Substituted, State Subject 
Area Requirements must equal A1, AG, AH, BI, CT, EC, EL, EN, EQ, FE,  FL, GE, MA,  NC, PE, PF, PL, or WH, or 
blank. If Course Number, Substituted is blank, Course Substituted, State Subject Area Requirements must 
be blank. If Course Substituted, State Subject Area Requirements is blank, then Course Number, 
Substituted must be blank.  
**Result:** Record rejected
EXAMPLE  
In the example below, the first record would be loaded to the database assuming  no other reject rule 
would cause it to be rejected. The second record would be rejected since the Course Substituted, State 
Subject Area Requirements code is invalid.  
Course Number  Course Number 
Substituted  Course 
Subst ituted, 
State Subject 
Area 
Requirements  
0800300  1802300  PE 
* 0800300  1802300  PP 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Course 
Substituted, State Subject Area Requirements co de and resubmit the record.  
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /   
## Reject Rules

### 30. The School Year – Record Submission must be correct for the submission specified by the district.  
**Result:** Record rejected
EXAMPLE  
The School Year – Record Submission on the JCL and the records being submitted for processing must 
match. Otherwise, the records will be rejected.  

**District Responsibility:** Correct the School Year – Record Submission either on the transmission JCL or the records being 
submitted and resubmit all records for processing.  
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
  
 
Student Database 202 6-2027 /  REJECT RULES  

### 36. If School Number, Where Credit Earned does not begin with P, then Course Number must not equal 
5022000, or 2200300 -2200330 (study hall) and must not have a Sort Level of 1 (Basic Education PK -5) or 2 
(Basic Education 6 -8) on the Course Code Directory file DPS.DISTRICT.K9.F62806.Yyyyy.  
**Result:** Record rejected
EXAMPLE  
The third and fourth records listed below would be loaded to the database  assuming no other reject rule 
would cause their rejection. The first record listed below would be rejected because it is a Study Hall 
course. The second record would be rejected because it is a middle/junior high school course.  
Florida Education 
Identifier  School Year  Course 
Number  School Number, 
Where Credit 
Earned  
* FL123456789100  ****  2200300  5201  
FL123456789200  ****  0702020  5211  
FL123456789300  ****  2003310  5201  
FL123456789300  ****  1302300  5201  
                                   **** = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district should correct the 
Course Numbers and resubmit the records.  
 
 
 
 
 
 
 
 
 
  
  
 
Student Database 202 6-2027 /  REJECT RULES  

### 37. Florida Education Identifier (FLEID) is alphanumeric and must be entered as FL” in the first 2 positions 
followed by twelve numeric digits. No blanks, spaces or all zeros for the twelve numeric digits are  
allowable.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Florida Education Identifier (FLEID) 
is not a valid FLEID.  
District Number, Current Enrollment  Florida Education  Identifier  
01 FL340945895734  
01 FL004583948567  
* 01  FL000000000000  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Florida 
Education Identifier and resubmit the record f or processing.  
 
 
 
 
 
 
 
 
 
 
 
 
  
  
 
Student Database 202 6-2027 /  STATE VALIDATION RULES  

### 50. Each Student Course Transcript must have a matching Student Demographic Record based on District 
Number, Current Enrollment; Florida Education Identifier; Survey Period Code and School Year – Record 
Submission matched to Year.  
## State Validation

EXAMPLE  
The  record listed below which is marked with an asterisk would 
cause a message to be generated because it does not have a matching Student Demographic Information 
record.  
Student  Course Transcript Information records  
District Number, Current 
Enrollment  Florida Education Identifier  School Year -Record 
Submission  Survey Period Code  
* 01 FL123456789100  1011  5 
01 FL123456789200  1011  5 
01 FL123456789300  1011  5 
 
Student Demographic Information records  
District Number, Current 
Enrollment  Florida Education Identifier  Year  Survey Period Code  
01 FL123456789 200 1011  5 
01 FL123456789 300 1011  5 

**District Responsibility:** The district must delete the  record or add a Student Demographic 
Information record to match the key fields on the  record.  
 
 
 
 
 
 
 
 
  
  
 
Student Database 202 6-2027 /  EXCEPTION REPORTS  

### 80. Grade Level must be in the range 06 -12, or 30.  
## Exception Reports

EXAMPLE  
The second, third and fourth records listed below would pass this edit. The first record would cause an 
error message to be generated because the student is reported as being in grade level 05.  
School Year  Grade Level  Term  Credit Earned, Course  
* 9900  05 1 050 
9900  10 2 050 
0001  11 1 050 
0203  08 2 050 

**District Responsibility:** The district should verify the Grade Level submitted and correct the record if in error.  
 
 
 
 
 
 
 
 
 
 
 
 
 
  
  
 
Student Database 202 6-2027 /  EXCEPTION REPORTS   

### 81. If Grade Level is less than 09 and Credit Earned, Course is greater than zero, then Course Flag must be 9.  
## Exception Reports

EXAMPLE  
The second, third and fourth records listed below would pass this edit. The first  record would cause an 
error message to be generated because the student is reported as being in grade level 07, but does not 
have a Course Flag code of 9.  
School Year  Course Number  Grade Level  Course Flag  Credit Earned, 
Course  
* ****  1200310  07  050 
****  1001350  10 R 050 
****  1001370  11  050 
****  1200310  08 9 050 
**** = Valid fiscal year for data submission.  

**District Responsibility:** The district should verify the Course Flag code submitted and correct the record if in error.  
 
 
 
 
 
 
 
 
 
 
 
 
  
  
 
Student Database 202 6-2027 /  EXCEPTION REPORTS  

### 82. For each Course Flag of I, there must be a Course Flag of X on another course record for the same District 
Number, Current Enrollment; School Number, Current Enrollment; Florida Education Identifier; School 
Year – Record Submission and Course, State Subjec t Area Requirements.  
## Exception Reports

EXAMPLE  
The second and third records listed below would pass this edit. The first and fourth records would cause 
an error message to be generated because for the same Florida Education Identifier and the same Course 
Number there are no matching Course Flags of I a nd X.  
Florida Education 
Identifier  School Year 
Record 
Submission  Term  Course 
Number  Grade 
Level  Course State 
Subject Area 
Requirements  Course 
Flag Credit 
Earned 
Course  
* FL123456789100  1011  3  09 MA  000 
FL123456789200  1011  3  10 EN X 000 
FL123456789300  1011  3  11 EN I 100 
*FL123456789 100 1011  3  10 MA I 100 

**District Responsibility:** The district should verify the Course Flags submitted along with other elements listed in the edit 
statement and correct the records if in error.  
 
 
 
 
 
 
 
 
 
 
  
  
 
Student Database 202 6-2027 /  EXCEPTION REPORTS  

### 83. If Course Flag is N  then Credit Earned, Course must be zero.  
## Exception Reports

EXAMPLE  
The second and third records listed below would pass this edit. The first record  would cause an error 
message to be generated because there is a Course Flag of N, but Credit Earned, Course does not equal 
zero.  
Florida Education 
Identifier  School Year  Course 
Number  Course 
Grade  Course 
Flag Credit 
Earned 
Course  
* FL123456789100  00001  1200310  A N 100 
FL123456789200  0203  1001340  B-  100 
FL123456789100  0001  1200320  B  100 

**District Responsibility:** The district should verify the Course Flag and the Credit Earned, Course and correct the record if in error.  
 
 
 
 
 
 
 
 
 
 
 
 
 
  
  
 
Student Database 202 6-2027 /  EXCEPTION REPORTS  
UPDATED 7/1/2026  

### 84. If the Course Number is not one of those listed below, the Credit Attempted, Course must be less than or 
equal to 100.  
## Exception Reports

Basic Education Courses Offering Multiple Credit:  
 
1000412 1000414 1000416 1000418 1002380 1002381 0500370  
1200400 1400340  1302355  
 
Vocational Courses Offering Multiple Credit:  
 
8100100 8100410 8200420 8200410 8200100 8300420  
8400100 8400410 8500100 8500410 8700100 8700400  
8800100 8800410 8900100 8900410 8900420 8200400 8200430  
8300100 8300430 8501000 8501420  
8601420 8601800 8601900 8603000 8800420 8901000 9000420  
9001820 9001920 9009200 9200420 9201000 9500420  
9603110 9603120 9603130 9603140 9603150 9603160 9603170  
9603180 9700420 9701000 8801000 8905190 9000100 9501000  
E91010A E91010C E91010K E91010B E91010E E91010X E91010S  
E91010F E91010G E91010H E91010N E91010D E91010Y E91010L  
E91010J E91010M E91010T  9601100 9601200 9601300 9601400  
9601500  
 
Exceptional Education Courses Offering Multiple Credit:  
 
7915010 7912070 7915015 7915020 7919010 7912065  
7910120 7912080 7910125 7912095 7912075 7912090  
7910130 7910135 7921027 7921330 7920011 7920015  
7920020 7920025 7920022 7920050 7921020 7921015  
7921025 7960010 7963010 7963130  
7965010 7963140 7967020 7963070 7963040 7965030  
7963090 7963050 7965040 7963080 7963060 7967010  
7963150 7963160 7963170 7963180 7967025 7967015  
7980110 7980120 7980040 7980150 7980130 7980190  
7912120 7921031 7921032 7921033  7921023 7921024  
7921050  
 
EXAMPLE  
The third record listed below would pass this edit. The first and second records would not pass this edit 
because Credit Attempted, Course is greater than 100 and the Course Number is not one of the 
exceptions.  
 
  
 
Student Database 202 6-2027 /  DISTRICT RESPONSIBILITY  
The district should verify the Credit Attempted, Course submitted and correct the records if in error.  
  
  
 
Student Database 202 6-2027 /   
## Exception Reports

UPDATED 7/1/2026  

### 85. If the Course Number is not one of those listed below, the Credit Earned, Course must be less than or 
equal to 100.  
## Exception Reports

Basic Education Courses Offering Multiple Credit:  
 
1000412 1000414 1000416 1000418 1002380 1002381 0500370 1200400 1400340  1302355  
 
Vocational Courses Offering Multiple Credit:  
 
8100410 8100100 8200420 8200100 8200400 8200410 8200430 8300100 8300420 8300430 8400100 
8500410 8500100 8501000 8501420 8601420 8601800 8601900 8603000 8700100 8700400 8800100 
8800410 8800420 8900100 8900410 8900420 8901000 8905190 9000100 9000420 9001820 9001920 
9009200 9200420 9201000 9500420 9603110 9603120 9603130 9603140 9603150 9603160 9603170 
9603180 9700420 9701000 8801000 8905190 9000100 9501000 E91010A E91010C E91010K E91010B 
E91010E E91010X E91010S E91010F E91010G E91010H E91010N E91010D E91010Y E91010L E91010J 
E91010M E91010T 9601100 9601200  9601300 9601400 9601500  
 
Exceptional Education Courses Offering Multiple Credit:  
 
 7915010 7912075 7912080 7910125 7910130 7919010 7921330 7912090 7920011 7910135 7920050 
7912065 7960010 7963010 7963130 7912095 7980120 7915015 7965010 7910120 7980130 7920025 
7921015 7912070 7963040 7965030 7980040 7980150 7921027 7915020 7963050 7965040  7920022 
7980190 7921025 7920015 7920020 7921020 7963060 7921021 7921022 7967015 7963140 7967020 
7963070 7963160 7963170 7963080 7963180 7963090 7963150 7967025 7967010 7980110 7912120 
7921031 7921032 7921033  7921023 7921024  7921050  
 
EXAMPLE  
The third record listed below would pass this edit. The first and second records would not pass this edit 
because Credit Earned, Course is greater than 100 and the Course Number is not one of the exceptions.  
Course Number  Credit Attempted, Course  Credit Earned, Course  
* 7921060  100 200 
* 7920060  100 150 
8100410  200 200 

**District Responsibility:** The district should verify the Credit Earned, Course submitted and correct the records if in error.