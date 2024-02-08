# Technical Test Analyst Exam

## [TTA-2.8.1: Non-Safety-Related Systems](../../2-white-box-test-techniques/2.8-selecting-a-white-box-test-technique.md#281-non-safety-related-systems)

### Question #10 (3 Points) - K4

You work for a software house that provides software solutions for medical systems. Currently you are testing a software component that operates the defibrillator machine controlling the dose of electric current delivered to the heart. During the code review, the reviewers noticed that one
decision in the module under test consists of 20 independent atomic conditions. You are obliged to perform white-box testing for this module and you are expected to finish it in one month.

**Which white-box test technique should you choose for this scenario?**

    a. Multiple condition testing
    b. MC/DC testing
    c. Decision testing
    d. API testing

**Select ONE option.**

---

<details>
<summary><strong>Show Answer</strong></summary>

#### Correct Answer: b

    a. Is not correct. Multiple condition testing is the most thorough technique, but for a decision with 20 independent atomic conditions we would have to design 220 = 1,048,576 tests to achieve full multiple condition coverage, which would be impossible to finish in one month (if at all)
    b. Is correct. This is a medical, safety-critical system, whose failure or malfunction may result in death or serious injury to people. Therefore, it must be tested thoroughly. Full multiple condition coverage is impossible to achieve (see answer a), hence, MC/DC is the most reasonable choice as it is stronger than decision testing, but,compared to multiple condition testing, requires only a linear number of test cases – for example, the decision with 20 conditions requires only 21 test cases to achieve full MC/DC coverage
    c. Is not correct. Decision testing is a relatively weak criterion compared to MC/DC, and so not suitable for a safety-critical system
    d. Is not correct. There is no information about API in this scenario. Also, this would not guarantee the thorough level of testing required for such a safety-critical system

</details>

---

[↑ Table of Contents](../../README.md#table-of-contents) | [← Previous Page](question-9.md) | [Next Page →](question-11.md)
