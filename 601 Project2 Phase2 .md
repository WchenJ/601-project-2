# EC-601-report
#ECE601
programme ECE 601 is used for tracing the news on US open Tennis competition through twitter API

Building for tennis fans.

The project is built on the base of twitter and google NLP to accomplish the following functions:
The program search and post twitters from the official accounts from international competitions, tennis players, tennis players, other related staffs and famous analyzing accounts. The program aims to get the locations, texts and times.
The location and time part will be used on marking the traveling map for every posted player which acted like google map. When the user point on one of the locations, the specific twitter will pop out. We have now successfully get the loc and time but still trying to implement them on map.
The time and name key words in the text of twitters from the open competition accounts will be recognized and used to form the schedule of every big competition. 
The google NLP will be used on the predicting part before every competition, the program will gather twitter with key words of player names and certain competition names based on the schedule and those twitters from related staffs and analyzers will be gathered together and analyzed by google NLP API to see if the twitter is positive to the player on the competition. All results will be shown on a bar to see the percentage of positive and negative ideas from the rarely professional aspect.We have now accomplish the sentiment analyzing of the most recent tweets under the keyword.We are able to clean the tweets, choose those who have more stable attitude to avoid the unprecise part from google NLP and show all consequense in a bar chart form with explanation.

MVP

The APP is used for tennis fans to keep pace on competitions and players. Fans could search and see attitudes from the public easily as well as keep pace on locations of the players, which could act as a key to trace the hotspot of tennis field.

User stories

1.	Tennis fans who would like to keep on pace to certain player or competition in a extremely convenient way. The program allow them to see the schedule and the traveling route of the one they are interested in vividly just by a click.
2.	Analyzers who want to make a model surrounding the game, players about their relationship, ability or possibility to win a certain game.
3.	Staff and manager of a certain player to see the status and most interest topic of fans and communicate better with them.


Sample output

testcase1： Functionality under normal use case
discription： searching tweets based on keywords by inserting keyword without @
input case： keyword：‘US open Thiem’ total——tweets： 50
output:
the total attitude score is -0.03000000089406968 



here is the attitude contradiction bar 
 

     [******||||||||||]     
positive            negative

 

the attitude is NEGATIVE 
 which is calculate from 34 samples in which 29 samples has been count and 13 is neutral
 
 
 
 

testcase2: Functionality under normal use case
discription： searching user by inserting keyword with @ at the front of it
input case： keyword：‘@rogerfederer’ total——tweets： 50
output:
Location: Switzerland



testcase3:Error Handling
discription： error occurs because of the API or tweepy misusing
input case:  keyword：‘@1’ total——tweets： 50
output:
A mistake occur, please search according to: 
403 Forbidden
63 - User has been suspended.



testcase4: too many tweets
discription: API do not support getting the amount of tweets needed(80)
input case:  keyword：‘Nadal’ total——tweets： 100
the total attitude score is 0.42770010178934763 



here is the attitude contradiction bar 
 

     [********************||||||]     
positive                      negative

 

the attitude is POSITIVE 
 which is calculate from 80 samples in which 53 samples has been count and 27 is neutral
Twitter API only afford to count in 80 tweets, the tweets out of 80 are no included.



testcase4: too many tweets
discription: API unable to find enough tweet needed
input case:  keyword：‘tennisAAAAA’ total——tweets： 80
output:
the total attitude score is 0.00000000000000000 



here is the attitude contradiction bar 
 

     []     
positivenegative

 

the attitude is NEUTRAL 
 which is calculate from 0 samples in which 0 samples has been count and 0 is neutral
Unable to find enough tweets, 0 tweets are calculated.
