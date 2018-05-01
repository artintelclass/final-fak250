# AccioBot

## Team Members: 
Farzan Khan, Manas Pant, Ali Shazal

## Project Description: 
This is a chatbot trained using data from a facebook group called "NYUAD Room of Requirement." This is a facebook group for the student population of NYUAD, where students ask a variety of questions ranging from comments on courses to gauging interest for student groups and other students respond with help in one way or another. The bot is deployed on a webpage. 

## Data Scraping
For the data, we were targeting data made up of atleast 100,000 words from the group for the posts and the comments on the posts. We initially tried to look for help using the Facebook API but that approach proved to be unsuccessful so we tried using javascript and the webpage console instead. Using developer tools, we inspected the markup and found the class names for the post, the post text and the comment text. Then using the data scraping script, we were able to obtain files for both comments and posts, which were then cleaned using separate python scripts that are included in the repo. 


## Challenges
1. One of the challenges that we faced was the problem of autoscroll. We tried using autoscroll to go down to enough posts for a satisfactory amount of data but the browser would either crash or stop responding because of too much data loaded. To tackle this problem, we started navigating to specific dates according to months and using key phrases that were recurring in many facebook posts like, "hey." This came up to about 5000/6000 words per iteration so using this we were able to get to our data. 

2. Another problem was that using the strategy above, the comments weren't showing so using the class of the link that shows comments along with javascript, we were were able to expedite the process of loading all of the posts on a page with the comments. This script is included in the comment scraper file. 

3. Another challenge was that every post has multiple comments so we need the comments to be grouped according to the posts in order for it to be trainable data for the bot as the bot will see things as questions and answers. To do this, we added a seperator to the array that the comments were being pushed to so that the data could be cleaned accordingly.


