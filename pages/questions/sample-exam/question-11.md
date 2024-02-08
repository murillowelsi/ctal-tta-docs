# Technical Test Analyst Exam

## [TTA-3.2.1: Control Flow Analysis](../../3-static-and-dynamic-analysis/3.2-static-analysis.md#321-control-flow-analysis)

### Question #11 (2 Points) - K3

Below is the pseudo-code for a TRICKY program:

```pesudo
0   program TRICKY
1     var1, var2, var3 : integer
2   begin
3     read(var2)
4     read(var1)
5     while var2 < 10 loop
6       var3 = var2 + var1
7       var2 = 4
8       var1 = var2 + 1
9       print(var3)
10      if var1 = 5 then
11        print(var1)
12      else
13        print(var1+1)
14      endif
15      var2 = var2 + 1
16    endloop
17    print(“Wow – that was tricky!”)
18    print(“But the answer is...”)
19    print(var2+var1)
20  end program TRICKY
```

**Which of the following statements about the TRICKY program MOST correctly describes any control flow anomalies in it?**

    a. The TRICKY program contains no control flow anomalies
    b. The TRICKY program contains unreachable code and an infinite loop
    c. The TRICKY program contains unreachable code and no infinite loop
    d. The TRICKY program contains a loop with multiple entry points

**Select ONE option.**

---

<details>
<summary><strong>Show Answer</strong></summary>

#### Correct Answer: b

    a. Is not correct. See the correct justification for details
    b. Is correct. The decision at line 10 will always be true as var1 will always be 5 at line 10, thus line 13 is unreachable. The loop at line 5 can only be left if var2 is 10 or more, but each time through the loop var2 is reset at line 7 back to 4 and only incremented by 1 in the loop at line 15, so it only ever reaches 5
    c. Is not correct. See the correct justification for details
    d. Is not correct. There is only one entry point to the WHILE loop (with the control flow 4 → 5)

</details>

---

[↑ Table of Contents](../../README.md#table-of-contents) | [← Previous Page](question-10.md) | [Next Page →](question-12.md)
