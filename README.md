## Contents

1. [Project description](##1.-Project-description)
2. [Other project goals](##-2.-Other-project-goals)
3. [Some background on this project](##-3.-Some-background-on-this-project)
4. [Software utilized](##-4.-Software-utilized)
5. [R packages utilized](##-5.-R-packages-utilized)
6. [Installing software/packages](##-6.-Installing-software/packages)
7. [Included files](##-7.-Included-files)
8. [Other notes](##-8.-Other-notes)

## 1. Project description

This project outputs a .pdf file containing a list of spelling words and sight words. The list(s) are broken down by week number and by day-of-the-week for each numbered week.

## 2. Other project goals

* Work with *readxl* package since data file was in .xlsx format
* Continue working/practicing with `git` commands via the command line

## 3. Why this project

This project came about in March/April 2020 when the first guidelines for COVID-19 were starting to come out. Schools had recently closed and our school administration was working on a plan to help children continue with their learning. At that time, noone knew if the schools were going to re-open, and if so, when.

My wife and I wanted our child to keep up with the school curriculum as much as possible while isolating at home. Aside from other topics we could cover at home, we decided one important thing we could do is to continue practicing spelling words and going over sight words until further guidance came from the school board/school.

We already had a sizeable list of words from various materials that the teachers had sent home throughout the school year up to this point in time. We decided to start there while we waited on the school administration's continuing education plan. But, we didn't want to just review the word lists in a rote fashion. Instead, my wife asked me if I could develop something that could shuffle the word lists and also break them down into smaller groups by day and by week. So we split our efforts...she put the word lists in an Excel spreadsheet and I developed the script that shuffled the words and output the resulting product that we could review with our child over an 8-week period, 5-days per week.

My wife and I were happy to share the .pdf file with our child's teacher and other friends. The teacher, also working on putting study-at-home materials together, liked the list and shared it with other families in the class.

## 4. Software utilized

* MacOS Catalina    version 10.15.4
* RStudio           version 1.2.1335
* R                 version 3.6.0 (2019-04-26) -- "Planting of a Tree"
* MacTex-2018 Distribution

## 5. R packages utilized

* *tidyverse* version 1.2.1, which contains the following packages:
    + *ggplot2*   version 3.2.1
    + *purr*      version 0.3.3
    + *tibble*    version 2.1.3
    + *dplyr*     version 0.8.3
    + *tidyr*     version 1.0.0
    + *stringr*   version 1.4.0
    + *readr*     version 1.3.1
    + *forcats*   version 0.4.0
* *readxl* version 1.3.1
* *kableExtra* version 1.1.0

## 6. Installing software/packages 

NOTE: For all software installations, be sure to read the instructions for each software platform you plan to install. 

* Installing R
    + See the *Getting Started* section of the R Project homepage at https://www.r-project.org.
    + The software is open-source and freely available.
* Installing RStudio
    + You can download the Open Source Edition at the RStudio products page at https://rstudio.com/products/rstudio/.
    + There is a Open Source Edition and a commercial option (RStudio Desktop Pro) available. Ensure that you select the appropriate version that suits your needs.
* Installing MacTex
    + Download MacTex from the Tex Users Group website at https://www.tug.org/mactex/.
    + The software is open-source and freely available.
* Installing R packages
    + In the R or RStudio console, type the command `install.packages("package name")`. 
    + R-bloggers, a popular blog posts about R, also has some good information to help with installing R packages at https://www.r-bloggers.com/installing-r-packages/.

## 7. Included files

| Filename | Description |
| --- | --- |
| README.md | Info about project / repository |     
| spelling_sight_words.xlsx | Data file containing two columns of words |     
| spelling_practice.Rmd | Project source code file |
| spelling-practice.pdf | Project output file |

## 8. Other notes

* The .Rmd script produces 8-weeks of daily word lists, as written. To change the number of weeks to your desired duration, simply change the value of the `numweeks` variable (code line 86).
* If you don't have a LaTex distribution, like MacTex, installed, you can create a Word document instead. Simply change code line 3 to `word_document: default`. 
* This script reads data from a .xlsx file. It can be adapted to read a .csv or other type of delimted file as needed.