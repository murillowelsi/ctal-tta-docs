# Technical Test Analyst Exam

## [TTA-6.2.1: Fault Seeding Tools](../../6-test-tools-and-automation/6.2-specific-test-tools.md#621-fault-seeding-tools)

### Question #40 (1 Point) - K2

**Which of the following statements about fault seeding tools is correct?**

    a. These tools insert defects into the source code to test the input checking capabilities of the software
    b. These tools insert defects into the source code to check the level of fault tolerance of the software
    c. These tools insert defects into the source code to test the effectiveness of the test suite
    d. These tools are generally used by the test analyst to measure the coverage achieved by specified tests

**Select ONE option.**

---

<details>
<summary><strong>Show Answer</strong></summary>

#### Correct Answer: c

    a. Is not correct. Input checking can be done by mutating test inputs, but to test input checking the inputs would need to be mutated
    b. Is not correct. This is the task of the fault injection tools
    c. Is correct. The mutated code is executed against the test suite to determine how well the test suite can detect the mutations (defects)
    d. Is not correct. These tools are generally used by the technical test analyst, or the developer when testing newly developed code

</details>

---

[↑ Table of Contents](../../README.md#table-of-contents) | [← Previous Page](question-39.md) | [Next Page →](question-41.md)
