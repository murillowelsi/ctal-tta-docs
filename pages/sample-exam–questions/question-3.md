# Technical Test Analyst Exam

## [TTA-2.2: Statement Testing](../2-white-box-test-techniques/2.2-statement-testing.md)

### Question #3 (2 Points) - K3

**Consider the simplified logic of a tea-making machine:**

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

### Answer

#### Correct Answer: a

    a. Is not correct. The TA would be expected to work with users
    b. Is not correct. The TA would be expected to work with business analysts
    c. Is not correct. The TA would be expected to work with project sponsors
    d. Is correct. The TTA is expected to work with the technical stakeholders on the project, including the developers

---

[↑ Table of Contents](../../README.md#table-of-contents) | [← Previous Page](question-2.md) | [Next Page →](question-4.md)
