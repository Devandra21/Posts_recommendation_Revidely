# Posts_recommendation_Revidely
The input variables chosen are views, upvote, downvote, Comments,  Shares, Timespent(ona a post), Link Opened.
The dataset contains:
1) 200 users having user_id 1 to 200 using kutools.
2) 1000 posts having post_id from 1 to 1000 using kutools.
3) Total views are random integers between 1 to 200 using kutools.
4) upvotes are random integers which are less than the views.
5) downvotes are random integers which are less than the views.
6) Comments are random integers between 0 to 50 using kutools.
7) Shares are random integers between 0 to 40 using kutools.
8) Time spent per posts are random real numbers between 1 to 60 seconds using kutools.
9) link opened are assigned randomly 0 or 1 or 2, 0 for no link present , 1 for link present but not opening , 2 for link present and opening.
Finally a new score is given based on the formula:
Score = (.5)*(views) + (.38)*(upvote) + (-.14)*(downvote) + (.21)*(Comments) + (.16)*(Shares) + (-.15)*(timespent) + (.04)*(link opened)
Reasons to assign such values:
1) All the coeffiecients sum to 1.
2) All the variables used are normalized variables.
3) Highest weight(.5) is given to views as if a post has many views it becomes trending and more and more people wants to know about trending.
4) Then next highest to upvote as more number of people upvoted the post so it may be useful to others too.
5) Negative weight is assigned to downvote because a negative impression is considered less and negative vies of people will make the post less recommended.
6) More commented post can attract people.
7) Sharing will also bring attention of people so it is also important variable.
8) Negative weight is assigned to timespent as accordinf to data timespend shows the amount of time spent by people and if amount of time spent on a post is less the users can see more posts ,so negative weight is assigned.
9) If a link is present in a post and if it is opened or not contributes very less to recommend a post so least weight is given to it.

Finally Posts are predicted using the user-user similarity.

The Sheet Raw_data has all the data.
The Sheet Predicted_output has all the user ids with there predicted output.
