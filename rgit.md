# Setting up R studio and github.
From a fresh computer

1) [Download R](https://cran.r-project.org/bin/macosx/)
2) [Download RStudio](https://www.rstudio.com/products/rstudio/download/)
3) Install git
    * Search for terminal in finder on a Mac
    * First [install homebrew](https://brew.sh/) using `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
    * You may have to run three lines that begin with "echo" after this step
    * Then use `brew install git`
5) Setup your git user configuration.
    ```
    $ git config --global user.name "John Doe"
    $ git config --global user.email johndoe@example.com
    ```
6) Finally, you need to authenticate with github using a personal access token.
7) Go to [https://github.com/settings/tokens](https://github.com/settings/tokens) and click “Generate token”. Copy this token that is pretty long to somewhere safe so you can access again if needed. 
8) Now, within R, install the gitcreds package `install.packages('gitcreds')` and load the library: `library(gitcreds)`
9) When you enter the command: `gitcreds::gitcreds_set()`, you will get the following message: `Enter password or token:` 
10) Add your personal access token here. You should get the following messages:
    ```
    -> Adding new credentials...
    -> Removing credentials from cache...
    -> Done.
    ```
11) You should now be able to use Rstudio with github. In the top right corner, where it says "no project", click `create new project`, which will bring up the new project wizard. Select `Version Control`, then `Git`, then enter the repository URL. After you create Project, you should then be able to commit, pull and push from the github directory.
12) Happy Githubbing!
