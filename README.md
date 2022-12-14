# Phase_1 Project

## Description
  To help the head of the newly formed Microsoft Studios get insight into the kind of movies that are currently doing well at the box office. 
  
## Data Source
  I made use of the `im.db` dataset and the `bm.gross.movie.csv` file for our analysis
  
## Getting Started - How success is defined
  I defined success of a movie based on the revenue generated by a movie.
  Of course, there are other metrics that can define success,  but from a business perspective, since the aim of any business is to be profitable,
  I only considered the total gross amount.
  
### Question 1
First question that I would like to answer is: What kind of movies are the most successful? 
This can be also be extrapolated into other questions like: What are audience's tastes like? Are there any genres that are more successful than others? How many different genres are there? etc. 

#### Answer Methodology
The `movie_basics` table, from the `im.db` dataset lists the movie titles and their respective genres. I combined it with the `bm.gross.movie.csv` data to get data of the top 10 genres that generated the most revenue. Now, I can pinpoint to a particular genre and say: 'This is the genre that generated the most money.'

### Question 2
Second question that needs answering is: Which is the largest market for movies?
Part of any business feasibility plan is gauging market demand. This is done to get an idea about where the demand for the product is the highest to give itself the highest chance of success. I did the same to check for the region that grossed the most money.

#### Answer Methodology
The `bom.movie_gross.csv` lists the gross amounts of each movie region-wise. I calculated the `total_gross` as the sum of `domestic_gross` and `foreign_gross` to see how much revenue each movie has generated. Then, by using the `.groupby()` method,I grouped the data based on the `region` to display the `total_gross` amounts of each `region.` 

### Question 3
Now that I've ranked genres and markets by total_gross, to get an idea, the next question is: What are the kinds of movies that are most successful in the largest market?

#### Answer Methodology
By creating a slice of the `bom.movie_gross.csv` df to filter out the largest market and using `.groupby()` to calculate `total_gross` amounts per genres,
I can look at the gross amounts of the top 10 or top 5 genres in the largest market.

# Conclusion
By figuring out the largest market and the genres of movies that are most successful in the same, I can recommend to Microsoft Studio the kinds of movies that they should look to be producing and their target audience.
