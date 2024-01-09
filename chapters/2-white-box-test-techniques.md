# Chapter 2: White-Box Test Techniques

## 2.1 Introduction

- [x] **Date Completed:** 08/01/2024 - **Understanding Level:** 😊
  - White-box test techniques apply to code and structures with control flow.
  - Techniques enable systematic test case derivation and focus on specific aspects of the structure.
  - Test cases aim to satisfy coverage criteria and achieve full coverage.
  - Test inputs are generated to exercise specific parts of the code.
  - Expected results are determined based on external sources like requirements or design specifications.
  - Techniques covered in the syllabus include:
    - Statement testing
    - Decision testing
    - Modified condition/decision testing
    - Multiple condition testing
    - API testing
  - Foundation Syllabus introduces statement and decision testing.
  - Modified condition/decision and multiple condition techniques detect defects based on decision predicates.
  - [ISO 29119] provides more details and examples for these techniques.

## 2.2 Statement Testing

- [x] **Date Completed:** 08/01/2024 - **Understanding Level:** 😊
  - Statement testing exercises executable statements in code.
  - Coverage is measured as the ratio of executed statements to total executable statements (expressed as a percentage).
  - Achieving full statement coverage is ideal but not always possible due to time or effort constraints.
  - High percentages of statement coverage may still miss some defects in code logic.
  - Unreachable code can make achieving 100% statement coverage impossible, often due to default cases in switch statements when all possible cases are explicitly handled.
  - Constraints on available time and effort can limit achieving full statement coverage.
  - Certain defects in code logic may go undetected even with high statement coverage.

### Statement Coverage Example

- Consider a simple Python function:

```python
def divide(a, b):
    result = 0
    if b != 0:
        result = a / b
    return result
```

- In this code, the executable statements are the ones inside the if block. Statement coverage would involve executing those statements.
- However, achieving 100% statement coverage may not guarantee that all potential issues are caught, such as checking for negative values or other edge cases.

### Limitations/Difficulties

- **Limited Time/Effort:** If you have a large codebase, testing every statement may take too long or require too much effort, making it impractical.
- **Incomplete Coverage:** Achieving 100% statement coverage may not guarantee that all code paths and edge cases are tested. For example:

```python
def divide(a, b):
    result = 0
    if b != 0:
        result = a / b
    else:
        print("Division by zero!")
    return result
```

- Even with 100% statement coverage, you may miss testing the "Division by zero!" message.

```python
def unreachable_example(x):
    if x > 0:
        print("x is positive")
    else:
        print("x is non-positive")
```

- Achieving 100% statement coverage here is impossible because only one of the if or else branches will ever be executed, not both.

## 2.3 Decision Testing

- [x] **Date Completed:** 09/01/2024 - **Understanding Level:** 😊

  - Decision testing focuses on testing decision outcomes in code.
  - Test cases follow control flows from decision points **(e.g., IF, CASE, LOOP statements)**.
  - Coverage is measured as a percentage of decision outcomes exercised by tests.
  - It evaluates TRUE and FALSE outcomes of decisions, regardless of internal complexity.
  - Branch testing is often used interchangeably with decision testing and covers control flow branches.
  - For programs with no decisions, ISO 29119-4 requires at least one test to achieve 100% decision coverage.
  - **Applicability:** critical code and any models with decision points.
  - **Limitations:** not considering details of decisions with multiple conditions and potential defect detection issues.
  - If you have nested IF decisions, you can use a simple formula to solve the exercise.

  ```javascript
  (Number of IFs + 1)
  ```

### Decision Testing Example

- How many test cases would you design to achieve 100% decision coverage?

  ```javascript
  IF A THEN
      IF B THEN
          Statement Q
      ELSE
          Statement R
      ENDIF
  ELSE
      Statement S
      IF C THEN
          Statement T
      ELSE
          Statement U
      ENDIF
  ENDIF
  Statement V
  ```

- Minimum test cases for a 100% Decision Coverage = **4**
- Number of IFs = **3** + **1** = **4 Test Cases**

## 2.4 Modified Condition/Decision Testing

- [x] **Date Completed:** 09/01/2024 - **Understanding Level:** 😐

  - Modified Condition/Decision Testing (MC/DC) is a testing technique that focuses on how decisions are structured, especially when they contain multiple conditions.
  - Each decision predicate consists of one or more atomic conditions, and MC/DC checks if each atomic condition independently influences the decision's outcome.
  - It provides stronger coverage than statement and decision coverage when dealing with decisions with multiple conditions.
  - Achieving MC/DC typically requires testing a decision N+1 times, assuming N unique, mutually independent atomic conditions.
  - **Applicability:** MC/DC is especially useful in safety-critical industries like aerospace and automotive, where software failures can have catastrophic consequences.
  - **Limitations:** difficulties may arise when multiple occurrences of the same variable in a decision with multiple conditions are coupled, making it challenging to achieve MC/DC.
  - Some compilers or interpreters exhibit short-circuiting behavior, which can affect MC/DC testing by preventing the evaluation of all conditions in a decision.
  - Configuring compilers to disable short-circuiting may not be allowed in safety-critical applications where code testing and delivered code must be identical.

  - Applying the Modified Condition/Decision Testing (MC/DC) technique to the scenario `(A && (B | C))`

    | Tests | A   | B   | C   | Outcome |
    | ----- | --- | --- | --- | ------- |
    | 1     | T   | T   | T   | T       |
    | 2     | T   | T   | F   | T       |
    | 3     | T   | F   | T   | T       |
    | 4     | T   | F   | F   | F       |
    | 5     | F   | T   | T   | F       |
    | 6     | F   | T   | F   | F       |
    | 7     | F   | F   | T   | F       |
    | 8     | F   | F   | F   | F       |

  - For **A**: {1,5} {2,6} {3,7} `This demonstrates that **A** independently affects the outcome.`
  - For **B**: {2,4} `This demonstrates that **B** independently affects the outcome.`
  - For **C**: {3,4} `This demonstrates that **C** independently affects the outcome.`

## 2.5 Multiple Condition Testing

- [x] **Date Completed:** 09/01/2024 - **Understanding Level:** 😊

  - Multiple condition testing is used to test all possible combinations of atomic conditions in a decision.
  - It requires exercising a decision 2^N times, where N is the number of unique, mutually independent atomic conditions.
  - Coverage is measured as the percentage of exercised atomic condition combinations over all decisions in the test object.
  - **Applicability:** This technique is used for high-risk and embedded software expected to run reliably for extended periods.
  - **Limitations:** large number of test cases required and potential reduction in condition combinations due to short-circuiting in compilers.

  - Applying the **Multiple Condition Testing** technique to the scenario `(A && (B | C))`

    | Tests | A   | B   | C   | Outcome |
    | ----- | --- | --- | --- | ------- |
    | 1     | T   | T   | T   | T       |
    | 2     | T   | T   | F   | T       |
    | 3     | T   | F   | T   | T       |
    | 4     | T   | F   | F   | F       |
    | 5     | F   | T   | T   | F       |
    | 6     | F   | T   | F   | F       |
    | 7     | F   | F   | T   | F       |
    | 8     | F   | F   | F   | F       |

  - Minimum Test Cases for 100% Multiple Condition Testing coverage is 2^N
  - N is the number of conditions
  - In this case above we should have 8 test cases -> 2^8.

## 2.6 Basis Path Testing

- [ ] **Date Completed:** - **Understanding Level:** 😊😐🤢🤮

## 2.7 API Testing

- [ ] **Date Completed:** - **Understanding Level:** 😊😐🤢🤮

## 2.8 Selecting a White-Box Test Technique

- [ ] **Date Completed:** - **Understanding Level:** 😊😐🤢🤮

### 2.8.1 Non-Safety-Related Systems

- [ ] **Date Completed:** - **Understanding Level:** 😊😐🤢🤮

### 2.8.2 Safety-related systems

- [ ] **Date Completed:** - **Understanding Level:** 😊😐🤢🤮

---

[Previous Chapter](1-technical-test-analysts-tasks-in-risk-based-testing.md) | [Next Chapter](3-static-and-dynamic-analysis.md)
