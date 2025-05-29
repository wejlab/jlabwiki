# Tips and Resources for Developers

These best practices will help you write clear, reproducible, and well-documented code, making code reviews and collaborations smoother.

---

## 1. Request Reviews Early

The earlier you ask for feedback, the less likely you'll need to make major revisions later.

---

## 2. Follow a Style Guide

Adhering to language-specific style guides improves readability and consistency.

**For R (tidyverse style):**
- [R tidyverse style guide](https://style.tidyverse.org/syntax.html)
- [styler package](https://styler.r-lib.org/): Automatically reformats code to match tidyverse standards.

---

## 3. Write Clear, Maintainable Code

### General Guidelines

- Use **descriptive variable names** (avoid `temp`, `final`, `var1`, etc.).
- Keep **lines under 80 characters** wide for readability.
- Functions should be **<50 lines long** to encourage modular, reusable code.

### For Packages

- Use small, focused functions with clear [`roxygen2`](https://roxygen2.r-lib.org/articles/roxygen2.html) headers.
- Inline comments should not be needed—function docs should be self-explanatory.

### For Analyses

- Use **R Markdown** files:
    - Include informative narrative text for each code block.
    - Minimize inline comments by using well-documented functions.
    - Store reusable functions in an `R/` directory and document with `roxygen2`.

### For Scripts

- Use **R Markdown** when possible.
- Comment generously throughout standalone scripts.

---

## 4. Use GitHub Effectively

All project code should be hosted on GitHub. Best practices include:

### For Analyses, Projects, or Papers

- Organize your repository with:
    - An R Markdown file for the analysis
    - A knit PDF version
    - Custom functions in an `R/` folder
    - A `README.md` with usage instructions
    - A `DESCRIPTION` file

### For Packages

- Follow [Hadley Wickham’s package guide](https://r-pkgs.org/)
- Follow Bioconductor standards

### GitHub Tips

- Ensure repositories contain everything needed to reproduce your results.
- Use GitHub Issues for bug tracking, feature requests, and reviewer feedback.
- Commit and push regularly (after verifying that your code works).
- Keeping your working version on GitHub helps prevent accidental loss and supports collaborative development.

---

## 5. Write Tests

Automated testing ensures that your code behaves as expected and is safe for others to use.

### When to Use Tests

- **Required** for code that will be reused or shared (e.g., packages).
- **Optional but recommended** for one-off analyses or exploratory code.

### Testing Best Practices

- Run standard checks:
    - `R CMD check`
    - `BiocCheck` (for Bioconductor submissions)

- Build in **input validation** with user-friendly error messages:
    - Use `if` statements to catch invalid inputs early.
    - Make error messages clear and actionable.

- Test **edge cases and expected behavior**:
    - Use [testthat](https://r-pkgs.org/testing-basics.html) for automated tests.

