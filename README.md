# Books Recommendation System

## Content-Based Recommendation System Notebook
- In this notebook, we will explore and implement a content-based recommendation system. Content-based recommendation systems suggest items to users based on the characteristics of the items and a profile of the user's preferences.
- This approach is particularly useful when we have a lot of information about the items and the users' preferences. We will build a simple content-based recommendation system using Python and the scikit-learn library.

### Read Data 

``` python
books = pd.read_csv(r"C:\Users\ARYA GUPTA\Desktop\Projects Data\Books Recommendation\Books.csv")
ratings = pd.read_csv(r"C:\Users\ARYA GUPTA\Desktop\Projects Data\Books Recommendation\Ratings.csv")
users = pd.read_csv(r"C:\Users\ARYA GUPTA\Desktop\Projects Data\Books Recommendation\Users.csv")

```

