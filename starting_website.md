---
layout: default
---

# Introduction:

Everyone loves movies! They provide entertainment and escape from the stresses of daily life, and it's no surprise that the movie industry plays a significant role in the global entertainment market. In fact, the global box office was worth $42.2 billion in 2019, showing the huge demand for movies and the potential for financial success.

But what makes a movie financially successful? Is it the duration of the movie, the presence of certain actors and their notoriety, the genre it belongs to, or the budget dedicated to the movie? In this data story, we aim to use a data-driven approach to uncover the factors that contribute to a movie's financial profitability. To do this, we will analyze a subset of movies that were released in the US between 1980 and 2010, using the CMU Movies dataset and enriching it with data from Wikidata, TMDb, and IMDb. By measuring the success of a movie using the Profit feature, defined as the difference between the revenue and the budget, we will reveal the key factors that can drive the financial success of a movie.

# The dataset:

The CMU movies dataset appears to contain information about movies, including metadata such as the movie's Wikipedia and Freebase IDs, name, release date, box office revenue, runtime, languages, countries, and genres. We augmented it with additional data from external sources. This included movie ratings from IMDB and budget and revenue data from wikidata and TMDb. These data sources were scraped in order to obtain budget and revenue information for movies from the United States. Which will be then used to understand the financial success of the movies in the dataset.

Before analyzing the data, Some preprocessing steps to ensure that the data was clean and ready for analysis. This included checking for missing values and dropping movies or actors with missing data.

Once everything is set up, in order to homogenise all our financial data values according to inflation over the year. Inflation is an important factor to consider when analyzing financial data, especially when comparing data from different time periods. This is because inflation can affect the value of money over time, making it difficult to accurately compare financial data from different periods without taking it into account.

![Inflation](inflation_hausse.jpg) 

For example, if we consider a movie A that was released in the 1980s and made $50 million at the box office, and another movie B was released in the 2010s and made the exact same amount of money.

Without taking inflation into account, it might seem like both movies were equally financially successful. However, due to the effects of inflation, the $50 million that Movie A made at the box office may not be equivalent to the $50 million that Movie B made in terms of purchasing power. This is because the value of money can change over time due to inflation, meaning that the same amount of money may be worth more or less in different time periods.

By accounting for inflation, it is possible to get a more accurate picture of the financial performance of both movies. For example, if inflation was 2% per year between the 1980s and the 2010s, the $50 million that Movie A made at the box office in the 1980s would be worth around $129 million in the 2010s. In this case, it would be clear that Movie B was more financially successful than Movie A, even though both movies made the same amount of money at the box office.

This inflation adjustment was performed using the cpi library, such that all our financial data was adjusted according to the year 2010. Once all datapoints in our dataset are comparable, let's dive in and look at our data.



