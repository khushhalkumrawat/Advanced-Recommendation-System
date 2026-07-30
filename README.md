# Advanced-Recommendation-System-based-on-Content-and-Collaborative-Filtering

[![HitCount](http://hits.dwyl.com/PaulSudarshan/Advanced-Recommendation-System-based-on-Content-and-Collaborative-Filtering.svg)](http://hits.dwyl.com/PaulSudarshan/Advanced-Recommendation-System-based-on-Content-and-Collaborative-Filtering)

The repo deals with an more advanced version of Recommendation Systems which is based on two different popularly known filtering mechanisms which are the Content Based Filtering and Collaborative Based Filtering. In Content based Filtering the main focus is on the item characteristics and features which are used to predict other items of similar nature. 
The main idea behind Collaborative based filtering is that we are given a matrix of preferences by users for items, and these are used to predict missing preferences and recommend items with high predictions. All we need in a dataset are the collection of user_ids and item_ids with user's preference for different items which maybe in the form of ratings or other parameters.

![](images/recommender_system.png)

# Dataset Details
Dataset Details
There are 3 files.

users.csv - Users dataset containing user's details like name, id, gender etc.

posts.csv - Post dataset containing posts details like title category etc.

views.csv - Views dataset contains the mapping which user views which post(s)
## Users
 _id: a unique alphanumeric id of the user (string)
 name: Name of user (string)
 gender: Gender of user (male | female)
 academics: Education of the use (undergraduate | graduate)
## Posts
 _id: a unique alphanumeric id of the post (string)
 title: Title of the post (string)
 category: Category of the post (string)
 post_type: Type of the post (blog | artwork | skill | project)
## Views
 user_id : a unique alphanumeric id of the user (string)
 post_id : a unique alphanumeric id of the post (string)
 time stamp: timestamp of when user viewed the post (ISO time format)

# Tools and Libraries Used
1. Jupyter Notebook
2. Pandas Library (for Data Manipulation)
3. sklearn

# Methodology (For Content-Based)
1. Loading the data 
2. Creating a TF-IDF Vectorizer for the different post categories in 'category' column.
3. Generating Vector Space Model for the vectorised values and finding cosine similarity between them to obtain a user-item matrix.
4. The Final stage is to form a function that would take in various post title as input and recommend a list of most suitable post titles based on the content.

# Methodology (For Collaborative-Based)
1. In this type we take into account the user preferences for posts as well and therefore generate three matrices namely
  (a). USER-ITEM MATRIX.
  (b). ITEM-ITEM MATRIX.
  (c). USER-USER MATRIX
2. Various categorical features are label encoded and their values are added to the corresponding vectorised post category values to form a new feature named 'vectorised features'.
3. A recommender function is created which takes in post titles as input and returns the titles of similar posts based on user interests in both the items.
4. A similar function is created which takes in user_id as input and finds other correlated users(similar) finds thier mutual interests in posts and returns the post titles.

# Conclusion
Hence, a fully-functional recommender system in Python with content-based filtering as well as collaborative based filtering is implemented. A sample output for the given two recommender systems in shown below:
## CONTENT-BASED RECOMMENDER ENGINE
![](images/content_based.jpg)
## COLLABORATIVE BASED RECOMMENDER ENGINE (ITEM-ITEM)
![](images/collaborative_item.jpg)
## COLLABORATIVE BASED RECOMMENDER ENGINE (USER-ITEM)
![](images/collaborative_user.jpg)

# Further Scope of Project
The basic model of this project can be further extended to generate sophisticated recommendation results to users which will be more accurate and extensively based on the applications of both the type of filtering, it is named as Hybrid Filtering based Recommendation Systems. I look forward to implement the the Hybrid Recommendation System soon.
