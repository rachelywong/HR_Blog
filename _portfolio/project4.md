---
title: You may like... Recommender Systems
subtitle: A look into collaborative filtering
image: https://raw.githubusercontent.com/BlackrockDigital/startbootstrap-agency/master/src/assets/img/portfolio/04-full.jpg
alt: 

caption:
  title: You may like... Recommender Systems
  subtitle: A look into collaborative filtering
  thumbnail: https://raw.githubusercontent.com/BlackrockDigital/startbootstrap-agency/master/src/assets/img/portfolio/project4/transparent.png
---
## You may also like... Recommender Systems

Back in the 1950s, there were three major TV networks, each with as many shows as you could count on one hand. Kellogs had three main cereal brands. Bored? You can choose from one of three video games - one of which was Tic-Tac-Toe. Fast forward to 2021 and the world has become a dizzying place of endless choices. Netflix has over 5,000 shows, the cereal shelf has no problem going on for two whole aisles and there were over 10,000 games released on Steam in 2020 alone. Consumer indecision is paralyzing the world and the only available treatment is: the recommender system - an all knowing helpful sidekick who lets us know what to watch, what to buy and who to date. 

The recommender system is a fill in the blank problem at its heart. There’s some known ratings of people and products but there’s a bunch more unknown that we need to figure out. We’ll discuss one of the most popular methods below. 

#### **The Collaborative Filtering Approach**

Fittingly called the collaborative approach, this method is all about using shared information from other users to predict what unknown ratings for other users will be. Here’s an example. We know that Ana and Elsa are similar in many ways and rated the following purchased items as follows:

![orig.png](./assets/img/portfolio/project4/orig.PNG){:class="img-responsive"}

The chart above is called a utility matrix. Here, we’re trying to solve for the red question mark. Filling in the blank is essentially answering: What would Elsa rate the toque? There’s a few ways to create some baseline solutions. 

We can consider a per user average, where we simply take the average of the ratings Elsa has rated previously. In this case, she would rate the toque a 2.5 and likely not be too interested.

![peruseravg.png](./assets/img/portfolio/project4/peruseravg.PNG){:class="img-responsive"}

Another method is to consider the per item average. Here, we look across users to average out how the toque has been rated by others. Since our dataset only has one other user, we would predict that Elsa also rates this item as a 5. 

![peritem.png](./assets/img/portfolio/project4/peritem.PNG){:class="img-responsive"}

The last approach we look at here is the K-Nearest Neighbours average. There’s more info about this model in the "Next Top Model" blog post. In this case, we only look at the closest one neighbour (n=1). This method averages the closest rating amongst users and products (assuming the products and users are ordered by similarity) and gives a rating of 4.7. 

![knnavg.png](./assets/img/portfolio/project4/knnavg.PNG){:class="img-responsive"}

#### **The Reality**

The baseline approaches above are a good start, but of course, this is not exactly how a recommender system works in practice. In reality, most recommender systems rely on Principal Component Analysis (PCA). This is the process of transforming high dimensional data into lower dimensional data for processing. For a utility matrix with millions of users and products, it’s not computationally efficient to be considering every entry in the matrix. Instead, we use PCA to extract only the most meaningful information (hence reducing dimensions) for filling in the blank values of our matrix. 

#### **Benefits & Limitations**

The Collaborative model is effective in several ways:

✅ Leverages the strength of a social network in predictions. We can rely on the similarity of users and products for our prediction.

✅ No need to understand the item content. We could be predicting movies for Netflix or products on Amazon. As long as there are users and ratings, we treat the process similarly. 

But here are a few limitations:

❗️ Cold start problem. We need some access to other users and their ratings before we can predict for unknown problems. 

❗️ Hard to interpret. Since we are leveraging shared information, we can’t explicitly trace back what led to a specific rating. 

The basic concept behind a collaborative filtering approach is to fill in the missing entries of a utility matrix. However, in reality, there’s other elements to consider such as diversity in recommendations, freshness of the recommendations, how long recommendations should last, etc… At the end of the day, building an effective recommender system involves doing a little math but more importantly, understanding users and their behaviour. 


_________


{:.list-inline}
- Date: April 2021
- Category: Machine Learning

