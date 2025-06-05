# Manuscript Submission Checklist
When working on a manuscript to submit to a journal, these are the ideal tasks 
that should be completed prior to submission. Some circumstances might 
necessitate adaptation, in which case, please talk to Evan about adapting any 
of the below items.

## Manuscript
- [ ] Written and styled according to Journal Guidelines
- [ ] Shared with Pod for feedback w/ accompanying code (see below)
- [ ] Feedback from Pod incorporated
- [ ] Shared with collaborators w/ accompanying code
- [ ] Submitted to biorxiv or other preprint server
- [ ] Submit to Journal

### Code to Accompany Manuscript
- [ ] All Code is hosted on GitHub
    - [ ] R Markdown file that follows the flow of your manuscript, including:
        - [ ] Starting with raw data retrieval
        - [ ] Cleaning/pre-processing data
        - [ ] Analyzing data
        - [ ] Figure creation
        - [ ] `sessionInfo()` code block
        - [ ] Descriptions throughout the document
    - [ ] R Markdown PDF/HTML
        - Timeless instance of your work 
    - [ ] R folder
        - [ ] Separate file for any functions you created to simplify your 
        RMarkdown file or that other users should use to implement your findings 
        in their own work
        - [ ] Each function should have a roxygen description
        - [ ] Functions that readers should use should include an example in the
        roxygen description
    - [ ] README file
        - [ ] Description of how to use the files in the repository
        - [ ] Point to the R Markdown file that contains manuscript analyses
        and figures
       - [ ] Specifically direct the user to functions that they should use in 
       their own work (or to packages that may contain this info)
    - [ ] DESCRIPTION file
        - [ ] See requirements for R packages (https://r-pkgs.org/description.html)
        - [ ] Includes: package (analysis) name, title, authors, imports 
        (list of all required packages), R version used, etc
    - [ ] Data Folder (if data is not hosted elsewhere and retrieved in 
    rMarkdown file)
        - [ ] Contains all data for analysis
- [ ] Data has been submitted to an appropriate database (ex: Sequence Read 
Archive)
- [ ] Repository provided to Pod for Review, including:
    1. Fork the repository to your own GitHub
    2. Replicate the R Markdown on personal machine
        - [ ] Should match the knit PDF R markdown file provided in the 
        repository
        - [ ] Can you access all the data used in the analysis?
        - [ ] If differences exist, ensure it is not a version issue or a run
        time environment difference
        - [ ] Only move to steps 2 and 3 when this step is complete; meet as 
        soon as possible with the developer if problems arise
    3. Is the code clearly commented and easily readable?
        - [ ] R Markdown is clear and follows the flow of the manuscript
        - [ ] R folder functions all have clear roxygen comments
    4. Any other vital changes that may be needed
    5. Record Feedback as “Issues” and/or provide pull request for edits
- [ ] Code updated based on Reviewer Feedback
- [ ] Once finalized, ensure that a forked version is available on wejlab page 
(Evan, Jessica, or Aubrey can do this)
