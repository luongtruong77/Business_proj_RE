# Optimizing Fandor's Recommender Engine
---

Steve L Truong


## Abstract
---

In this project, I will build and optimize the recommender's engine for [Fandor](https://relaunch.fandor.com/) - a streaming service dedicated to hardcore film lovers. The raw [dataset](https://grouplens.org/datasets/movielens/) is obtained from [GroupLens](https://grouplens.org/), explored and cleaned using **Google Sheets** and **Tableau***; and finally, **Python** comes into play to help to build recommender's engine using the most efficient algorithms available.

## Design
---
##### Why do we need to optimize the recommender's engine?

- According to this [Deloitte article](https://www2.deloitte.com/us/en/insights/industry/technology/video-streaming-services-churn-rate.html): among customers who cut a streaming service, **62%** had signed up to watch a specific show then cancelled once they were done;  where **43%** of them cancelled the same day they decided they no longer wanted the service.
- Among several reasons why they churned, about **21%** of them responded that the service *lacks of new content they are interested in watching* as of October 2020 ([Deloitte article](https://www2.deloitte.com/us/en/insights/industry/technology/video-streaming-services-churn-rate.html)).
- According to survey conducted by Deloitte themselves, **27%** of responders say that they would be in the service if it has the release of an exclusive new movie or series they want to watch.

##### The impact of this project

- To avoid consumers churning from our platform, the simplest way to do is optimizing recommender's engine to provide the most relevant contents to them, as well as maintain their interests on our movies and shows.
- By stacking and combining several modern and sophisicated algorithms (one of them was part of $1,000,000 Netflix Prize winning algorithms) to build the engine, this project's mission is to reduce the number of churning customers by **10%** when launched, and **15%** in the span of three months.


## Data
---

- This [dataset](https://grouplens.org/datasets/movielens/) contains multiple small datatsets, and was put togetehr by the [GroupLens](https://movielens.org/) research group at the University of Minnesota (thanks to them) and contains of `100,000` ratings, `3,600` tags applied to `9,000` movies by `600` users. 
- The features of our data include `userId, movieId, titles, genres, tags`, which are critical to analyze, visualize, and build models.


## Algorithms
---

##### Feature Engineering
Extract *year* from the *name* and split *genres* into small *sub_genre* categories for further analysis.

##### Building the engines
I use several algorithms to build the models such as: content-based, user-based (KNN-inspired), item-based (KNN-inspired), SVD, and SVD++ (SVD++ is a part of the combination of algorithms that win $1,000,000 Netflix Prize on 2009).

##### Evaluation
- My go-to evaluating metric is **hit_rate** and **cumulative_hit_rate** since they will determine the best if customers click on the contents. Since the engine has not launched on production and we do not have customers to evaluate, I will use different metrics for the purpose of demonstration.
- I will use Root Mean Squared Error **RMSE** and Mean Absolute Error **MAE** to compare **6** different algorithms.
- Since the metrics are to measure errors, the lower the score, the better the algorithms:

![](https://github.com/luongtruong77/Business_proj_RE/blob/main/figures/metrics_barchart.png?raw=true)
- As the chart shows, SVD++ performs the best of them and Random performs the worst (as the name infers, random algorithm recommends contents to users *randomly*)

## Tools
---

- Google Sheets and Tableau to clean, explore, aggregate, and visualize data.
- Python packages (pandas, numpy, surprise, etc) to build and evaluate models.
- SQL and Flask to deploy models to production.


## Communication
---

- The presentation in pdf file is included to logically and visually convey the purpose, progress, and impacts of this project.
- Here are the [Google Sheets Link](https://docs.google.com/spreadsheets/d/1N85J2wBuYa-jgn66R3Ab2LTL4pjiXfWVykor-DyLO0E/edit?usp=sharing) and [Tableau Dashboard](https://public.tableau.com/profile/luong.q.truong#!/vizhome/movies_16195550176570/Dashboard1) associated with this project.






