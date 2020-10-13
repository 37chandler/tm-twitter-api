# Working with the Twitter API

Tweepy can be used to gather all sorts of information from Twitter. In the notebook, `Pulling Descriptions with Tweepy`, I have laid out
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
