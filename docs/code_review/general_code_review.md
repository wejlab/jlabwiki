# General Code Review Guidelines

## For Developers

To support an effective code review, developers should provide reviewers with:

- A **brief written description** of the code's **goal or objective**
- A **clear explanation of all inputs**
- A **sample input or dataset**
- A **code chunk of 150–200 lines** (maximum per review session)

## For Reviewers

Reviewers should:

- Plan to spend **~1 hour per 200 lines of code**
- Evaluate the code by considering:
    - Does the code run successfully and produce the intended output?
    - Is the code **well commented** and easy to follow?
    - Could **repeated code** be refactored into functions?
    - Are there **more efficient methods or functions** that could be used?
    - Is the **code readable and well-organized**?
    - Are **edge cases or input checks** addressed (especially for shared code)?
    - What did you learn that you might apply in your own work?
- Provide a **written summary** that includes:
    - **Constructive suggestions**
    - **Positive feedback**
- Aim to provide feedback **promptly**, so the developer isn't blocked from progressing

## Feedback Formats

### Offline Exchange

- Developer sends:
    - Code file
    - Data file or data access instructions
- Reviewer responds with:
    - A **written review**, similar to a manuscript critique
- Both parties **agree on a turnaround time**

### Real-time Meeting (Preferred)

- Reviewer provides:
    - **Real-time comments**
    - **Written notes** summarizing needed changes
- Ideal workflow:
    - Developer and reviewer **schedule a meeting** (e.g., Wednesday at 3 PM)
    - Code is shared **two business days before** (e.g., by EOD Monday)
    - Meeting held for discussion
    - Any unresolved items are **followed up in writing**

## Setting Specific Expectations

These general guidelines should be adapted depending on the review context. Lab members are expected to participate regularly in the following review types:

- [Informal Code Review](informal_code_review.md)
- [Lab Meeting Code Review](lab_meeting_code_review.md)
- [Manuscript Submission Code Review](manuscript_code_review.md)
