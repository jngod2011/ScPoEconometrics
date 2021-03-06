# ScPo UG Econometrics

**Unix ShinyApp Tests and Book Build**: [![Build Status](https://travis-ci.org/ScPoEcon/ScPoEconometrics.svg?branch=master)](https://travis-ci.org/ScPoEcon/ScPoEconometrics)

**Windows ShinyApp Tests**: [![AppVeyor Build Status](https://ci.appveyor.com/api/projects/status/github/ScPoEcon/ScPoEconometrics?branch=master&svg=true)](https://ci.appveyor.com/project/ScPoEcon/ScPoEconometrics)

[![Gitter Chat](http://badges.gitter.im/ScPoEcon/ScPoEconometrics.svg)](https://gitter.im/ScPoEconometrics/Lobby)

This is the git repo for the UG Econometrics book taught to 2nd year students at SciencesPo.

## Usage and Installation

In order to participate in the course and to use the course material, you need to 

1. install `R`: download for free at [https://www.r-project.org](https://www.r-project.org)
2. install **this** `R` package in your computer. To do so, just copy and paste those lines into your `R` console:

```R
if (!require(devtools)) {install.packages("devtools"); library(devtools)}
install_github(repo = "ScPoEcon/ScPoEconometrics")
```

### Shiny Apps

A key part of this course are a series of interactive applications (or *apps*) that we developed with the `shiny` framework. You launch the apps from a running `R` session on your computer. The app will run in your web browser. You launch an app like this from `R`:

```R
library(ScPoEconometrics)   # load our library
launchApp('SSR_cone')       # runs the `SSR_cone` app in browser

launchApp()                 # no arg produces an error that shows all available apps
Error: Please run `launchApp()` with a valid app as an argument.
Valid apps are: 'anscombe', 'confidence_intervals', 'corr_continuous', 
'datasaurus', 'reg_constrained', 'reg_dummy', 'reg_dummy_example', 
'reg_full', 'reg_multivariate', 'reg_simple', 'reg_standardized', 
'sampling', 'SSR_cone', 'standard_errors_changeN', 'standard_errors_simple'
```

Here is a screenshot of the `SSR_cone` app:

![SSR_cone](images/SSR_cone.png)

### Tutorials

In order to run the accompanying tutorials you would type, for example:

```R
library(learnr)
run_tutorial("chapter3",package="ScPoEconometrics")
```

## Contribution Workflow

1. fork this repository
1. clone your fork to your computer: `git clone url_or_your_fork`
1. Start to work on your things on a new branch: `git checkout -b new_branch`
1. **commit** your work to that new branch! 
1. Place your new stuff on top of the most recent `upstream/master`:
	1. add the upstream repo as a remote: `git remote add upstream git@github.com:floswald/ScPoEconometrics.git`
	1. Use the `rebase` command
    ```
    # git add your stuff
    # git commit your stuff
    git fetch upstream   # get stuff from upstream
    git rebase upstream/master  # merge upstream master and put your commits on top of it
    ```
1. push that branch to your fork: `git push origin new_branch`
1. create pull request on `upstream`


## Technology

this book is made using bookdown.
You can find the preview of an example at https://bookdown.org/yihui/bookdown-demo/


## License

This work is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-nc-sa/4.0/)
![](images/cc.png)

You are free to:

* Share — copy and redistribute the material in any medium or format
* Adapt — remix, transform, and build upon the material

**under the following terms**:

1. Attribution — You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use. We are happy to suggest the following citation if you use our material in your work:

```
@book{
  oswald_robin_2018, 
  title={Introduction to Econometrics with R},
  url={https://scpoecon.github.io/ScPoEconometrics/}, 
  publisher={github.com}, 
  author={Oswald, Florian and Robin, Jean-Marc}, year={2018}
}
```
2. NonCommercial — You may not use the material for commercial purposes.
3. ShareAlike — If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.

### Attributions

Under the CC licence above, we are obliged to attribute any material that this book uses and which was shared under the same license:

1. Chapter 1 *Introduction to R* is copied almost entirely from [appliedstats](https://daviddalpiaz.github.io/appliedstats/) by [David Dalpiaz](https://daviddalpiaz.com). I added a couple of practical tasks and made some minor edits. 
1. Chapter 2 is partly based on [appliedstats](https://daviddalpiaz.github.io/appliedstats/), but only up to *scatterplots*.
