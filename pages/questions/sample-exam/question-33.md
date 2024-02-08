# Technical Test Analyst Exam

## [TTA-5.2.1: Architectural Reviews](../../5-reviews/5.2-using-checklists-in-reviews.md#521-architectural-reviews)

### Question #33 (3 Points) - K4

You are participating in an architectural design review of a new product design. This is a webbased currency trading product that provides real-time information on prices for currencies selected by the user.

The following list of practices are mentioned in the design as options for ensuring response times of less than 1 second and real-time data accuracy under maximum expected loads.

**Which of the following practices would you highlight as the MOST promising for achieving the requirement?**

    a. Load balancing
    b. Data caching
    c. Object orientation
    d. Data replication

**Select ONE option.**

---

<details>
<summary><strong>Show Answer</strong></summary>

#### Correct Answer: a

    a. Is correct. Load balancing should ensure that peak volumes of traffic can be handled by spreading the load among available servers
    b. Is not correct. Caching data may provide fast response times but may not guarantee that rapidly changing currency rates are accurately shown in real-time
    c. Is not correct. Object orientation practices do not target performance efficiency
    d. Is not correct. Data replication may not guarantee that the constantly changing currency rates are accurately shown in real-time

</details>

---

[↑ Table of Contents](../../README.md#table-of-contents) | [← Previous Page](question-32.md) | [Next Page →](question-34.md)
