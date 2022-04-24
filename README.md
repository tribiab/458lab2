# Lab 2: Geo-tagged tweet collection and visualization

## Abstract
The data collection process for this lab is the first time I've experienced real-time **web scraping**. 
Utilizing live twitter data to determine geolocation through the use of an API is extremely convienient for exploratory research. Thus, I wanted to see if I could observe a basic trend through twitter data. I'm interested in observing a geographical difference between coasts regarding partying culture. Considering today is a Saturday, I predict that we can see a difference in tweets regarding partying from the East coast and West coast. I compiled a list of keywords that I thought heavily associated with partying, such as drinking alcohol: 
- "drink/drinks"
- "alcohol"
- "club"
- "turnt"
- "lit"
- "drunk"

Furthermore, by utilizing the StreamListener object to collect twitter data at different time intervals, I may be able to observe a geographic trend in tweets. Therefore, I framed my research to collect data at 2:00 pm PST, and 9:30 PM PST. The scope of my research is within the USA, and I want to asess if there is an influx in tweets on either coasts depending on the time I collected the data. Thus, I hypothesize that people are more likely to tweet about drinking alcohol later in the day, I expect to see an increase in tweets in the latter data (9:45 data). 

## Methods
Utilizing the Stream Listener object, I made the following manipulations to the code to filter tweets based on my keywords:  
`words = ['drinks', "drink", "shot", "beer", "alcohol", "club", "vodka", "turnup", "turnt", "lit", "drunk"]`
`stream.filter(languages = ["en"], track = words)`

I casted these keywords as an umbrella, hoping to capture as many tweets that would fall under the category of partying with an emphasis on drinking. I assume that people are typically interested in partying later in the day, and thus would make tweets about drinking or going to the club later in the day. Therefore, by scraping twitter data in the afternoon and then later in the evening, I hope to capture this human phenomenon. 

# Maps & Word Clouds
## Map 1: Tweets about alcohol ~ (2:00PM PST / 5:00PM EST)
![Map at 2PM](/images/lab2map2.png)
Here we can observe a concentration of tweets on the East coast in comparison to the West coast-- this was expected. People are more likely to think about partying and alcohol at 5:00PM then 2:00PM. So, in addition to the cluster of tweets on the East coast, we must also observe the absence of tweets on the West coast. **People are less likely to be thinking about drinking or partying at 2:00 PM.** Below is the word cloud which visualizes the most occuring keywords in the tweets that I've collected. 
![Word Cloud 2PM](/images/wordart2pm.png)
The word cloud does a great job of visualizing the most common keywords by manipulating the size of the text. The greater the size and stronger opacity symboilzes frequency. Therefore, keywords such as **"Drink, Beer, Club, Shot** are some of the most common keywords found in the tweets collected at 2:00 PM PST. Please note that the word cloud is in the shape of the time that the data was collected. 

## Map 2: Tweets about alcohol ~ (9:45PM PST / 12:45AM EST)
![Map at 9:45](/images/lab2map946.png)
In map 2, we can visibly see a difference in the distribution of tweets. In comparison to map 1, we can see a significant decrease in tweets regarding partying and drinking on the East coast. The absence of tweets on the East coast can partly be explained by the time-- 12:45 AM. I would argue that most people are already partying/drinking at this time, and would be less likely to make tweets. 
However, we can see a slight increase in tweets on the West coast, especially in the Pacific North West area around Washington. In reference to Map 1, the increase in tweets can be explained by the time as well. On the contrary to Map 1, **9:45 PM is a probable time for people to be more interested in the act of partying or drinking alcohol.** The related word cloud is presented below. 
![Word Cloud 9:45](/images/wordart945pm.png)
In this word cloud, which was created from an aggregation of tweets from 9:45 PM, we can assess the content of those tweets by visualizing it in different sizes. Similar to the first word cloud, the size of the keyword and it's opacity signifies it's frequency in the data. A difference that I can observe between the two word clouds is the presence of the word: "Drunk" in the 9 PM word cloud. My hypothesis is that people are more likely getting drunk at 9PM than 2PM, thus tweets with the keyword "drunk" didn't appear until 9PM. 

# Conclusion 
In this lab, I explored twitter data and tried to represent the literal time difference from the West coast and East coast through observing tweets referencing partying and drinking. 

I had the hypothesis that there would be less tweets about drinking and partying at 2:00 PM PST than 9:00 PM. I utilized a StreamListener object and Twitter API keys to webscrape live twitter data for 10 minute intervals. With this data in CSV format, I visualized the tweets based on their longitude and latitude found from the Twitter metadata.  

### Results
The differences between maps are not obvious, I could only observe a minor increase in tweets on the West, and a decrease in tweets on the East from Map1(2PM) to Map2(9PM). If I were to conduct this research again, I would be more intentional with the time selection, for example I would rather collect data from early in the morning for a more contrasting result when I collect data at 9:00 PM. Furthermore, I will let the StreamListener collect data for longer than 15 minutes. I was surprised that the data I collected was small in size, thus giving me an unrepresentative sample. In the future, I will keep these limitations in mind and make better judgement. 