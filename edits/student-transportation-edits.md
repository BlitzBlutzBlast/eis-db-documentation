# Student Transportation — Edits and Reject Rules

Source: Florida DOE
Manual: Student Database 2026-2027

Student Database 202 6-2027 /  
## Reject Rules

UPDATED 07/01/2026   

### 1. District Number, Current Instruction/Service must be numeric and active (A) on the Appendix C: District 
Name Table.  
**Result:** Record rejected
 EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected since the District Number, Current 
Instruction/Service is not in the appropriate range.  
  
District Number,  
Current Instruction/  
Service  Florida  
Education  
Identifier  
01 FL123456789100  
01 FL123456789200  
*00 FL123456789300  

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the District 
Number, Current Instruction/Service and resu bmit the record.  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 2. District Number, Current Instruction/Service must be correct for the district  submitting the data.   
**Result:** Record rejected
EXAMPLE  
If district 01 is submitting records, District Number, Current Instruction/Service must be 01 for all 
records. In the records listed below, the first two records would be loaded to the database assuming no 
other reject rule would cause their rejection. The  third record would be rejected since the District 
Number, Current Instruction/Service is 02 rather than 01 (the number of the district submitting the 
record).    
  
District Number,  
Current Instruction/  
Service  Florida  
Education  
Identifier  
01 F123456789100  
01 F123456789200  
*02 F123456789300  

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the District 
Number, Current Instruction/Service and resu bmit the record.  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 4. Survey Period Code must be 1, 2, 3, or 4 and must be correct for the submission specified by the district.   
**Result:** Record rejected
EXAMPLE  
The Survey Period Code as specified in the transmission JCL or in the statements for tape transmission is 
identified as Survey Period Code "2" and records are coded with Survey Period Code "3". All updates, 
adds, or deletes with this inconsistency are reje cted.  

**District Responsibility:** Correct the Survey Period Code either on the records coming in or the transmission JCL and resubmit all 
of the records.  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 5. The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent 
batch/update submissions, if A is specified then the record must not already exist on the database; if C 
or D is specified then the record must exist on the database.   
**Result:** Record rejected
EXAMPLE  
For all original transmissions, the Transaction Code must be "A". An original transaction is the first 
submission of a record during a survey period. After original transmission of records, changes to the 
record for elements other than the key elements mus t be done with a "C" as the Transaction Code. To 
delete a record, the Transaction Code must be a "D". To change key elements in a batch transaction, the 
record must FIRST be deleted with a "D" and then added with an "A". Records with an incorrect 
Transacti on Code are rejected.  

**District Responsibility:** If the rejected records should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected records to be applied to the database, the district must correct the 
Transaction Code and resubmit the records.  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 6. Fiscal Year must be correct for the submission specified by the district.   
**Result:** Record rejected
 EXAMPLE  
 The Fiscal Year as specified in the Transmission JCL or in the statements for tape transmission is 
identified as the valid year for data submission but records being submitted have the previous Fiscal Year 
coded. All updates adds or deletes that have this  inconsistency are rejected.  

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the Fiscal 
Year and resubmit the records.  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 7. Days in Term (for FTE Purposes) must be numeric, greater than zero and  less than 100.  
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second and third records would be rejected because the Days in Term (for FTE 
Purposes) is not numeric or contains blanks.  
  
District Number,  
Current Instruction / 
Service  Florida  
Education  
Identifier  Survey  
Period  
Code  Days in Term  
(for FTE  
Purposes)  
01 F123456789200  2 090 
*01 F123456729200  2 A90 
*01 F123456189200  3 90 

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct Days in 
Term (for FTE Purposes) and resubmit the records . 
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 8. Year -Round/Extended School Year FTE Indicator must be A or Z.   
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Year -Round Extended School Year 
FTE Indicator code is not valid on this format.    
District Number,  
Current Instruction / 
Service  Florida  
Education  
Identifier  Survey  
Period  
Code  Year -Round/  
Extended School Year  
FTE Indicator  
01 FL123456789100  2 A 
01 FL123456789200  2 Z 
*01 FL123456789300  2 B 

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Year -
Round/Extended School Year FTE Indicator code an d resubmit the record.  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 9. Bus Number must not contain all spaces (blanks).   
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the number contains all blanks.  
District Number,  
Current Instruction / 
Service  Florida  
Education  
Identifier  Bus 
Number  
01 F123456789100  123456789  
01 F123456789200  1234567ABC  
*01 F123456789300   

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Bus 
Number and resubmit the record.  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 10. Bus Route Number must not contain all spaces (blanks).   
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Bus Route Number contains all 
blanks.  
District Number,  
Current Instruction / 
Service  Florida  
Education  
Identifier  Bus 
Route  
Number  
01 FL123456789100  12345678  
01 FL123456789200  65432ABC  
*01 FL123456789300   

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Bus 
Route Number and resubmit the record.  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 11. Vehicle Category must be B, E, P , or G.    
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Vehicle Category code is not valid.  
District Number,  
Current Instruction / 
Service  Florida  
Education  
Identifier  Vehicle  
Category  
01 FL123456789100  B 
01 FL123456789200  G 
*01 FL123456789300  H 

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Vehicle 
Category code and resubmit the record.  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 12. Transportation Membership Category must be F, G, L, M, or N.  
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Transportation Membership 
Category code is not valid.  
District Number,  
Current Instruction / 
Service  Florida  
Education  
Identifier  Transportation  
Membership  
Category  
01 FL123456789100  L 
01 FL123456789200  M 
*01 FL123456789300  D 

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Transportation Membership Category code and resubmit the record.  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 13. Each  record must be unique based on District Number, Current 
Instruction/Service; Florida Education Identifier; Survey Period Code, Fiscal Year and Year -
Round/Extended School Year FTE Indicator.    
**Result:** First record accepted, all other duplicate records rejected
EXAMPLE  
The first, third and fourth records listed below would be loaded to the database assuming no other 
reject rule would cause their rejection. The second and fifth records would be rejected since they are 
duplicates (same District Number, Current Instruction/ Service; Florida Education Identifier; Survey Period 
Code; Fiscal Year and Year -Round/Extended Year FTE Indicator) of the first and fourth records, 
respectively.   
District Number , 
Current Instruction / 
Service  Florida  
Education  
Identifier  Survey  
Period  
Code  Fiscal  
Year  Year -Round/  
Extended  
School Year  
FTE Indicator  
01 FL123456789100  2 ****  A 
*01 FL123456789 100 2 ****  A 
01 FL123456789200  2 ****  A 
01 FL123456789400  2 ****  A 
*01 FL123456789 400 2 ****  A 
 ****= Valid fiscal year for data transmission.  

**District Responsibility:** If the records that were accepted and loaded to the database are correct ones, no action is required. 
However, if the district wishes the data in the rejected records to be loaded to the database, the district 
must delete any invalid records, correct any r ejected records if necessary, and resubmit the corrected 
records.   
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 14. If Vehicle Category equals B, then Bus Number must not be all Zs.    
**Result:** Record rejected
 EXAMPLE  
 The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Bus Number contains all Zs.  
  
District Number,  
Current Instruction / 
Service  Vehicle  
Category  Bus 
Number  
01 B 12345678  
01 B 65432ABC  
*01 B ZZZZZZZZZZZZZZZ  

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Bus 
Number and resubmit the record.  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 15. If Vehicle Category equals B, then Bus Route Number must not be all Zs.    
**Result:** Record rejected
EXAMPLE  
 The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Bus Route Number contains all Zs.  
District Number,  
Current Instruction/  
Service  Vehicle  
Category  Bus 
Route  
Number  
01 B 12345678  
01 B 65432ABC  
*01 B ZZZZZZZZZZZZZZZ  

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Bus 
Route Number and resubmit the record.  
  
  
Student Database 202 6-2027 /  
## Reject Rules

UPDATED 07/01/2026   

### 16. District Number, Current Enrollment must be numeric and active (A) on the Appendix C: District Name 
Table.    
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be written to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the District Number, Current 
Enrollment is not in the appropriate range.  
District Number,  
Current Enrollment  District Number , 
Current Instruction/  
Service  Florida  
Education  
Identifier  
01 01 FL123456789100  
01 42 FL123456789200  
*00 01 FL123456789300  
 
RESPONSIBILITY  
If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the District 
Number, Current Enrollment and resubmit the record.  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 17. The Student Number Identifier, Local may be any combination of letters, numbers and blanks. (All blanks 
are allowable.) It must be left -justified with trailing blanks.    
**Result:** Record rejected
EXAMPLE  
The first three records listed below would be loaded to the database assuming no other edit would 
cause their rejection. The fourth record would be rejected because the Student Number Identifier, Local 
contains a symbol (@). The fifth record would be rejec ted because it is right -justified rather than left -
justified.  
District Number,  
Current Enrollment  Student Number  
Identifier, Local  
01 0123456789  
01 ABC123DEF9  
01 3001  28K  
*01 2121@xyz  
*01 123456  

**District Responsibility:** If the rejected records should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected records to be loaded to the database, the district must correct the 
Student Number Identifier, Local and resubmit the r ecords.  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 18. Item 2 - Filler on this format in position numbers 3 -12 must be all spaces.   
**Result:** Record rejected
EXAMPLE  
The first record listed below would be loaded to the database assuming no other reject rule would cause 
its rejection. The second record would be rejected because the data reported is not all spaces.  
District Number,  
Current Instruction/  
Service  Filler  
Item  
#2 
01  
*01 265456789X  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must fill the positions 
noted with all spaces and resubmit the record.  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 19. If Transportation Membership Category is G then Hazardous Walking Code must be 111111, otherwise 
must be 000000 for all other Transportation Membership Categories (F, L, M, N).    
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause its rejection. The third record would be rejected because Transportation Membership Category 
code is G and Hazardous Walking Code is not 111111.    
District Number,  
Current Instruction/  
Service  Florida  
Education  
Identifier  Transportation  
Membership  
Category  Hazardous  
Walking  
Code  
01 FL123456789100  G 111111  
01 FL123456789200  L 000000  
*01 FL123456789200  G 000000  

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Transportation Membership Category code or Hazardous Walking Code and resubmit the record.  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 21. Florida Education Identifier (FLEID) is alphanumeric and must be entered as “FL” in the first 2 positions 
followed by twelve numeric digits. No blanks, spaces or all zeros for the twelve numeric digits are 
allowable.   
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Florida Education Identifier (FLEID) 
is not a valid FLEID.  
District Number,  
Current Enrollment  Florida Education  
Identifier  
01 FL340945895734  
01 FL004583948567  
*01 FL000000000000  

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Florida 
Education Identifier and resubmit the record f or processing.  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 22. If the Survey Period is 2 or 3 and the District Number, Current Enrollment exists on the Less than 180 
Days Regular School Year table, then the Days in Term (for FTE Purposes) should not exceed the days in 
the survey reported on the Less than 180 Days Regu lar School Year table. Match on by Year and District 
Number, Current Enrollment.   
**Result:** Record rejected
Note: Less than 180 Days Regular School Year table can be found at (DPS.DISTRICT.GQ.F71497.Yyyyy).  
 
EXAMPLE  
The first and second records listed below would be loaded to the database assuming no other reject rule 
would cause their rejection. The third record would be rejected because the district previously informed 
the department that the Days in Term for Survey  3 is 86.   
District Number,  
Current  
Enrollment  Florida  
Education  
Identifier  Survey  
Period  
Code  Days in Term  
(for FTE  
Purposes)  
24 FL123456789100  2 85 
24 FL123456789200  2 82 
*24 FL123456789300  3 88 

**District Responsibility:** If the rejected record should not have been submitted, no action is required.  However, if the district 
wishes the rejected record to be loaded to the database, the district must correct the Days in Term field 
on the  format and resu bmit the record.  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 23. If Transportation Membership Category is L or N, then Vehicle Category must be B.  
**Result:** Record rejected
 EXAMPLE  
 The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Vehicle Category code is not valid.   
District Number,  
Current Instruction/  
Services  Florida  
Education  
Identifier  Vehicle  
Category  Membership  
Category  
01 FL123456789100  B N 
01 FL123456789200  B L 
*01 FL123456789300  E N 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the Vehicle 
Category code and resubmit the record.  
  
  
Student Database 202 6-2027 /  
## Reject Rules

### 24. If District Number, Current Enrollment is 68 or 83, then Transportation Membership Category must be N.   
**Result:** Record rejected
EXAMPLE  
The first two records listed below would be loaded to the database assuming no other reject rule would 
cause their rejection. The third record would be rejected because the Vehicle Category code is not valid.  
District Number,  
Current Enrollment  Florida  
Education  
Identifier  Transportation  
Membership  
Category  
68 FL123456789100  N 
68 FL123456789200  N 
*68 FL123456789300  G 

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district 
wishes the data in the rejected record to be loaded to the database, the district must correct the 
Transportation Membership Category and resubmit the re cord.  
  
  
Student Database 202 6-2027 /  
## State Validation

### 50. Each  record must have a matching Student Demographic record based on District 
Number, Current Enrollment; Florida Education Identifier; Survey Period Code; and Fiscal Year.   
## State Validation

Note:   Students transported and reported by one district (District Number, Current Instruction/Service) 
but officially enrolled in another district (District Number, Current Enrollment), should have a matching 
Student Demographic Information record sent by the district in which the student is officially enrolled, 
not by the district providing the transportation. For a list of  records that do not 
have a matching Student Demographic Information record, refer to district -level transporta tion report 
F71026.   
 EXAMPLE  
The  record listed below which is marked with an asterisk would cause a message 
to be generated because it does not have a matching Student Demographic record.  
 records  
District Number,  
Current Instruction/  
Service  District Number,  
Current  
Enrollment  Florida  
Education  
Identifier  Survey  
Period  
Code  Fiscal  
Year  
*01 01 FL123456789100  2 ****  
01 01 FL123456789200  2 ****  
01 42 FL123456789300  2 ****  
  
Student Demographic Information records  
District Number,  
Current Instruction/  
Service  District Number,  
Current  
Enrollment  Florida  
Education  
Identifier  Survey  
Period  
Code  Fiscal  
Year  
01 01 FL123456789100  2 ****  
42 42 FL123456789200  2 ****  
 **** = Valid fiscal year for data submission.  

**District Responsibility:** The district must delete the  record or add a Student Demographic record to 
match the key fields on the  record.  
  
  
Student Database 202 6-2027 /  
## State Validation

### 51. If Transportation Membership Category = L, then there must be a matching Exceptional Student record 
where Exceptionality, Primary code is not L based on District Number, Current Enrollment; Florida 
Education Identifier; Year and Survey Period Code.  
## State Validation

Note:  Students reported under Transportation Membership Category “M” can be Exceptional or non -
Exceptional. Those exceptional students reported with code “M” must have a matching Exceptional 
Student record based on District Number, Current Enrollment; Florida E ducation Identifier; Year and 
Survey Period Code.   
EXAMPLE  
An error message would be generated for the  record marked with an asterisk 
below because there is no matching Exceptional Student record.  
 records  
District Number,  
Current  
Enrollment  Florida  
Education  
Identifier  Transportation  
Membership  
Category  
01 FL123456789100  L 
*01 FL123456789200  L 
 
Exceptional Student records  
District Number,  
Current  
Enrollment  School Number,  
Current  
Enrollment  Florida  
Education  
Identifier  Exceptionality,  
Primary  
01 0021  FL123456789100  C 
01 0021  FL123456789200  K 

**District Responsibility:** The district must correct the Transportation Membership Category code on the  
record or submit a matching Exceptional Student record.  
  
  
Student Database 202 6-2027 /  
## State Validation

### 52. If Transportation Membership Category = L, or M, then Grade Level on the matching Student 
Demographic Information record must be PK -12. The match should be made using the following 
elements: District Number, Current Enrollment; Florida Education Identifier ; Survey Period Code; and 
Year.  
## State Validation

EXAMPLE  
An error message would be generated for the  record marked with an asterisk 
below because Grade Level on the Student Demographic record is not PK -12.  
 records  
District Number,  
Current  
Enrollment  Florida  
Education  
Identifier  Transportation  
Membership  
Category  
01 FL123456789100  L 
*01 FL123456789200  M 
 
Student Demographic Information records  
District Number,  
Current  
Enrollment  School Number,  
Current  
Enrollment  Florida  
Education  
Identifier  Grade  
Level  
01 0021  FL123456789100  PK 
01 0021  FL123456789200  30 

**District Responsibility:** The district must correct the Transportation Membership Category code on the  
record or the Grade Level on the Student Demographic Information record.  
  
  
Student Database 202 6-2027 /  
## State Validation

### 53. If Grade Level on the Demographic Information record is 07 -12 then the Hazardous Walking Code must 
be 000000. The match is done using the following elements: District Number, Current Enrollment; Florida 
Education Identifier; Survey Period Code; and Fiscal Year.    
## State Validation

EXAMPLE  
An error message would be generated for the  record with the asterisk because of 
the invalid association between Hazardous Walking Code and Grade Level.    
  records  
District Number,  
Current 
Enrollment  Florida  
Education  
Identifier  Survey  
Period  
Code  Fiscal  
Year  Hazardous  
Walking  
Code  
01 FL123456789100  2 0708  000000  
*01 FL123456789200  2 0708  123456  
 
Student Demographic Information records  
District Number,  
Current 
Enrollment  Florida  
Education  
Identifier  Survey  
Period  
Code  Fiscal  
Year  Grade  
Level  
01 FL123456789100  2 0708  07 
01 FL123456789200  2 0708  08 

**District Responsibility:** The district must review the records and correct the Hazardous Walking Code on the Student 
Transportation record or the Grade Level on the Student Demographic Information record.  
  
  
Student Database 202 6-2027 /  
 AGGREGATE EXCEPTION REPORTS  
UPDATED 07/01/25  

### 90. The number of students for each school bus (vehicle category = B) must be greater than 5.  
Aggregate exception  
Note:  The following information will be listed on the exception report for buses that do not meet the 
aggregate exception edit above:  
• District Number, Current Instruction/Service  
• Bus Number  
• Total Student Count  
 
EXAMPLE  
Bus 1992ABC has only 4 students on the Transportation table. The figure is less than 5 students. An 
aggregate edit error message is generated for Bus 1992ABC on the exception report indicating that the 
bus failed this aggregate exception edit.  

**District Responsibility:** The district must verify the data for Bus Number 1992ABC on the  records and 
correct this field if it is in error on one or more records.