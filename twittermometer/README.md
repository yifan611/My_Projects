# twittermometer
  Twitter scraping and word visualisation.

## Twittermometer© ##
Python version 3.9

Project for the Python Programming module of the Data Analyst program (DA24STO) at Hyper Island Stockholm.

### Authors: ###
**Anna Högman** - https://github.com/annahogman  
**Guilherme Bracco** - https://github.com/guibracco  
**Yifan Yang** - https://github.com/yifan611

### Description: ###
 **Twittermometer©** aims to gauge the general sentiment expressed on Twitter, during the last four FIFA World Cups events (South Africa in 2010, Brazil in 2014, Russia in 2018 and Qatar in 2022), by visualising the most used English words in tweets marked with the hashtag #worldcup. Only the last four championships can be searched because Twitter was not yet comercially available before that.

Unfortunately, tweepy, the popular Twitter module, cannot be used, as of today even enterprise API access only provides data from the previous 30 days. Therefore, we are using the snscrape module, which doesn't have a limit of number of days or tweets.

To set the scope and get a more distributed sample of tweets, the script scrapes a fixed number of tweets per day for each championship period. With 500 tweets per day, it's hard to predict runtime, as the same script run for 7 hours, 8 hours and 66 minutes in the last three executions. That must be due to server response — busy servers, throttled search, cached queries? As expected, changing the number of tweets per
day shifts the frequency of the words.

For visualisation, the wordcloud module is chosen. It cannot be installed for Python 3.10 and above, so Python 3.9 is selected. Aside from common stop words already provided by the module, like conjunctions and prepositions, some words are excluded from the visualisation because they are too obvious and of no consequence for the purpose of the script.
