# :star2:Titanic Dataset : Guided Predictive Learning with Logistic Regression:star2:

This work contains guided predictive analysis of the legendary Titanic dataset, downloaded from Kaggle. The term "guided" refers to the fact that there are steps and assumptions that have been predetermined before by my supervisor at dibimbing.id, who later commented my work being "*very impressive*" . This analysis however is carried out in R (Rstudio).

![ide](https://img.shields.io/badge/RStudio-75AADB?style=for-the-badge&logo=RStudio&logoColor=white)
![kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=Kaggle&logoColor=white)

Just in case you didn't know. The codes are contained in the .Rmd (Rmarkdown) file, whereas the results and codes are neatly combined in the .html file (knitted version of Rmarkdown). Feel free to download and open it [here](https://indrayantom.github.io/ames_directedDEA/) 😃😉.

## Objectives
Titanic dataset is the legendary dataset which contains demographic and traveling information of some Titanic passengers, and the goal is to predict the survival of these passengers. The accident happened in 1912 when the ship RMS Titanic struck an iceberg on its maiden voyage and sank, resulting in the deaths of most of its passengers and crew.  The problems that have to be answered in this work consist of:

- Do quick analysis for these variables : Sex, Age dan Pclass. Is it good to use them as a predictor for the target variable?
- Build the logistic regression model to predict the Survived variable by using Age, Pclass and Sex . Use threshold = 0.5 and evaluate your model whether it gives such a good result.
- Analyze the mistakes of your model!

## Libraries
This work mainly done using tidyverse environment. However, i also used another libraries to make plots and do certain calculations such as :

- [tidyverse](https://www.tidyverse.org/)
- [caret](https://cran.r-project.org/web/packages/caret/vignettes/caret.html)
- [patchwork](https://patchwork.data-imaginist.com/)
- [psych](https://cran.r-project.org/web/packages/psych/index.html)
- [caTools](https://cran.r-project.org/web/packages/caTools/index.html)

## Result preview
According to my hypotheses, the US Economy Crisis had an impact on house sale activity at the time. As a result, this phenomenon could be linked to why there are houses with large ground living area at such low prices.
![preview](https://user-images.githubusercontent.com/92590596/145586144-61ee3f84-26f2-438d-9634-abe93e6c45e2.png)
According to https://www.investopedia.com/terms/g/great-recession.asp , The Great Recession was the sharp decline in economic activity during the late 2000s. It is considered the most significant downturn since the Great Depression. The term Great Recession applies to both the U.S. recession, officially lasting from December 2007 to June 2009, and the ensuing global recession in 2009. The economic slump began when the U.S. housing market went from boom to bust, and large amounts of mortgage-backed securities (MBS’s) and derivatives lost significant value. In Ames however, we get interesting result that that the prices were stagnant during 2006-2010. These years was surely a nightmare for all real estate inventors because the prices didn’t raise year after year.

## References
Logistic Regression is primarily not much different than the Linear Regression in regression problem. It still uses the "linear form" to calculate the Log odd (or Logit, that's why it's called Logistic), which the term "odd" here refers to the probability of positive label divided by the probability of negative label. The log function itself comes from the sigmoid function, which exists to make sure that the Probability of a sample is neither smaller than 0 nor higher than 1. Furthermore, the Logistic Regression uses Maximum Likelihood Estimation method to determine each variable's coefficient, not the Least Square method that is used in the Linear Regression. To obtain more comprehensive explanation about this topic, watch [this](https://www.youtube.com/watch?v=yIYKR4sgzI8) great video by StatQuest.

