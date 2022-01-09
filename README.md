#stock-analysis
#Module 2 of MSU Data Analytics Bootcamp - VBA

## Overview and Purpose
The purpose of this analysis is to quickly summarize annual returns and volume for a list of stocks. Beginning with a dataset indexed by day and ticker with the variables volume and price, I created a VBA script to allow our friend Steve analyze a group of green energy stocks to assist in his investment decision making. The previous iteration of this code has opportunity to improve speed. This project focuses on refactoring that code to run much faster. This was successfully accomplished by creating a for loop through all rows of data that employs an array to store output values. The previous iteration looped through all rows for all tickers to find the same data.

## Results

### Code Performance
Both 2017 and 2018 ran in ~0.3 seconds. See images for run times and VBA script of the data-finding for loop. Refactoring the code increased speed to under 0.1 seconds. Over a 3x increase in speed. Details below.

#### For Loop before refactor
https://github.com/ShaneDoane/stock-analysis/blob/main/Resources/New_for_loop.png

#### For Loop after refactor
https://github.com/ShaneDoane/stock-analysis/blob/main/Resources/New_for_loop.png

Notable changes: 	The new iteration of the for loop using an output array to store values produced results for 2018 and 2017 in under 0.1 seconds (over 3x faster) for the same list of stocks. See code and runtime images below. Note the subsection 1b) where output arrays are created and 2b) where the new for loop utilizes a "tickerIndex" to run for each stock vs. looping through all tickers in the old version.

#### Run times for 2017 and 2018 before refactor
https://github.com/ShaneDoane/stock-analysis/blob/main/Resources/2017_old_runtime.png
https://github.com/ShaneDoane/stock-analysis/blob/main/Resources/2018_old_runtime.png

#### Run times after refactor
https://github.com/ShaneDoane/stock-analysis/blob/main/Resources/2017_new_runtime.png
https://github.com/ShaneDoane/stock-analysis/blob/main/Resources/2018_new_runtime.png

### Stock Performance
https://github.com/ShaneDoane/stock-analysis/blob/main/Resources/2017_stocks.png
https://github.com/ShaneDoane/stock-analysis/blob/main/Resources/2018_stocks.png

On average, most green energy stocks analyzed had significant positive returns in 2017 and negative in 2018. Ticker ENPH by far had the most impressive 2 year CAGR for 2017 and 2018, with increased volume in 2018. This could suggest that given the negative returns of all but one other stock in 2018, ENPH has relative strength vs its peer group. This may suggest market leadership in green energy. Given pure stock performance, ENPH would have been the best investment from this list of stocks on a risk-adjusted basis for 2017 and 2018. Past performance is not indicative of future performance. More research should be done on the underlying fundamentals of the businesses. 

### Summary
#### Advantages & Disadvantages of Refactoring and application to this project
The primary advantage of refactoring code is the ability to save time writing code. Beginning with a functional project and looking to only improve and iterate enables the code writer to focus on single components as opposed to the whole. Refactoring can also illuminate blindspots that otherwise may have existed. After all, 0.3 seconds (original run time) is not necessarily slow, but for a growing list of stocks it could become cumbersome, and refactoring reduced that risk. 

The main disadvanntage of refactoring is that it can be difficult to know where weak points are. Because of this a lot of time could be wasted trying to find where time is being wasted. In other words, perfect could become the enemy of good. In this project, as mentioned above, 0.3 seconds is an impressive run time! Had I not found a faster method, I could have wasted time on a fruitless endeavor. While that was not the case here, this could become a time sink on other projects.
