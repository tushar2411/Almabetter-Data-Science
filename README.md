<h1 align="center"> Play Store App Review Analysis</h1>
<h3 align="center"> AlmaBetter Verfied Project - <a href="https://www.almabetter.com/"> AlmaBetter </a> </h5>
<p align="center"> 


## Abstract ✒️
A huge number of designers working freely on designing the apps and making them successful. With the enormous challenge from everywhere throughout the globe, it is important for a developer to know whether he/she is continuing the correct way or not. Since most Play Store applications are free, the income model is very obscure and inaccessible regarding how the in-application buys, in-application adverts and memberships add to the achievement of an application. In this way, an application's prosperity is normally dictated by the quantity of installation of the application and the client appraisals that it has gotten over its lifetime instead of the income is created.
The objective of this experiment is to deliver insights to understand customer demands better and thus help developers to popularize the product. We have tried to discover the relationships among various attributes such as which application is free or paid, what are the user reviews, rating of the application.
  
  
  ##  🏹 Project Files Description

<p>This Project includes 1 colab notebook, 1 technical documentation as well as 1 presentation:</p>


### Output:
- [Google Colab](https://github.com/tushar2411/Almabetter-Data-Science/blob/a41f5fcb45be113457042534c6665b870f1c829b/myPlay_Store_App_Review_Analysis_Capstone_Project.ipynb) - All the outputs are visible in the provided colab notebook.

### Input Files:
  <li><b>Play Store Data.csv</b> - It contains the basic details of the app like number of user reviews, ratings, etc.</li>
  <li><b>User Reviews.csv</b> - It contains the user reviews and its sentiment score for the respective app.</li>

### Data Source:
- [Dataset](https://learn.almabetter.com/courses/take/team-capstone-projects/texts/19443175-play-store-app-review-analysis-dataset) - Dataset taken from Almabetter


##  📖 Introduction:
Today's Day to day scenario we can see that mobile apps playing an important role in any individual’s life. With enormous challenge from everywhere throughout the globe, it is
important for a designer to realize that he/she is continuing in the right way or not. To hold this income and their place in the market the application designers may need to figure out how to stick into their present position.
The dataset with 10k Play Store applications is available to analyze the market of android. It can be examined to analysis the different category such as family, communication,entertainment, tools, music, camera etc. In this project we examine the different attributes present in the data set that affect the popularity of the application. We focused on to answer the questions like, what makes an app popular, what should be the price and size of the app, is there some trends in user sentiments. 
In our data set we have two csv files for data analysis:
Play Store data
User Reviews
At first, we analysis the play store data and in the play store data we have 10841 rows and 13 columns & in the user review data we have 64295 rows and 5 columns of data. We have to take the maximum outcomes from the data which help us to analysis the which type of app is most preferable and comparisons between different insights. Our goal is to filter and make plots accordingly for a better EDA with respect to the final data. We need to explore and analyze the data to discover key factors responsible for app engagement and success. 


## 📋Problem Statements-:
1. What are the top categories on Play Store?
2. Are majority of the apps Paid or Free?
3. How importance is the rating of the application?
4. Which categories from the audience should the app be based on?
5. Which category has the most no. of installations?
6. How are ratings affected when the app is a paid one?
7. How are reviews and ratings co-related?
8. Lets us discuss the sentiment subjectivity.
9. Is subjectivity and polarity proportional to each other?
10. What is the percentage of review sentiments?


## 📔 **What is Exploratory Data Analysis?**
Exploratory data analysis (EDA) is used by data scientists to analyze and investigate data sets for patterns, and anomalies (outliers), and form hypotheses based on our understanding of the dataset and summarize their main characteristics, often employing data visualization methods. It is an important step in any Data Analysis or Data Science project. It helps determine how best to manipulate data sources to get the answers you need.

EDA involves generating summary statistics for numerical data in the dataset and creating various graphical representations to understand the data better and make it more attractive and appealing.

The following are the various steps involved in the EDA process:
1. <b>Problem Statement</b> - We shall brainstorm and understand the given data set. We shall study the attributes present in it and try to do a philosophical analysis about their meaning and importance for this problem.
2. <b>Hypothesis</b> - Upon studying the attributes present in the data base, we shall develop some basic hypothesis on which we can work and play with the data to look for the varied results which we can get out of it.
3. <b>Univariate Analysis</b> - It is the simplest form of analyzing the data. In this we would initially pick up a single attribute and study it in and out. It doesn't deal with any sort of co-relation and it's major purpose is to describe. It takes data, summarizes that data and finds patterns in the data.
4. <b>Bivariate Analysis</b> - This analysis is related to cause and the relationship between the two attributes. We will try to understand the dependency of attributes on each other.
5. <b>Multivariate Analysis</b> - This is done when more than two variables have to be analyzed simultaneously.
5. <b>Data Cleaning</b> - We shall clean the dataset and handle the missing data, outliers and categorical variables.
6. <b>Testing Hypothesis</b> - We shall check if our data meets the assumptions required by most of the multivariate techniques.



## 📖	Steps Involved
After loading the dataset, we can start the exploration but before that, we need to check and see that the dataset is ready for performing several exploration operations or not, so let’s first have a look at the structure and the manner in which the data is organized.

### Data Cleaning
Our data set contains a large number of null values in the rating column, so we drop them. Some of the columns have a smaller number of null values, so we replace the null values in these columns with the mode value of that particular column. Our data set also contain the duplicate rows for a single application. We also drop the duplicate rows because the rows contain the identical data. Also drop the rows, which have rating greater than 5.

### Data Transforming 
From the information of data frame, we can see that all the columns except rating have the object data type but some of the columns like, reviews, size, installs and price have the numerical value. So, we have to transform them in proper data type and also remove the unwanted values from the numerical columns like ‘+’ and ‘,’ from installs and ‘$’ from price. In the size column we have some values in KB and some values in MB, so we transform all the values in MB.

### Exploratory Data Analysis
After establishing a good sense of each feature, we proceeded with plotting a pairwise plot between all the quantitative variables to look for any evident patterns or relationships between the features. There is a high variance in the number of installs and in number of reviews. To overcome this problem, we add two new columns to the data frame named: log_installs and log_review, which contain the logarithmic values of installs and review columns, respectively.

### Single Variate Analysis
After that we analysis all the columns one by one to examine whether the particular column contain some useful information or not:

### Category
We breakdown the apps by category and observe that family and game categories have the maximum number of apps in the play store. Weather, house and home, comics, events, beauty, and parenting are the categories which have a few numbers of apps.

### Data wrangling
Apart from this, two new columns were added to the main data frame, namely, “Rating Group”, and “Revenue”. This is done to improve simplify the analysis and come up with different meaningful visualizations

* <b>Rating Group:</b> This column groups the apps based on the average user rating. (4-5: Top rated, 3-4: Above average, 2-3: Average, 1-2: Below average).
*	<b>Revenue:</b> This column gives the revenue generated by the app through app installs alone.
By doing these operations on the original dataset, we are ready with the data pipeline, and data visualizations can be done on it.
All the apps in play store have the rating between 0.5 to 5. Maximum apps have the rating between 3.8 to 4.5.



## 📋 Conclusion:
After Analyzing the dataset I have got answers to some of the serious & interesting question which any of the android users would love to know.
In this project of analyzing play store applications, we have worked on several parameters which would help Google PlayStore to do well in launching their apps on the play store.
*	Percentage of free apps = ~92%
*	Percentage of apps with no age restrictions = ~82%
*	Most competitive category: Family
*	Category with the highest number of installs: Game
*	Category with the highest average app installs: Communication
*	Percentage of apps that are top rated = ~80%
*	There are 20 free apps that have been installed over a billion times
*	Category in which the paid apps have the highest average installation fee: Finance
*	Most popular app in the Play Store based on the number of reviews: Facebook
*	The apps whose size varies with device has the highest number average app installs.
*	Helix Jump has the highest number of positive reviews and Angry Birds Classic has the highest number of negative reviews.

## 💶 Credits

[![LinkedIn](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](www.linkedin.com/in/tushar-khairnar-b73659191)

[![GitHub](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)]([https://github.com/](ttps://github.com/tushar2411))

## 📚 References
*	GeeksforGeeks
*	Analytics Vidhya
*	Stackoverflow
*	Towards data science
*	Python libraries documentation
*	Data camp
* Medium
