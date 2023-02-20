# ps05-rmarkdown-plot
# title: "gapminder"
# author: "Jin Hee Lee"
# date: '2022-02-17'
# output: html_document

library(utils)
library(tidyverse)
# 1. (1pt) For solving the problems, and answering the questions, create a new rmarkdown document with an appropriate title. See https://faculty.washington.edu/otoomet/info201-book/
## r-markdown.html#r-markdown-rstudio-creating.

# 2. (2pt) Load data. How many rows/columns do we have?
gap <- read_delim("gapminder 2.csv")
nrow(gap)
ncol(gap)

# 3. (2pt) Print a small sample of data. Does it look OK?
gap %>%
head(3)

# <2 Descriptive statistics (15pt)?> 

# 1. (3pt) How many countries are there in the dataset? Analyze all three: iso3, iso2 and name.
# 2. If you did this correctly, you saw that there are more names than iso-2 codes, and there are
# even more iso3 -codes. What is going on? Can you find it out?
# (a) (5pt) Find how many names are there for each iso-2 code. Are there any iso-2 codes that correspond to more than one name? What are these countries?
# (b) (5pt) Now repeat the same for name and iso3-code. Are there country names that have more than one iso3-code? What are these countries?
# Hint: two of these entitites are CHANISL and NLD CURACAO.
# 3. (2pt) What is the minimum and maximum year in these data?