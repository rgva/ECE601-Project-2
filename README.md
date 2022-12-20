# ECE601: Project 2 - Analyzing Trending UFC Fighters
## Phase 1(a): Twitter API Tool Tests
### '0-authentication'
This script is the authentication script used in every following python notebook implementing a few of the different tools of interest for Project 2. 
### '1-list_tweets'
In this script, I am playing around with the functionality of listing tweets from a users timeline. Implenting pandas dataframes, I was able to create a list of tweets, replies, and reference IDs exported as a .csv file 'tweetslist'. This particular test involved my own account, and the .csv file was successfully generated. 

<table>
  <tr>
    <td> Tweet Features </td>
    <td> Tweet Text </td>
  </tr>
  <tr>
    <td><img src="https://user-images.githubusercontent.com/113293032/208766706-303151f1-0619-4104-9123-6df77d5040ab.PNG" width=560 height=480></td>
    <td><img src="https://user-images.githubusercontent.com/113293032/208766742-6629cfdf-57ce-4e3e-b1c7-b284793db22a.PNG" width=400 height=480></td>
  </tr>
</table>
  

### '2-interacttweets'
In this script, I am using the twitter API to interact with a singular tweet. This can then be used to pull analytics from the tweet - such as number of likes, retweets, etc. but I am currently limited by the access level of the API in doing so.
### '3-automatefollows'
Similarly to the second script, this script is not able to be performed at the current access level. However, it automates following users which the @UFC account follows, given the parameter of greater than 300 friends, and greater than 300 followers to limit the amount of bot accounts followed.

### 'UFC-araujo-grasso_tweets'
This script performs a search of recent tweets relating to the upcoming UFC Fight Night: Araujo v Grasso, storing them in panda dataframes. The implementation for sentiment analysis is fairly simple in this script - mainly pulling the last 1000 tweets relating to both 'Viviane Araujo' and 'Alexa Grasso', and analyzing the overall sentiment of these tweets. Further implementations will give a more detailed review of positive (such as proportions of positive/neutral/negative, etc. You may see that in these tests, both queries for both fighters turn out mostly negative sentiments in the last 1000 tweets for each (unsurprising given the nature of Twitter). 

<table>
  <tr>
    <td> Araujo Tweets </td>
  </tr>
  <tr>
    <td><img src="https://user-images.githubusercontent.com/113293032/208766832-7772c9ea-707b-4e13-9c68-d62ed6c79d49.PNG" width=720 height=840></td>
  </tr>
</table>

<table>
  <tr>
    <td> Grasso Tweets </td>
  </tr>
  <tr>
    <td><img src="https://user-images.githubusercontent.com/113293032/208766840-6d9deb63-1e0b-4a4c-bc7e-bb6f85523bbb.PNG" width=720 height=840></td>
  </tr>
</table>

<table>
  <tr>
    <td> Sentiment Analysis on Fighters </td>
  </tr>
  <tr>
    <td><img src="https://user-images.githubusercontent.com/113293032/208766860-bad71fb3-61d6-4aa7-8043-24857fe96fdd.PNG" width=720 height=840></td>
  </tr>
</table>

### 'singlebot-UFC'
This is a very basic test of the funcionality of the Botometer library. In theory, the function should take the the input string '@UFC' and verify if it is a bot or not using criteria defined by the Botometer. However, when run, the output raises 'Not authorized' - after much troubleshooting, and changing the subscription on RapidAPI to 'Botometer Pro' this is still not rectified, and I will have to verify with my instructor to see why. 

## Phase 1(b): Google NLP

## 'google_nlp'
The Google Cloud uses an interactive version of Python in the cloud shell with the NLP libraries pre-installed. Given the difficulty of exporting these results as a legible .ipynb (since authentication is not a simple process outside of the cloud development environment), I have attached the file 'google_nlp' including the results I obtained on the Cloud Terminal. Please note this is not able to run on any outside IDE. For sentiment analysis, the Google NLP is very adept at recognizing positive and negative sentiments. The phrase: "Alexa Grasso is a terrible fighter!" scored -70.0% (indicating substantial negative sentiment), and likewise, the phrase: "Viviane Araujo is a great fighter!" scored 90.0% (indicating overwhelmingly positive sentiment). 

![GoogleNLP](https://user-images.githubusercontent.com/113293032/208766886-b5284ed4-6041-4f3b-bb26-c7df65bc7206.PNG)


## Phase 2(a): User Stories
### User Stories
Cory Sandhagen (Bantamweight Div., UFC): "Wow, I'm really torn between these two fighters - I'm not sure who I should support publicly in order to safeguard my reputation!"

![CorySandhagen](https://user-images.githubusercontent.com/113293032/194916540-80b71802-a320-4f6c-a7b5-4536898d194c.jpg)

Jimmy Random (Someville, Ohio): "I just got my paycheck, and I wanna double it - but I don't know which fighter to bet on, bruh!"

![jimmyrandom](https://user-images.githubusercontent.com/113293032/194916939-c9e45de8-6c3f-47e0-b947-4d40d2729750.jpg)

Joe Rogan (Podcast Host): "I wish there was a way I could pad my UFC Fight Night talks with statistics that'll make me sound smart, man!" 

![JoeRogan](https://user-images.githubusercontent.com/113293032/194917103-11ed734f-2122-4731-8196-3d1e8b79c1ec.jpg)

In general, the users for this application will be fans, fighters, and commentators, all of whom have different interests in accessing this data.

### MVP: 
The product should do these things at a minimum:
- Pull thousands of tweets relating to a certain fighter.
- Format the tweets in a legible form. 
- Perform sentiment analysis, identify what the overhwelming sentiment is toward that fighter, and provide a limited set of examples from the tweets.

## References
YouTube: CodingEntrepreneurs - '30 Days of Python - Day 21 - Twitter API with Tweepy - Python TUTORIAL'

Samuel Diaz, Data Scientist - 'Twitter Sentiment Analysis & Botometer — Part 2' via medium.com

Google Developer Codelabs - Using Natural Language API with Python
