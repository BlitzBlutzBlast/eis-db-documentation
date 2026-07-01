# 2025-26 Student Transportation

Source: [FLDOE Database Manuals](https://www.fldoe.org/accountability/data-sys/database-manuals-updates/2025-26-student-info-system/student-transportation.stml)
Last Updated (per source page): 7/1/2025

## Description

1. Submit this record during Survey periods 1-4 for any PK-12 student in membership during survey week who is assigned to a school bus, passenger car or other vehicle and was transported at least once during the five-day survey period or once during the preceding six scheduled school days.
2. A student may be counted only once and only on one mode of travel, even if more than one mode is used.
3. The district must have a policy regarding reporting of students who transfer from one bus to another during survey week either on the sending or receiving bus. For example, a student transported from home to school and then to a vocational center may only be counted once.
4. Students who are transported by general purpose transportation (city buses, trains, etc.) or privately owned motor vehicles or boats (for isolated or disabled students) are reported as any other transported students.
5. For students transported to another district to receive instruction submit a Student Transportation format only. Report the number of the district supplying the transportation in the element District Number, Current Instruction/Service and the number of the district supplying the instruction in District Number, Current Enrollment.
6. ERROR CODES: This field is used by the Department to report to districts the specific errors found in the record during the state edit process. This field should contain filler (spaces, blanks) when the record is transmitted to the Department.
7. KEY FIELDS: The key fields for this format are item numbers 1, 3, 4, 5 and 16. If a key field needs to be changed, the record must be deleted and re-submitted as an add.

`*` indicates key fields.

## Record Layout

| Item No. | From-To | Size | Field Char. | Field Description |
|---|---|---|---|---|
| 1 | 1-2 | 2 | N/R | District Number, Current Instruction/Service * |
| 2 | 3-12 | 10 | A/N | Filler |
| 3 | 13-13 | 1 | A/N | Survey Period Code * |
| 4 | 14-17 | 4 | N | Fiscal Year * |
| 5 | 18-18 | 1 | A/N | Year-Round/Extended School Year FTE Indicator * |
| 6 | 19-21 | 3 | N | Days In Term (For FTE Purposes) |
| 7 | 22-22 | 1 | A | Transportation Membership Category |
| 8 | 23-23 | 1 | A | Vehicle Category |
| 9 | 24-35 | 12 | A/N | Bus Number |
| 10 | 36-50 | 15 | A/N | Bus Route Number |
| 11 | 51-51 | 1 | A | Transaction Code |
| 12 | 52-53 | 2 | N/R | District Number, Current Enrollment |
| 13 | 54-59 | 6 | N | Hazardous Walking |
| 14 | 60-62 | 3 | A/N | Filler |
| 15 | 63-72 | 10 | A/N | Student Number Identifier, Local |
| 16 | 73-86 | 14 | A/N | Florida Education Identifier * |
| 17 | 87-152 | 66 | A/N | Filler |
| 18 | 153-160 | 8 | A/N | Filler/Error Codes |

## Data Element Reference Notes

- Key fields for record matching: items 1, 3, 4, 5, 16
- A student counts once per survey period regardless of mode or number of vehicles used (e.g., a bus-to-bus transfer to a vocational center is still one record)
- Cross-district transportation: when another district supplies transportation for a student instructed elsewhere, report the transporting district in District Number, Current Instruction/Service and the instructing district in District Number, Current Enrollment
