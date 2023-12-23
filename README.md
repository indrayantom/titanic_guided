# :star2:Titanic Dataset : Guided Predictive Learning with Logistic Regression:star2:

This work contains guided predictive analysis of the legendary Titanic dataset, downloaded from Kaggle. The term "guided" refers to the fact that there are steps and assumptions that have been predetermined before by my supervisor at dibimbing.id, who is later also the one who reviewed this assignment . This analysis however is carried out in R (Rstudio).

![ide](https://img.shields.io/badge/RStudio-75AADB?style=for-the-badge&logo=RStudio&logoColor=white)
![kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=Kaggle&logoColor=white)

Just in case you didn't know. The codes are contained in the .Rmd (Rmarkdown) file, whereas the results and codes are neatly combined in the .html file (knitted version of Rmarkdown). Feel free to download and open it [here](https://indrayantom.github.io/titanic_guided/) 😃😉.

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
One of the key findings is Pclass and Sex have the potential to be good predictors of the Survived variable. However, given that the Age distributions for both 1 and 0 Survived Passengers are roughly similar, Age may not have the same impact on Survived as Pclass and Age. It does provide an important information though that passengers under the age of eight have a better chance of survival.
![age_bin](https://user-images.githubusercontent.com/92590596/156569663-93dbb536-1573-46c5-a947-acd78f0f5a46.jpg)
Furthermore, after the modeling was conducted, the confusion matrix shows that the model performs well, with an accuracy of about 83 percent on the test dataset (15% of total data). However, because the model was trained on data with a small number of observations, I believe the model's accuracy may decreases if it is applied to test data with a larger number of observations. Another point to mention is that as expected, the model appears to be better at predicting passengers who did not survive. According to the confusion matrix, the model correctly guesses 56/64 (87.5 %) passengers who did not survive, which is considered better than guessing the survived passengers with 34/44 correct answers (77 %). It is also evident that the Precision on test data is 81%, which is quite high.  The reason for this deficiency may comes from the imbalances distribution of the target variable: Survived itself, that makes our model has more resources on learning the passengers who did not survive and becomes slightly biased.

## References
Logistic Regression is primarily not much different than the Linear Regression in regression problem. It still uses the "linear form" to calculate the Log odd (or Logit, that's why it's called Logistic), which the term "odd" here refers to the probability of positive label divided by the probability of negative label. The log function itself comes from the sigmoid function, which exists to make sure that the Probability of a sample is neither smaller than 0 nor higher than 1. Furthermore, the Logistic Regression uses Maximum Likelihood Estimation method to determine each variable's coefficient, not the Least Square method that is used in the Linear Regression. To obtain more comprehensive explanation about this topic, watch [this](https://www.youtube.com/watch?v=yIYKR4sgzI8) great video by StatQuest.

