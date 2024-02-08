# Technical Test Analyst Exam

## [TTA-3.2.1: Data Flow Analysis](../../3-static-and-dynamic-analysis/3.2-static-analysis.md#322-data-flow-analysis)

### Question #13 (3 Points) - K3

Below is the pseudo-code for a program that calculates and prints sales commissions:

```pseudo
0  program Calculate Commission
1  total, number : integer
2  commission_hi, commission_lo : real
3  begin
4      read(number)
5      while (number ≠ -1) loop
6          total = total + number
7          read(number)
8      endloop
9      if (total > 1000) then
10         commission_hi = 100 + 0.2 * (total - 1000)
11     else
12         commission_lo = 0.15 * total
13     endif
14     write("This salesman’s commission is:")
15     write(commission_hi)
16  end program Calculate Commission
```

**The code contains data flow anomalies on lines 6 and 12 (highlighted text). Which examples of data flow anomalies can be found on these lines?**

    a. line 6: variable “total” is not assigned a value before using it line 12: variable “commission_lo” is defined but subsequently not used
    b. line 6: an invalid value is assigned to variable “total” line 12: variable “commission_lo” is redefined before it is used
    c. line 6: variable “total” is out of scope line 12: the “hard-coded” value “0.15” should not be used
    d. line 6: the variable “number” is undefined line 12: the variable “total” is redefined before it is used

**Select ONE option.**

---

<details>
<summary><strong>Show Answer</strong></summary>

#### Correct Answer: a

    a. Is correct. The variable ‘total’ is used at line 6 before it is defined. The variable ‘commission_lo’ is defined at line 12 with no subsequent use
    b. Is not correct. The variable ‘number’ is a valid value to assign to the variable ‘total’: The variable ‘commission_lo’ is not defined before line 12
    c. Is not correct. The variable ‘total’ is in scope at line 6 Use of the “hard-coded” value “0.15” is not a data flow anomaly
    d. Is not correct. The variable ‘number’ is defined at line 4. The variable ‘total’ is defined at line 6, and not redefined before line 12

</details>

---

[↑ Table of Contents](../../README.md#table-of-contents) | [← Previous Page](question-12.md) | [Next Page →](question-14.md)
