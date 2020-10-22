# Working with the Twitter API

## Jordan's Introduction
Tweepy can be used to gather all sorts of information from Twitter. In the notebook, `Pulling Data with Tweepy`, I have laid out
ways to gather follower information as well as Tweets containing a certain key 
phrase or Twitter handle. One thing to keep in mind while going through the notebook is that Twitter 
only allows so many pulls per fifteen minute periods, so if you are choosing to grab followers from accounts 
with hundreds of thousands to millions of followers, it will take hours, and possibly upto days to complete. I showed how to 
grab certain objects from followers/tweets, but if there's something in particular you think would be 
interesting (Geo location, favorite/retweet numbers, following counts, etc.) there is almost certainly a way 
to do it, so feel free to go hunt for it in the Twitter Dev documentation.

If you don't waste hours a day on Twitter like me, here's some things to keep in mind about Twitter 
(the platform, not the API). Each Tweet can contiain at most 280 characters, so a few NLP-type 
statistics about text/word length won't lend themselves well to analysis. Each Tweet can also be favorited or 
retweeted, where retweeting someone elses Tweet will share it to your own followers timeline. 
Lastly, hashtags are a decent way to follow a topic/conversation. You'll see in the exercise that 
I grabbed Tweets from the hashtag #WorldMentalHealthDay, but almsot any large organization/event/topic 
has their own hashtag that they try to encourage others to engage with. Some others include #Debates2020, #NBAFinals, etc. 

## Twitter Assignment

In this assisgnment we're going to pull a handful of fields for all the followers of several Twitter
accounts. 

In the code provided by Jordan, he picks two WNBA teams and pulls (some of) the followers screen_names and
descriptions. This assignment will extend that work. 

Pick at least two Twitter accounts that you'll be comparing. Those accounts should be on different sides 
of some sort of divide. The divide could be ideological, sports-related, public health-related, age, etc.

Ideally the accounts will have somewhere between 
100K and 500K followers. We're picking that range so that the results won't take _too_ long with
Twitter's rate limiting. 
If you'd like to pick a few accounts to represent one "side" that have that many followers in 
aggregate, that's fine. 

Once you've chosen your accounts, write code that pulls all the followers of the accounts (or set of accounts). 

* screen_name
* name
* id
* location
* followers_count
* friends_count
* description

These fields are all located in the `user` object accessed in the code. 

Write these fields out to two tab-delimited text files. I recommend following
the example code and including the name of the initial account in the file name. 

Note that the output of this assignment should be **two** tab-delimited text files,
one for each starting account or set of accounts. 


## 10/22 Update from Jordan
Brenden Connors made some really useful code that grabs all user objects from our list of Twitter IDs. Instead of grabbing 300 records per fifteen minutes, you should now be able to grab about of 900,000. 
