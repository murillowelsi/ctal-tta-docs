# Technical Test Analyst Exam

## [TTA-2.5: Multiple Condition Testing](../../2-white-box-test-techniques/2.5-multiple-condition-testing.md)

### Question #7 (2 Points) - K3

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

**Assuming no short-circuiting, which set of test input values is required to achieve 50% multiple condition coverage?**

    a. 3, 4, 5, 8
    b. 1, 3, 5
    c. 2, 4, 6, 7, 8
    d. 2, 7

**Select ONE option.**

---

<details>
<summary><strong>Show Answer</strong></summary>

#### Correct Answer: a

    a. Is correct. Multiple condition testing requires testing the entire truth table (all combinations of true and false possible which equals 2<sup>N</sup>, where N is the number of uncoupled atomic conditions). So, this example requires 8 tests. 50% coverage is achieved with any 4 separate tests from the list
    b. Is not correct. This answer provides 3/8 (37.5%) coverage of the multiple condition testing
    c. Is not correct. This answer provides 5/8 (62.5%) coverage of the multiple condition testing
    d. Is not correct. This answer provides 2/8 (25%) coverage of the multiple condition testing

</details>

---

[↑ Table of Contents](../../README.md#table-of-contents) | [← Previous Page](question-6.md) | [Next Page →](question-8.md)
