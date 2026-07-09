# Student Assessment — Edits and Reject Rules

Source: Florida DOE
Manual: Student Database 2026-2027

Student Database 202 6-2027 /  
## Reject Rules

UPDATED 07/01/2026   

### 1. District Number, Current Enrollment must be numeric, active (A) on the Appendix C: District Name Table  
and must be correct for the district submitting the data.   
**Result:** Record rejected
EXAMPLE   
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the District Number, Current 
Enrollment is not in the appropriate range.  The fourth re cord would be rejected if district 01 submitted 
the record.  
 
District Number, Current 
Enrollment  School Number, Current 
Enrollment  Florida Education Identifier  
01 0021  FL123456789100  
01 0021  FL123456789200  
* 00  0021  FL123456789300  
* 02  0021  FL123456789000  

**District Responsibility:** If the rejected records should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
District Number, Current Enrollment and resubmit th e records.  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 2. The School Number, Current Enrollment must exist on the Master School Identification File as a valid 
active school in the district of enrollment.   
**Result:** Record rejected
EXAMPLE  
The fourth and fifth records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. Records one, two and three would be rejected because the School Number, 
Current Enrollment does not exist on the Master Sch ool Identification File as a valid active school 
number for the District Number, Current Enrollment.  
 
District Number, Current Enrollment  School Number, Current Enrollment  
* 09  8131  
* 13  0009  
* 15  C999  
57 0051  
63 0021  

**District Responsibility:** If the rejected records should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
School Number, Current Enrollment and resubmit the records.  
  
    
  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 4. Survey Period Code must be 5 and must be correct for the submission specified by the district.   
**Result:** Record rejected
 EXAMPLE   
The Survey Period Code as specified in the transmission Job Control Language (JCL) is identified as 
Survey Period "5". However, if records on the transmission have a Survey Period Code "2", all records 
updated, added or deleted with this inconsistency will  be rejected.  

**District Responsibility:** If the rejected records should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected records to be loaded to the database, the Survey Period Code should be 
corrected, and all records should be resubmitted .  
  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 5. School Year must be correct for the submission specified by the  district.   
**Result:** Record rejected
EXAMPLE   
The School Year as specified in the transmission JCL is identified as the valid year for data submission. 
However, if records on the transmission have the previous year coded, all records updated, added or 
deleted with this inconsistency would be rejected.   

**District Responsibility:** If the rejected records should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
School Year either on the records coming in or the transmission JCL and resubmit all records.   
   
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 6. Test Name must be APT, ASV, CAI or IBP as listed on the Test Name Table in Appendix I of the DOE 
Information Database Requirements Volume I -Automated Student Information System manual.   
**Result:** Record rejected
EXAMPLE   
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because the Test Name is invalid.  
 
Florida Education Identifier  Test Date  Test Name  
FL123456789100  01172006  APT 
* FL123456789200  01172006  SSL 

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Test 
Name and resubmit the record.  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 7. Test Publication Year must be numeric and a valid year in the range 1970 through the current year.   
**Result:** Record rejected
EXAMPLE   
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because the Test Publication Year is in the future. The 
third record would be rejected because the Te st Publication Year is not within the valid range of years.  
Florida Education Identifier  Test Date  Test Publication Year  
FL123456789100  0118****  2002  
* FL123456789200  1115****  2103  
* FL123456789300  0431****  1956  
 
****  = Valid year for data submission.  

**District Responsibility:** If the rejected records should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Test 
Publication Year and resubmit the records.   
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 8. Test Date must be numeric and a valid date that is not in the future.   
**Result:** Record rejected
EXAMPLE   
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Test Date is not a valid calendar 
date.  
 
Florida Education Identifier  Test Date  
FL123456789100  0118****  
FL123456789200  1115****  
* FL123456789300  0431****  
 
****  = Valid year for data submission.  

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Test 
Date and resubmit the record.   
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 9. The Test Subject Content code must be a valid code, specified in Appendix L of the DOE Information 
Database Requirements Volume I -Automated Student  Information System manual, for the Test 
Name/Code.  
**Result:** Record rejected
EXAMPLE   
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because the Test Subject Content code is invalid for 
the Test Code submitted. The third record would be rejected because the Test Subject Content code is 
blank.  
 
Florida Education Identifier  Test Code  Test Subject Content Code  
FL123456789100  STA 11 
*FL123456789200  STA 03 
*FL123456789300  STA  

**District Responsibility:** If the rejected records should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Test 
Subject Content codes and resubmit the records .  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 10. Item 3 - Filler on this format in position numbers 7 -16 must be all spaces.   
Record  rejected  
EXAMPLE   
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because the data reported is not all spaces.  
 
District Number, Current 
Enrollment  School Number, Current 
Enrollment  Filler, Item #3  
01 0151   
* 01  0151  265456789X  

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must fill the positions 
noted with all spaces and resubmit the record.    
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 11. Test Score (1) must be numeric and right justified with leading zeros.   
**Result:** Record rejected
EXAMPLE   
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because Test Score 1 contains alphabetic characters. 
The third record would be rejected because Test Score (1) does not have leading zeros.  
 
Florida Education Identifier  Test Date  Test Score 1 
FL123456789100  0119****  0071  
*FL123456789200  0119****  AA71  
*FL123456789300  0119****        71 
   
****  = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected records should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Test 
Score (1) and resubmit the records.  
    
  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 13. Test Score 2 must be numeric and right justified with leading zeros.   
**Result:** Record rejected
 EXAMPLE   
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because Test Score 2 contains alphabetic characters. 
The third record would be rejected because Test Score 2 does not have leading zeros.  
 
Florida Education Identifier  Test Date  Test Score 2  
FL123456789100  0119****  0071  
*FL123456789200  0119****  AA71  
*FL123456789300  0119****        71 
 
**** = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected records should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Test 
Score 2 and resubmit the records.  
  
    
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 14. The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent 
batch/update submissions, if A is specified then the record must not already exist on the database; if C 
or D is specified then the record must exist on the database.   
**Result:** Record rejected
EXAMPLE   
For all original transmissions, the Transaction Code must be "A". An original transaction is the first 
submission of a record during a survey period. After original transmission of records, changes to the 
record for elements other than the key elements mus t be done with a "C" as the Transaction Code. To 
delete a record, the Transaction Code must be a "D". To change key elements in a batch transaction, the 
record must FIRST be deleted with a "D" and then added with an "A".  Records with an incorrect 
Transact ion Code will be rejected.  

**District Responsibility:** If the rejected records should not have been submitted no action is required.  However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
Transaction Code and resubmit the records.     
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 18. Test Level must not be blank.  
**Result:** Record rejected
EXAMPLE   
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because the Test Level field is blank.  
 
Florida Education Identifier  Test Date  Test Level  
FL123456789100  0119****  11 
* FL123456789200  0119****   
 
****  = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Test 
Level and resubmit the record.  
  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 19. Test Form must not be blank.  
**Result:** Record rejected
EXAMPLE   
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because the Test Form field is blank.  
 
Florida Education Identifier  Test Date  Test Form  
FL123456789100  0119****  A 
* FL123456789200  0119****   
 
****  = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Test 
Form and resubmit the records.  
    
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 20. If Test Score Type (2) is ZZ then Test Score 2 must be 0000.   
**Result:** Record rejected
EXAMPLE   
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because the Test Score (2) is not 0000.  
 
Florida Education 
Identifier  Test Date  Test Score Type 2  Test Score 2  
FL123456789100  01192007  ZZ 0000  
* FL123456789200  01192007  ZZ 0200  

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Test 
Score (2) and resubmit the record.  
     
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 21. Each  record must be unique based on District Number, Current Enrollment; School 
Number, Current Enrollment; Florida Education Identifier; Survey Period Code; School Year; Test Name, 
Test Date and Test Subject  
Content.   
**Result:** First record accepted, all other duplicate records rejected
EXAMPLE   
The first, third and fourth records listed below would be loaded to the database assuming no other 
reject rule would cause their rejection. The second and fifth records would be rejected since they are 
duplicates (same District Number, Current Enrollment; School Number, Current Enrollment; Florida 
Education Identifier; Survey Period Code; School Year; Test Name, Test Date and Test Subject Content) 
of the first and fourth records, respectively.  
 
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
Code  School 
Year  Test 
Name  Test Date  Test 
Subject 
Content  
01 0411  FL123456789100  5 ****  CAI 09182006  3A 
* 01  0411  FL123456789100  5 ****  CAI 09182006  3A 
01 0411  FL123456789200  5 ****  APT 09222006  1A 
01 0411  FL123456789300  5 ****  IBP 09232006  NB 
* 01  0411  FL123456789300  5 ****  IBP 09232006  NB 
 
**** = Valid fiscal year for data submission.  

**District Responsibility:** If the records that were accepted and loaded to the database are correct ones, no action is required. 
However, if the district wishes the data in the rejected records to be loaded to the database, the district 
must delete any invalid records, correct any r ejected records if necessary, and resubmit the corrected 
records.  
    
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 22. The Student Number Identifier, Local may be any combination of letters, numbers and blanks. (All blanks 
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
*01 2121@xyz  
*01            123456  

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Student Number Identifier, Local and resubmit the rec ord.  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 23. School Number, Current Enrollment must be numeric in the range 0001 to 9899, excluding 3518, 7006 
and 9001.   
**Result:** Record rejected
EXAMPLE   
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The second two records would be rejected. The first of these would be rejected 
because the School Number, Current Enrollment is no t in the appropriate numerical range. The second 
of these two records would be rejected because the School Number, Current Enrollment is not numeric.  
 
District Number, Current 
Enrollment  School Number, Current 
Enrollment  Florida Education Identifier  
01 0151  FL123456789100  
01 0151  FL123456789200  
*01 9999  FL123456789300  
*01 C901  FL123456789000  

**District Responsibility:** If the rejected records should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
School Number, Current Enrollment and resubmit the records.  
    
  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 24. Test Score Type (1) must be SS for APT, CAI or IBP, and ZZ for ASV. Test Score Type (2) must be ZZ for 
APT, ASV, CAI or IBP.   
**Result:** Record rejected
EXAMPLE   
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because Test Score Type (2) is not ZZ.  
 
Florida Education 
Identifier  Test Date  Test Name  Test Score Type 1  Test Score Type 2  
FL123456789100  11012008  CAI SS ZZ 
*FL123456789100  11012008  CAI SS LX 

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct Test Score 
Type (2) and resubmit the record.   
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 26. If Test Name is CAI then Test Publication Year must be the year the data is being reported or the 
previous year.   
**Result:** Record rejected
EXAMPLE   
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because the Test Publication Year is not valid for the 
Test Name reported.    
 
Florida Education 
Identifier  Test Date  Test Name  Test Publication Year  
FL123456789100  06012009  CAI 2009  
*FL123456789100  06012009  CAI 2007  

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Test 
Publication Year and resubmit the record.   
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 27. If Test Name is CAI then Test Date must be June 1 (0601), June 2 (0602) November 1 (1101) or 
November 2 (1102) of the school year being reported.   
**Result:** Record rejected
EXAMPLE   
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because the Test Date is not valid for the Test Name 
reported.    
 
Florida Education 
Identifier  Test Date  Test Name  Test Publication Year  
FL123456789100  06012009  CAI 2009  
*FL123456789100  06012009  CAI 2009  

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Test 
Date and resubmit the record.  
    
  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 28. If Test Name is APT, ASV, CAI or IBP then Test Form must be Z.  
**Result:** Record rejected
EXAMPLE   
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because the Test Form is not valid for the Test Name 
reported.    
 
Florida Education 
Identifier  Test Date  Test Name  Test Form  
FL123456789100  06012009  CAI Z 
*FL123456789100  06012009  CAI A 

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Test 
Form and resubmit the record.  
    
  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 29. If Test Name is CAI then Test Level must be A or AS.  
**Result:** Record rejected
Note:  Test Level A is left justified with a trailing blank.  
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because the Test Level is not valid for the Test Name 
reported.  
 
Florida Education 
Identifier  Test Date  Test Name  Test Level  
FL123456789100  06012009  CAI AS 
*FL123456789100  06012009  CAI S 

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Test 
Level and resubmit the record.  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 30. If Test Name is CAI then Test Score must be  
• 0000, 0001, 0002, 0003, 0004, 0005, 0006, 0007, or 0008.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because the Test Score is not valid for the Test Name 
reported.    
 
Florida Education 
Identifier  Test Date  Test Name  Test Score  
FL123456789100  06012009  CAI 00007  
*FL123456789100  06012009  CAI B 

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Test 
Score and resubmit the record.  
    
  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 31. If Test Name is APT or ASV then Test Level must be ZZ.  
**Result:** Record rejected
EXAMPLE   
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because the Test Level is not valid for the Test Name 
reported.    
 
Florida Education 
Identifier  Test Date  Test Name  Test Level  
FL123456789100  06012009  APT ZZ 
*FL123456789100  06012009  APT AS 

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Test 
Level or Test Name code and resubmit the record.   
    
  
  
  
Student Database 202 6-2027 /  
## Reject Rules

UPDATED 09/12/2025  
32. 
• If Test Name is IBP then Test Level must be HL or SL.  
 Note: You may enter HL or SL for IBP.  
• If Test Name IBP and Test Subject Content Code is PT then Test Level must be ZZ.  
**Result:** Record rejected
Note: You may enter HL or SL for IBP.  
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because the Test Level is not valid for the Test Name 
reported.  
 
Florida Education 
Identifier  Test Date  Test Name  Test Form  
FL123456789100  06012009  IBP SL 
FL123456789100  06012009  IMP HL 
*FL123456789100  06012009  IBP AS 

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Test 
Level or Test Name code and resubmit the record.   
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 33. If Test Name is APT then Test Score (1) must be  
• 0001, 0002, 0003, 0004, or 0005.  
**Result:** Record rejected
EXAMPLE   
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because the Test Score is not valid for the Test Name 
reported.  
 
Florida Education 
Identifier  Test Date  Test Name  Test Score  
FL123456789100  06012009  APT 0003  
FL123456789100  06012009  APT B 

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Test 
Score and resubmit the record.  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 34. If Test Name is IBP then Test Score (1) must be  
• 0001, 0002, 0003, 0004,  0005, 0006, 0007, 0008, 0009, 0010, 0011, 0012, 0013 or 0014.  
**Result:** Record rejected
EXAMPLE   
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because the Test Score is not valid for the Test Name 
reported.    
 
Florida Education 
Identifier  Test Date  Test Name  Test Score  
FL123456789100  06012009  IBP 0007  
FL123456789100  06012009  IBP B 

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Test 
Score and resubmit the record.  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 35. Florida Education Identifier (FLEID) is alphanumeric and must be entered as “FL” in the first 2 positions 
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
*01 FL000000000000  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Florida 
Education Identifier and resubmit the record f or processing.  
  
  
Student Database 202 6-2027 /  
 VALIDATION RULES  

### 60. Each  record must have a matching Student Demographic Information record based 
on District Number, Current Enrollment; Florida Education Identifier; Survey Period Code and School 
Year.   
## State Validation

EXAMPLE   
The  record listed below marked with an asterisk would cause a message to be 
generated because it does not have a matching Student Demographic Information record.  
 records  
District Number, 
Current Enrollment  Florida Education 
Identifier  Survey Period Code  School Year  
*01 FL123456789100  5 ****  
01 FL123456789200  5 ****  
01 FL123456789300  5 ****  
 
Student Demographic Information Records  
District Number, 
Current Enrollment  Florida Education 
Identifier  Survey Period Code  School Year  
*01 FL123456789200  5 ****  
01 FL123456789300  5 ****  
 
**** = Valid fiscal year for data submission.  

**District Responsibility:** The district must delete the  record or add a Student Demographic Information 
record to match the above key fields.