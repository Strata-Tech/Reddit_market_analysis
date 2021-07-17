# Reddit_market_analysis
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
