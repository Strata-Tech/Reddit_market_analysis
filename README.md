# Reddit_market_analysis📈🚀💰💎👐
Analysis of reddit community 's most mentioned stocks and sentiment on the stocks(i.e bullish or bearish)


This app uses the PRAW reddit API to find the most mentioned US stock tickers. In this project, Vader sentiment analyzer is used to calculate the score of the various stock tickers. (i.e bullish score, bearish score, neutral score, total score).

# Parameters used for the Reddit PRAW API

subs = []           sub-reddit to search
post_flairs = {}    posts flairs to search || None flair is automatically considered
goodAuth = {}       authors whom comments are allowed more than once
uniqueCmt = True    allow one comment per author per symbol
ignoreAuthP = {}    authors to ignore for posts
ignoreAuthC = {}    authors to ignore for comment 
upvoteRatio = float upvote ratio for post to be considered, 0.70 = 70%
ups = int           define # of upvotes, post is considered if upvotes exceed this #
limit = int         define the limit, comments 'replace more' limit
upvotes = int       define # of upvotes, comment is considered if upvotes exceed this #
picks = int         define # of picks here, prints as "Top ## picks are:"
picks_ayz = int     define # of picks for sentiment analysis


# Data
This includes US stocks with their market capitalization more than USD 100 million. (exclude penny stocks)
Assumptions: We are taking into consideration only reddit comments which are upvoted to a certain score. Nevertheless the parameters can be amended to suit various needs.


#Sample of how output looks like:

Took 250 seconds to analyze 6000 comments in 75 posts in 5 subreddits post.

Top 5 most mentioned picks:
GME
AMC
SPCE
TSLA
PLTR


 Sentiment analysis of top 5 picks: 
                    GME      AMC     SPCE    TSLA          PLTR
Bearish          4.7150   6.1920   1.8120  0.5800  6.331781e-10
Neutral         58.4240  54.3040  19.1180  5.5010  2.546367e-09
Bullish         12.8600  11.5030   3.0700  1.9190  3.605879e-10
Total/Compound  17.5071  12.6682   0.9318  1.8647 -3.123409e-10


