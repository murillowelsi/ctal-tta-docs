# Technical Test Analyst Exam

## [TTA-2.3: Decision Testing](../../2-white-box-test-techniques/2.3-decision-testing.md)

### Question #4 (2 Points) - K3

The simplified logic of a program is as follows:

```js
Statement P
IF A THEN
    IF B THEN
        Statement Q
    ELSE
        Statement R
    ENDIF
ELSE
    Statement S
    IF C THEN
        Statement T
    ELSE
        Statement U
    ENDIF
ENDIF
Statement V
```

**Assume that decisions B and C are independent of each other. What is the minimum number of test cases required to achieve 100% decision coverage?**

    a. 2
    b. 3
    c. 4
    d. 5

**Select ONE option.**

---

<details>
<summary><strong>Show Answer</strong></summary>

#### Correct Answer: c

    a. Is not correct. As shown in (c), 4 tests are needed to achieve 100% decision coverage
    b. Is not correct. As shown in (c), 4 tests are needed to achieve 100% decision coverage
    c. Is correct. The following conditions ensure that all decision outcomes are tested:
        1. A = true, B = true
        2. A = true, B = false
        3. A = false, C = true
        4. A = false, C= false
    d. Is not correct. As shown in (c), 4 tests are enough to achieve 100% decision coverage

</details>

---

[↑ Table of Contents](../../README.md#table-of-contents) | [← Previous Page](question-3.md) | [Next Page →](question-5.md)
