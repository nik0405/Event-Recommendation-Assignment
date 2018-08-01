# Team-16-Event-Recommendation-Assignment-
Event Recommendation AI/ML Assignment - Genpact Digital

Problem-Predict what events our users will be interested in based on events they’ve responded to in the past, user demographic information, and what events they’ve seen and clicked on in our app.

Looking at the problem we could figure out that the problem was a type of Supervised Classification Problem since we knew what was to be predicted . i.e events which the user will be intrested in.

The Data cant be uploaded here due to size contraints.
It is uploaded in One Drive - 
https://genpactonline-my.sharepoint.com/:f:/r/personal/703177888_genpact_com/Documents/Assignment_DataFinal?csf=1&e=1YZBbd


Files Description-

1.Assignment_1_ClusterEvent - Here we try to figure out ‘event cluster by topic’. The events_min1.csv file has the frequencies of common words for each event. These events are hence clustered by these words. We have used k-means algorithm for clustering these events and create cluster_events.csv . We then use this as a Feature in our model.

2.Assignment_2_DataPreProcessor - We extracted certain features from the dataset we believed were important to train our model. We try to get some of the features(eight) and then create a feature_train.csv which contains all the features required to train our model.

3.Assignment_3_LaebellingFeatures - Here we try to label the data which are repeating values and the boolean values. We labelled -'user_locale', 'same_city', 'user_joinedAt', 'same_country', 'user_gender', 'admin_friend','cluster' . Then we write it into feature_train_labelled.csv

4.Assignment_4_Model - Here we try to predict using the feature_train_labelled.csv created earlier. We used Random Forest and Logistic Regression to calculate the predictions and find accuracy score and log loss.


Data Description-

1.events_min1.csv - We had to minimize the data , so we used SQL query to extract some data from train.csv,events.csv and user.csv and then filtered out the missing blanks and then created events_min1.csv which we used to start with data preprocessing.
Columns- event_id, user_id, start_time, city, state, zip, country, lat, and lng .The last 101 columns are count_1, count_2, ..., count_100, count_other, where count_N is an integer representing the number of times the Nth most common word stem appears in the name or description of this event.  count_other is a count of the rest of the words whose stem wasn't one of the 100 most common stems.

2.event_attendees -It contains information about which users attended various events, and has the following columns: event_id, yes, maybe, invited, and no.

3.users.csv- It contains demographic data about our some of our users (including all of the users appearing in the train and test files), and it has the following columns: user_id, locale, birthyear, gender, joinedAt, location, and timezone. user_id is the id of the user in our system.

4.user_friends.csv - It contains social data about this user, and contains two columns:  user and friends.

5.train.csv- It has six columns:  user, event, invited, timestamp, interested, and not_interested.

6.test.csv - It contains the same columns as train.csv, except for interested and not_interested.



Steps to run-

1.Download all the data and put in a data folder

2.Downloada all scripts and put in parent folder of data folder.

3.Run the scripts in jupyter IDE.
4.Run the scripts in order of the labelled scripts sequence.
