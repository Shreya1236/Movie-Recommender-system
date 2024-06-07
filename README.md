# Movie-Recommender-system

What is a Recommendation System?

A Recommendation System is a filtration program whose prime goal is to predict a user’s “rating” or “preference” toward a domain-specific item or item. In our case, this domain-specific item is a movie. Therefore, the main focus of our recommendation system is to filter and predict only those movies that a user would prefer, given some data about the user.

Why Recommendation Systems?

Recommendation Systems are essential for several reasons:

1. Recommendation Systems offer personalized suggestions based on user preferences and user ratings, ensuring that they discover content and products that are relevant and interesting to them.

2. By providing tailored recommendations, users are more likely to engage with the platform, increasing user satisfaction and retention.

3. E-commerce platforms like Amazon use recommendation engines to promote products, leading to higher sales and revenue as users discover and purchase items they might not have considered.

4. In today’s digital landscape, recommendation systems help users navigate the overwhelming amount of available content, making it easier to find a particular movie or series they seek or in any language they want, like English or Korean.

5. Recommendation algorithms expose users to new and diverse content, expanding their horizons and introducing them to items they might have overlooked.

6. Relying on past behavior and preferences, recommendation systems help users make informed decisions about complex and subjective choices such as movies, music, or books.


Types of Recommendation Systems

There are 2 types of recommendation systems- Content-based filtering and Collaborative Filtering. 

Lets discuss them now.
Movie Recommendation System

Content-based Filtering
Content-based filtering is a recommendation strategy that suggests items similar to those a user has previously liked. It calculates similarity (often using cosine similarity) between the user’s preferences and item attributes, such as lead actors, directors, and genres. For example, if a user enjoys ‘The Prestige,’ the system recommends movies with Christian Bale, the ‘Thriller’ genre, or films by Christopher Nolan.

However, content-based filtering has drawbacks. It limits exposure to different products, preventing users from exploring a variety of items. This can hinder business expansion as users might not try out new types of products.

Collaborative Filtering
Collaborative filtering is a recommendation strategy that considers the user’s behavior and compares it with other users in the database. It uses the history of all users to influence the recommendation algorithm. Unlike a content-based recommender system, a collaborative filtering recommender relies on multiple users’ interactions with items to generate suggestions. It doesn’t solely depend on one user’s data for modeling. There are various approaches to implementing collaborative filtering, but the fundamental concept is the collective influence of multiple users on the recommendation outcome.

There are 2 types of collaborative filtering algorithms:

User-based Collaborative filtering
User-based collaborative filtering aims to recommend items to a user (A) based on the preferences of similar users in the database. It involves creating a matrix of items rated/liked/clicked by each user, computing similarity scores between users, and then suggesting items that user A hasn’t encountered yet but similar users have liked.

For example, if user A likes particular movies like Batman Begins, Justice League, and The Avengers and user B like Thor, they share similar interests in the superhero genre. Therefore, it is highly likely that user A would enjoy a popular movie like Thor and user B would like The Avengers, one with the highest movie ratings.

Disadvantages

User-based collaborative filtering has several disadvantages:

1. Fickle User Preferences: User preferences can change over time, making initial similarity patterns between users outdated. This can result in inaccurate recommendations as users’ tastes evolve and they start watching new movies.
2. Large Matrices: As the number of users is typically much larger than the number of items, maintaining large matrices becomes challenging and resource-intensive. Regular recomputation is required to keep the data up-to-date.
3. Vulnerability to Shilling Attacks: Shilling attacks involve creating fake user profiles with biased preference patterns to manipulate the recommendation system. User-based collaborative filtering is susceptible to such attacks, potentially leading to biased and manipulated recommendations.

   
Item-based Collaborative Filtering
Item-based Collaborative Filtering focuses on finding similar movies instead of similar users to recommend to user ‘A’ based on their past preferences. It identifies pairs of movies rated/liked by the same users, measures their similarity across all users who rated both, and then suggests similar films based on the similarity scores.

For example, when comparing movies ‘A’ and ‘B,’ we analyze the ratings from users who rated both movies. If these ratings show high similarity, it indicates that ‘A’ and ‘B’ are similar movies. Thus, if someone liked ‘A’, they should be recommended ‘B’, and vice versa.

Advantages over User-based Collaborative

Filtering includes stable movie preferences, as popular movies do not change people’s tastes. Maintaining and computing matrices is more accessible as there are usually fewer items than users. Shilling attacks are also more challenging since items cannot be faked, making this approach more robust.

Movie Recommendation System Code
In this implementation, when the user searches for a movie, we recommend the top 10 similar movies using our movie recommendation system. We will be using an item-based collaborative filtering algorithm for our purpose. The training set used in this demonstration is the movie lens-small dataset.
