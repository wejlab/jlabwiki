# Manuscript Submission Code Review

Manuscript submission code reviews are the most in-depth reviews conducted in 
the lab. Their primary goals are to ensure that **all code related to a 
manuscript** is:

- Publicly accessible  
- Reproducible  
- Well-documented  
- Well-organized

This includes code for **data access, preprocessing, analysis, and table/figure 
generation**.

## When to Initiate a Review

A manuscript code review should take place **before submitting the final draft** 
to a journal or preprint server. At least **two pod members** must complete the 
review, which could be discussed in a scheduled pod meeting.

- **Give reviewers at least 1 week** to complete their review
- Provide each reviewer with:
    - A link to the GitHub repository
    - A draft of the manuscript

---

## Manuscript GitHub Repository

All analysis-related materials must be included in a single GitHub repository. 
Data may be hosted externally, but the repository must contain clear 
instructions or code to **retrieve that data**.

> Tip: Well-documented, modular code written throughout the project will reduce 
the workload during manuscript prep.

### Recommended Repository Structure

- **R Markdown file**
    - Follows the manuscript's logic and structure:
        - Raw data retrieval
        - Data cleaning and preprocessing
        - Data analysis
        - Figure/table creation
        - `sessionInfo()` block
        - Clear narrative text throughout
- **PDF of the R Markdown**
    - A static, reproducible version of the work
- **`R/` folder**
    - Custom functions split into separate `.R` files
    - All functions documented using `roxygen2`
    - Include usage examples for key user-facing functions
- **`README.md`**
    - Overview of repository structure
    - Instructions for running the analysis (i.e., point to the specific `.md` file)
    - Direct user to key functions
- **`DESCRIPTION` file**
    - Follows [R package standards](https://r-pkgs.org/description.html)
    - Must include: name, title, authors, R version, and required packages

---

## Reviewer Responsibilities

Reviewers should **clone the repository** and assess the following:

1. ### Reproducibility
    - Can the R Markdown be run start-to-finish on your machine?
    - Output should match the included PDF.
    - All required data should be accessible (no local paths or hardcoded directories).
    - If errors occur, confirm whether they stem from environment/version differences.
    - Resolve these issues **before** moving to steps 2 and 3.

2. ### Code Quality
    - R Markdown is clear and matches the manuscript's structure.
    - Code is well-commented.
    - Functions in the `R/` folder have clear `roxygen2` documentation.

3. ### General Feedback
    - Provide suggestions for improvement.
    - Reference the [General Guidelines for Reviewers](#) for additional points.

---

## Giving Feedback

- Use **GitHub Issues** for detailed comments
- A brief **written summary** is also encouraged—include both praise and suggestions
- Reviewers should be able to:
    - Reproduce the analysis independently
    - Understand how to use any included functions

If clarification is needed, the author must update the code (e.g., improve 
README, improve object names, or expand function descriptions).
