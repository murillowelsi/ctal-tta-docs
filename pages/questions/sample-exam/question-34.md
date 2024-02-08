# Technical Test Analyst Exam

## [TTA-5.2.2: Code Reviews](../../5-reviews/5.2-using-checklists-in-reviews.md#522-code-reviews)

### Question #34 (3 Points) - K4

You are participating in a code review and have noticed a problem in the following section of pseudo-code (assume \*\*\* indicates a comment).

```pseudo
***This code checks for the validity of a card type:***
if credit card is type “Discover” then
    Display error message 437
else if credit card is type “Visa” or “MasterCard” then
    Process purchase
else if credit card is type “AmericanExpress” then
    Display error message 439
else
    Display error message 440
end if
```

**Which of the following problems is demonstrated in this section of code and why should it be corrected?**

    a. The comment in the code is incorrect, resulting in a maintainability impact
    b. An external library should be used to validate the credit card; thus, the code is inefficient because it does not re-use existing components
    c. The most likely case is not tested first, resulting in a potential performance impact
    d. There is no default clause, resulting in potential cases not being handled

**Select ONE option.**

---

<details>
<summary><strong>Show Answer</strong></summary>

#### Correct Answer: c

    a. Is not correct. The comment is correct – the code does check the validity of the card
    b. Is not correct. It is unlikely that there is an external library available that provides this functionality
    c. Is correct. It is unlikely that invalid ‘Discover’ cards will be entered more often than valid cards, so it is most likely the card will be Visa or MasterCard, and so that check should be performed first
    d. Is not correct. The ‘else’ handles all conditions not met by the preceding ‘if’ statements

</details>

---

[↑ Table of Contents](../../README.md#table-of-contents) | [← Previous Page](question-33.md) | [Next Page →](question-35.md)
