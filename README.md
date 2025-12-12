Excel Project PR.1 Fundamental Booster
Overview

This project demonstrates the use of essential Excel functions related to data analysis, referencing, lookup operations, logical formulas, date functions, text manipulation, and dynamic ranges.
The project is divided into three datasets:

Students Grade Sheet

Sales Data Sheet

Employee Data Sheet

Each sheet includes tasks aligned with the required topics and functions.

Contents and Tasks Completed
1. Relative & Absolute References

Used relative references (A1) in calculations.

Used absolute references ($A$1) for fixed values such as grade cutoffs and discount thresholds.

2. IF Formulas and Nested IFs
Student Grades:

Classified grades based on total marks using nested IF.

Example:
=IF(F2>=90,"A",IF(F2>=80,"B",IF(F2>=70,"C","D")))

Sales Discounts:

Calculated discount based on amount thresholds.

Example:
=IF(E2>30000, E2*0.10, E2*0.05)

3. IF with AND/OR
Students:

Identified students scoring above 80 in both Math and Science.
=IF(AND(C2>80, D2>80), "Yes", "No")

Sales:

Discount eligibility using OR.
=IF(OR(B2="Laptop", E2>20000), "Eligible", "Not Eligible")

4. COUNTIFS, SUMIFS, AVERAGEIFS
Students:

Counted number of students scoring above 50 in Math.
=COUNTIFS(C2:C100, ">50")

Sales:

Summed sales for a specific region and product.
=SUMIFS(E2:E100, C2:C100, "East", B2:B100, "Keyboard")

Students:

Calculated average score above 60.
=AVERAGEIFS(F2:F100, F2:F100, ">60")

5. Lookup Functions (VLOOKUP, XLOOKUP, XMATCH)
Student Name Lookup:

Retrieved student name from ID.
=VLOOKUP(A10, 'Students Grade'!A2:I21, 2, FALSE)

Product Price Lookup (Sales Data):

Fetched product price by product code.
=VLOOKUP(H2, A2:E21, 5, FALSE)

XLOOKUP – Employee Salary:

Returned salary based on employee ID.
=XLOOKUP(G2, A2:A100, D2:D100, "Not Found")

XMATCH – Product Position:

Found the position of a product in the list.
=XMATCH("Laptop", B2:B21)

6. INDEX and MATCH
Salesperson Monthly Sales:

Extracted sales based on salesperson and month.
=INDEX(E2:E100, MATCH(1, (D2:D100=H2)*(G2:G100=I2), 0))

7. TEXT Functions

Extracted first name:
=LEFT(B2, FIND(" ", B2)-1)

Converted to uppercase and lowercase using UPPER() and LOWER().

8. INDIRECT and OFFSET
Dynamic Range using INDIRECT:

Referenced a user-selected sheet or range dynamically.

OFFSET – Dynamic Salary Range:

Created dynamic range for salary trend analysis.
=OFFSET(D2, 0, 0, COUNTA(D:D)-1, 1)

9. Date & Time Functions
Years of Service:

Calculated years of service while handling future dates.
=IF(E2>TODAY(),"Not Available",DATEDIF(E2, TODAY(), "Y"))

Difference in Days:

Found duration between two dates.
=DATEDIF(E2, TODAY(), "D")

10. Math Functions

Rounded salary using:
=ROUND(D2, -3)

Used CEILING and FLOOR for rounding up or down:
=CEILING(D2, 1000)
=FLOOR(D2, 1000)

11. FILTER Function

Extracted all students scoring above 80%.
=FILTER(A2:I100, F2:F100>80, "No students above 80")

Summary

This project covers all essential Excel analytical techniques including logical formulas, lookup operations, text and date functions, dynamic referencing, and filtering.
All required tasks under the “Fundamental Booster” assignment have been completed and demonstrated in the respective worksheets.
