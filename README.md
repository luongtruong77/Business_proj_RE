# Project Propsal
## Improve the streaming service's recommender engine
---

Proposed by Steven L. Truong

---

### Who is this project for?
- [Fandor](https://relaunch.fandor.com/) is a streaming service dedicated to hardcore film lovers and currently is celebrating 10 years of streaming independent, art house, classic, and international films at the place where it all began. They'd just announced plans to expand to original programming after was acquired by [Cinedigm](https://en.wikipedia.org/wiki/Cinedigm) in 2021.
- For hardcore Fandor's fans, they still are able to subscribe to Fandor channel through [Amazon Prime](https://www.amazon.com/gp/video/storefront/ref=sxts_1_0_edd32cad-acfd-4298-8c2a-68bae5fb7510?benefitId=fandor&ie=UTF8&pd_rd_r=a7ad5a14-cab9-47a7-8e46-3e2557c40ac1&pd_rd_w=1Gn0B&pd_rd_wg=DWsSU&pf_rd_p=edd32cad-acfd-4298-8c2a-68bae5fb7510&pf_rd_r=2H92VKSENCN2F80T7VJQ&qid=1614878606) with the price of $10/mo or $90/year; but in order to be an independent original programming and compete with huge sharks such as Netflix, Hulu, or Disney+ , the team needs to improve the customers' experiences through their recommender engine to avoid customer attrition.

#### How does this project help?
- It's very common that customers cancel their subscription after their free trail; however, once they commit to the service, how do we keep them from churning? The answer is as sample as to improve their experience by enhancing the **recommender system** to keep them using the service.
- One of the most common customers' reactions is to feel the need to find a new movie, new show, or something similar to what they've watched. If we don't recommend them what they like, the next two or three times they see something pops up that is not in their liking, they will cancel the service and we lose customers.

#### Data description:
- This [dataset](https://grouplens.org/datasets/movielens/) contains multiple small datatsets, and was put togetehr by the [GroupLens](https://movielens.org/) research group at the University of Minnesota (thanks to them) and contains of `100,000` ratings, `3,600` tags applied to `9,000` movies by `600` users. 
- The features of our data include `userId, movieId, titles, genres, tags`, which are critical to analyze, visualize, and build models.
- We will build models mainly using the techniques of `user-based collaborative filtering` and `item-based collaborative filtering` to improve the recommender system. Furthermore, if there are movies that are note rated by users (since we will use ratings as our primary attribute), we will use `K-Nearest Neighbor (KNN)` to group similar movies (in terms of genres or popularity) together and predict its ratings.

#### Tools:
- I will use Google Sheets and Tableau to clean, explore, aggregate, and visualize data.
- I will build the baseline model using Python, pandas, numpy.
 
#### MVP:
- The recommending engine thats provides the next 5 movies that one might like in descending order. For example: if one has watched and liked *Pulp Fiction (1994) and Goodfellas (1990)*, the next five movies one might like could be:
    1. Kill Bill: Vol. 1 (2003)
    2. Inglourious Basterds (2009)
    3. Django Unchained (2012)
    4. The Hateful Eight (2015)
    5. The Shawshank Redemption (1994)

*Note:* I am the one who's watched and liked *Pulp Fiction (1994) and Goodfellas (1990)* and the results are very good. I have watched (multiple times) and love these 5 movies.
