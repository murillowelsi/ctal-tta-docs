# Technical Test Analyst Exam

## [TTA-2.4: Modified Condition/Decision Testing](../../2-white-box-test-techniques/2.4-modified-condition-decision-testing.md)

### Question #6 (2 Points) - K3

You are testing a photo-enforcement system for traffic control at an intersection. The requirements state a photo shall be taken if the signal light is red (RED), or the car is speeding (SPEED), and if the front wheels of the car are over the line marking the beginning of the intersection (WHEELS). The logic in the code looks like the following:

```javascript
IF ((RED OR SPEED) AND WHEELS) THEN
 Take the photo
ELSE
 Do not take the photo
ENDIF
```

Consider these test input values:

    1. RED + SPEED + WHEELS
    2. RED + SPEED + not WHEELS
    3. RED + not SPEED + WHEELS
    4. RED + not SPEED + not WHEELS
    5. not RED + SPEED + WHEELS
    6. not RED + SPEED + not WHEELS
    7. not RED + not SPEED + WHEELS
    8. not RED + not SPEED + not WHEELS

**Assuming there is no short-circuiting, which set of test input values is required to achieve full modified condition/decision coverage?**

    a. 1, 3, 8
    b. 2, 6, 8
    c. 3, 4, 5, 7
    d. 1, 5, 7, 8

**Select ONE option.**

---

<details>
<summary><strong>Show Answer</strong></summary>

#### Correct Answer: c

    a. Is not correct. Covers the outcomes but not the atomic conditions that affect the decision outcome. Also, for three independent atomic conditions, then four tests are needed to achieve MC/DC level of coverage
    b. Is not correct. Does not sufficiently cover the atomic conditions affecting the decision outcome. Also, for three independent atomic conditions, then four tests are needed to achieve MC/DC level of coverage.
    c. Is correct. This answer provides the following:
        Test inputs for (RED or SPEED) and WHEELS OUTCOME
            3. RED + not SPEED + WHEELS TRUE
            4. RED + not SPEED + not WHEELS FALSE
            5. not RED + SPEED + WHEELS TRUE
            7. not RED + not SPEED + WHEELS FALSE
        #3 and #7 show that RED can independently affect the overall outcome.
        #5 and #7 show that SPEED can independently affect the overall outcome.
        #3 and #4 show that WHEELS can independently affect the outcome.
    d. Is not correct. Does not sufficiently cover the atomic conditions affecting the decision outcome. #1 combined with any of the other three (#5, #7, #8) cannot show that any single condition can independently affect the overall outcome

</details>

---

[↑ Table of Contents](../../README.md#table-of-contents) | [← Previous Page](question-5.md) | [Next Page →](question-7.md)
