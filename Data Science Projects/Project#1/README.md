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

_It is always a good practice to check the assumptions upfront, this can help catch the serious issues early on. For an example, the district prices that your system outputs are going to be fed into a downstream Machine Learning System, and you assume that these prices are going to be used as such.
But what if the downstream system converts the prices into categories (e.g. "cheap", "medium", or "expensive") and then uses those categories instead of the prices themselves? In this case getting the prices right is not important at all; your system just needs to get the category right. If that's so, then the problem should have been framed as a classification task , and not a regression task. And one would like ot find this out after working on a regression system for months._

</details>

### 2. Get the Data:
<details>
<summary>For this we need to consider the following questions...</summary>
Note: automate as much as possible so one can easily get the fresh data.

1. List the data you need and how much you need.
2. Find and document where you can get that data.
3. Check how much space it will take.
4. Check legal obligations, and get authorizations if necessary.
5. Get access authorizations.
6. Create a workspace (with enough storage space).
7. Get the data.
8. Convert the data to a format you can easily manipulate (without changing the data itself).
  This is also a very important step, so that the transformations on data are easily reproducible and we do not loose the original data.
9. Ensure sensitive information is deleted or protected (e.g. anonymized).
10. Check the size and type of data (time series, sample, geographical, etc.).
11. Sample a test set, put it aside, and never look at it (no data snooping!).
  This step would ensure that you are imitating the test set as the real unseen data that model will be seeing for the first time; so any surprises etc if there are to be considering let's say the data distributions etc would be challenged here and would provide a good opportunity to reassess the imputations,transformations pipelines accordingly.  

</details>
  
---
[![how-to](https://img.shields.io/badge/how--to-use-blue.svg)](https://github.com/jonatasemidio/multilanguage-readme-pattern/blob/master/STEPS.md)
