# Manuscript Submission Code Review
Manuscript submission code reviews are the most extensive review in our lab. The
purpose of these reviews is to ensure that all code provided within the context 
of the manuscript (including data access, data pre-processing, analysis, 
table/figure generation, etc) is accessible to the public, reproducible, 
well-documented, and well-organized. When preparing to submit a draft manuscript
to a publication site, a simultaneous code review should occur before submitting
a completed manuscript and associated code. This code review should be completed
by at least two pod members and then discussed during a planned pod meeting. Be 
mindful of your reviewer’s time and give them at least 1 week to properly review
your code before meeting to discuss any recommended revisions. Provide the 
GitHub repository and a draft of your manuscript to each reviewer.

## Manuscript GitHub Repository
All analysis manuscript materials should be available as a single GitHub 
repository, except data, which may be hosted on a publicly available database 
elsewhere. If the data is hosted elsewhere, the GitHub repository must contain 
a file, function, or R markdown section that retrieves the data. Organizing a 
repository as follows eases the ability for others to replicate your work and 
use it in their own work. Creating these files and this repository may require 
rewriting/reformatting your analysis files; however, taking the time throughout 
an analysis to properly document your work, develop functions, and follow a 
style guide will minimize the amount of work needed when it comes time to 
publish.

### GitHub Repository Organization
- R Markdown file that follows the flow of your manuscript, including:
    - Starting with raw data retrieval
    - Cleaning/pre-processing data
    - Analyzing data
    - Figure creation
    - `sessionInfo()` code block
    - Descriptions throughout the document
- R Markdown PDF
    - Timeless instance of your work 
- R folder
    - Separate file for any functions you created to simplify your RMarkdown 
    file or that other users should use to implement your findings in their own 
    work
    - Each function should have a roxygen description
    - Functions that readers should use should include an example in the roxygen 
    description
- README file
    - Description of how to use the files in the repository
        - Point to the R Markdown file that contains manuscript analyses and 
        figures
        - Specifically direct the user to functions that they should use in 
        their own work (or to packages that may contain this info)
- DESCRIPTION file
    - See requirements for R packages (https://r-pkgs.org/description.html)
    - Includes: package (analysis) name, title, authors, imports (list of all 
    required packages), R version used, etc

## Reviewers’ Role
The reviewers should be able to clone the manuscript repository from GitHub and 
provide feedback on the following:
1. Replicate the R markdown on their machine
    - Should match the knit PDF R markdown file provided in the repository
    - Can you access all the data used in the analysis?
        - Avoid local data storage when possible (aka, should not need calls to 
        user files or working directory)
    - If differences exist, ensure it is not a version issue or a runtime 
    environment difference
    - Only move to steps 2 and 3 when this step is complete; meet as soon as 
    possible with the developer if problems arise
2. Is the code clearly commented and easily readable?
    - R Markdown is clear and follows the flow of the manuscript
    - R folder functions all have clear roxygen comments
3. Any other vital changes that may be needed (see General Guidelines for 
reviewers)

Feedback should be provided as “Issues” on the GitHub repository whenever 
possible, but can also include a written summary (remember to include praise).
The reviewer should be able to independently recreate the R Markdown file 
(including accessing raw data, creating all figures/tables, completing analyses,
etc) and should be able to understand how to use associated functions. If the 
reviewer needs to reach out for clarification, the author MUST modify the code 
(perhaps a better README description, description blocks in the R Markdown file,
or roxygen descriptions for functions).
