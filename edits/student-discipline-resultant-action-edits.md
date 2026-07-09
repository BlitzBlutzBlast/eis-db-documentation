# Student Discipline Resultant Action — Edits and Reject Rules

Source: Florida DOE
Manual: Student Database 2026-2027

STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  
UPDATED 07/01/2026  

### 1. District Number, Current Enrollment must be numeric, active (A) on the Appendix C: District Name Table  
and must be correct for the district submitting the data.   
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected since the District Number, Current Enrollment is 
not active (A) on the Appendix C: District Name Table.  
District Number, Current 
Enrollment  School Number, Current 
Enrollment  Florida Education 
Identifier  
01 0021  FL123456789100  
01 0021  FL123456789200  
* 00  0021  FL123456789300  

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district should correct the 
District Number, Current Enrollment and resubmit th e record.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 2. School Number, Current Enrollment must be numeric in the range 0001 to 9899, excluding 9001 and 
7006, or it must be N998 or N999.   
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rules would 
cause their rejection. The last two records would be rejected. The first of these would be rejected 
because the School Number, Current Enrollment is not  in the appropriate numerical range. The second 
of these two records would be rejected because the School Number, Current Enrollment is not numeric.  
District Number, Current 
Enrollment  School Number, Current 
Enrollment  Florida Education 
Identifier  
01 0021  FL123456789100  
01 0021  FL123456789200  
* 01  9999  FL123456789300  
* 01  C901  FL123456789400  

**District Responsibility:** If the rejected records should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected records to be loaded to the database, the district should correct the 
School Number, Current Enrollment and resubmit th e records.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 4. Survey Period Code must be 2, 3 or 5 and must be correct for the submission specified by the district.   
**Result:** Record rejected
EXAMPLE  
The Survey Period Code as specified in the transmission JCL or in statements for tape transmission is 
identified as Survey Period "5". However, records on the transmission have a Survey Period Code "1". All 
updates, adds or deletes with this inconsistency would be rejected.   

**District Responsibility:** The district must correct Survey Period Code either on the records coming in or the Transmission JCL and 
all records must be submitted.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 5. School Year must be correct for the submission specified by the district.   
**Result:** Record rejected
EXAMPLE  
The School Year as specified in the transmission JCL or in statements for tape transmission is identified as 
the valid year for data submission. However, records on the transmission have the previous School Year 
coded. All updates, adds or deletes with thi s inconsistency will be rejected.  

**District Responsibility:** The district must correct the School Year either on the records coming in or the transmission JCL and 
resubmit all the records.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 6. The Discipline/Resultant Action Code must be alphabetic and must be C, E, F, H, I, N, O, P , S or U.   
**Result:** Record rejected
EXAMPLE  
The third record listed below would be loaded to the database assuming no other reject rule would 
cause its rejection. The first two records below would be rejected because the Discipline/Resultant 
Action code is invalid.  
District Number, Current Enrollment  Florida Education Identifier  Discipline/Resultant Action Code  
* 40  FL123456789100  B 
* 40  FL123456789200  W 
40 FL123456789300  C 

**District Responsibility:** If the rejected records should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected records to be loaded to the database, the district should correct the 
Discipline/Resultant Action Code and resubmit the  records.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 7. Each Student Discipline/Resultant Action record must be unique based on the keys of District Number, 
Current Enrollment; Florida Education Identifier; Discipline/Resultant Action Code; School Number, 
Where Discipline/Resultant Action Occurred; Incident, Id entifier; Survey Period Code and School Year.   
**Result:** Record rejected
EXAMPLE  
The first, third and fourth records listed below would be loaded to the database assuming no other 
reject rule would cause their rejection. The second and fifth records would be rejected since they are 
duplicates of the first and fourth records, respective ly (same District Number, Current Enrollment; Florida 
Education Identifier; Discipline/Resultant Action Code; School Number, Where Discipline/Resultant 
Action Occurred; Incident, Identifier; Survey  Period Code; and School Year).  
District 
Number, 
Current 
Enrollment  Florida Education 
Identifier  Discipline/Resultant 
Action Code  Survey 
period 
Code  School 
Number 
Where 
Discipline 
Resultant 
Action 
Occurred  School 
Year  Incident, 
Identifier  
02 FL123456789100  C 5 0211  ****  A0012345  
* 02  FL123456789100  C 5 0211  ****  A0012345  
02 FL123456789200  O 5 0211  ****  C2345678  
02 FL123456789300  I 5 0211  ****  D9876543  
* 02  FL123456789300  I 5 0211  ****  D9876543  
  
**** = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected records should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must delete any invalid 
records, correct any rejected records if nec essary, and resubmit the corrected records.  
    
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 8. The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent 
batch/update submissions, if A is specified then the record must not already exist on the database; if C 
or D is specified then the record must exist on the database.   
**Result:** Record rejected
EXAMPLE  
For all original transmissions, the Transaction Code must be "A". An original transaction is the first 
submission of a record during a survey period. After the original transmission of records, changes to the 
record for elements other than the key elements  must be done with a "C" as the Transaction Code. To 
delete a record, the Transaction Code must be a "D". To change key elements in a batch transaction, the 
record must FIRST be deleted with a "D" and then added with an "A".  Records with an incorrect 
Tran saction Code would be rejected.  

**District Responsibility:** If the rejected records should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected records to be loaded to the database, the district should correct the 
Transaction Code and resubmit the records.   
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 9. Incident, Identifier must be alphanumeric, may not be zero, and must not contain blanks.   
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be rejected. The first record would be rejected because the 
Incident, Identifier code is all zeroes. The second record would be rejected because the Incident, 
Identifier code contains leading blanks. The third recor d would be loaded to the database assuming no 
other edit caused it to be rejected.  
District Number, Current Enrollment  Florida Education Identifier  Incident, Identifier  
* 01  FL123456789100  00000000  
* 01  FL123456789200  46 
01 FL123456789400  00000045  

**District Responsibility:** If the rejected records should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
Incident, Identifier and resubmit the records.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 10. Incident, Date must be numeric, must be a valid date, in the range of 07/01/**** to 08/31/**** and not 
greater than the last day of the survey period.   
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because the Incident, Date is greater than the last day 
of the survey period. The third record would be rejected because Incident, Date is not a valid date.  
District Number, Current 
Enrollment  Survey 
Period Code  School Number, Where 
Incident Occurred  Incident, 
Identifier  Incident, 
Date  
01 03 0271  A0000001  0122****  
* 01  03 0271  X0000002  0308****  
* 01  03 0271  D0000003  0230****  
  
**** = Valid year for data submission.  

**District Responsibility:** If the rejected records should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
Incident, Date and resubmit the records.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 11. The Duration, Discipline Action must be a three -digit  numeric code indicating length of Discipline action.   
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because Duration, Discipline Action is not a 
valid code.  
District Number, Current 
Enrollment  School Number, Current 
Enrollment  Florida Education 
Identifier  Duration Discipline 
Action  
01 0271  FL123456789100  008 
01 0271  FL123456789200  001 
* 01  0271  FL123456789300  C01 

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Duration, Discipline Action code and resubmit the rec ord.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 12. Item 3 - Filler on this format in position numbers 7 -16 must be all spaces.   
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because the data reported is not all spaces.  
  
District Number,  
Current Enrollment  School Number,  
Current Enrollment  Filler,  
Item #3  
01 0151   
* 01  0151  265456789X  

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must fill the positions 
noted with all spaces and resubmit the record.   
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 13. Student, Involved in Hate Crime code must be Y or N.   
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Student, Involved in Hate Crime 
code is not a valid code.  
School Number, District Number, 
Current Enrollment  Where Incident 
Occurred  Student Incident 
Identifier  Involved in Hate 
Crime  
01 0271  00000001  Y 
01 0271  00000002  N 
* 01  0271  00000003  Z 

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Student, Involved in Hate Crime code and resubmit the  record.  
  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 14. Student, Use of Alcohol code must be Y or N.   
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Student, Use of Alcohol code is not 
a valid code.  
District Number, Current 
Enrollment  School Number, Where 
Incident Occurred  Incident, 
Identifier  Student, Use of 
Alcohol  
01 0271  00000001  Y 
01 0271  00000002  N 
* 01  0271  00000003  Z 

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Student, Use of Alcohol code and resubmit the record.   
  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 15. Student, Use of Drugs code must be Y or N.   
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Student, Use of Drugs code is not a 
valid code.  
 
District Number, Current 
Enrollment  School Number, Where Incident 
Occurred  Incident, 
Identifier  Student, Use of 
Drugs  
01 0271  A0000001  Y 
01 0271  B0000002  N 
* 01  0271  C0000003  Z 

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Student, Use of Drugs code and resubmit the record.   
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 16. Student, Weapon Use code must be Y or N.   
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Student, Weapon Use code is not a 
valid code.  
 
District Number, Current 
Enrollment  School Number, Where Incident 
Occurred  Incident, 
Identifier  Student, Weapon 
Use 
01 0271  00000001  Y 
01 0271  00000002  N 
* 01  0271  00000003  Z 

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Student, Weapon Use code and resubmit the record.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 17. If the Discipline/Resultant Action code is C or N, then Duration, Discipline Action must be zero.  
**Result:** Record rejected
EXAMPLE  
The first and third records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. The second record would be rejected because the Duration, Discipline 
Action is greater than zero.         
District Number, Current 
Enrollment  Florida Education 
Identifier  Discipline Resultant 
Action Code  Duration, Discipline 
Action  
36 FL123456789100  C 000 
* 36  FL123456789200  C 010 
36 FL123456789300  E 090 

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Duration, Discipline Action or the Discipline/Resulta nt Action Code and resubmit the record.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 18. If the Discipline/Resultant Action code is O, then Duration, Discipline Action must be greater than zero 
and less than or equal to 10.  
**Result:** Record rejected
EXAMPLE  
The first and third records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. The second record would be rejected because the Duration, Discipline 
Action is greater than 10.  
 
District Number, Current 
Enrollment  Florida Education 
Identifier  Discipline Resultant 
Action Code  Duration, Discipline 
Action  
36 FL123456789100  O 008 
* 36  FL123456789200  O 020 
36 FL123456789300  O 010 

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Duration, Discipline Action or the Discipline/Resulta nt Action Code and resubmit the record.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 19. If the Discipline/Resultant Action code  is I, then Duration, Discipline Action must be greater than zero 
and less than or equal to 10.  
**Result:** Record rejected
EXAMPLE   
The first and third records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. The second record would be rejected because the Duration, Discipline 
Action is greater than 10.  
 
District Number, Current 
Enrollment  Florida Education 
Identifier  Discipline Resultant 
Action Code  Duration, Discipline 
Action  
36 FL123456789100  I 004 
* 36  FL123456789200  I 012 
36 FL123456789300  I 010 

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Duration, Discipline Action or the Discipline/Resulta nt Action Code and resubmit the record.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 20. If the School Number, Current Enrollment is not N998 or N999, then it must exist on the Master School 
Identification File as a valid active school number in the district of enrollment.   
**Result:** Record rejected
EXAMPLE   
The record listed below would be rejected because the School Number, Current Enrollment is not valid 
and active on the Master School Identification File for the District Number, Current Enrollment.  
District Number, Current 
Enrollment  School Number, Current 
Enrollment  Florida Education 
Identifier  
* 01  0351  FL123456789100  

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district should correct the 
School Number, Current Enrollment and resubmit the record.   
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 21. The School Number, Where Discipline/Resultant Action Occurred must exist on the Master School 
Identification File as a valid active school number in the district of enrollment.   
**Result:** Record rejected
EXAMPLE  
The record listed below would be rejected because the school number (last four positions of 
Discipline/Resultant Action Code) is not valid and active on the Master School Identification File for the 
District Number, Current Enrollment.  
 
District Number, Current 
Enrollment  Florida Educator Identifier  School Number, Where 
Discipline/Resultant Action 
Occu rred  
* 40  FL123456789100  0112  

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district should correct the 
School Number, Where Discipline/Resultant Action Oc curred and resubmit the record.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RECORD  

### 22. If the Discipline/Resultant Action code is S, the Duration, Discipline Action must be equal to or greater 
than zero and less than or equal to 90.    
**Result:** Record rejected
EXAMPLE   
The first and third records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. The second record would be rejected because the Duration, Discipline 
Action is not equal to or great than zero and less than  or equal to 90.  
 
District Number, Current 
Enrollment  Florida Education 
Identifier  Discipline Resultant 
Action Code  Duration, Discipline 
Action  
36 FL123456789100  S 004 
* 36  FL123456789200  S Blank  
36 FL123456789300  S 012 

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Duration, Discipline Action or the Discipline/Resulta nt Action Code and resubmit the record.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 23. Birth Date must be numeric and a valid date in the format MMDDYYYY .   
**Result:** Record rejected
EXAMPLE  
Each of the records listed below would be rejected. The first record would be rejected because Birth 
Date is not numeric; the second record would be rejected because Birth Date is an invalid date.  
Florida Education Identifier  Survey Period Code  Year  Birth Date  
* 123456789100  2 ****  ZZZZZZZZ  
* 123456789200  2 ****  02301985  
 
**** = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected records should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Birth 
Date and resubmit the records.   
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 24. Sex code must be M or F.   
**Result:** Record rejected
EXAMPLE  
The records listed below would be rejected. The first record would be rejected because the sex code is 
not M or F. The second record would be rejected because sex code was left blank.  
Florida Education Identifier  Sex 
*FL123456789100  Z 
*FL123456789200   

**District Responsibility:** If the rejected records should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the sex 
code and resubmit the records.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  
UPDATED 07/01/2026  

### 25. District Number, Where Incident Occurred must be numeric  and active (A) on the Appendix C: District 
Name Table.  
**Result:** Record rejected
EXAMPLE  
In the records listed below, the first two records would be loaded to the database assuming no other 
reject rule would cause their rejection. The third record would be rejected because the District Number, 
Where Incident Occurred is not active (A) on the Appendix C: District Name Table.  
 
District Number, Where Incident 
Occurred  School Number, Where Incident 
Occurred  Incident, 
Identifier  
01 0271  A0000001  
37 0531  A0000002  
* 70  0011  D0000003  

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the District 
Number, Where Incident Occurred and resubmit  the records.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 26. English Language Learners, PK -12 code must be LA, LY , LF, LP , LZ, or ZZ.   
**Result:** Record rejected
EXAMPLE  
The records listed below would be rejected. The first record would be rejected because the English 
Language Learners, PK -12 code is not valid. The second record would be rejected because the English 
Language Learners, PK -12 code was left blank.  
Florida Education Identifier  English Language Lea rners, PK -12 
*FL123456789100   
*FL123456789200  00 

**District Responsibility:** If the rejected records should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
English Language Learners, PK -12 codes and resubmit  the records.   
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 27. Lunch Status Must be 0, 1, 3, 4, C, D, E, F, N or R.   
**Result:** Record rejected
EXAMPLE  
Both records listed below would be rejected because the Lunch Status codes are invalid.  
District Number, Current 
Enrollment  Florida Education 
Identifier  Survey Period 
Code  Lunch 
Status  
* 01  FL123456789100  2 5 
* 01  FL123456789200  2 K 

**District Responsibility:** If the rejected records should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Lunch 
Status codes and resubmit the records.   
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 28. Birth Date must be less than or equal to the survey date.   
**Result:** Record rejected
EXAMPLE   
If the survey week for the records listed below were October 8 -12, 2002, the first record would be 
rejected because the Birth Date is not less than the Survey Date. The second and third records would be 
loaded to the database assuming no other reject rule would cause their rejection.  
Florida Education Identifier  Survey Period Code  Year  Birth Date  
*FL123456789100  2 ****  11042002  
FL124356789200  2 ****  03121991  
FL123456789300  2 ****  08111992  
 
**** = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Birth 
Date and resubmit the record.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 29. If Survey Period Code = 2 or 3, Grade Level code must be PK, KG or 01 -12.  If  
Survey Period Code = 5, Grade Level code must be PK, KG or 01 -12.   
**Result:** Record rejected
EXAMPLE  
The records listed below would be rejected. The first record would be rejected because the Grade Level 
code is invalid. The second record would be rejected because the Grade Level code was left blank.  
 
Florida Education Identifier  Grade level  
* FL123456789100  K 
* FL123456789200   

**District Responsibility:** If the rejected records should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Grade 
Level codes and resubmit the records.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RECORD  

### 2A. If the Discipline/Resultant Action code is U, the Duration, Discipline Action must be greater than zero and 
less than or equal to 45.   
**Result:** Record rejected
EXAMPLE  
The first and third records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. The second record would be rejected because the Duration, Discipline 
Action is greater than 45.  
 
District Number, Current 
Enrollment  Florida Education 
Identifier  Discipline/Resultant Action 
Code  Duration, 
Discipline Action  
36 FL123456789100  U 010 
* 36  FL123456789200  U 050 
36 FL123456789300  U 045 

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Duration, Discipline Action or the Discipline/Resulta nt Action Code and resubmit the record.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 2B. There must be a valid association between the Grade Level listed below and the student's age.  For 
Survey Periods 2 and 3, age will be determined as of Date Certain (Friday) of the survey period.  For 
Survey Period 5, age will be determined as of June 30.  
 
Grade Level  Age 
PK not equal to 9+  
KG not equal to 0 -3, 11+  
1 not equal to 0 -4, 12+  
2 not equal to 0 -4, 13+  
3 not equal to 0 -4, 14+  
4 not equal to 0 -4, 15+  
5 not equal to 0 -4, 16+  
6 not equal to 0 -4, 18+  
7 not equal to 0 -4, 19+  
8 not equal to 0 -4, 20+  
9 not equal to 0 -4, 27+  
10 not equal to 0 -4, 28+  
11 not equal to 0 -4, 29+  
12 not equal to 0 -4, 30+  
**Result:** Record rejected
EXAMPLE  
The records below without an asterisk would be loaded to the database assuming no other reject rule 
would cause their rejection. The records below which are marked with an asterisk would be rejected 
because of the invalid association between the Grade Leve l of the student and the student’s Birth Date.  
 
Florida Education  
Identifier   
Year  Grade  
Level  Birth  
Date  
* FL123456789100  0405  02 02021990  
FL123456789200  0405  08 05062003  
FL123456789300  0405  PK 12022003  
* FL123456789400  0405  12 08172014  

**District Responsibility:** STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  If the rejected records should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
students’ Grade Level or Birth Date and resubmit th e records.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 2C. If the Discipline/Resultant Action code is H, then Duration, Discipline Action must be greater than zero 
and less than or equal to 90.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second and third records would be rejected because the Duration, Discipline Action is 
equal to 0 or greater than 90.  
District Number, Current 
Enrollment  Florida Education 
Identifier  Discipline/Resultant Action 
Code  Duration, 
Discipline Action  
36 FL123456789100  H 008 
* 36  FL123456789200  H 000 
* 36  FL123456789300  H 103 

**District Responsibility:** If the rejected records should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
Duration, Discipline Action element or Discipline/R esultant Action code and resubmit the records.    
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 2D. The Student Number Identifier, Local may be any combination of letters, numbers and blanks. (All blanks 
are allowable.) It must be left -justified with trailing blanks.   
**Result:** Record rejected
EXAMPLE  
The first three records listed below would be loaded to the database assuming no other edit would 
cause their rejection. The fourth record would be rejected because the Student Number Identifier, Local 
contains a symbol (@). The fifth record would be rejec ted because it is right -justified rather than left -
justified.    
District Number, Current Enrollment  Student Number Identifier, Local  
01 0123456789  
01 ABC123DEF9  
01 3001  28K  
* 01  2121@xyz  
* 01  123456  

**District Responsibility:** If the rejected records should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
Student Number Identifier, Local and resubmit the r ecords.   
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 2F. School Number, Where Discipline/Resultant Action Occurred must be numeric and a valid school number 
in the range 0001 to 9899, excluding 9001.   
**Result:** Record rejected
EXAMPLE  
The third record listed below would be loaded to the database assuming no other reject rule would 
cause its rejection. The first two records below would be rejected because the School Number, Where 
Discipline/Resultant Action Occurred is invalid.  
District Number, Current 
Enrollment  Florida Education 
Identifier  School Number, Where Discipline/Resultant 
Action Occurred  
*40 FL123456789100  C201  
*40 FL123456789200  9999  
40 FL123456789300  0021  

**District Responsibility:** If the rejected records should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected records to be loaded to the database, the district should correct the 
School Number, Where Discipline/Resultant Action Occurred and resubmit the records.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 2G. Student, Involved in Bullying must be Y or N.   
**Result:** Record rejected
EXAMPLE   
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because Student, Involved in Bullying is not a 
valid code.  
District Number, Current 
Enrollment  School Number, Current 
Enrollment  Incident, 
Identifier  Student, Involved in 
Bullying  
01 0271  00000001  Y 
01 0271  00000002  N 
* 01  0271  00000003  Z 

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Student, Involved in Bullying code and resubmit the r ecord.   
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 2H. School Number, Where Incident Occurred must be numeric in the range 0001 – 9899.   
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the School Number, Where Incident 
Occurred is not in the appropriate numerical range. T he fourth record would be rejected because the 
School Number, Where Incident Occurred is not numeric.  
District Number, Current 
Enrollment  School Number, Where Incident 
Occurred  Florida Education 
Identifier  
01 0271  FL123456789100  
01 0271  FL123456789200  
* 01  9999  FL123456789300  
* 01  C901  FL123456789400  

**District Responsibility:** If the rejected records should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the School 
Number, Where Incident Occurred and resubmit  the records.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 2I. School Number, Where Incident Occurred must exist on the Master School Identification File as a valid 
active school in the District Number, Current Enrollment.   
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the School Number, Where Incident 
Occurred is not a valid active school number for the district.  
District Number, Current 
Enrollment  School Number, Where Incident 
Occurred  Florida Education 
Identifier  
01 0271  FL123456789100  
01 0271  FL123456789200  
* 01  0062  FL123456789300  

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the School 
Number, Where Incident Occurred and resubmit t he record.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 2J. Zero -Tolerance:  Expulsions code must be Y , N or Z.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Zero -Tolerance:  Expulsions code is 
not a valid code.    
  
District Number, Current Enrollment  Florida Education Identifier  Zero -Tolerance: Expulsion s 
01 FL123456789100  Y 
01 FL123456789200  Z 
* 01  FL123456789300  G 

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Zero -
Tolerance:  Expulsions code and resubmit the rec ord.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 2K. If the Zero -Tolerance : Expulsions  code is Y or N, then Discipline/Resultant Action Code must be E, F or U.  
If the Discipline/Resultant Action Code is E, F or U then the Zero -Tolerance : Expulsions  code must be Y or 
N.   
**Result:** Record rejected
EXAMPLE  
The first and second records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. The third record would be rejected because the Discipline/Resultant Action 
code is not E, F or U.  
 
District Number, 
Current Enrollment  Florida Education 
Identifier  Zero -Tolerance: 
Expulsions Code  Discipline/Resultant 
Action Code  
36 FL123456789100  Y F 
36 FL123456789200  N U 
*36 FL123456789300  Y O 

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Discipline/Resultant Action Code or the Zero -Toleranc e: Expulsions  code and resubmit the record.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  REJECT RULES  

### 2L. Florida Education Identifier (FLEID) is alphanumeric and must be entered as “FL” in the first 2 positions 
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
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  STATE VALIDATION  RULES  

### 31. For surveys 2 and 3, each Student Discipline/Resultant Action record must have a matching Student 
Demographic record based on District Number, Current Enrollment; Florida Education Identifier; Survey 
Period Code and School Year unless School Number/Current  Enrollment is N998 or N999. For survey 5, 
each Student  
Discipline/Resultant Action record must have a matching Student Demographic and  
Student End of Year Status record based on District Number, Current Enrollment; Florida Education 
Identifier; Survey Period Code and School Year unless School Number/Current Enrollment is N998 or 
N999.          
## State Validation

EXAMPLE  
The first two records below would not pass this edit because they do not have matching Student 
Demographic records. The third record below would pass this edit because there is a matching Student 
Demographic Information record.    
  
 Student Discipline/Resultant Action   
District Number, Current Enrollment  Florida Education Identifier  Survey Period Code  School Year  
* 01  FL123456789100  5 ****  
* 01  FL123456789200  2 ****  
01 FL123456789300  2 ****  
  
District Number, Current Enrollment  Florida Education Identifier  Survey Period Code  School Year  
* 01  FL123456789100  5 ****  
* 01  FL123456789200  2 ****  
01 FL123456789300  2 ****  
   
Student Demographic Information    
District Number, Current Enrollment  Florida Education Identifier  Survey Period Code  School Year  
01 FL123456789300  2 ****  

**District Responsibility:** The district must delete the Student Discipline/Resultant Action records or add matching Student 
Demographic Information records.  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  STATE VALIDATION RULES  

### 33. If the Student, Use of Drugs code is Y , then the Drug Description code on the matching Student 
Environmental Safety Incident Report (SESIR) format must be M, N, O or P . The records match is done 
using the District Number, Current Enrollment on the Student Discipline/Resultant Action format 
matched to the District Number,   
Where Incident Occurred on the SESIR format; along with matching School Year, Survey Period Code and 
Incident, Identifier.     
## State Validation

EXAMPLE  
The first and third records listed below would meet the criteria specified in the edit above. The second 
record would cause a message to be generated because the Drug Description code is incorrect for the 
Student, Use of Drugs code reported.  
  
 Student Discipline/Resultant Action Records  
District Number, Current 
Enrollment  Florida Education 
Identifier  Incident, 
Identifier  Student Use of, 
Drugs  
36 FL123456789100  0000001  Y 
* 36  FL123456789200  0000002  Y 
36 FL123456789300  0000003  Y 
  
School Environmental Safety Incident Report (SESIR) Records   
District Number, Where 
Incident Occurred  School Number, Where 
Incident Oc curred  Incident, 
Identifier  Drug 
Description  
36 0271  00000001  M 
* 36  0271  00000002  Z 
36 0271  00000003  M 

**District Responsibility:** The district should review the Student, Use of Drugs code and the Drug Description code and correct the 
code that is in error.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  STATE VALIDATION RULES  

### 34. If Incident, Weapon -Related code on the School Environmental Safety Incident Report  is 1, 2, 3 or 4, then 
Student, Weapon Use may be Y or N. If Incident, Weapon  Related code is N, then Student, Weapon Use 
code must be N.  
The records should match on District Number, Current Enrollment on the Student Discipline Resultant 
Action record and District Number, Where Incident Occurred on the School Environmental Safety 
Incident Report record; Survey Period Code; School Year; Incid ent Identifier; and Incident Date.   
## State Validation

EXAMPLE  
The first two records below would pass the edit above. The third record below would fail the edit 
because the Incident, Weapon -Related code is N and the Incident, Student, Weapon Use is coded Y .  
  
 Records   
District Number, Current Enrollment  Incident, Identifier  Incident, Date  Student Weapon, Use  
01 C0000121  1211****  N 
01 C0000122  1106****  Y 
* 01  C0000123  1022****  Y 
  
School Environmental Safety Incident Report Records  
District Number, Where Incident 
Occurred  Incident, 
Identifier  Incident, 
Date  Incident Weapon -
Related  
01 C0000121  1211****  1 
01 C0000122  1106****  2 
* 01  C0000123  1022****  N 
  
**** represents a valid year for the data.    

**District Responsibility:** The district must review the Student, Weapon Use and Incident, Weapon -Related codes and correct the 
one that is in error by submitting a change to the incorrect record.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  STATE VALIDATION RULES  

### 35. If Survey = 2 or 3 and if the Discipline/Resultant Action code is E, then Withdrawal Code, PK -12 on at 
least one Prior School Status/Student Attendance (PSS/SA) record must = W21. If Survey = 5 and if the 
Discipline/Resultant Action code is E, then the Wit hdrawal Code, PK -12 on at least one PSS/SA record 
must = W21.  
The records should be matched on the following items: District Number, Current Enrollment; Florida 
Education Identifier; Survey Period Code; and School Year.     
## State Validation

EXAMPLE  
The first record listed below would meet the criteria specified in the edit above.  The second record 
would cause a message to be generated because the Discipline/Resultant Action Code = E, the Survey 
Period = 5, but  the Withdrawal Code, PK -12 does not equal W21.    
    
Student Discipline/Resultant Action  
District Number, Current 
Enrollment  Florida Education 
Identifier  Discipline/Resultant Action 
Code  Survey 
Period  
36 FL123456789100  E 5 
* 36  FL123456789200  E 5 
 
Prior School Status/Student Attendance  
District Number, Current 
Enrollment  Florida Education 
Identifier  Withdrawal Code, PK -
12 Survey 
Period  
36 FL123456789100  W21  5 
* 36  FL123456789200  W3A  5 

**District Responsibility:** The district should review the Discipline/Resultant Action code and the Withdrawal Code, PK -12 and 
correct the code that is in error.  
    
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  STATE VALIDATION RULES  

### 36. If the Discipline/Resultant Action code is E, then there must not be a matching Exceptional Student 
record unless the Exceptionality, Primary = L (Gifted) and Exceptionality, Other = Z. The match should be 
done on District Number, Current Enrollment; Surve y Period Code; School Year matched to Year and 
Florida Education Identifier.  
## State Validation

EXAMPLE  
The first record listed below would pass the edit above. The second record would cause a message to be 
generated because the Discipline/Resultant Action Code = E and the student is a student with a disability 
(exceptionality code other than L).    
    
Student Discipline/Resultant Action Records   
District Number, Current 
Enrollment  Florida Education 
Identifier  Discipline/Resultant Action 
Code  Survey 
Period  
36 FL123456789100  E 5 
* 36  FL123456789200  E 5 
  
Exceptional Student Records  
District Number, 
Current Enrollment  Florida Education 
Identifier  Exceptionality, 
Primary  Exceptionality, 
Other  Survey 
Period  
36 FL123456789100  L Z 5 
* 36  FL123456789200  J L 5 

**District Responsibility:** The district should review the Discipline/Resultant Action code, the Exceptionality, Primary and the 
Exceptionality, Other and correct the code that is in error.    
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  STATE VALIDATION RULES  

### 37. If Student, Weapon Use on the  format = Y , then Weapon, Description 
on the School Environmental Safety Incident Report format must not = Z.  
The records should match on District Number, Current Enrollment on the Student Discipline Resultant 
Action record and District Number, Where Incident Occurred on the School Environmental Safety 
Incident Report record; School Number, Where Incident Occurred  on the SESIR format matched to 
School Number, Where Discipline/Resultant Action Occurred on the SDRA format; Survey Period Code;  
School Year; Incident Identifier; and Incident Date.   
## State Validation

EXAMPLE  
The first record below would pass the edit above. The second record below would fail the edit because 
Student, Weapon Use is coded Y and the matching School Environmental Safety Incident Report record  
Weapon, Description code is Z.  
 
 Records   
District Number, 
Current Enrollment  School Number, Where 
Discipline/Resultant Action 
Occurred  Incident, 
Identifier  Incident, 
Date  Student 
Weapon, Use  
01 0021  0121  1211****  Y 
* 01  0021  0121  1022****  Y 
  
School Environmental Safety Incident Report Records   
District Number, 
Current Enrollment  School Number, Where 
Discipline/Resultant Action 
Occurred  Incident, 
Identifier  Incident, 
Date  Weapon, 
Description  
01 0021  0121  1211****  F 
*01 0021  0121  1022****  Z 
**** represents a valid year for the data.  

**District Responsibility:** The district must review the Student, Weapon Use and Weapon, Description codes and correct the one 
that is in error by submitting a change to the incorrect record.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  STATE VALIDATION RULES  

### 38. If the Discipline/Resultant Action code is U, then there must be a matching Exceptional Student record 
with   
• Exceptionality, Primary not equal to L or with Exceptionality, Primary = L (Gifted) and Exceptionality, 
Other not equal to Z, and •  an Exceptional Student, Dismissal Date of zero or an Exceptional Student, 
Dismissal Date that is greater than (after) the Incident Date, and   
• an Exceptional Student, Placement Date that is less than or equal to the Incident Date.    
The match should be done on District Number, Current Enrollment; Florida Education Identifier; Survey 
Period Code; and School Year matched to Year.         
## State Validation

EXAMPLE  
The first record listed below would pass this edit. The second record would cause a message to be 
generated because the Discipline/Resultant Action Code is U and the student is not a student with a 
disability (exceptionality code other than L).    
  
Student Discipline/Resultant Action Records  
District Number, Current 
Enrollment  Florida Education 
Identifier  Discipline/Resultant Action 
Code  Survey 
Period  
36 FL123456789100  U 5 
* 36  FL123456789200  U 5 
  
Exceptional Student Records   
District Number, 
Current Enrollment  Florida Education 
Identifier  Exceptionality, 
Primary  Exceptionality, 
Other  Survey 
Period  
36 FL123456789100  J Z 5 
* 36  FL123456789200  L Z 5 

**District Responsibility:** The district should review the Discipline/Resultant Action code, the Exceptionality, Primary and the 
Exceptionality, Other and correct the item that is in error.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  STATE VALIDATION RULES  

### 39. If the Discipline/Resultant Action Code is U, then one of the following must be true:  
a. Student, Use of Drugs must be Y; or b. Student, Weapon Use must be Y; or  
c. there is a matching School Environmental Safety Incident Report (SESIR) record with an Incident, 
Injury -Related code of A or B.  
The records should match on District Number, Current Enrollment on the Student Discipline Resultant 
Action (SDRA) record and District Number, Where Incident Occurred on the SESIR record; School 
Number, Where Incident Occurred on the SESIR format matched to  School Number, Where 
Discipline/Resultant Action Occurred on the SDRA format; Survey Period Code; School Year; Incident 
Identifier; and Incident Date.    
## State Validation

EXAMPLE  
The first record below would pass the edit above. The second record below would fail the edit because 
the Discipline/Resultant Action Code is U and none of the three conditions are true. The Student, Use of 
Drugs code is not Y . The Student, Weapon Use code  is not Y . The Incident, Injury -Related code is not A or 
B on the matching School Environmental Safety Incident Report record.  
 
 Records   
District 
Number, 
Current 
Enrollment  School Number 
Where 
Discipline/Resultant 
Action Occurred  Incident 
Identifier  Incident 
Date  Discipline/Resultant 
Action  Code  Student 
Use of 
Drugs  Student 
Weapon 
Use 
01 0021  0121  1211****  U Y N 
* 01  0021  0325  1022****  U N N 
  
School Environmental Safety Incident Report Records   
District Number, 
Current Enrollment  School Number Where 
Incident Occurred  Incident 
Identifier  Incident, 
Date  Incident, Injury -
Related  
01 0021  0121  1211****  Z 
* 01  0021  0325  1022****  Z 
  
**** represents a valid year for the data.  

**District Responsibility:** STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  The district must review the Discipline/Resultant Action Code; Student, Use of Drugs code; Student, 
Weapon Use code and the Incident, Injury -Related code and correct the one that is in error by 
submitting a change to the incorrect record.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  STATE VALIDATION RULES  

### 3A. If Discipline/Resultant Action Code on the Student Discipline/Resultant Action format = S, then there 
must be a matching record on the School Environmental Safety Incident Report (SESIR) format.   
The records should match on District Number, Current Enrollment on the Student Discipline Resultant 
Action [SDRA] record and District Number, Where Incident Occurred on the School Environmental Safety 
Incident Report [SESIR] record; School Number, Where In cident Occurred on the SESIR format matched 
to School Number, Where Discipline/Resultant Action Occurred on the SDRA format; Survey Period Code; 
School Year; Incident Identifier; and Incident Date.    
## State Validation

EXAMPLE  
The first record below would pass the edit above. The second record below would fail the edit because 
Discipline/Resultant Action Code = S and there is no matching School Environmental Safety Incident 
Report record.  
  
Student Discipline/Resultant Action Records  
District Number, 
Current 
Enrollment  School Number Where 
Discipline/Resultant Action  
Occurred  Incident 
Identifier  Incident, 
Date  Discipline/Resultant 
Action Code  
01 0021  0121  1211****  S 
* 01  0021  0122  1022****  S 
  
School Environmental Safety Incident Report Records     
District Number, Current 
Enrollment  School Number Where Incident 
Occurred  Incident 
Identifier  Incident, 
Date  
01 0021  0121  1211****  
 **** represents a valid year for the data.  

**District Responsibility:** The district must determine if the Student Discipline/Resultant Action record is in error or if a School 
Environmental Safety Incident Report record should be added and respond with the appropriate action.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  EXCEPTION REPORT  

### 40. If the Discipline/Resultant Action code is F or P , then Duration, Discipline Action must be greater than 
zero and less than or equal to 210.  
## Exception Reports

EXAMPLE  
The first and third records listed below would meet the criteria specified in the edit above. The second 
record would cause a message to be generated because the Duration, Discipline Action is greater than 

### 210. District Number, Current 
Enrollment  Florida Education 
Identifier  Discipline/Resultant Action 
Code  Duration, 
Discipline Action  
36 FL123456789100  P 050 
* 36  FL123456789200  P 365 
36 FL123456789300  F 210 

**District Responsibility:** The district should verify the Discipline/Resultant Action Code and the Duration, Discipline Action code 
and correct if in error.  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  EXCEPTION REPORT  

### 41. If the Discipline/Resultant Action code is E, then Duration, Discipline Action must be greater than zero 
and less than or equal to 210.   
## Exception Reports

EXAMPLE  
The first and third records listed below would meet criteria specified in the edit above. The second 
record would cause a message to be generated because the Duration, Discipline Action is greater than 

### 210. District Number, Current 
Enrollment  Florida Education 
Identifier  Discipline/Resultant Action 
Code  Duration, 
Discipline Action  
36 FL123456789100  E 050 
* 36  FL123456789200  E 365 
36 FL123456789300  E 210 

**District Responsibility:** The district should verify the Discipline/Resultant Action Code and the Duration, Discipline Action code 
and correct if in error.    
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  EXCEPTION REPORT  

### 42. If Grade Level is KG -12, the student must be at least 5 years old on or before September 1 of the school 
year being reported.   
Note : Students  who transfer to Florida from states with different minimum starting ages are accepted 
into the grade into which they are transferring.  
## Exception Reports

EXAMPLE  
The record listed below would cause a message to be generated because Grade Level is KG and age is 
less than 5.  
 
Florida Education Identifier  Year  Survey Period Code  Grade Level  Birth Date  
*FL123456789100  1011  2 KG 02192009  

**District Responsibility:** The district should verify the Birth Date and Grade Level and correct one of these if there is an error.   
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  EXCEPTION REPORT  

### 44. If Survey Period Code is equal to 5, and Discipline/Resultant Action code is H, then there must be a 
matching Student Discipline/Resultant Action record with code E, F, or P . The match should be done 
using District Number, Current Enrollment; Florida Educa tion Identifier; School Number, Where  
Discipline/Resultant Action Occurred; Incident, Identifier, Survey Period Code; Incident Date; and School 
Year.   
## Exception Reports

EXAMPLE  
The first set of records listed below would meet the criterion specified in the edit above. The second set 
of records would cause a message to be generated because the Discipline/Resultant Action Code of H 
does not have a matching record with a Discipline/ Resultant Action Code of E, F, or P .  
  
Florida Education Identifier  Discipline/Resultant Action Code  Incident Identifier  
FL123456789100  E 12345678  
FL123456789200  H 12345678  
    
Florida Education Identifier  Discipline/Resultant Action Code  Incident Identifier  
* FL123456789100  H 23456781  
* FL123456789200  U 23456781  

**District Responsibility:** The district should verify the Discipline/Resultant Action Code of H and correct it if it is in error. If it is not 
in error, the district should submit a matching record with a Discipline/ Resultant Action Code of E, F or P , 
if appropriate.   
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  EXCEPTION REPORT  

### 45. If Survey = 5 and if the Discipline/Resultant Action code is E, then the Withdrawal Reason on the Student 
End of Year Status record must = W21.   
The records should be matched on the following items: District Number, Current Enrollment; Florida 
Education Identifier; Survey Period Code; and School Year  
## Exception Reports

EXAMPLE  
The first record listed below would meet the criteria specified in the edit above.  The second record 
would cause a message to be generated because the Discipline/Resultant Action Code = E, the Survey 
Period = 5, but the Withdrawal Reason does not equal W2 1.    
   
Student Discipline/Resultant Action   
District Number, Current 
Enrollment  Florida Education 
Identifier  Discipline/Resultant Action 
Code  Survey 
Period  
36 FL123456789100  E 5 
* 36  FL123456789200  E 5 
 
Student End of Year Status  
District Number, Current 
Enrollment  Florida Education 
Identifier  Withdrawal 
Reason  Survey 
Period  
36 FL123456789100  W21  5 
* 36  FL123456789200  W03  5 

**District Responsibility:** The district should review the Discipline/Resultant Action code and the Withdrawal Reason code and, if 
one is found to be in error, revise the incorrect code.  
  
  
  
  
STUDENT DISCIPLINE/RESULTANT ACTION  
Student Database 202 6-2027 /  AGGREGATE EXCEPTION  

### 60. If Survey Period is 5, for each district there must be at least one record with a Discipline/Resultant Action 
Code of E or F (expelled from school with or without services).  
Note : An error message will be printed on the exception report for districts that do not meet the 
aggregate exception edit above.    
## Exception Reports

EXAMPLE  
There are no records for District 01 (Alachua) with a Discipline/Resultant Action code of E or F in Survey 
Period 5 on the Student Database Student Discipline/ Resultant Action table. It is expected that the 
district will have at least one incidence of a s tudent being expelled during the school year.    
An aggregate exception error message is generated for District 01 on the exception report indicating that 
the district failed this aggregate exception edit.    

**District Responsibility:** The district must review official expulsion records for the year and submit any missing Student 
Discipline/Resultant Action records.