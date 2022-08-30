# Predicting California Median Housing Prices README
[![en](https://img.shields.io/badge/lang-en-red.svg)](https://github.com/jonatasemidio/multilanguage-readme-pattern/blob/master/README.md)
[![pt-br](https://img.shields.io/badge/lang-pt--br-green.svg)](https://github.com/jonatasemidio/multilanguage-readme-pattern/blob/master/README.pt-br.md)
[![es](https://img.shields.io/badge/lang-es-yellow.svg)](https://github.com/jonatasemidio/multilanguage-readme-pattern/blob/master/README.es.md)
[![test](https://img.shields.io/badge/en-hi-blue)](https://www.google.com)

This is the Read Me file for the project on the California Housing Prices. This README file is supposed to be read along with the .ipnb project file to consolidate the understanding as to how the end to end Data Science projects are executed.

In order to start a Data Science Project from the scratch we need to work on the following points.
### 1. Frame the Problem and Look at the Big Picture:
<details>
<summary>For this we need to consider the following questions...</summary>
First of all , we need to understand the business objective.Just building a model is not the end goal; What is the precise objective of the model, and how exactly is it going to be used?

Following questions need to be gathered:
1. Define the objective in the business terms.
2. How will your solution be used?
  
For this project it is gathered that this model's output will be fed to another Machine Learning system, along with many others signals. The downstream system will determine whether its worth investing in the given area or not. Getting this signal right is critical as it directly affects the revenue.

3.   What are the current solutions/workarounds (if any)?

*The current situation often gives a reference for performance, as well as insights on how to solve the problem. The information gathered here is that is currently estimated manually by the experts: a team gathers up-to-date information about a district, and when they cannot get the median housing price, they estimate it using complex rules. This is costly and time consuming and their estimates are not great; in cases where they manage to find out the actual median housing price, they often realize that their estimates were off by more than 20%.*

4.   How the problem should be framed (supervised/ unsupervised, online/offline, etc.)?

*This is clearly a typical supervised learning task, since you are given labeled training example (each instance comes with the expected output, i.e., the district's median housing price).
It is also a typical regression task, since it is about predicting a value.
More specifically this is a multiple regression problem, since the system will use multiple features to make a prediction.*
*It is also a* **univariate** *regression problem, since we are only trying to predict a single value for each district; if it would have been multiple values per district then it would have been a* **multivariate** *regression problem.*

*And finally, since there is no continuous flow of datacoming into the system, there is no particular need to adjust to changing data rapidly, and the data is small enough to fit in memory, so plain* **batch learning** *should be fine.*

5.   How should performance be measured?
  
_A typical performance measure for the regression problems is the Root Mean Square Error (RMSE). It gives an idea of how much error the system typically makes in its predictions, with a_ _**higher weight for large errors.**_
  
_Even though RMSE is generally the preferred performance measure for regression tasks, in some contexts one may prefer to use another function. For example, suppose that there are many outlier districts. In that case, one may consider using the mean absolute error (MAE, also called the average/mean absolute deviation).
There are various other metrics like RMSE, MAE etc. , they all are ways to measure the distance between actual and the predicted vector._ 

6.   Is the performance measure aligned with the business objective?
7.   What would be the minimum performance needed to reach the business objective?
8.   What are comparable problems? Can one reuse experience or tools?
9.   Is the human expertise available?
10.   How would you solve the problem manually?
11.   List the assumptions been made so far.
12.   Verify assumptions if possible.

</details>

---
[![how-to](https://img.shields.io/badge/how--to-use-blue.svg)](https://github.com/jonatasemidio/multilanguage-readme-pattern/blob/master/STEPS.md)
