<p align="center">
<a href="https://dscommunity.in">
	<img src="https://github.com/Data-Science-Community-SRM/template/blob/master/Header.png?raw=true" />
</a>
	<h2 align="center">  Forecasting the upcoming-elections-in-the-us-extracting-tweets
  </h2>
	<h4 align="center">  Introduction</h4>
<h5>
Objective: Extraction of tweets and Perform sentiment analysis on the presidential candidature of Donald Trump, Joe Biden and Kanye West in the upcoming elections in US in November,2020.

In this project we've extracted tweets using Twitter's API, and GetOldTweets library to overcome the timeframe limitations of Twitter API. After extraction, we have done preprocessing for cleaning the datasets, basic EDA, sentiment analysis to observe polarity towards each candidate, used classification models on these sentiments and created visualisations.
Preprocessing Of Tweets

Preprocessing Of our data is very vital for this project as it pertains to cleaning actual tweets by users. This cleaning will prove to be a massive factor for the success rate of our project. This reduces complexity of data under analysis as data in real world is unclean.
The preprocessing that was carried out in this project was mainly done on the tweets. 
Firstly, the data has to be cleaned. For this we used various methods like checking for any null values , checking for duplicates ( & if any to remove them).
After checking this, we move on with the actual preprocessing. There were many methods used. They are listed below – 
1)Using Regular Expressions to remove Emojis from Tweets
2)Using Regular Expressions to remove any retweets (if they exist) 
3)Using Regular Expressions to remove the usernames from the tweets as they do not provide any additional information
4)Using Regular Expressions to remove any URLs, websites,etc
5)Using Regular Expressions to identify for any hashtags in the tweet, & if they exist, remove the hashtag & keep the word. This can be very useful when modelling as it does not remove any possible words that might be a major factor in calculating the sentiment
6)Using Regular Expressions to remove any special characters, numbers , punctuations 
7)Converting everything to lower case
8)Lastly, we used the Tweet-Preprocessor Module for cleaning any leftover junk. 

This was the major portion of preprocessing our tweets. Next, we have to get it ready for calculating our sentiment as well. So we will be performing certain tasks using NLTK Module. These are listed below –
1)NLTK Module was used to tokenize all words
2)NLTK Module was used for removing any existing stop words (eg. Or , from , them, Does , etc)
3)NLTK Module was used to perform stemming
4)Words that were less than a length of 2 were dropped



Sentiment Analysis
Sentiment Analysis refers to processing and analyzing text and categorizing it into different states and emotions. Natural Language Processing is used for performing sentiment analysis, which is a subfield of artificial intelligence and linguistics to process and analyze large amounts of natural data. 
To calculate the Sentiment of each tweet, we used the vader_lexicon file from NLTK which was used from the SentimentIntensityAnalyzer() package from NLTK module
Using this we calculated the polarity of each tweet & created a dataframe. Each tweet was classified as Negative, Neutral, Positive & Compound with a score between zero & one pertaining to how close the tweet is to the column.
The final sentiment was decided on the final score of the compound column. ( If less than zero, it would be classified as negative ;greater than zero, it would be classified as positive ; zero then neutral)
Using these , we proceeded with making the final model.
Some Visual Analysis outcome:


  <h5>
</p>


<br>
<p align="center">
<img src = "https://github.com/Data-Science-Community-SRM/extracting-tweets-forecasting-the-upcoming-elections-in-the-us/blob/master/Graphs/Bidden_daily_sentiment.png">
</p>
<h5>In the above graph, we have the three broad sentiments on X axis and No. of tweets of that particular sentiment in our dataset, along with the dates of them being tweeted. A general observation here is that there is a majority of positive tweets on most of days. So, the general reaction towards Biden is affirmative.</h5>

<br>
<p align="center">
<img src = "https://github.com/Data-Science-Community-SRM/extracting-tweets-forecasting-the-upcoming-elections-in-the-us/blob/master/Graphs/Bidden_geomap.png">
</p>
<h5>This is a geomap. It shows the location of the users when they tweeted the respective tweets. We can observe that there’s a lot of density towards the eastern and south-east part of the United States which includes cities like Miami, Georgia, Virginia, North Carolina, Dallas, Chicago, Pennsylvania.</h5>

<br>
<p align="center">
<img src = "https://github.com/Data-Science-Community-SRM/extracting-tweets-forecasting-the-upcoming-elections-in-the-us/blob/master/Graphs/Geomap_senti_Bidden.jpg">
</p>
<h5>This geomap shows the sentiment of people around the country.</h5>
<br>
<p align="center">
<img src = "https://github.com/Data-Science-Community-SRM/extracting-tweets-forecasting-the-upcoming-elections-in-the-us/blob/master/Graphs/Sourceoftweet_bidden.png">
</p>
<h5>This is a barplot with Source on X axis and Count on the Y axis. Source here refers to the medium used by the person to tweet, which can be Twitter Web App, Iphone, Android, ipad etc. Here we can see a major no. of user’s tweet using Web Application, followed by Iphone and the Ipad. The least used source is Hootsuite.com. </h5>
<br>
<p align="center">
<img src = "https://github.com/Data-Science-Community-SRM/extracting-tweets-forecasting-the-upcoming-elections-in-the-us/blob/master/Graphs/Countperday_bidden.png">
</p>
<h5>The above barplot is depicting the counts of tweets per day for Biden in our time frame i.e. from July 13th to July 21st.  The Y axis denotes the no. of tweets on the corresponding day on X axis. The maximum no. of tweets observed in the given timeframe is on July 21st. </h5>
<br>
<p align="center">
<img src = "https://github.com/Data-Science-Community-SRM/extracting-tweets-forecasting-the-upcoming-elections-in-the-us/blob/master/Graphs/countperhr_bidden.png">
</p>
<h5>The above graph is giving the no. of tweets hourwise on particular day. This shows the time of the day when users are most active, and that is around 17 : 00  hrs.   </h5>
<br>
<p align="center">
<img src = "https://github.com/Data-Science-Community-SRM/extracting-tweets-forecasting-the-upcoming-elections-in-the-us/blob/master/Graphs/Word_map_Bidden.jpeg">
</p>
<h5>Wordmap Of tweets for Bidden</h5>






## Contributors

<table>
<tr align="center">


<td>

Shubhangi Soni

<p align="center">
<img src = "https://github.com/Data-Science-Community-SRM/template/blob/master/logo-light.png?raw=true"  height="120" alt="Your Name Here (Insert Your Image Link In Src">
</p>
<p align="center">
<a href = "https://github.com/ShubhangiSoni1603"><img src = "http://www.iconninja.com/files/241/825/211/round-collaboration-social-github-code-circle-network-icon.svg" width="36" height = "36"/></a>
<a href = "https://www.linkedin.com/in/shubhangi-soni/">
<img src = "http://www.iconninja.com/files/863/607/751/network-linkedin-social-connection-circular-circle-media-icon.svg" width="36" height="36"/>
</a>
</p>
</td>

<td>

Rohan Mathur

<p align="center">
<img src = "https://github.com/Data-Science-Community-SRM/template/blob/master/logo-light.png?raw=true"  height="120" alt="Your Name Here (Insert Your Image Link In Src">
</p>
<p align="center">
<a href = "https://github.com/RohanMathur17"><img src = "http://www.iconninja.com/files/241/825/211/round-collaboration-social-github-code-circle-network-icon.svg" width="36" height = "36"/></a>
<a href = "https://www.linkedin.com/in/rohanmathur17">
<img src = "http://www.iconninja.com/files/863/607/751/network-linkedin-social-connection-circular-circle-media-icon.svg" width="36" height="36"/>
</a>
</p>
</td>

<td>
Tejas Chintala

<p align="center">
<img src = "https://github.com/Data-Science-Community-SRM/template/blob/master/logo-light.png?raw=true"  height="120" alt="Your Name Here (Insert Your Image Link In Src">
</p>
<p align="center">
<a href = "https://github.com/arcado10"><img src = "http://www.iconninja.com/files/241/825/211/round-collaboration-social-github-code-circle-network-icon.svg" width="36" height = "36"/></a>
<a href = "https://www.linkedin.com/in/tejas-chintala-/">
<img src = "http://www.iconninja.com/files/863/607/751/network-linkedin-social-connection-circular-circle-media-icon.svg" width="36" height="36"/>
</a>
</p>
</td>

<td>
Bhavya Chhabra

<p align="center">
<img src = "https://github.com/Data-Science-Community-SRM/template/blob/master/logo-light.png?raw=true"  height="120" alt="Your Name Here (Insert Your Image Link In Src">
</p>
<p align="center">
<a href = "https://github.com/bhavya1600"><img src = "http://www.iconninja.com/files/241/825/211/round-collaboration-social-github-code-circle-network-icon.svg" width="36" height = "36"/></a>
<a href = "https://www.linkedin.com/in/bhavya-chhabra-1600">
<img src = "http://www.iconninja.com/files/863/607/751/network-linkedin-social-connection-circular-circle-media-icon.svg" width="36" height="36"/>
</a>
</p>
</td>

<td>

Sampada Bareja

<p align="center">
<img src = "https://github.com/Data-Science-Community-SRM/template/blob/master/logo-light.png?raw=true"  height="120" alt="Your Name Here (Insert Your Image Link In Src">
</p>
<p align="center">
<a href = "https://github.com/sampadabareja"><img src = "http://www.iconninja.com/files/241/825/211/round-collaboration-social-github-code-circle-network-icon.svg" width="36" height = "36"/></a>
<a href = "https://www.linkedin.com/in/sampada-bareja-43930818b">
<img src = "http://www.iconninja.com/files/863/607/751/network-linkedin-social-connection-circular-circle-media-icon.svg" width="36" height="36"/>
</a>
</p>
</td>



  
## License
[![License](http://img.shields.io/:license-mit-blue.svg?style=flat-square)](http://badges.mit-license.org)

<p align="center">
	Made with :heart: by <a href="https://dscommunity.in">DS Community SRM</a>
</p>

