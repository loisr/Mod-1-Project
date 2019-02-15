# Mod-1-Project

This project is for the completion of Mod 1 of Flatiron Data Science program. Our group was Lois, Grace and Nan.

We compared New York Times Hardcover Best Sellers from May 2008 to July 2018 to Goodreads data. We wanted to see if New York Times Best Sellers were popular on Goodreads.

First, we accessed The New York Times dataset from kaggle as a json file, but it still needed quite a bit of cleaning. Each book is a dictionary with many of its values requiring parsing to rid of unwanted terms such as
'$numberLong' and '$numberInt'. After the data was cleaned, we put the data in a dataframe.  After realizing that the 'title' needed to be adjusted to match the corresponding output in Goodreads, we made the necessary changes such as replacing spaces between words with + signs.  Finally, we concluded there were 2300 unique titles that appeared on the Best Sellers list during that time.

Concurrently, we accessed data on these 2300 books from Goodreads using a combination of Goodreads' API and webscraping with BeautifulSoup.  With the data format in xml, BeautifulSoup was applied to read the data.  We built functions that returned and cleaned values of interest, such as the title, author, ratings count and average rating. We also wanted to gather more author information, such as gender and works count.  So we applied similar method with BeautifulSoup again to author urls to attain those information.  Using pandas, these two datasets were then put into dataframes and merged.

With our respective dataframes from the New York Times and from Goodreads ready to go, we created a final merge.  Since some books did not match by title or author, we eliminated them from consideration, resulting in the final dataframe consisting of 1355 books for analysis. 

We found some interesting insights:

1. The average rating on Goodreads for a NYT bestseller is 3.9 (out of 5).  
2. The strongest positive correlation are between the ratings count on Goodreads and longest duration on the NYT best seller list.
3. Besides somewhat more male authors than female authors (580 to 487) who appeared on the list, there were miminal distinction in other areas, such as average rating and number of weeks on the list.
4. Most books spent 2 weeks on the list, but there were two that spent 100 weeks ("The Help" and "All The Light We Cannot See").
5. Some of the most popular words that appeared on the titles of these books were "Love", "Death", and "Place"

In conlusion, books are awesome and reading ia amazing!!!!!
