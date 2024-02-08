# Technical Test Analyst Exam

## [TTA-4.3: Performance Testing](../../4-quality-characteristics-for-technical-testing/4.5-performance-testing.md)

### Question #25 (2 Points) - K3

The system integration testing for a new version of a stocks trading system is being planned. You are planning the performance efficiency tests as part of this testing. The new version has increased functionality, but the basic architecture remains the same.

The current system has so far received a positive response and the number of users has steadily increased. It enables users to trade individual stocks with a simple transaction consisting only of the user identity, stock number, quantity, and action (buy or sell).

The current system’s response time to user inputs is regularly monitored by conducting performance tests supported by a tool and using a fully representative test environment. At present the system runs reliably and response times to user trading transactions are just below the maximum specified.

The marketing department anticipates that with the new functionality being introduced in the next version, the number of users is expected to double over the next 12 months. You have included scalability tests into your performance testing strategy.

**When planning the performance efficiency tests, which of the following types of defects would you target in the system integration test plan as being the MOST likely to occur?**

    a. The simulated increase in the number of users will result in data volumes exceeding the bandwidth of the test environment
    b. The system fails to meet future response time requirements for the anticipated numbers of users
    c. The disk capacity requirements will exceed the resources available once more users are added
    d. The system’s response time will degrade when running the system for a long time under a nominal load

**Select ONE option.**

---

<details>
<summary><strong>Show Answer</strong></summary>

#### Correct Answer: b

    a. Is not correct. The test plan does not target defects in the test environment, but it targets defects in the product
    b. Is correct. Scalability testing focuses on the ability of a system to meet future performance efficiency requirements, which may be beyond those currently required. The scenario states that the current system’s response to user inputs is just below the maximum specified time, but that the number of users is expected to double over the next 12 months. There is a high risk that the planned scalability tests will show that the system fails to meet future requirements for the expected numbers of users
    c. Is not correct. There is no indication in the scenario that the system uses disk capacity resources. Compared to option b this is less likely to be a source of defects
    d. Is not correct. The scenario states that “At present the system runs reliably” - which suggests it does not have issues related to long time operation under nominal load and it is unlikely that the increase in the number of users will cause a degradation in response times when the system is run for a long time

</details>

---

[↑ Table of Contents](../../README.md#table-of-contents) | [← Previous Page](question-24.md) | [Next Page →](question-26.md)
