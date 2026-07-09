# School Environmental Safety Incident Report — Edits and Reject Rules

Source: https://www.fldoe.org/core/fileparse.php/20909/urlt/2627ses.pdf
Manual: Student Database 2026-2027

This document covers the edits across three categories: Reject Rules (record rejected), State Validation (cross-format matching), and Exception Reports (advisory, does not reject). Edit numbering is non-sequential; gaps and alphanumeric IDs (e.g., 1A, 2H, 4G) are as published in the source.

---

## Reject Rules

### 1. District Number, Current Enrollment must be numeric
District Number, Current Enrollment must be numeric and active (A) on the Appendix C: District Name Table and must be correct for the district submitting the data.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the District Number, Current Enrollment and resubmit the record.

### 2. School Number, Where Incident Occurred must exist on Master School Identification File
School Number, Where Incident Occurred must be numeric in the range 0001 to 9899, or it must be N998 or N999, and it must exist on the Master School Identification File as a valid school number in the district of enrollment.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the School Number, Where Incident Occurred and resubmit the records.

### 3. Survey Period Code must be valid
Survey Period Code must be 2, 3, or 5 and must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** The district must correct Survey Period Code either on the records coming in or the transmission JCL and all records must be resubmitted.

### 4. School Year correct for submission
School Year must be correct for the submission specified by the district.
**Result:** Record rejected

**District Responsibility:** The district must correct School Year either on the records coming in or the transmission JCL and all records must be resubmitted.

### 5. Incident, Identifier must be alphanumeric
The Incident, Identifier must be alphanumeric and must not be all spaces.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Incident, Identifier and resubmit the record.

### 6. Transaction Code validity and existence match
The Transaction Code must be A, C or D. For the original transmission, only A is valid. For subsequent batch/update submissions, if A is specified then the record must not already exist on the database; if C or D is specified then the record must exist on the database.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Transaction Code and resubmit the records.

### 7. Record uniqueness
Each School Environmental Safety Incident Report record must be unique based on the keys of District Number, Current Enrollment; School Number, Where Incident Occurred; School Year; Survey Period Code; and Incident, Identifier.
**Result:** First record accepted, all other duplicate records rejected

**District Responsibility:** If the record that was accepted and loaded to the database is the correct one, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must delete an invalid record, correct any rejected record if necessary, and resubmit the corrected record.

### 8. Incident, Type code validity
Incident, Type must be a valid code on Appendix P. 
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Incident, Type and resubmit the record.

### 9. Incident, Date format and validity
Incident, Date must be a valid date in the format MMDDYYYY and must not be in the future.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Incident, Date and resubmit the records.

### 11. Incident, Weapon-Related code validity
Incident, Weapon-Related must be 1, 2, 3, 4, or Z.
**Result:** Record rejected

**District Responsibility:** If the rejected records should not have been submitted, no action is required. However, if the district wishes the data in the rejected records to be loaded to the database, the district must correct the Incident, Weapon-Related code and resubmit the records.

### 12. Incident, Basis - Adult code validity
Incident, Basis - Adult must be Y or N.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Incident, Basis - Adult code and resubmit the record.

### 1C. Weapon-Related code requires valid Weapon Type
If Incident, Weapon-Related is 1, 2, 3, or 4, then at least one of the Weapon Type codes must not be Z. If Incident, Weapon-Related is Z, then all Weapon Type codes must be Z.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Incident, Weapon-Related or Weapon Type codes and resubmit the record.

### 1D. Incident, Bullying-Related code validity
Incident, Bullying-Related must be Y or N.
**Result:** Record rejected

**District Responsibility:** If the rejected record should not have been submitted, no action is required. However, if the district wishes the data in the rejected record to be loaded to the database, the district must correct the Incident, Bullying-Related code and resubmit the record.

---

## State Validation

### 41. Matching Student Discipline/Resultant Action record required
If Incident, Type is BUL or HAR, there must be at least one matching Student Discipline/Resultant Action record where Incident, Type equals BUL or HAR. The match should be based on District Number, Current Enrollment; School Year; Survey Period Code; and Incident, Identifier.
**Result:** State validation

**District Responsibility:** The district must delete the School Environmental Safety Incident Report record or add a Student Discipline/Resultant Action record to match the above key fields.

### 43. Drug-related incidents require valid Drug Description
If Incident, Type equals DRU, then at least one Drug Description code on a matching Student Discipline/Resultant Action record must not be Z.
**Result:** State validation

**District Responsibility:** The district must correct the School Environmental Safety Incident Report record or the Student Discipline/Resultant Action record so that the appropriate relationship exists.

### 45. Weapon-Related 1-4 requires valid Discipline Weapon Type
If Incident, Weapon-Related on the SESIR format is 1, 2, 3, or 4, there must be a matching Student Discipline/Resultant Action record where Weapon, Description is not Z.
**Result:** State validation

**District Responsibility:** The district must correct the applicable School Environmental Safety Incident Report record or matching Student Discipline/Resultant Action record so that the appropriate relationship exists.

---

## Exception Reports

### 50. Total Incidents should not exceed standard baseline
The total number of School Environmental Safety Incident Report records for a school should not exceed the established baseline limit for typical reporting within a single Survey Period Code unless correctly documented.
**Result:** Exception report

**District Responsibility:** The district should verify the submitted records for the school and ensure no duplicate incidents were reported under different identifiers. 

### 60. Incident, Gang-Related Y requires verification
If Incident, Gang-Related is Y, the district should verify that the incident fits the statutory definition of gang-related activity.
**Result:** Exception report

**District Responsibility:** The district should verify the Incident, Gang-Related code and correct if in error.