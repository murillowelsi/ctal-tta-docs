# Technical Test Analyst Exam

## [TTA-5.1: Technical Test Analyst Tasks in Reviews](../../5-reviews/5.1-technical-test-analyst-tasks-in-reviews.md)

### Question #32 (3 Points) - K4

You are participating in an architectural review of a new product design. This is an embedded product that has severe memory restrictions. Consider the following programming practices and problems that can result from using those practices.

Programming Practices:

- (1) Connection pooling
- (2) Data caching
- (3) Lazy instantiation
- (4) Transaction concurrency

Problems:

- (A) Performance impact when the instantiation is needed
- (B) Transaction loss due to processor unavailability
- (C) Errors in multi-threading logic
- (D) Stale data

**Which of the above programming practices could be used to reduce unnecessary memory use in this scenario and what are the possible problems in using this practice?**

    a. Practice 2, Problem D
    b. Practice 4, Problem C
    c. Practice 3, Problem A
    d. Practice 1, Problem B

**Select ONE option.**

---

<details>
<summary><strong>Show Answer</strong></summary>

#### Correct Answer: c

    a. Is not correct. Data caching helps with performance, not memory use
    b. Is not correct. Transaction concurrency uses more memory than running transactions sequentially
    c. Is correct. This would reduce unnecessary memory use but does have the possible problem of a delayed response when instantiation is performed
    d. Is not correct. Connection pooling can help memory and performance, but the possible problem is running out of connections, not losing a transaction

</details>

---

[↑ Table of Contents](../../README.md#table-of-contents) | [← Previous Page](question-31.md) | [Next Page →](question-33.md)
