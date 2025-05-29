# Tips and Resources for Developers
1. The earlier you request a review, the less likely you will be asked to make large modifications.
2. Be familiar with the style guide for the languages you use.
    - [R tidyverse style guide](https://style.tidyverse.org/syntax.html):
        - Package that provides automatic test for adherence to the R tidyverse 
        style guide
    - [styler](https://styler.r-lib.org/):
        - Package that reformats files, directories, or packages to adhere to 
        the R tidyverse style guide
3. Write Clear Code
    - Packages should contain small functions with well-defined descriptions 
    (roxygen headers) and should not need in-line comments
    - Analyses should be in R Markdown and contain informative descriptions for 
    each code block. There should be minimal comments in the code and custom 
    functions should be used and documented in a separate folder.
    - Scripts should have comments throughout and should be in R Markdown files 
    with associated functions whenever possible
    - Use well-defined variable names
        - Avoid: var1, temp, random, v, final, etc
    - Functions should be <50 lines (this helps maintain good documentation 
    without needing comments in the code)
    - Lines should be <80 characters wide to maintain readability
    - Use [roxygen](https://roxygen2.r-lib.org/articles/roxygen2.html) 
    descriptions for functions 
    
4. Use GitHub
    - All code should be hosted on GitHub
        - For analyses/papers: analyses in R Markdown file, include a knit PDF,
        functions in an R/ directory, a README.md, and a DESCRIPTION file
        - Packages should follow 
        [Hadley Wickham’s Package guide](https://r-pkgs.org/)
    - Repository should have all details needed to replicate your 
    results/figures
    - Use the issue tracker for peers to report problems and for you to mark 
    when they are resolved
    - Push often (after testing and knowing that additions/changes work)
    - Should alleviate the “I don’t want to break my code” concerns since your 
    last working version should always be available on GitHub
5. Create tests
    Tests can be helpful tools to easily and automatically ensure that your code 
    runs as expected. Tests may not be necessary for analyses or one-off code, 
    but any code written and intended for others to use should:
    - Pass developer checks
        - R CMD
        - BiocCheck
    - Have checks/safeguards against incorrect use built into the code
        - Ex: if statements with printout telling the user why their input is 
        invalid
        - Please think of the user when creating your warning message and try to
        be as clear as possible to point them to a solution
    - Be tested for edge cases
        - Create automatic tests for edge cases as well as expected use cases 
        using [testthat](https://r-pkgs.org/testing-basics.html)
