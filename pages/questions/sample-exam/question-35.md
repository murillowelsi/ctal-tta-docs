# Technical Test Analyst Exam

## [TTA-5.2.2: Code Reviews](../../5-reviews/5.2-using-checklists-in-reviews.md#522-code-reviews)

### Question #35 (3 Points) - K4

You are participating in a code review and have noticed a problem in the following section of pseudo-code (assume \*\*\* indicates a comment).

```pseudo
*** this pseudo-code calculates the average sales per month achieved by an organization ***
0 program SALES
1 month_counter, sales_in_month, total_sales, fileID, number_of_months: integer
2 average_sales: float
3 begin
4     *** open the sales file***
5     fileID = open file ( “Sales” )
6     if (fileID = 0) then
7         *** File cannot be opened***
8         Display error message 333
9     else
10        *** get the number of months you want to consider
11        Read (number_of_months)
12        month_counter = 1
13        total_sales = 0
14        while month_counter <= number_of_months loop
15            *** get sales for month from sales file using the GetSales function***
16            sales_in_month = GetSales (month_counter, fileID)
17            *** add the sales to the total***
18            total_sales = total_sales + sales_in_month
19            month_counter = month_counter + 1
20        endloop
21        *** calculate the average monthly sales and output that value***
22        average_sales = total_sales / number_of_months
23        Write (average_sales)
24     endif
25 end program SALES
```

**Which of the following problems is demonstrated in this section of code?**

    a. Files are not checked for existence before attempting to access
    b. Divisors are not tested for zero
    c. Comments are inconsistent with the code
    d. There are unused variables

**Select ONE option.**

---

<details>
<summary><strong>Show Answer</strong></summary>

#### Correct Answer: b

    a. Is not correct. The variable “fileID” is checked before attempting to access the sales file (see lines 6, 7 and 8)
    b. Is correct. On line 22 the divisor “number_of_months” is not checked for 0. This should be checked before line 22 is executed
    c. Is not correct. Comments and code are consistent
    d. Is not correct. All declared variables (lines 1 and 2) are used in the code

</details>

---

[↑ Table of Contents](../../README.md#table-of-contents) | [← Previous Page](question-34.md) | [Next Page →](question-36.md)
