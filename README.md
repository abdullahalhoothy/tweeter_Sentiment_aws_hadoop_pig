# tweeter_Sentiment_aws_hadoop_pig
Practice project on using hadoop through pig through aws


# Project source
Sentiment Analysis on Demonetization – Pig Use Case (https://acadgild.com/blog/pig-use-case-sentiment-analysis-on-demonetization)
the usecase in the link NOT using aws.

#### -- Project Status: [In-progress]
https://

## Project Intro/Objective
The purpose of this practice project is for me to get a hands on expereince on how to use hadoop.
After learning about hadoop structure and that it's language is in Java i decided to use pig latin since won't be likely creating andy custom functions (UDFs)
i didn't want to install a virtual machine on my computer because i didn't want to potentially introduce unforseen errors due to installation and i figured this would be a good time to learn how to use aws
and in this project i will be defining setp by step approach i took.


### Methods Used
* AWS setup 
* Exploratory analysis
* ~~Descriptive analysis~~
* ~~Data Visualization~~
* ~~Predictive Modeling~~
* ~~Linear model~~
* ~~DecisionTreeRegressor~~
* ~~XGboost~~
* ~~Random Forests~~

### Technologies/packages
* Pig latin(grunt shell)
* Hadoop
* ~~Python.~~
* ~~Pandas, jupyter.~~
* ~~Scikit-learn.~~
* ~~Seaborn.~~


## Project Description
Given data about tweets we would like to know how people feel about the subject of "demontaization of currency". tweets are from india. the challenge is to analyze the sentiment based on the tweets given in the data.
The Features of data included things like (Metadata)
id (int)
Text (Tweets)
favorited (Binary)
favoriteCount(int)
replyToSN(text)
created(time stamp)
truncated (binary)
replyToSID (int)
id (int)
replyToUID (int)
statusSource (text)
screenName (text)
retweetCount (int)
isRetweet (Binary)
retweeted (binary)

## AWS setup
to use AWS EMR (Elastic Map Reduce) i needed the data to also be on AWS (S3).
so step one is upload the data to a bucket in aws S3.
step two is go to EC2 and then to security and chose to make a new keypair unless you already have one.download the keypair.pem.
step three download putty and puttygen. 
step four using puttygen convert the .pem to .ppk 
step five go to AWS EMR and creat a cluster . make sure to choose the pair key from the dropdownmenu.
step six watch this video (https://www.youtube.com/watch?v=CoJ6L_dEA5Y&t=311s).
* Make sure EC2 instance is running.
* Check your security group rules. You need a security group rule that allows inbound traffic from your public IPv4 address on the *proper port.
* Check the network access control list (ACL) for the subnet. The network ACLs must allow inbound and outbound traffic from your local IP address on the proper port. The default network ACL allows all inbound and outbound traffic.
* Check the route table for the subnet. You need a route that sends all traffic destined outside the VPC to the internet gateway for the VPC.
step seven open putty and in the Host Name field, type hadoop@ecxxxxxxxxx.compute-1.amazonaws.com[Master public DNS:SSH].
step 8 in putty go to connections and then to auth and load the ppk pair key and then press open.
an EMR connection should connect with big EMR written 
step eight type "pig" which would launch pig instance using grunt shell
step nine the grunt shell by typing the following code.
To load the data into a alias:
load_tweets = LOAD 's3://bigdatapracticetweeter/demonetization-tweets.csv' USING PigStorage(',');
to view the data in the first alias:
dump
Each row(tuple) looks like the following:
("1","RT @rssurjewala: Critical question: Was PayTM informed about #Demonetization edict by PM? It's clearly fishy and requires full disclosure &amp;�",FALSE,0,NA,"2016-11-23 18:40:30",FALSE,NA,"801495656976318464",NA,"<a href=""http://twitter.com/download/android"" rel=""nofollow"">Twitter for Android</a>","HASHTAGFARZIWAL",331,TRUE,FALSE)

## Needs of this project

- ~~data exploration/descriptive statistics.~~
- ~~data processing/cleaning.~~
- ~~statistical modeling.~~
- ~~writeup/reporting.~~

## Exploring the Data




