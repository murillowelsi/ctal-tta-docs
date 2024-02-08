# Technical Test Analyst Exam

## [TTA-2.2: Statement Testing](../../2-white-box-test-techniques/2.2-statement-testing.md)

### Question #3 (2 Points) - K3

Consider the simplified logic of a tea-making machine:

```js
Turn on the machine
IF enough water THEN
    Boil water
    Add tea
    Show message “milk?”
    IF milk = yes THEN
        Show message “low fat?”
        IF low fat = yes THEN
            Add low fat milk
        ELSE
            Add normal milk
        ENDIF
    ENDIF
    Show message “sugar?”
    IF sugar = yes THEN
        Add sugar
    ENDIF
    Stir
    Wait 3 minutes
    Show message “please take your tea”
ELSE
    Show message “please fill up water”
ENDIF
```

**What is the minimum number of test cases required to achieve 100% statement coverage of the logic for the tea-making machine?**

    a. 3
    b. 2
    c. 5
    d. 6

**Select ONE option.**

---

<details>
<summary><strong>Show Answer</strong></summary>

#### Correct Answer: a

    a. Is correct. The three test cases are defined by the following inputs:
        - Enough water, low fat milk, sugar
        - Enough water, normal milk, sugar or not sugar
        - Not enough water
    b. Is not correct. With two tests, one of the paths covered by the tests of answer (a) will be missed, and the lines of code in this path will not be tested – failing to achieve 100% statement coverage
    c. Is not correct. The question asked for the minimal number of tests to achieve 100% statement coverage. This can be achieved with 3 tests, as shown in (a)
    d. Is not correct. The question asked for the minimal number of tests to achieve 100% statement coverage. This can be achieved with 3 tests,as shown in (a)

</details>

---

[↑ Table of Contents](../../README.md#table-of-contents) | [← Previous Page](question-2.md) | [Next Page →](question-4.md)
