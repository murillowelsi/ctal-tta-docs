# Technical Test Analyst Exam

## [TTA-3.2.3: Using Static Analysis for Improving Maintainability](../../3-static-and-dynamic-analysis/3.2-static-analysis.md#323-using-static-analysis-for-improving-maintainability)

### Question #15 (2 Points) - K3

You have been provided with the following system-wide average measures for the four systems, W, X, Y and Z, using static code analysis.

|            Metric            |  W   |   X    |   Y    |   Z    |
| :--------------------------: | :--: | :----: | :----: | :----: |
|  Cyclomatic Complexity (CC)  |  23  |   8    |   12   |   7    |
|        Cohesion (CH)         | High | Medium |  Low   |  High  |
|        Coupling (CP)         | Low  |  High  | Medium | Medium |
|     Commented Code (CO)      | 60%  |  10%   |  45%   |   8%   |
| Repeated code instances (RE) |  9   |   2    |   3    |   12   |

Budget is available to improve the maintainability of the code in each of the four systems by applying the results of static analysis to the individual components.

**Which of the following is the BEST way to improve maintainability of the code if you can address only two metrics per system?**

    a. W – CO, RE | X – CC, CH | Y – CP, CO | Z – CC, RE
    b. W – CC, CP | X – CH, CO | Y – CC, CH | Z – CO, RE
    c. W – CC, RE | X – CP, CO | Y – CC, CH | Z – CO, RE
    d. W – CH, CO | X – CC, RE | Y – CP, RE | Z – CC, CH

**Select ONE option.**

---

<details>
<summary><strong>Show Answer</strong></summary>

#### Correct Answer: c

**Cyclomatic Complexity (CC)** indicates the number of independent paths tough the code. - The higher the CC number, the worse code maintainability is likely to be, hence system W and Y should be addressed in this area.

**Cohesion (CH)** is a measure to which a module is self-contained and focused on a single task. - The lower it is, the worse the code maintainability is likely to be. Hence system Y should be addressed in this area.

**Coupling (CP)** is a measure of the degree to which modules rely on each other. - The higher it is, the worse the code maintainability is likely to be. Hence system X should be addressed in this area.

**Commented Code (CO)** indicates how much of the code is documented by comments. - Less comments indicates worse code maintainability. Hence systems X and Z should be addressed in this area.

**Repeated code instances (RE)** count how many code instances are duplicated. - The higher the number, the worse the code maintainability is likely to be. Hence systems W and Z should be addressed in this area.

Thus:

    a. Is not correct
    b. Is not correct
    c. Is correct (W – CC, RE | X – CP, CO | Y – CC, CH | Z – CO, RE)
    d. Is not correct

</details>

---

[↑ Table of Contents](../../README.md#table-of-contents) | [← Previous Page](question-14.md) | [Next Page →](question-16.md)
