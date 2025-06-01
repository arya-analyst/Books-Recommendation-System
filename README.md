# Books Recommendation System

In this recommendation system we wil build a couple of recommenadtion systems:
  - Popularity Based Recommendation System: We can create a custom formula to calculate a popularity based recommendation system. However, we are 

## Content-Based Recommendation System Notebook
- In this notebook, we will explore and implement a content-based recommendation system. Content-based recommendation systems suggest items to users based on the characteristics of the items and a profile of the user's preferences.
- This approach is particularly useful when we have a lot of information about the items and the users' preferences. We will build a simple content-based recommendation system using Python and the scikit-learn library.

### Read Data 

``` python
books = pd.read_csv(r"C:\Users\ARYA GUPTA\Desktop\Projects Data\Books Recommendation\Books.csv")
ratings = pd.read_csv(r"C:\Users\ARYA GUPTA\Desktop\Projects Data\Books Recommendation\Ratings.csv")
users = pd.read_csv(r"C:\Users\ARYA GUPTA\Desktop\Projects Data\Books Recommendation\Users.csv")

```

## Collaborative Filtering Based Recommendation System

We cannot use each and every user's input to build our recommendation system as we might run into the risk of overfitting our prediction model.

  -  Applying the *GroupBy* function to group the data and filter effectively

``` python

book_ratings.groupby('User-ID').count()

```

  - We are taking only those users into accout here who have reviewed atleast 100 books

``` python
a = book_ratings.groupby('User-ID').count()['Book-Rating'] > 100
filtered_users = a[a].index

filtered_users_list = book_ratings[book_ratings['User-ID'].isin(filtered_users)]
```

  -  We are taking only those books into accout here which have been reviewed atleast 30 times.

``` python
b = filtered_users_list.groupby('Book-Title').count()['Book-Rating'] > 30
filtered_books = b[b].index

filtered_books_list = filtered_users_list[filtered_users_list['Book-Title'].isin(filtered_books)]
```

  














