# Docker-Twitter-Pipeline

Dockerized Data Pipeline that analyzes the sentiment of tweets and a Slack Bot that publishes selected tweets.

First a python script accesses the Twitter stream via their API. The stream filters tweets in relation to a specific topic collects and saves them into MongoDB. Then, with an ETL job maintained on Docker transforms and loads the metadata to Postgres database. Tweetbot pipeline also analyzes the sentiment of the tweets via VaderSentiment and rates the tweets from -1 to 1. One being very positive and negative one being very negative. . Finally, it posts the tweets to a Slack channel.
