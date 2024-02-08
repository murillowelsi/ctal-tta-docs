# Technical Test Analyst Exam

## [TTA-2.8.1: Non-Safety-Related Systems](../../2-white-box-test-techniques/2.8-selecting-a-white-box-test-technique.md#281-non-safety-related-systems)

### Question #9 (3 Points) - K4

You are the Technical Test Analyst working on the testing of software that will control the movement of the roof on a new national sports stadium that seats 100,000 spectators. A failure analysis has shown that if the software system fails it may cause the roof to break up and fall on the spectators. The government has requested that the level of testing for this software exceeds that required by the IEC 61508 standard.

**Which level of test coverage would you expect to be achieved in the testing of the control software for the stadium roof?**

    a. Decision coverage + Modified Condition/Decision coverage
    b. Decision coverage + Statement coverage
    c. Modified Condition/Decision coverage
    d. Multiple Condition coverage

**Select ONE option.**

---

<details>
<summary><strong>Show Answer</strong></summary>

#### Correct Answer: d

    a. Is not correct. This is the same as MC/DC, because decision coverage is subsumed by MC/DC
    b. Is not correct. This is the same as decision coverage because statement coverage is subsumed by decision coverage. Decision coverage, however, provides a lower level of rigor than MC/DC or multiple condition coverage
    c. Is not correct. MC/DC is required for the highest-level criticality software according to IEC 61508, but this scenario requires the level of testing to exceed this, so this is not a correct option
    d. Is correct. MC/DC is required for the highest-level criticality software according to IEC 61508, which is presumably because several thousand spectators could be killed/injured. Multiple condition coverage provides a higher level of coverage than MC/DC and as this ‘exceeds’ that provided by MC/DC this is the correct option for this scenario

</details>

---

[↑ Table of Contents](../../README.md#table-of-contents) | [← Previous Page](question-8.md) | [Next Page →](question-10.md)
