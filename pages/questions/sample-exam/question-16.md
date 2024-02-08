# Technical Test Analyst Exam

## [TTA-3.2.3: Using Static Analysis for Improving Maintainability](../../3-static-and-dynamic-analysis/3.2-static-analysis.md#323-using-static-analysis-for-improving-maintainability)

### Question #16 (2 Points) - K3

Below is the pseudo-code for a TRICKY program:

```pseudo
0 program TRICKY
1 var1, var2, var3 : integer
2 begin
3   read(var2)
4   read(var1)
5   while (var2 < 10) loop
6     var3 = var2 + var1
7     var2 = 4
8     var1 = var2 + 1
9     print(var3)
10     if (var1 == 5) then
11       print(var1)
12     else
13       print(var1+1)
14     endif
15     var2 = var2 + 1
16   endloop
17   print(“Wow – that was tricky!”)
18   print(“But the answer is...”)
19   print(var2+var1)
20 end program TRICKY
```

**Which TWO fixes to improve code maintainability would MOST likely be proposed after performing static analysis?**

    a. Restructuring the code
    b. Improving the naming of variables
    c. Reduce program coupling
    d. Improving the amount of comments
    e. Improving the indentation of code

**Select TWO options.**

---

<details>
<summary><strong>Show Answer</strong></summary>

#### Correct Answer: b, d

    a. Is not correct. The code is clearly structured with control elements (e.g., loop, if-then-else). Static analysis is unlikely to identify any improvements to the control structure
    b. Is correct. Variable naming used in the program does not clearly indicate what the variable represents. Static analysis can apply naming convention rules which would identify these maintenance issues in the program and recommend that the variables be given names that are readable and conform to any applicable naming rules
    c. Is not correct. There are no global variables defined and no other programs called. Coupling is not an improvement area
    d. Is correct. Static analysis identifies code which has a low level of commenting compared to executable code. Since the program has no comments at all, this would be highlighted as an area for improving code maintainability
    e. Is not correct. Static analysis can apply indentation rules but in the case of the TRICKY program there is already adequate indentation

</details>

---

[↑ Table of Contents](../../README.md#table-of-contents) | [← Previous Page](question-15.md) | [Next Page →](question-17.md)
