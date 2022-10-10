# ECE601: Project 2 - Analyzing UFC Fight Trends
## Phase 1(a): Twitter API Tool Tests
### '0-authentication'
This script is the authentication script used in every following python notebook implementing a few of the different tools of interest for Project 2. 
### '1-list_tweets'
In this script, I am playing around with the functionality of listing tweets from a users timeline. Implenting pandas dataframes, I was able to create a list of tweets, replies, and reference IDs exported as a .csv file 'tweetslist'.
### '2-interacttweets'
In this script, I am using the twitter API to interact with a singular tweet. This can then be used to pull analytics from the tweet - such as number of likes, retweets, etc. but I am currently limited by the access level of the API in doing so.
### '3-automatefollows'
Similarly to the second script, this automates following users which the @UFC account follows, given the parameter of greater than 300 friends, and greater than 300 followers to limit the amount of bot accounts followed.

### 'UFC-araujo-grasso_tweets'
This script performs a search of recent tweets relating to the upcoming UFC Fight Night: Araujo v Grasso, storing them in pandas. This gives us the base for sentiment analysis.

## Phase 1(b): Botometer Sentiment Analysis

## References
YouTube: CodingEntrepreneurs - '30 Days of Python - Day 21 - Twitter API with Tweepy - Python TUTORIAL'
