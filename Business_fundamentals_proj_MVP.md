# Optimizing Fandor's Recommender Engine - MVP

---

Steven L. Truong

---

- From the [dataset](https://grouplens.org/datasets/movielens/) that is provided by [MovieLens](https://movielens.org/), I utilized `Google Sheets` and `Tableau` to clean, aggregate, and visualize the data for insights. Here are the [Google Sheets Link](https://docs.google.com/spreadsheets/d/1N85J2wBuYa-jgn66R3Ab2LTL4pjiXfWVykor-DyLO0E/edit?usp=sharing) and [Tableau Dashboard](https://public.tableau.com/profile/luong.q.truong#!/vizhome/movies_16195550176570/Dashboard1).
- Then I went on and used `Python` to extract more attributes from the raw dataset, such as **genres** and **year**.
- In order to optimize the recommender engine, I use several algorithms to build the models such as: content-based, user-based, item-based, SVD, and SVD++ (SVD++ is a part of the combination of algorithms that win $1,000,000 Netflix Prize on 2009).
- Preliminary results: SVD++ seems to work the best amongs other algorithms and it produces reliable outcomes.
- Here is the result based on a user who likes `Pulp Fiction, Fight Club and the Hateful Eight`:
- ![](https://github.com/luongtruong77/Business_proj_RE/blob/main/figures/SVD++_result.png?raw=true)