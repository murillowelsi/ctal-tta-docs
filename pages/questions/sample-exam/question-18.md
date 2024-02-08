# Technical Test Analyst Exam

## [TTA-4.2.5: Data Security and Data Protection](../../4-quality-characteristics-for-technical-testing/4.2-general-planning-issues.md#425-data-security-and-data-protection)

### Question #18 (3 Points) - K4

Assume you are working as a Technical Test Analyst on a project where a new banking system is being developed. This system will store customer financial data, including personal information, account numbers, balances, and transaction histories, but no real customer data will become available until after the system is deployed operationally.

**Based on this information, which of the following topics are you MOST likely to include in the system test plan?**

    a. Test data anonymization
    b. Coordination of distributed components
    c. Testing of data encryption
    d. Testing in production

**Select ONE option.**

---

<details>
<summary><strong>Show Answer</strong></summary>

#### Correct Answer: c

    a. Is not correct. While subsequent releases of this system may be tested with real customer data, this is a new system and no existing customer data is available
    b. Is not correct. There is no indication this is a distributed system
    c. Is correct. It is highly likely the bank is required by regulation to encrypt the customer financial data, which has testing implications
    d. Is not correct. It is not clear whether this system will be used in-house (thus a production environment might be available) or sold to customers (thus production environments would likely not be available)

</details>

---

[↑ Table of Contents](../../README.md#table-of-contents) | [← Previous Page](question-17.md) | [Next Page →](question-19.md)
