# Teacher Course — Edits and Reject Rules

Source: Florida DOE
Manual: Student Database 2026-2027

Student Database 202 6-2027 /  
## Reject Rules

UPDATED 07/01/2026   

### 1. District Number, Current Instruction/Service must be numeric and active (A) on the Appendix C: District 
Name Table . 
**Result:** Record rejected
EXAMPLE  
If district 01 is submitting records, District Number, Current Instruction/Service must be 01 for all 
records. In the records listed below, the first two records would be loaded to the database assuming no 
other reject rule would cause their rejection. The  record indicated with the asterisk would be rejected 
since the District Number, Current Instruction/Service is 02 rather than 01 (the number of the district 
submitting the record).  
District Number,  
Current Instruction/  
Service  School Number,  
Current  
Instruction  Social  
Security  
Number  
01 0021  012345677  
01 0021  012345678  
*02 0021  012345679  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the District 
Number, Current Instruction/Service and resub mit the record.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 2. School Number, Current Instruction/Service must be numeric in the range 0001 to 9899 (excluding 
9001), 9996 or it must be C901 to C928, U970 to U981, P001 - P999 or N999.  
**Result:** Record rejected
EXAMPLE  
The third record listed below would be loaded to the database assuming no other reject rule would 
cause its rejection. The first and second records would be rejected because the School Number, Current 
Instruction/Service is not within the specified range.  
District Number,  
Current Instruction/  
Service  School Number,  
Current Instruction/  
Service  Survey  
Period  
Code  Fiscal  
Year  Social  
Security  
Number  
*31 0800  2 ****  123456789  
*31 C801  2 ****  123456790  
31 0021  2 ****  123456791  
 **** = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the School 
Number, Current Instruction/Service and resub mit the records.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 3. Survey Period Code must be 1, 2, 3, or 4 and it must be correct for the submission specified by the 
district.  
**Result:** Record rejected
EXAMPLE  
The Survey Period Code as specified in the transmission JCL or in the statements for tape transmission is 
identified as Survey Period Code "2" and records are coded as Survey Period Code "3". All updates, adds, 
or deletes that have this inconsistency would  be rejected.  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Survey 
Period Code and resubmit the records.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 4. Fiscal Year must be correct for the submission specified by the district.  
**Result:** Record rejected
EXAMPLE  
The Fiscal Year as specified in the Transmission JCL or in the statements for tape transmission is 
identified as the valid year for data submission but records being submitted have the previous Fiscal Year 
coded. All updates adds or deletes that have this inconsistency would be rejected.  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Fiscal 
Year and resubmit the records.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 5. Course Number must not contain blanks.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second and third records would be rejected since the Course Number contains blanks.  
District Number,  
Current Instruction/  
Service  School Number,  
Current Instruction/  
Service  Survey  
Period  
Code  Fiscal  
Year  Course  
Number  
01 0401  2 ****  1002360  
*01 10401  2 ****  100237  
*01 0401  2 ****  100 31  
 **** = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Course 
Number and resubmit the record.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 6. Section Number must not be all blanks . Allowable characters are 0 -9, A-Z, space, hyphen ( -), dollar sign 
($), pound sign (#), ampersand (&), percent (%), forward slash (/) and colon.  
**Result:** Record rejected
EXAMPLE  
The first record would be loaded to the database assuming no other reject rule would cause its rejection. 
The second record would be rejected because the Section Number contains all blanks.  
District Number,  
Current Instruction/  
Service  School Number,  
Current Instruction/  
Service  Course  
Number  Section  
Number  
01 0201  1002360  1 
*01 0201  1002360   

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
Section Number and resubmit the records.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 7. Period Number must be numeric and greater than or equal to zero.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second and third records would be rejected because the period number contains blanks 
or alphabetic characters.  
District Number,  
Current Instruction/  
Service  School Number,  
Current Instruction/  
Service  Course  
Number  Section  
Number  Period  
Number  
01 0201  1002360  00100  0000  
*01 0201  1002360  00200  E801  
*01 0321  1002360  00300  02 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Period 
Number and resubmit the records.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 8. Florida Educators Certificate Number must be numeric with no embedded blanks.  
**Result:** Record rejected
EXAMPLE  
The first record would be loaded to the database assuming no other reject rule would cause its rejection. 
The second and third records would be rejected because the Florida Educators Certificate Number 
contains blanks.  
District Number,  
Current Instruction/  
Service  School Number,  
Current Instruction/  
Service  Survey  
Period  
Code  Florida Educators  
Certificate  
Number  
59 0421  2 0000291125  
*59 0421  2  
*59 0421  2 291125  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Florida 
Educators Certificate Number and resubmit th e records.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 9. The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent 
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
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 10. Each  record must be unique based on the following: District Number, Current 
Instruction/Service; School Number, Current  
Instruction/Service; Survey Period Code; Fiscal Year; Term; Course Number; Section Number; Period 
Number; and Social Security Number (or Staff Number Identifier).  
**Result:** First record accepted, all other duplicate records rejected
EXAMPLE  
The first, second and third records would be loaded to the database assuming no other reject rule would 
cause their rejections. The fourth record would be rejected because the following fields: District Number, 
Current Instruction/Service; School Number, C urrent Instruction/Service; Survey Period Code; Fiscal Year; 
Term; Course Number; Section Number; Period Number; and Social Security Number are duplicate fields 
as in the first record.  
District  
Number,  
Current 
Instruction/  
Service  School 
Number,  
Current 
Instruction/  
Service  Survey  
Period  
Code  Fiscal  
Year  Term  Course  
Number  Section  
Number  Period  
Number  Social  
Security  
Number  
59 0421  2 ****  1 1200300  00200  0505  123456789  
59 0421  2 ****  1 1206310  00100  0606  123456790  
59 0421  2 ****  1 1205540  00200  0404  123456791  
*59 0421  2 ****  1 1200300  00200  0505  123456789  
 **** = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the key 
items: District Number, Current Instruction/Servic e; School Number, Current Instruction/Service; Survey 
Period Code; Fiscal Year; Term; Course Number; Section Number; Period Number; and Social Security 
Number and resubmit the record.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 11. Social Security Number (SSN) must be numeric and greater than zero, excluding the value 999999999, 
unless it is a Staff Number Identifier and the first two positions are “CS” and the last seven positions are 
numeric. Nine -character SSN's should be left -justified, with a trailing blank.  
**Result:** Record rejected
EXAMPLE  
The first record would be loaded to the database assuming no other reject rule would cause their 
rejection. The second, third and fourth records would be rejected. The second record would be rejected 
because the Social Security Number is not numeric. The t hird record would be rejected because the 
Social Security Number is not left justified. The fourth record would be rejected because the Social 
Security Number contains a blank.  
District Number,  
Current Instruction/  
Service  Florida Educators  
Certificate  
Number  Social  
Security  
Number  
01 0000291125  123456789  
*01 0000291126  ZZZZZZZZZ  
*01 0000291128       123456790  
*01 0000291129   

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Social 
Security Number and resubmit the records.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

UPDATED 04/03/2026  

### 12. If School Number, Current Instruction/Service = 7001, the Florida Educators Certificate Number must be 
a regular number assigned by the Bureau of Educator Certification of the Florida Department of 
Education in the following ranges: 0000000001 - 6001999999 , 6002000001 - 6002999999, 6003000001 – 
6003999999, 6004000001 - 6004999999,  6007000001 – 6007999999 , or 7777777777, excluding 
0000999999, and may not contain blanks.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected since the Florida Educators Certificate Number is all 
zeros and not within the range of valid numbers . The third record would reject because the Florida 
Educators Certification Number contains blanks.  
District Number,  
Current Instruction/  
Service  School Number,  
Current Instruction/  
Service  Survey  
Period  
Code  Fiscal  
Year  Florida Educators  
Certificate  
Number  
01 0401  2 ****  0004567890  
*01 0401  2 ****  0000000000  
*01 0401  2 ****   
 **** = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Florida 
Educators Certificate Number and resubmit th e record.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 14. If Survey Period Code is 1 -4, the Term/Survey Indicator must be Y or N.  
**Result:** Record rejected
EXAMPLE  
The first, second and third records would be loaded to the database assuming no other reject rule would 
cause their rejections. The fourth record would be rejected because the Term/Survey Indicator must be Y 
or N.  
District 
Number,  
Current  
Instruction/  
Service  School  
Number,  
Current  
Instruction/  
Service  Survey  
Period  
Code  Fiscal  
Year  Term  Term/  
Survey  
Indicator  Social  
Security  
Number  
59 0421  2 ****  1 Y 123456789  
59 0421  2 ****  1 Y 123456790  
59 0421  2 ****  1 Y 123456791  
*59 0421  2 ****  2 Z 123456792  
 **** = Valid fiscal year for data submission.  

**District Responsibility:** z 
If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Term/Survey Indicator or the Survey Period code and re submit the record.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 15. If Survey Period Code is 1 -4 and Term is 3, the Term/Survey Indicator must be Y .  
**Result:** Record rejected
EXAMPLE  
The first, second and third records would be loaded to the database assuming no other reject rule would 
cause their rejections. The fourth record would be rejected because the Term/Survey Indicator must be 
Y .  
District 
Number,  
Current  
Instruction/  
Service  School  
Number,  
Current  
Instruction/  
Service  Survey  
Period  
Code  Fiscal  
Year  Term  Term/  
Survey  
Indicator  Social  
Security  
Number  
59 0421  2 ****  3 Y 123456789  
59 0421  2 ****  3 Y 123456790  
59 0421  2 ****  3 Y 123456791  
*59 0421  2 ****  3 N 123456792  
 **** = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Term/Survey Indicator or the Term and resubmit the rec ord. 
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 16. If Survey Period Code is 2 and Term is 1, the Term/Survey Indicator must be Y .  
**Result:** Record rejected
EXAMPLE  
The first, second and third records would be loaded to the database assuming no other reject rule would 
cause their rejections. The fourth record would be rejected because the Term/Survey Indicator must be 
Y .  
District 
Number,  
Current  
Instruction/  
Service  School  
Number,  
Current  
Instruction/  
Service  Survey  
Period  
Code  Fiscal  
Year  Term  Term/  
Survey  
Indicator  Social  
Security  
Number  
59 0421  2 ****  1 Y 123456789  
59 0421  2 ****  1 Y 123456790  
59 0421  2 ****  1 Y 123456791  
*59 0421  2 ****  1 N 123456792  
 **** = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Survey 
Period Code, Term, or Term/Survey Indicator and  resubmit the record.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 17. If Survey Period Code is 3 and Term is 2, the Term/Survey Indicator must be Y .  
**Result:** Record rejected
EXAMPLE  
The first, second and third records would be loaded to the database assuming no other reject rule would 
cause their rejections. The fourth record would be rejected because the Term/Survey Indicator must be 
Y .  
District 
Number,  
Current  
Instruction/  
Service  School  
Number,  
Current  
Instruction/  
Service  Survey  
Period  
Code  Fiscal  
Year  Term  Term/  
Survey  
Indicator  Social  
Security  
Number  
59 0421  3 ****  2 Y 123456789  
59 0421  3 ****  2 Y 123456790  
59 0421  3 ****  2 Y 123456791  
*59 0421  3 ****  2 N 123456792  
 **** = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Survey 
Period Code, Term, or Term/Survey Indicator and  resubmit the record.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 18. If Course Number is 5100580 or 5100590, then Certification/Licensure/ Qualification Status code must 
be V.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second and third records would be rejected because the 
Certification/Licensure/Qualification Status code is not valid for the course number.  
District 
Number,  
Current  
Instruction/  
Service  School  
Number,  
Current  
Instruction/  
Service  Survey  
Period  
Code  Fiscal  
Year  Course  
Number  Social  
Security  
Number  Certification/  
Licensure/  
Qualification  
Status  
01 0071  2 ****  5100580  123456789  V 
*01 0071  2 ****  5100580  123456790  O 
*01 0071  2 ****  5100580  123456791  I 
 **** = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
Certification/Licensure/Qualification Status codes o r the Course Numbers and resubmit the records.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 19. If Course Number does not equal 5100620 , 5100580 or 5100590. Then 
Certification/Licensure/Qualification Status code must not be V.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Certification/Licensure 
/Qualification Status code is not valid for the course.  
District 
Number,  
Current  
Instruction/  
Service  School  
Number,  
Current  
Instruction/  
Service  Survey  
Period  
Code  Fiscal  
Year  Course  
Number  Social  
Security  
Number  Certification/  
Licensure/  
Qualification  
Status  
01 0021  2 ****  1200300  123456789  I 
31 0021  2 ****  1200300  123456790  O 
*31 0021  2 ****  1200300  123456791  V 
 **** = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Certification/Licensure/Qualification Status code or t he Course Number and resubmit the record.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 20. Facility Type code must be in the range 00 to 20.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second and third records would be rejected because the Facility Type code is not within 
the specified range of 00 to 20.  
District Number,  
Current Instruction/  
Service  School Number,  
Current Instruction/  
Service  Social  
Security  
Number  Facility  
Type  
01 0321  123456781  00 
*01 0321  123456782  99 
*01 0321  123456783  21 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Facility 
Type code and resubmit the record.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 21. For Survey Periods 1 -4, Days in Term (for FTE purposes) must be numeric, greater than zero and less than 

### 300. Record rejected  
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second and fourth records would be rejected because the Days in Term (for FTE 
Purposes) is not numeric or contains blanks.  
District Number,  
Current Instruction/  
Service  School Number,  
Current Instruction/  
Service  Social  
Security  
Number  Survey  
Period  
Code  Days in Term  
(for FTE  
Purposes)  
01 0201  123456789  2 090 
*01 0201  234567891  2 A90 
*01 0201  345678912  2   90 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct Days in 
Term (for FTE Purposes) and resubmit the records . 
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 23. Certification/Licensure/Qualification Status code must be A, B, C, H, I, L, M, N, O, P , S, T or V .  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the 
Certification/Licensure/Qualification Status code is not valid.  
District Number,  
Current 
Instruction/  
Service  School Number,  
Current 
Instruction/  
Service  Survey  
Period  
Code  Fiscal  
Year  Course  
Number  Social  
Security  
Number  Certification/  
Licensure/  
Qualification  
Status  
31 0021  2 ****  1200300  123456789  I 
31 0021  2 ****  1200300  123456790  O 
*31 0021  2 ****  1200300  123456791  Z 
 **** = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Certification/Licensure/Qualification Status code and resubmit the record.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 26. If Survey Period Code is 2 or 3, then the first five positions and positions 7 - 16 of Classroom Identification 
(FISH) Number must be numeric. Positions 17 -21 may be alpha or numeric. If position 6 is O, positions 
17-21 may be symbols. If Survey Period Code  is 1 or 4, then each position of the Classroom Identification 
(FISH) Number must contain one of the following: blank (space), Z or zero.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because positions 7 -11 of the Classroom 
Identification (FISH) Number are alphabetic instead of numeric.  
District Number,  
Current Instruction/  
Service  School Number,  
Current Instruction/  
Service  Classroom  
Identification  
(FISH) Number  Survey  
Period  
Code  
01 0321  00256A0123400456ABCDE  2 
01 0321  00015O000014444412ABC  2 
*01 0321  12365ABCDRF98745HMM21  2 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Classroom Identification (FISH) Number and resubmit th e record.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 27. If Survey Period Code is 2 or 3, then position 6 of the Classroom Identification (FISH) Number must be A, 
C, F or O.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because position 6 of the Classroom 
Identification (FISH) Number is not valid.  
District Number,  
Current Instruction/  
Service  School Number,  
Current Instruction/  
Service  Classroom  
Identification  
(FISH) Number  Survey  
Period  
Code  
01 0321  00256A0123400456ABCDE  2 
01 0321  00015O000014444412ABC  2 
*01 0321  41236Z8524698745HMM21  2 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Classroom Identification (FISH) Number and resubmit th e record.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 28. If Survey Period Code is 2 or 3, then Scheduling Method must be A. B, C,  D, G, I, M , S or W. If Survey 
Period Code is 1 or 4, then Scheduling Method must be Z.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second and third records would be rejected because the Scheduling Method codes are 
invalid.  
District Number,  
Current 
Instruction/  
Service  School Number,  
Current 
Instruction/  
Service  Course  
Number  Section  
Number  Period  
Number  Scheduling  
Method  Survey  
Period  
Code  
01 0321  1002360  00100  0000  A 2 
01 0321  1002360  00200  1111  D 2 
*01 0321  1002360  00300  1002  R 2 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
Scheduling Method and resubmit the records.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 29. If Survey Period Code is 2 or 3 and if position 6 of the Classroom Identification (FISH) Number is O, then 
Facility Type must not be 00. Survey Period Code is 2 or 3 and if position 6 of the Classroom Identification 
(FISH) number is C, then Facility Type m ust be 19.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because position 6 of the Classroom Identification 
(FISH) Number is O therefore Facility Type must no t be 00. The third record would be rejected because 
position 6 of the Classroom Identification (FISH) Number is C and Facility Type is not 19.  
District Number,  
Current Instruction/  
Service  School Number,  
Current Instruction/  
Service  Facility  
Type  Classroom  
Identification  
(FISH) Number  
01 0321  00 00256A0123400456ABCDE  
01 0321  00 00256O0123400456ABCDE  
*01 0321  01 00256C0123400456ABCDE  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct either the 
Classroom Identification (FISH) Number or the F acility Type code and resubmit the record.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 2A. If Survey Period is 2 or 3, and If position 6 of the Classroom Identification (FISH) Number is A, C or F the 
number must be a valid FISH number on the FLDOE FISH database.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Classroom Identification (FISH) 
Number is not a valid FISH number and position 6 is  not O.  
District Number,  
Current Instruction/  
Service  School Number,  
Current Instruction/  
Service  Classroom  
Identification  
(FISH) Number  Survey  
Period  
Code  
01 0321  00256A01234004561234  2 
01 0321  00015F0000144444123AB  2 
*01 0321  44444C444444444444444  2 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Classroom Identification (FISH) Number and resubmit th e record.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 2B. If Certification/Licensure/Qualification Status is H, I, M, O, P or S, then the  
Florida Educators Certificate Number must not be 0000000000, 0000999999, 7777777777, 8888888888 
or 9999999999.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the 
Certification/Licensure/Qualification Status code is not valid for the Florida Educ ators Certificate 
Number.  
District 
Number,  
Current 
Instruction/  
Service  School  
Number,  
Current 
Instruction/  
Service  Survey  
Period  
Code  Fiscal  
Year  Course  
Number  Social  
Security  
Number  Certification/  
Licensure/  
Qualification  
Status  Florida  
Educators  
Certificate  
Number  
31 0021  2 ****  1200300  123456789  H 0000000001  
31 0021  2 ****  1200300  123456790  S 0001000000  
*31 0021  2 ****  1200300  123456791  O 0000000000  
 **** = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Certification/Licensure/Qualification Status code or t he Course Number and resubmit the record.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 2C. If Certification/Licensure/Qualification Status code is A or T, then the Florida Educators Certificate 
Number must be 7777777777.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the 
Certification/Licensure/Qualification Status code is not valid for the Florida Educ ators Certificate 
Number.  
District 
Number,  
Current 
Instruction/  
Service  School  
Number,  
Current 
Instruction/  
Service  Survey  
Period  
Code  Fiscal  
Year  Course  
Number  Social  
Security  
Number  Certification/  
Licensure/  
Qualification  
Status  Florida  
Educators  
Certificate  
Number  
31 0021  2 ****  1200300  123456789  T 7777777777  
31 0021  2 ****  1200300  123456790  A 7777777777  
*31 0021  2 ****  1200300  123456791  O 7777777777  
 **** = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Certification/Licensure/Qualification Status code or t he Course Number and resubmit the record.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 2D. If Certification/Licensure/Qualification Status code is L, then the Florida Educators Certificate Number 
must be 8888888888.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the 
Certification/Licensure/Qualification Status code is not valid for the Florida Educ ators Certificate 
Number.  
District 
Number,  
Current 
Instruction/  
Service  School  
Number,  
Current 
Instruction/  
Service  Survey  
Period  
Code  Fiscal  
Year  Course  
Number  Social  
Security  
Number  Certification/  
Licensure/  
Qualification  
Status  Florida  
Educators  
Certificate  
Number  
31 0021  2 ****  1200300  123456789  L 8888888888  
31 0021  2 ****  1200300  123456790  L 8888888888  
*31 0021  2 ****  1200300  123456791  O 8888888888  
 **** = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Certification/Licensure/Qualification Status code or t he Course Number and resubmit the record.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 2E. If Scheduling Method is C or S, then the Primary Instructor Indicator code must be Y .  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second and third records would be rejected because the Scheduling Method codes are 
invalid for the Primary Instructor Indicator.  
District Number,  
Current 
Instruction/  
Service  School Number,  
Current  
Instruction/  
Service  Course  
Number  Section  
Number  Period  
Number  Scheduling  
Method  Primary  
Instructor  
Indicator  
01 0321  1002360  00100  0000  C Y 
*01 0321  1002360  00200  1111  S N 
*01 0321  1002360  00300  1002  C N 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
Scheduling Method or Primary Instructor Indicator an d resubmit the records.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 2F. If the Team Teacher Training code is not Z and Scheduling Method equals C, then Primary Instructor 
Indicator code must equal Y .  
**Result:** Record rejected
EXAMPLE  
The first and third records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. The second record would be rejected because the Team Teacher Training 
and Scheduling Method codes are invalid for the Primar y Instructor Indicator.  
District Number,  
Current Instruction/  
Service  School Number,  
Current  Instruction/  
Service  Social  
Security  
Number  Team  
Teacher  
Training  Primary  
Instructor  
Indicator  Scheduling  
Method  
01 0321  123456781  A Y C 
*01 0321  123456782  B N C 
01 0321  123456783  C Y C 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Team 
Teacher Training code, Scheduling Method or Prima ry Instructor Indicator code and resubmit the record.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 2G. If Certification/Licensure/Qualification Status code is C, then the Classical indicator in the MSID file must 
be Y .  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the MSID Classical code is not valid for 
the Florida Educators Certificate Number.  
District 
Number,  
Current 
Instruction/  
Service  School 
Number,  
Current 
Instruction/  
Service  Survey  
Period  
Code  Fiscal  
Year  Course  
Number  Social  
Security  
Number  Certification/  
Licensure/  
Qualification  
Status  MSID  
Classical  
Indicator  
31 0021  2 ****  1200300  123456789  C Y 
31 0021  2 ****  1200300  123456790  C Y 
*31 0021  2 ****  1200300  123456791  C N 
 **** = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Certification/Licensure/Qualification Status code or c orrect/confirm the MSID Classical indicator on the 
MSID database and resubmit the record.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 31. The Staff Number Identifier, Local may be any combination of letters, numbers and blanks. All blanks are 
not allowable. It must be left -justified with trailing blanks.  
**Result:** Record rejected
EXAMPLE  
The first three records listed below would be loaded to the database assuming no other edit would 
cause their rejection. The fourth record would be rejected because the Staff Number Identifier, Local 
contains a symbol (@). The fifth record would be rejecte d because it is right -justified rather than left -
justified.  
District Number,  
Current Enrollment  Staff Number Identifier,  
Local  
01 0123456789  
01 ABC123DEF9  
01 3001 28K  
*01 2121@xyz  
*01 123456  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Staff 
Number Identifier, Local and resubmit the reco rds. 
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 33. If Course Number Class Size Core Course Indicator on the Course Code Directory = Y , the last two digits of 
the Period Number are not 88, the Survey Period Code is 2 or 3, and Scheduling Method is C or I, then 
the Team Teacher Training code must be A -D.  
**Result:** Record rejected
EXAMPLE  
The first and third records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. The second record would be rejected because the Team Teacher Training 
code is not A -D for a Scheduling Method of I.  
District Number,  
Current Instruction/  
Service  School Number,  
Current Instruction/  
Service  Social  
Security  
Number  Team  
Teacher  
Training  Survey  
Period  
Code  Scheduling  
Method  
01 0321  123456781  A 2 C 
*01 0321  123456782  Z 2 I 
01 0321  123456783  B 2 C 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Team 
Teacher Training code or the Scheduling Method co de and resubmit the record.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 34. For Survey Period Codes 2 and 3, Team Teacher Training must be A -D or Z. For Survey Period Codes 1 and 
4, Team Teacher Training must be Z.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because the Team Teacher Training code is not valid 
for the survey period reported. The third record would be rejected because the Team Teacher Training 
code is not a valid code.  
District Number,  
Current Instruction/  
Service  School Number,  
Current Instruction/  
Service  Social  
Security  
Number  Team  
Teacher  
Training  Survey  
Period  
Code  
01 0321  123456781  A 2 
*01 0321  123456782  B 1 
01 0321  123456783  M 2 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Team 
Teacher Training codes and resubmit the records . 
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

UPDATED 07/01/2026   

### 35. If District Number, Current Instruction/Service is active (A) on the Appendix C: District Name Table  and  
• if School Number, Current Instruction/Service is not 7001, 7006 7004, or 7023 and  
• if the School Number, Current Instruction/Service is not one that has a School Function Setting  
   of V and a Charter School Status not equal to Z on the Master School Identification file, then  
   Facility Type must not equal 20.  
**Result:** Record rejected
EXAMPLE  
In the list below, the first two records would be loaded to the database assuming no other reject rule 
would cause their rejection. The third record would be rejected because Facility Type equals 20.  
District Number,  
Current Instruction/  
Service  School Number,  
Current Instruction/  
Service  Facility  
Type  
06 0021  00 
29 7004  20 
*01 0021  20 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Facility 
Type or the School Number, Current Instructi on/Service and resubmit the record.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 36. If District Number, Current Instruction/Service is 71, or if the School Number, Current Instruction/Service 
is one for which the School Function Setting = V and Charter School Status does not equal Z on the 
Master School Identification file, then Facility type must equal 20.  
**Result:** Record rejected
EXAMPLE  
In the list below, the first record would be loaded to the database assuming no other reject rule would 
cause its rejection. The second record would be rejected because Facility Type does not equal 20.  
District Number,  
Current Instruction/  
Service  School Number,  
Current Instruction/  
Service  Facility  
Type  
06 0500  20 
*71 0700  10 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Facility 
Type and resubmit the record.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 37. If Survey Period Code is 2, or 3, then Fund Source: ESSA Title III must be coded Y or N. If Survey Period 
Code is 1 or 4, then Fund Source ESSA Title III must be Z.  
**Result:** Record rejected
EXAMPLE  
The first and second records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. The third record would be rejected because the Fund Source: ESSA Title III is 
blank.  
District Number,  
Current Instruction/  
Service  School Number,  
Current Instruction/  
Service  Social  
Security  
Number  Fund  
Source  
ESSA Title III  
06 0500  123456781  Y 
01 0321  123456782  N 
*01 0700  123456783   

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Fund 
Source: ESSA Title III code and resubmit the reco rd. 
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 38. Florida Education Identifier (FLEID) is alphanumeric and must be entered as “FL” in the first 2 positions 
followed by twelve numeric digits. No blanks or spaces are allowable.   
**Result:** Record rejected
EXAMPLE  
Florida Education Identifier:  
• FL012345678910  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Florida 
Education Identifier and resubmit the record f or processing.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 39. If Course Number equals 5100620. Then Certification/Licensure/Qualification Status code must be I or V.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Certification/Licensure 
/Qualification Status code is not valid for the course.  
District 
Number,  
Current  
Instruction/  
Service  School  
Number,  
Current  
Instruction/  
Service  Survey  
Period  
Code  Fiscal  
Year  Course  
Number  Social  
Security  
Number  Certification/  
Licensure/  
Qualification  
Status  
01 0021  2 ****  1200300  123456789  I 
31 0021  2 ****  1200300  123456790  V 
*31 0021  2 ****  1200300  123456791  O 
 **** = Valid fiscal year for data submission.  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Certification/Licensure/Qualification Status code or t he Course Number and resubmit the record.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 40. School Number, Current Instruction/Service must be valid and active on the Master School Identification 
File or must be C901 to C928, U970 to U981, P001 -P999, 9996, or N999.   
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second and third records would be rejected because the School Number, Current 
Instruction/Service is not valid and active on the Mast er School Identification file.  
District Number,  
Current Instruction/  
Service  School Number,  
Current Instruction/  
Service  Social  
Security  
Number  
01 0151  123456789  
*01 0661  123456781  
*01 0010  123456782  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the School 
Number, Current Instruction/Service and resub mit the records.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 41. All numeric Course Numbers must be on the Course Code Directory file unless School Number, Current 
Instruction/Service is P001 -P999.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second and third records would be rejected because the Course Numbers are not valid 
on the Course Code Directory file and School Numb er, Current Instruction/Service is not P001 -P999.  
District Number,  
Current Instruction/  
Service  School Number,  
Current Instruction/  
Service  Course  
Number  Period  
Number  
06 0151  2107810  0101  
*01 0151  0001111  0202  
*01 0151  3100000  0303  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Course 
Number and resubmit the records.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 42. The first two digits of Period Number must be 00 to 80. The last two digits of Period Number must be 00 
to 80, or 88 and must be greater than or equal to the first two digits.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
their rejection. The second and third records would be rejected because the last two digits of Period 
Number are not greater than or equal to the first two digits.  
District Number,  
Current Instruction/  
Service  School Number,  
Current Instruction/  
Service  Course  
Number  Period  
Number  
01 0151  2107810  1111  
*01 0151  2107810  0201  
*01 0151  2107810  4433  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Period 
Number and resubmit the records.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 46. All alphanumeric Course Numbers must be either on the Course Code Directory file or on the Statewide 
Course Numbering System file unless the School Number, Current Instruction/Service equals N999 or 
P001 -P999.  
**Result:** Record rejected
EXAMPLE  
The first and third records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. The second record would be rejected because the Course Number is not 
valid on the Course Code Directory file or the Statewid e Course Numbering System file nor is the School 
Number, Current Instruction/Service N999 or P001 -P999.  
District Number,  
Current Instruction/  
Service  School Number,  
Current Instruction/  
Service  Course  
Number  Period  
Number  
01 0151  A010301  0101  
*01 0151  AAA1111  1111  
*01 0151  H170103  0202  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Course 
Number and resubmit the records.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 48. Primary Instructor Indicator code must be Y or N.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Primary Instructor Indicator code is 
not valid.  
District Number,  
Current 
Instruction/  
Service  School Number,  
Current 
Instruction/  
Service  Social  
Security  
Number  Course  
Number  Section  
Number  Period  
Number  Primary  
Instructor  
Indicator  
18 0091  123456789  5100060  001 0106  Y 
18 0091  123456790  5100070  002 0106  N 
*18 0091  123456791  5100080  003 0106  Z 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Primary 
Instructor Indicator code and resubmit the rec ord. 
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 49. Term must be either 1 -9, B-O or S -X.   
**Result:** Record rejected
EXAMPLE  
The records in the first and third examples listed below would be rejected because the Term code is 
invalid. The second record would be rejected because the Term code was left bank.  
Florida  
Education  
Identifier  Course  
Number  Term  
* FL240123457000  1200310  P 
* FL240123457000  1001310   
* FL240123457000  2000310  A 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Term 
and resubmit the record.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 4A. Blended Learning Course code must be Y or N.   
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Blended Learning Course code is 
not valid.  
District Number,  
Current 
Instruction/  
Service  School Number,  
Current 
Instruction/  
Service  Social  
Security  
Number  Course  
Number  Section  
Number  Period  
Number  Blended  
Learning  
Course  
18 0091  123456789  5100060  001 0106  Y 
18 0091  123456790  5100070  002 0106  N 
*18 0091  123456791  5100080  003 0106  Z 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Blended Learning Course code and resubmit the record.  
  
  
 
Student Database 202 6-2027 /  
## Reject Rules

### 4B. If School Number, Current Instruction/Service = 7001, 7004, 7006 or 7023; or District Number, Current 
Instruction/Service =71; or Charter School Status is not Z and School Function/ Setting equals V on the 
Master School Identification file, then Blended Le arning Course must equal N.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Blended Learning Course code is 
not a valid code.  
District Number,  
Current Instruction/  
Service  School Number,  
Current Instruction/  
Service  Florida  
Education  
Identifier  Course  
Number  Blended  
Learning  
Course  
01 0021  FL123456789000  1200310  Y 
01 0021  FL123456790000  1200310  N 
*01 7001  FL123456791000  1200300  Y 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Blended Learning Course code and resubmit the record.  
  
  
 
Student Database 202 6-2027 /  
## State Validation

### 51. Each  Schedule record must have a matching Student Course Schedule record based on 
District Number, Current Instruction/Service; School Number, Current Instruction/Service; Survey Period 
Code; Fiscal Year; Term; Course Number; Section Number and Period Number.  
## State Validation

EXAMPLE  
The first  Schedule record listed below would pass this edit because it has a matching 
Student Course Schedule record based on District Number, Current Instruction/Service; School Number, 
Current Instruction/Service; Survey Period Code; Fisca l Year; Term; Course Number; Section Number and 
Period Number. The second  Schedule record listed below would cause a state validation 
error report message to be generated because there is no matching Student Course Schedule record.  
 Student Course Schedule records  
Florida  
Education  
Identifier  District 
Number,  
Current 
Instruction/  
Service  School 
Number,  
Current 
Instruction/  
Service  Survey  
Period  
Code  Fiscal  
Year  Term  Course  
Number  Section  
Number  Period  
Number  
FL101234567899  01 0421  2 ****  1 1200300  00200  04014  
FL101234567888  01 0421  2 ****  1 1200300  00200  0404  
FL101234567888  01 0421  2 ****  1 1200300  00100  0303  
  
  Schedule records  
District 
Number,  
Current 
Instruction/  
Service  School 
Number,  
Current 
Instruction/  
Service  Survey  
Period  
Code  Fiscal  
Year  Term  Course  
Number  Section  
Number  Period  
Number  Social  
Security  
Number  
01 0421  2 ****  1 1200300  00200  04014  123456789  
*01 0421  2 ****  1 1200300  00100  0404  123456790  
 **** = Valid fiscal year for data submission  

**District Responsibility:** The district must verify if the  Schedule record is valid, then submit a matching Student 
Course Schedule record for that class based on District Number, Current Instruction/Service; School 
Number, Current Instruction/Service; Survey Period C ode; Fiscal Year; Term; Course Number; Section 
Number; and Period Number.   
  
 
Student Database 202 6-2027 /  
## State Validation

### 53. If Survey Period Code equals 2 or 3 and  
• District of Instruction is not = 68 or 71  
• School of Instruction is not = 9996, or begins with an alpha character and  
• School of Instruction’s function setting on MSID does not equal D or V (DJJ or Virtual) and  
• Blended Learning Course = N and  
• Period Number does not end in 88 and  
• Facility Type = 00, 01, 03, 04, 11 -20 and  
• Facility Type = 09 with numeric course and  
• Class Size Core Course Indicator on the Course Code Directory = Y ,  
Then for each  record with a Scheduling Method equal to A, all other  
records with the same District Number, Current Instruction Service; School Number, Current 
Instruction/Service; Period Number; Term; Classroom Identification Number; Survey Period Code and 
Fiscal Year must have the same Scheduling Method unless the Scheduling Method is I.  
OR  
Then for each  record with a Scheduling Method equal to C or M, at least one other 
 record must exist with the same District Number, Current Instruction Service; School 
Number, Current Instruction/Service; Period Number; Term; C lassroom Identification Number; Survey 
Period Code and Fiscal Year and a Scheduling Method of C or M.  
## State Validation

EXAMPLE  
The first and third  records listed below would pass this edit. The second  
record would not pass this edit because Scheduling Method is not identical to another  
record based on the key fields listed in the edit n or does Scheduling Method equal I and Period Number 
does not end in 88.  
District 
Number,  
Current 
Instruction/  
Service  School 
Number,  
Current 
Instruction/  
Service  Term  Period  
Number  Classroom  
Identification  
(FISH)  
Number  Scheduling  
Method  Survey  
Period  
Code  Fiscal  
Year  
62 0151  3 0106  12345A123451234512345  A 3 ****  
*62 0151  3 0106  12345A123451234512344  C 3 ****  
62 0151  3 0106  12345A123451234512345  I 3 ****  
 **** = Valid fiscal year for data submission.     

**District Responsibility:** Student Database 202 6-2027 /  
 
 The district must verify whether the  record is valid and, if so, submit a matching Teacher 
Course record based on School Number, Current Instruction/Service; Period Number; Term; Classroom 
Identification Number, Survey Period Code and Fiscal  Year.  
  
  
 
Student Database 202 6-2027 /  
## State Validation

### 54. Instruction/Service; School Number, Current Instruction/Service; Fiscal Year; Survey Period Code; 
Classroom Identification (FISH) Number; Course Number; and Period Number the following conditions 
must be true:  
• If Survey Period Code is 2 or 3, Term is 6 and Term/Survey Indicator is Y , then records with Term 7 
must have a Term/Survey Indicator of N.  
• If Survey Period Code is 2 or 3, Term is 7 and Term/Survey Indicator is Y , then records with Term 6 
must have a Term/Survey Indicator of N.  
## State Validation

EXAMPLE  
The  Schedule records listed below which are marked with an asterisk would cause a state 
validation error report message to be generated because their Term codes are different,  but their 
Term/Survey Indicator codes are both Y .  
The two records below have been reported with the same Classroom Identification (FISH) Number.  
District Number,  
Current 
Instruction/  
Service  School 
Number,  
Current 
Instruction/  
Service  Survey  
Period  
Code  Fiscal  
Year  Term  Course  
Number  Period  
Number  Term/  
Survey  
Indicator  
*59 0421  2 ****  6 1200300  0505  Y 
*59 0421  2 ****  7 1200300  0505  Y 
 **** = Valid fiscal year for data submission.  

**District Responsibility:** The district must review the records and correct the Term and/or Term/Survey Indicator code that is in 
error.  
  
  
 
Student Database 202 6-2027 /  
## State Validation

### 55. For all  records that match on District Number, Current In struction/Service; School 
Number, Current Instruction/Service; Fiscal Year; Survey Period Code; Classroom Identification (FISH) 
Number; Course Number; and Period Number the following conditions must be true:  
• If Survey Period Code is 2 or 3, Term is 8 and Term/Survey Indicator is Y , then records with Term 9 
must have a Term/Survey Indicator of N.  
• If Survey Period Code is 2 or 3, Term is 9 and Term/Survey Indicator is Y , then records with Term 8 
must have a Term/Survey Indicator of N.  
## State Validation

EXAMPLE  
The  Schedule records listed below which are marked with an asterisk would cause a state 
validation error report message to be generated because their Term codes are different,  but their 
Term/Survey Indicator codes are both Y .  
The two records below have been reported with the same Classroom Identification (FISH) Number.  
District Number,  
Current 
Instruction/  
Service  School 
Number,  
Current 
Instruction/  
Service  Survey  
Period  
Code  Fiscal  
Year  Term  Course  
Number  Period  
Number  Term/  
Survey  
Indicator  
*59 0421  2 ****  8 1200300  0505  Y 
*59 0421  2 ****  9 1200300  0505  Y 
 **** = Valid fiscal year for data submission.  

**District Responsibility:** The district must review the records and correct the Term and/or Term/Survey Indicator code that is in 
error.  
  
  
 
Student Database 202 6-2027 /  
## State Validation

### 56. For all  records that match on District Number, Current Instruction/Service; School 
Number, Current Instruction/Service; Fiscal Year; Survey Period Code; Classroom Identification (FISH) 
Number; Course Number; and Period Number the following c ondition must be true:  
If Survey Period Code is 2 and Term is J, K, or L, only one of these Terms may have a Term/Survey 
Indicator of Y .  
## State Validation

EXAMPLE  
The  Schedule records listed below which are marked with an asterisk would cause a state 
validation error report message to be generated because two of the records have Term/Survey Indicator 
codes of Y .  
The three records below have been reported with the same Classroom Identification (FISH) Number.  
District Number,  
Current 
Instruction/  
Service  School 
Number,  
Current 
Instruction/  
Service  Survey  
Period  
Code  Fiscal  
Year  Term  Course  
Number  Period  
Number  Term/  
Survey  
Indicator  
*59 0421  2 ****  J 1200300  0505  Y 
*59 0421  2 ****  K 1200300  0505  N 
*59 0421  2 ****  L 1200300  0505  Y 
 **** = Valid fiscal year for data submission.  

**District Responsibility:** The district must review the records and correct the Term and/or Term/Survey Indicator code that is in 
error.  
  
  
 
Student Database 202 6-2027 /  
## State Validation

### 57. For all  records that match on District Number, Current Instruction/Service; School 
Number, Current Instruction/Service; Fiscal Survey Period Code; Classroom Identification (FISH) Number; 
Course Number and Period Number the following conditio n must be true:  
If Survey Period Code is 3 and Term is M, N, or O, only one of these Terms may have a Term/Survey 
Indicator of Y .  
## State Validation

EXAMPLE  
The  Schedule records listed below which are marked with an asterisk would cause a state 
validation error report message to be generated because two of the records have Term/Survey Indicator 
codes of Y .  
The three records below have been reported with the same Classroom Identification (FISH) Number.  
District Number,  
Current 
Instruction/  
Service  School 
Number,  
Current 
Instruction/  
Service  Survey  
Period  
Code  Fiscal  
Year  Term  Course  
Number  Period  
Number  Term/  
Survey  
Indicator  
*59 0421  3 ****  M 1200300  0505  Y 
*59 0421  3 ****  N 1200300  0505  N 
*59 0421  3 ****  0 1200300  0505  Y 
 **** = Valid fiscal year for data submission.  

**District Responsibility:** The district must review the records and correct the Term and/or Term/Survey Indicator code that is in 
error.  
  
  
 
Student Database 202 6-2027 /  
## State Validation

### 58. For all  records that match on District Number, Current Instruction/Service; School 
Number, Current Instruction/Service; Fiscal Survey Period Code; Classroom Identification (FISH) Number; 
Course Number and Period Number the following conditio n must be true:  
If Survey Period Code is 2 or 3 and Term is E, F, G, H, or I, only one of these Terms may have a 
Term/Survey Indicator of Y .  
## State Validation

EXAMPLE  
The  Schedule records listed below which are marked with an asterisk would cause a state 
validation error report message to be generated because two of the records have Term/Survey Indicator 
codes of Y .  
The four records below have been reported with the same Classroom Identification (FISH) Number.  
District Number,  
Current 
Instruction/  
Service  School 
Number,  
Current 
Instruction/  
Service  Survey  
Period  
Code  Fiscal  
Year  Term  Course  
Number  Period  
Number  Term/  
Survey  
Indicator  
*59 0421  3 ****  E 1200300  0505  Y 
*59 0421  3 ****  F 1200300  0505  N 
*59 0421  3 ****  G 1200300  0505  N 
*59 0421  3 ****  H 1200300  0505  Y 
 **** = Valid fiscal year for data submission.  

**District Responsibility:** The district must review the records and correct the Term and/or Term/Survey Indicator code that is in 
error.  
  
  
 
Student Database 202 6-2027 /  
## State Validation

### 59. For all  records that match on District Number, Current Instruction/Service; School 
Number, Current Instruction/Service; Fiscal Survey Period Code; Classroom Identification (FISH) Number; 
Course Number and Period Number the following conditio n must be true:  
 If Survey Period Code is 2 or 3 and Term is B, C or D, only one of these Terms may have a Term/Survey 
Indicator of Y .  
## State Validation

EXAMPLE  
The  Schedule records listed below which are marked with an asterisk would cause a state 
validation error report message to be generated because two of the records have Term/Survey Indicator 
codes of Y .  
The three records below have been reported with the same Classroom Identification (FISH) Number.  
District Number,  
Current 
Instruction/  
Service  School 
Number,  
Current 
Instruction/  
Service  Survey  
Period  
Code  Fiscal  
Year  Term  Course  
Number  Period  
Number  Term/  
Survey  
Indicator  
*59 0421  3 ****  B 1200300  0505  Y 
*59 0421  3 ****  C 1200300  0505  N 
*59 0421  3 ****  D 1200300  0505  Y 
 **** = Valid fiscal year for data submission.  

**District Responsibility:** The district must review the records and correct the Term and/or Term/Survey Indicator code that is in 
error.  
  
  
 
Student Database 202 6-2027 /  
## State Validation

### 5A. For all  records that match on District Number, Current Instruction/Service; School 
Number, Current Instruction/Service; Fiscal Year; Survey Period Code; Classroom Identification (FISH) 
Number; Course Number; and Period Number the following c ondition must be true:  
If Survey Period Code is 2 or 3 and Term is T, U, V, W or X, only one of these Terms may have a 
Term/Survey Indicator of Y .  
## State Validation

EXAMPLE  
The  Schedule records listed below which are marked with an asterisk would cause a state 
validation error report message to be generated because two of the records have Term/Survey Indicator 
codes of Y .  
The four records below have been reported with the same Classroom Identification (FISH) Number.  
District Number,  
Current 
Instruction/  
Service  School 
Number,  
Current 
Instruction/  
Service  Survey  
Period  
Code  Fiscal  
Year  Term  Course  
Number  Period  
Number  Term/  
Survey  
Indicator  
*59 0421  3 ****  T 1200300  0505  Y 
*59 0421  3 ****  U 1200300  0505  N 
*59 0421  3 ****  V 1200300  0505  N 
*59 0421  3 ****  W 1200300  0505  Y 
 **** = Valid fiscal year for data submission.  

**District Responsibility:** The district must review the records and correct the Term and/or Term/Survey Indicator code that is in 
error.  
  
  
 
Student Database 202 6-2027 /  
## State Validation

### 5B. If Survey Period Code is 2 or 3, then all  records that match on District Number, Current 
Instruction/Service; School Number, Current Instruction/Service; Fiscal Year; Survey Period Code; 
Classroom Identification (FISH) Number; Course Number;  Period Number and Term must have the same 
Term/Survey Indicator.  
## State Validation

 EXAMPLE  
The  Schedule records listed below which are marked with an asterisk would cause a state 
validation error report message to be generated because they have different Term/Survey Indicator 
codes.  
The two records below have been reported with the same Classroom Identification (FISH) Number.  
District Number,  
Current 
Instruction/  
Service  School 
Number,  
Current 
Instruction/  
Service  Survey  
Period  
Code  Fiscal  
Year  Term  Course  
Number  Period  
Number  Term/  
Survey  
Indicator  
*59 0421  2 ****  6 1200300  0505  Y 
*59 0421  2 ****  6 1200300  0505  N 
 **** = Valid fiscal year for data submission.  

**District Responsibility:** The district must review the records and correct the Term and/or Term/Survey code that is in error.  
  
  
 
Student Database 202 6-2027 /  
## State Validation

### 5C. If Survey Period Code is 2 or 3, then at least one Primary Instructor Indicator Code must be Y for Teacher 
Course Schedule records that are matched on District Number, Current Instruction/Service; School 
Number, Current Instruction/Service; Survey Period C ode; Fiscal Year; Term; Classroom Identification 
(FISH) Number and Period Number.  
## State Validation

EXAMPLE  
The  Schedule records listed below would cause a state validation error report message to 
be generated because there is no record with the Primary Instructor Indicator of Y for records matched 
based on District Number, Current  
Instruction/Service; School Number, Current Instruction/Service; Survey Period Code; Fiscal Year; Term; 
Classroom Identification (FISH) Number and Period Number.  
Social  
Security  
Number  District 
Number,  
Current 
Instruction/  
Service  School 
Number,  
Current 
Instruction/  
Service  Survey  
Period  
Code  Term  Classroom  
Identification  
(FISH)  
Number  Period  
Number  Term/  
Survey  
Indicator  
*0123456789  01 0421  2 1 # 0404  N 
*0896456891  01 0421  2 1 # 0404  N 
*1258456766  01 0421  2 1 # 0404  N 
 # The FISH NUMBER used in the examples above is 00421A000210000400121  

**District Responsibility:** The district must determine which teacher is the primary instructor for the class listed and change the 
Primary Instructor Indicator on that  Schedule record to Y .  
  
  
 
Student Database 202 6-2027 /  
## State Validation

### 5E. If Survey Period Code is 2 or 3 and if  records match on District Number, Current 
Instruction/Service; School Number, Current Instruction/Service; Fiscal Year; Survey Period Code; Term; 
Course Number; Section Number; and Period Number; then C lassroom Identification (FISH) Number 
must be the same.  
## State Validation

EXAMPLE  
The first set of  records listed below would pass this edit because the matching Teacher 
Course records have the same Classroom Identification (FISH) Numbers. The second set of Teacher 
Course records listed below would cause a state validatio n error report message to be generated 
because the matching  records have different Classroom Identification (FISH) Numbers.  
 records    
 Record 1  Record 2  
District Number, Current  
Instruction/Service  01 01 
School Number, Current  
Instruction/Service  0421  0421  
Survey Period Code  2 2 
Fiscal Year  ****  ****  
Term  1 1 
Course Number  1200300  1200300  
Section Number  00200  00200  
Period Number  0202  0202  
Social Security Number  123456789  226456790  
Classroom Identification (FISH) Number  12345A123451234512345  12345A123451234512345  
 
 Records  
 Record 1  Record 2  
District Number, Current  
Instruction/Service  01 01 
School Number, Current  
Instruction/Service  0421  0421  
Survey Period Code  2 2 
Fiscal Year  ****  ****  
Term  1 1 
Course Number  1200300  1200300  
  
 
Student Database 202 6-2027 /  
 
 Section Number  00200  00200  
Period Number  0404  0404  
Social Security Number  988654321  456897321  
Classroom Identification (FISH) Number  12345A123451234512345  45365A778451234512345  
 **** = Valid fiscal year for data submission.  

**District Responsibility:** If the two teachers are teaching the same class then the district must correct the Classroom 
Identification (FISH) Number on one of the  records so that the two records have the 
same FISH number. If one of the  records should no t have been submitted, the district 
should delete this incorrect record.  
  
  
 
Student Database 202 6-2027 /  
## State Validation

### 5F. For Survey Periods 2 and 3,  
• If the course is not a dual enrollment course at a postsecondary institution, and  
• If School Number, Current Instruction/Service is not 7001 or 7006, and  
• If School Number, Current Instruction/Service is not 7004 and 7023 in one of the following 
District Numbers, Current Instruction/Service: 02, 04, 07, 12, 14, 15, 19, 20, 21, 22, 23, 24, 25, 
26, 28, 30, 32, 33, 34, 38, 39, 40, 44, 45, 46, 47, 54, 62, 65, 67 , 73 and 75  
• If Charter School Status is not R, C, T or B and School Function Setting is not V,  
• If Location of Student code is not T on the Student Course Schedule record (matching on District 
Number, Current Instruction/Service; School Number Current Instruction/Service; Survey Period 
Code; Fiscal Year; Term; Course Number; Section Number and Period  Number),  
  
then each  Schedule record must have a matching Staff Demographic Information record 
based on District Number, Current Instruction/Service; Survey Period Code; Fiscal Year; Social Security 
Number and Staff Number Identifier, Local,  
  
Dual enrollment records are those with School Number, Current Instruction/Service of C901 -C928, U970 -
U981 or P001 -P999 and those with an alphanumeric course number at any School Number, Current 
Instruction/Service.  
## State Validation

EXAMPLE  
The first  Schedule record listed below would pass this edit because it has a matching 
Staff Demographic Information record based on District Number, Current Instruction/Service; Survey 
Period Code; Fiscal Year; Social Security Number and Sta ff Number Identifier, Local. The second Teacher 
Course Schedule record listed below would cause a state validation error report message to be 
generated because there is no matching Staff Demographic Information record.  
  Schedule records  
District Number,  
Current Instruction/  
Service  Survey  
Period  
Code  Fiscal  
Year  Social  
Security  
Number  Staff Number,  
Identifier,  
Local  
01 2 ****  123456789  ABC123DEF9  
*01 2 ****  123456790  BCD456EFG8  
 **** = Valid fiscal year for data submission.  
 
  
 
Student Database 202 6-2027 /  
 
  
Staff Demographic Information records  
District Number,  
Current Instruction/  
Service  Survey  
Period  
Code  Fiscal  
Year  Social  
Security  
Number  Staff Number,  
Identifier,  
Local  
01 2 ****  123456789  ABC123DEF9  
*01 2 ****  123456791  BCD456EFG8  
 **** = Valid fiscal year for data submission.  

**District Responsibility:** The district must verify that the  Schedule record is valid and submit a matching Staff 
Demographic Information record on the Staff Information Database based on District Number, Current 
Instruction/Service; Survey Period Code; Fiscal Year; S ocial Security Number and Staff Number Identifier, 
Local.  
  
  
 
Student Database 202 6-2027 /  
 
 VALIDATION RULE  

### 5G. If Survey Period Code is 2 or 3, and the Scheduling Method code is D, there must be a matching Staff 
Demographic Information record based on District Number, Current Instruction/Service; Survey Period 
Code; Fiscal Year; Social Security Number; and Staff Nu mber Identifier, Local; for which the Job Code on 
the matching Staff Demographic Information record must be 59050.  
## State Validation

EXAMPLE  
The first  record listed below would pass this validation because there is a matching Staff 
Demographic Information record based on the key fields and Job Code is 59050 for Teacher 
Apprenticeship Program Indicator code of Y . The second Teache r Course record would not pass this edit 
because the matching Staff Demographic Information record does not have a Scheduling Method code D. 
The third  record would not pass this edit because the Job Code on the matching Staff 
Demographic Inf ormation record is not 59050.  
  
District Number, 
Current 
Instruction/Service  School Number, 
Current 
Instruction/Service  Survey 
Period 
Code  Fiscal 
Year  Term  Course 
Number  Section 
Number  SSN Staff 
Number 
Identifier, 
Local  Scheduling 
Method  
01 0421  2 ****  1 1200300  00200  123456789  ABC123  D 
* 01  0421  2 ****  1 1206310  00100  987654321  DEF456  A 
* 01  0421  3 ****  4 1206320  00100  997654321  DEF123  D 
 
Staff Demographic Information  
District Number, 
Current 
Instruction/Service  Survey 
Period 
Code  Fiscal 
Year  Social 
Security 
Number  Staff 
Number 
Identifier, 
Local  Job 
Code  Teacher 
Apprenticeship 
Program 
Indicator  
01 2 ****  123456789  ABC123  59050  Y 
*01 2 ****  987654321  DEF456  59050  Y 
*01 3 ****  997654321  DEF123  61000  Y 
**** = Valid fiscal year for data submission.  
 
  
 
Student Database 202 6-2027 /  

**District Responsibility:** The district must verify the relationship between the Scheduling Method code on the  
record and the Job Code on the matching Staff Demographic Information record. If the Scheduling 
Method code is D and the Job Code is not 59050 , the district must determine which code is incorrect. If 
the Job Code is incorrect, the district must correct the Job Code on the Staff Demographic Information 
record. If the Scheduling Method is incorrect, the district must correct the Scheduling Method code on 
the Tea cher Course record to a valid code other than D for that staff member. Then, the corrected 
record(s) must be resubmitted.  
  
  
 
Student Database 202 6-2027 /  
 
 VALIDATION RULE  

### 5H. If Survey Period Code 2 or 3, for each  record with a Scheduling Method equal to D  there 
must exist at least one other  record with a different Social Security Number and a 
different Scheduling Method that is not G, I, or D base d on District Number, Current Instruction/Service; 
School Number, Current Instruction/Service; Survey Period Code; Fiscal Year; Term; Course Number; 
Section Number; and Period Number.  
## State Validation

EXAMPLE  
The first and second  records listed below will pass this edit. The third record listed below 
would not pass this edit because another  record based on the indicated fields of the edit 
does not exist.  
  
District Number, 
Current 
Instruction/Service  School Number, 
Current 
Instruction/Service  Survey 
Period 
Code  Fiscal 
Year  Term  Course 
Number  Section 
Number  Period 
Number  SSN Staff 
Number 
Identifier, 
Local  Scheduling 
Method  
01 0421  2 ****  3 1200300  00200  0104  123456789  ABC123  D 
* 01  0421  2 ****  3 1200300  00200  0104  987654321  DEF456  S 
* 01  0421  2 ****  3 1206320  00100  0506  997654321  DEF123  D 
 
**** = Valid fiscal year for data submission.  

**District Responsibility:** The district must verify whether the  record is valid, and, if so, whether a matching 
 record is needed based on District Number, Current Instruction/Service; School Number, 
Current Instruction/Service; Period Code; Fiscal Year;  Term; Course Number; Section Number; and Period 
Number.  
  
  
 
Student Database 202 6-2027 /  
## Exception Reports

UPDATED 04/03/2026  

### 63. Florida Educators Certificate Number must be in the following ranges: 0000000001 – 0000999998, 
0001000000 - 6001999999, 6002000001 - 6002999999, 6003000001 - 6003999999, 6004000001 - 
6004999999,  6007000001 – 6007999999 , or 0000000000, 0000999999, 7777777777, 8888888888 or 
9999999999.  
## Exception Reports

EXAMPLE  
The  records below would cause an exception report to be generated because the Florida 
Educators Certificate Numbers are not valid or in the specified ranges.  
District Number,  
Current Instruction/  
Service  School Number,  
Current Instruction/  
Service  Social  
Security  
Number  Florida Educators  
Certificate  
Number  
*01 0151  123456789  9999999998  
*01 0151  234567891  6123456789  
*01 0151  345678912  8888888889  

**District Responsibility:** The district should verify the Florida Educators Certificate Numbers and correct if in error.  
  
  
 
Student Database 202 6-2027 /  
## Exception Reports

### 65. If Survey Period Code equals 2 or 3, for each  record with a Scheduling Method equal to C 
or M there must exist at least one other  record with a different Social Security Number 
and the same Scheduling Method (at least 2 C’s, 2  M’s) based on District Number, Current 
Instruction/Service; School Number, Current Instruction/Service; Period Number; Classroom 
Identification/FISH Number; Survey Period Code and Fiscal Year.  
## Exception Reports

EXAMPLE  
The first and second  records listed below would  pass this edit. The third record listed 
below would not pass this edit because another  record based on the indicated fields of 
the edit does not exist.  
The following records exist for Classroom Identification (FISH) Number 12345A123451234512345:   
District 
Number,  
Current 
Instruction/  
Service  School 
Number,  
Current 
Instruction/  
Service  Term  Period  
Number  Social  
Security  
Number  Scheduling  
Method  Survey  
Period  
Code  Fiscal  
Year  
*01 0151  3 0104  111223333  C 3 ****  
*01 0151  3 0104  444556666  C 3 ****  
*01 0151  3 0506  777889999  C 3 ****  
 **** = Valid fiscal year for data submission.  

**District Responsibility:** The district must verify whether the  record is valid, and, if so, whether a matching 
 record is needed based on District Number, Current Instruction/Service; School Number, 
Current Instruction/Service; Period Number; Classroom Identification/FISH Number, Survey Period Code 
and Fiscal Year.  
  
  
 
Student Database 202 6-2027 /  
## Exception Reports

### 66. If Survey Period Code equals 2 or 3 and District Number, Current Instruction/Service is not 71; for each 
 record with a Scheduling Method equal to I and the end period is not equal to 88, there 
must exist at least one other  rec ord with a Scheduling Method equal to A, B, C, M, S or 
W based on District Number, Current Instruction/Service; School Number, Current Instruction/Service; 
Period Number; Classroom Identification  (FISH ) Number; Survey Period Code and Fiscal Year, but with a 
different Social Security Number.  
## Exception Reports

EXAMPLE  
The first and second  records listed below would pass this edit. The third record listed 
below would not pass this edit because another  record based on the indicated fields of 
the edit does not exist. The fourth and fifth recor ds would not pass this edit because the two records 
have identical Social Security Numbers.  
District 
Number,  
Current 
Instruction/  
Service  School 
Number,  
Current 
Instruction/  
Service  Survey  
Period  
Code  Period  
Number  Classroom  
Identification  
(FISH)  
Number  Scheduling  
Method  Social  
Security  
Number  Fiscal  
Year  
62 0151  3 0106  12345A123451234512345  C 123456789  ****  
62 0151  3 0106  12345A123451234512345  I 123456780  ****  
*62 0151  3 0106  23456A234562345623456  I 123456781  ****  
*62 0151  3 0106  23456A234562345623457  S 123456782  ****  
*62 0151  3 0106  23456A234562345623457  I 123456782  ****  
**** = Valid fiscal year for data submission.  

**District Responsibility:** The district must verify whether the  record is valid, and, if so, whether a matching 
 record is needed (based on District Number, Current Instruction/Service; School Number, 
Current Instruction/Service; Period Number; Classroom  Identification  (FISH ) Number . 
  
  
 
Student Database 202 6-2027 /  
## Exception Reports

### 67. If Survey Period Code equals 2 or 3, for each  record with a Scheduling Method equal to 
A, there must exist at least one other  record with a different Course/Section combination 
and the same Scheduling Method (at least 2 A’s), District Number, Current Instruction/Service; School 
Number, Current Instruction/Service; Period Number; Classroom Identification (FISH) Number; Survey 
Period Code and Fiscal Year.  
## Exception Reports

EXAMPLE  
The first and second  records listed below would pass this edit. The third record listed 
below would not pass this edit because another  record based on the indicated fields of 
the edit does not exist.  
The following records exist for Classroom Identification (FISH) Number 12345A123451234512345:   
District 
Number,  
Current 
Instruction/  
Service  School 
Number,  
Current 
Instruction/  
Service  Course  Section  
Number  Period  
Number  Social  
Security  
Number  Scheduling  
Method  Survey  
Period  
Code   
Fiscal  
Year  
*01 0151  5010040  0104   111223333  A 3 ****  
*01 0151  5010040  0104   444556666  A 3 ****  
*01 0151  5012000  0506   777889999  A 3 ****  
 **** = Valid fiscal year for data submission.    

**District Responsibility:** The district must verify whether the  record is valid, and, if so, whether a matching 
 record is needed based on District Number, Current Instruction/Service; School Number, 
Current Instruction/Service; Period Number; Classroom Identification/FISH Number, Survey Period Code 
and Fiscal Year.  
  
  
 
Student Database 202 6-2027 /  
## Exception Reports

### 68. If Survey Period Code is 2 or 3 and  
• District of Instruction is not = 68 and  
• School of Instruction is not = 9996, or begins with an alpha character and  
• School of Instruction’s function setting on MSID does not equal D or V (DJJ or Virtual) and  
• Blended Learning Course = N and  
• Period Number does not end in 88 and  
• Facility Type = 00, 01, 03, 04, 11 -20 or  
• Facility Type = 09 with a numeric course and  
• Scheduling Method = C and  
• Class Size Core Course Indicator on the Course Code Directory = Y ,  
then for all  records that match on District Number, Current Instruction/Service; School 
Number, Current Instruction/Service;  
Fiscal Year; Survey Period Code; Classroom Identification (FISH) Number; Course Number; and Period 
Number and Scheduling Method “C”, the following conditions must be true:  
• At least one  record must have Certification/Licensure/ Qualification Status 
equal to A, H, I, L, M, P , S, T or V  
• At least one teacher in the group of  records must have at least a sum of three 
years’ experience on the Staff Experience format where Experience Type equals F, N, P or S. Must 
match by District Number, SSN, Survey Period, Year  
• Same teacher does not need to satisfy both conditions  
## Exception Reports

EXAMPLE  
The below records would cause an exception report to be generated because although the 
Certification/Licensure/Qualification Status is met, there must be at least one Staff Experience record 
where Experience Length is reported as three or more years for th e team.  
 records  
District 
Number,  
Current 
Instruction/  
Service  School 
Number,  
Current 
Instruction/  
Service  Fiscal  
Year  Survey  
Period  
Code  Social  
Security  
Number  Course  
Number  Period  
Number  Scheduling  
Method  Certification/  
Licensure/  
Qualification  
Status  
01 0151  ****  3 123456789  1002360  0106  C I 
01 0151  ****  3 345678910  1002360  0106  C M 
 ****= Valid fiscal year for data submission  
 Staff Experience records  
  
 
Student Database 202 6-2027 /  
 
 District Number,  
Current Instruction/  
Service  School Number,  
Current Instruction/  
Service  Survey  
Period  
Code  Fiscal  
Year  Experience  
Length  
01 123456789  3 ****  1 
01 345678910  3 ****  2 
 ****= Valid fiscal year for data submission  

**District Responsibility:** The district should verify the Certification/Licensure/Qualification Status on the  record 
and the Experience Length on the Staff Experience format, and correct if in error.  
  
  
 
Student Database 202 6-2027 /  
## Exception Reports

### 69. If Survey Period Code is 2 or 3 and  
• District of Instruction is not = 68 and  
• School of Instruction is not = 9996, or begins with an alpha character and  
• School of Instruction’s function setting on MSID does not equal D or V (DJJ or Virtual) and  
• Blended Learning Course = N and  
• Period Number does not end in 88 and  
• Facility Type = 00, 01, 03, 04, 11 -20 or  
• Facility Type = 09 with a numeric course and  
• Scheduling Method = I and  
• Class Size Core Course Indicator on the Course Code Directory = Y ,  
 
then for all  records that are also Class Size Core Course indicated with Y on the Course 
Code Directory that match on District Number, Current Instruction/Service; School Number, Current  
Instruction/Service; Fiscal Year; Survey Period Code; Classroom Identification (FISH) Number; and Period 
Number, the following conditions must be true:  
• At least one  record must have Certification/Licensure/Qualification Status  equal 
to A, H, I, L, M, P , S, T or V  
• At least one teacher in the group of  records must have at least a sum of three 
years’ experience on the Staff Experience format where Experience Type equals F, N, P or S.  
• Must match by District Number, SSN, Survey Period, Year  
• Same teacher does not need to satisfy both conditions  
## Exception Reports

EXAMPLE  
The records listed below would cause an exception report to be generated because it does not have a 
matching Staff Experience record for at least one teacher on the team that meets the Experience Length 
of three or more years.  
  records     
District 
Number,  
Current 
Instruction/  
Service  School 
Number,  
Current 
Instruction/  
Service  Fiscal  
Year  Survey  
Period  
Code  Social  
Security  
Number  Course  
Number  Period  
Number  Scheduling  
Method  Certification/  
Licensure/  
Qualification  
Status  
01 0151  ****  3 123456789  1004560  0505  I S 
31 0151  ****  3 123459876  1004560  0505  S I 
 ****= Valid fiscal year for data submission  
  
 
Student Database 202 6-2027 /  
 
  Staff Experience records  
District  
Number  Social  
Security  
Number  Survey  
Period  
Code  Fiscal  
Year  Experience  
Length  
01 123456789  3 ****  2 
01 123459876  3 ****  1 
 ****= Valid fiscal year for data submission  

**District Responsibility:** The district should verify the Certification/Licensure/Qualification Status on the  record 
and the Experience Length on the Staff Experience format, and correct if in error.