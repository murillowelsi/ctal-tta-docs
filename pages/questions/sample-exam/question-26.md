# Technical Test Analyst Exam

## [TTA-4.3: Security Testing](../../4-quality-characteristics-for-technical-testing/4.3-security-testing.md)

### Question #26 (1 Point) - K2

By entering the following phrase into the username field of the login form:

`abcd OR 1=1`

a tester performed an SQL injection attack and consequently obtained a list of all valid usernames for the system.

**Which of the following security aspects was MOST likely to have been addressed by this test?**

    a. Confidentiality
    b. Non-repudiation
    c. Accountability
    d. Availability

**Select ONE option.**

---

<details>
<summary><strong>Show Answer</strong></summary>

#### Correct Answer: a

    a. Is correct. This is an example of compromising confidentiality by gaining access to sensitive data by an unauthorized user
    b. Is not correct. We do not know if the event of gaining access to sensitive data can be proven to have taken place. To test for non-repudiation test steps concerning the server log-files are typically required
    c. Is not correct. We do not know if such an SQL injection attack can be traced uniquely to the person that performed it. To test for accountability, log-files must typically be checked against specific actions by authorized and non-authorized users
    d. Is not correct. Availability tests in the security context are typically performed by simulating denial-of-service scenarios

</details>

---

[↑ Table of Contents](../../README.md#table-of-contents) | [← Previous Page](question-25.md) | [Next Page →](question-27.md)
