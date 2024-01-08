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

- [ ] **Date Completed:** - **Understanding Level:** 😊😐🤢🤮
  - Statement testing exercises executable statements in code.
  - Coverage is measured as the ratio of executed statements to total executable statements (expressed as a percentage).
  - Achieving full statement coverage is ideal but not always possible due to time or effort constraints.
  - High percentages of statement coverage may still miss some defects in code logic.
  - Unreachable code can make achieving 100% statement coverage impossible, often due to default cases in switch statements when all possible cases are explicitly handled.
  - Constraints on available time and effort can limit achieving full statement coverage.
  - Certain defects in code logic may go undetected even with high statement coverage.

#### Statement Coverage Example

Consider a simple Python function:

```python
def divide(a, b):
    result = a / b
    return result
```

- To achieve 100% statement coverage, you need to write test cases that execute both lines of code:

  - Test Case 1: divide(6, 2) - This will execute both lines and return a result.
  - Test Case 2: divide(8, 0) - This will execute both lines and raise a ZeroDivisionError.

- However, achieving 100% statement coverage may not guarantee that all potential issues are caught, such as checking for negative values or other edge cases.

## 2.3 Decision Testing

- [ ] **Date Completed:** - **Understanding Level:** 😊😐🤢🤮

## 2.4 Modified Condition/Decision Testing

- [ ] **Date Completed:** - **Understanding Level:** 😊😐🤢🤮

## 2.5 Multiple Condition Testing

- [ ] **Date Completed:** - **Understanding Level:** 😊😐🤢🤮

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
