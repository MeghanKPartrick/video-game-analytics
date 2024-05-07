<h1>Video Game Analytics: Exploratory Data Analysis and Modeling </h1>

<h2>Description</h2>

This aim of this project was to locate a sufficient data set online and perform exploratory data analysis and modeling. Our group selected multiple csv files from [Simon Garanin on Kaggle](https://www.kaggle.com/datasets/gsimonx37/backloggd?select=developers.csv). Specifically, the **developers.csv**, **games.csv**, and **genres.csv**, ultimately joining these into one dataset, which we named **backloggd.csv**. These data sets contained video game information, including **video game name**, **genre**, **date released**, **average rating**, **number of reviews**, **number of plays**, **number of backlogs**, **wishlists** (number of times the game has been added to favorites), **description**, and **number of players currently playing**.
<br />
<br />
We then decided to create two exploratory data questions per person (10 total) and develop code to answer those questions. These questions ranged anywhere from in depth calculations and filtering  to figures and modeling. We developed a table or figure in order to come up with a complete answer for each question. Example questions include: Which game developer teams have the highest ratings? or How have video games' genres popularity evolved over time, and what factors are most associated with those changes? Using these ten questions, we developed four investigative follow-up questions, and produced code to provide answers for two of those follow-up questions. 
<br />
<br />
The first follow-up question we investigated: **Is there evidence to show that the top rated developers are just highly rated because they produce well-liked genres?**
<br />
<br />
We began by viewing the top 15 rated developers, removing any developers with ten or less ratings, in order to have a large enough sample size for a fair comparison. A bar plot was created with these top 15 developers to determine the most created genre. Ultimately, we could see that Adventure was easily the most created genre and from there we could analyze genre specfic ratings. A boxplot was created in order to view ratings for each genre, including their median and interquartile ranges. Considering almost every genre's median was included in the other genre's interquartile range, including Adventure, we could not conclude that any genre had particularly higher ratings than the others.
<br />
<br />
The second follow-up question we investigated: **Is there a possibility that these high ratings are due to the fact that number of reviews for these titles were low?**
<br />
<br />
We began by analyzing the relationship between ratings and number of reviews, observing that as a linear model without control variables. This did show high correlation, however, we are aware that this may not be the case when analyzing further in depth when including control variables. We used a smooth plot to graph the relationship.
<br />
<br />
Our **final paper** includes two entirely new modeling questions that we developed based off of our exploratory data analysis. We wanted to see if we could predict the success of the video game without knowing the publisher and if we could come up with metrics related to publisher to help us predict the rating of the game more accurately. Using cross validation, **Best Models** were determined based off of mean squared error calculations. We used MSE because of the ability to measure how far off the predictions are from actual values and because of the emphasis that MSE has on large errors compared to measures like mean absolute error. To begin the prediction without publisher information, we used 10-fold cross validation with Elastic Net regression to traverse through alpha values from 0 to 1 in increments of 0.1. A table of the top four models based upon the MSE is provided as well as a plot of the best alpha glmnet model. New publisher metrics were created to develop more in depth models including the standard deviation of ratings per publisher, average ratings per publisher, average number of active players per publisher, ratings of most recently released game per publisher, and the interaction of the standard deviation and game's age per publisher. This heavily decreased the MSE of the model, proving better predictions with publisher information included.
<br />
<br />
We effectively utilized our data science skills to work with a new dataset obtained online. After cleaning and understanding the data, we analyzed it to reveal interesting insights about game making patterns.
<br />
<br />
The full paper and exploratory data analysis can be found as HTML or RMD files above.
<br />
