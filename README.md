# Jake Ritmire's Portfolio

Data Science Portfolio

# [Project 1: Housing Sale Price Estimator: Ames, Iowa](https://github.com/jgritmire/Project_1_Housing_Regression)
* Used Numpy and Pandas to clean a dataset of 2,930 observations of 82 variables which detail the physical characteristics of homes sold in Ames, Iowa between 2006 and 2010
* Created data visualizations using Matplotlib to better understand the data set
* Used Scikitlearn to create a multivariate linear regression which was able to predict house pricing with an R2 value of 0.91
#### Concluding Remarks
For my final model, I elected to utilize interaction terms between the 5 variables with the highest correlation with sale price. This added 15 variables, increasing my number of input variables to 43. This model, with 95% confidence, has a R2 value of between 0.89 and 0.93. Most importantly, once I included the interaction terms the model no longer consistently undervalued the most expensive houses in the dataset. When applied to the testing data, this model models predictions were on average $23,300 off of the actual sale price.

![](/images/Housing_1.png)

![](/images/Housing_2.png)

![](/images/Housing_3.png)

# [Project 2: Web Scraping to Predict Social Media Virality](https://github.com/jgritmire/Reddit_Web_Scraper/blob/main/README.md)
* Utilized Selenium and BeatifulSoup to scrape key information on thousands of posts each day from Reddit
* Categorized posts as being image only, text only, or video
* Built a logistic regression that would predict whether a post would be successful based on a number of factors including day posted, time of day, and post content
* Performed data analysis to determine the optimal day, time, and type of post to get the greatest amount of post interaction
#### Concluding Remarks
My final model is a logistic regression model that does not include the TFIDF terms that I created. This model has a score of 0.59 with a 95% confidence interval of between 0.56 and 0.63. This model predicts on post content, title length, and when the post was posted. I standard scaled the data so that I would be able to look at the relative contributions of the variables to a post's chances of succes.

The model indicates that in order to give your post the highest chance of success, you should post a text only post on thursday between 10 and 11 am. Given the number of successful posts and the rate of post success in the various subreddits that I collected data from, I would recommend posting in either r/teenagers, or r/antiwork. A post with the worst chance at succeeding would be an image posted on a friday between 11:00pm and midnight, to a subreddit that does not generally reward images such as r/askreddit.

![](/images/Reddit_1.png)

![](/images/Reddit_3.png)

# [Project 3: Building a Movie Recommendation Algorithm](https://github.com/jgritmire/Movie_Recommender)
* Compiled relevant information from IMDB to build a dataset of 1.6 million films
* Restricted the dataset to 8,000 films based on popularity, as determined by the number of reviews the film had received
* Scraped Wikipedia for plot synopses for each of the 8,000 films, and used NLP to identify similarities between films
* Built a Python script that takes 3 films that a user likes, and returns a list of 10 recommended films based on cosine similarity scores
#### Concluding Remarks
I set out to build a movie recommender that could take user input (a list of several movies) and return recommendations based on these movies. I wanted to try and capture as many aspects of a film as possible through the construction of my dataset, but ultimately I overestimated the availability of this data, as well as the ease with which I could compile the existing data on the internet. When building my product based recommender, I found that the movies that my recommender would sometimes return odd films. I attributed this to my dataset being somewhat limited, as there are many intangible aspects of films that are difficult to measure with numbers, and due to the limitations of the hardware I was working with, I was unable to do extensive natural langauge processing on the complete synopses of the films to try and tease out more measurable similarities between films.

Next I built my review based recommender. The review based recommender returned much less suprising films as recommendations, but felt a little uninspired in its basic state. What I ultimately settled on was a hybrid recommender that took some recommendations from the review based recommender, and some recommendations from the product based recommender which would spit out a list of 5-7 more well known movies, and a few oddball movies that might be appealing to a more adventurous viewer.

![](/images/Movies_2.png)

![](/images/Movies_3.png)
