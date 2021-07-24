# What's the Happiest Generation?
Analysis of global suicide rates over the past 6 generations. 

<img src="images/Meseeks.gif" alt="drawing" width="400"/>



## Background and Motivtion
The last 100 years are split into 6 different generations:

Age-Generation Breakdown:

+ Generation Z: 1997-2012
+ Millenials (Generation Y): 1981-1996
+ Generation X: 1965-1980
+ Baby Boomers: 1946-1964
+ Silent Generation: 1928-1945
+ G.I. Generation: 1901-1927

The latest generation is called the Alpha generation and starts from year 2012. 

I would think that the population with the least amount of suicides would be considered the happiest, and I'd like to explore a little further to decide which generation might fall into that category as well. 

## Data

The data set spanned up until 2016 but the suicide rate was relativeley low for that year. I am not sure if this year was an outlier, of if the 2016 memes were true about it being the happiest year.

<img src="images/summer2016meme2.jpg" alt="drawing" width="400"/>

It could've also simply be because the data set is not complete (but that's less exciting). 

I also used a data set conaining the global populations for the same decade to compare the suicide rate to.


The data consisted of global suicide rates broken down into country and then by generation. After being split up by country and generation the data was also separate by sex. But for the purposes of this project, I will be using the total count male and female individuals 

The columns of the data that I kept included the following: 

<img src="images/suicide_rates_df.PNG" />

## Explotatory Data Analysis

To start, I thought to just count the total suicide counts for each generation in the entire 35 year time span:

### Total Suicide Counts per Generation (1985-2016)
<img src="images/t0tal_file_gen_counts.PNG" />

Of course it says that Generation Z has the lowest count. At the time that this data set was recorded, the eldest Generation Z individuals were 18-19 years old, while the youngest were 3 or 4. So I thought it would be best to use the more recent years of data (2006-2015), and then to start by looking at the suicide counts by country first, and then by generation to find out some more information. *Changes name of this presentation to "What's the Happiest Generation from 2006-2015*

After some analysis, I found that a there was a lot of zeroes for the suicide count when it came to the G.I. generation. This could be due to the decline of the population given the range of years that that they were born in and thus, the occurence of their natural deaths.

I decided to only look at the last 10 years of data. This is the global progression of suicide rates between the years of 2006 and the end of 2015:

<img src="images/Suicide_count_last_decade.png" />

I wanted to see whether any significant rise or drop in the rates had occurred in the final 10 years of the data collection and it seems that there was a drop from over 12,000 down to a little over 8,000 suicides per 100,000 people in a given population.


I then took the average suicide counts per 100,000 people for each country. I then arranged that list in ascending oder but average suicide as follows:

<img src="images/10_happiest_countries.png" />

Here are the counts for suicide deaths per generation in the top 10 happiest countries

<img src="images/suicide_by _generation.png" />:

First, given that the G.I. Generation was an outlier, I am going to consider the other five generations. Out of the five, the Boomers seem to be the happiest due to their suicide rates being lower than the othe four.


## Statistical Analysis

With the information that I had, I decided to conduct a hypothesis test. In the entire 10 year span for the countries provided in the data set, there were 2,300,872 suicide deaths. This averaged to about 230,087 deaths per year. 636,436 of the total count were Boomers alone (making our mu about .28). For simplification purposes I divided all my values by 1000.

I want to find the probaility that a suicide death in this time span was commited by a Boomer, where my null hypothesis is that a randomly selected suicide death in the deacade will not be a Boomer more than 28% of the time. 
         Boomer Suicide≈𝐵𝑖𝑛𝑜𝑚𝑖𝑎𝑙(636,0.28)

My alpha is 0.05. (success = the individual is a Boomer, failure = individual is not a Boomer)


<img src="images/hyp_dist.png" />:

p_value = 1 - normal_approx.cdf(636) --> p-value for 10 year suicide experiment: 0.64

<img src="images/p_val.png" />:


## Conclusion

I failed to reject my null hypothesis that a randomly selected suicide death in the deacade will not be a Boomer more than 28% of the time. 

## Future Steps

I would like to dig further to find a more complete data set because this one only contained 101 out of the 195 countries in the world. 

There was also a lot of years' worth of data that was missing and I compensated by using the mean of the years that we had. Though, I would like to have found a more accurate way to do so.

There was a column of data that provided the annual GDP for each country and I would also like to create a scatterplot to show whether there is any correlation between GDP and suicide rate.

A comparison between global suicide rates and global death rates would be interesting to see the impact.

I'd like to explore Bayesian AB testing for my statistical analysis next time, rather than that using frequentist techniques.

#### Thank you!!!

## Contact Information

Amy Williams
arw.62596@gmail.com