# yelp-dataset-analysis

## Sentimental Analysis and categorizing Yelp reviews in Subtopics 
## 1. Introduction

The pandemic has pushed businesses and consumers to shift to an online service over the last two years. With this impact, social media presence has become important to how well a business is performing. Yelp is a business that allows consumers to publish crowd-sourced reviews about businesses. Users can view ratings of any businesses which are measured by taking the average of overall ratings in reviews. There is an immense amount of data where users submit reviews about a businesses based on their food, service, pricing, ambience and much more. The reviews dataset can be explored and classified so businesses can find their areas of improvement. The focus on this project is to study reviews and filter reviews into categories: Food, service and pricing. Text mining solutions such as LDA and Sentimental analysis will be performed to improve ratings and categorize these reviews into Sub-topics.

## 2. Data Exploration 

The Yelp dataset contained the following JSON files and was a total size of approximately 23.5 GB: 
- Business
- Checkin 
- Covid features
- Review
- Tip
- User

For this research, only relevant files are business and reviews. Only reviews of restuarants with over 100 review count were filtered out. Then top 10 states with the most restuarants were extracted and analyzed. A restaurant called Buffet Palace with 383 reviews was randomly selected for further analysis. The overall rating for Buffetpalace is 3.5 stars. Lastly, only important attributes such as Review Id, Business Id, star rating, and text were extracted into a CSV file for further analysis.

![alt text](https://github.com/kundana-balijepalli/yelp-dataset-analysis/blob/main/Images/Preview%20of%20data.JPG)


## 3. Pre - processing

The following diagram illustrations the steps taken to pre-process the text:

![alt text](https://github.com/kundana-balijepalli/yelp-dataset-analysis/blob/main/Images/Pre-processing.JPG)

## 5. Topic prediction

First, each review was broken down into various dimensions or topics. As above mentioned, these dimensions can be service, food, pricing etc. For topic modelling, we will use un-supervised learning algorithm Latent Dirichlet Allocation (LDA) as our model. The reason for choosing this modelling technique is because LDA treats each document as a mixture of topics, and each topic as a mixture of words. 

I attempted LDA in R and found the available libraries to be limited. Hence, I am experiementing with the following Python libraries currently: LDA Gensim, Scikit-Learn and LDA Mallet

Here are the visuals of topic modeling using LDA Gensim library in python

![alt text](https://github.com/kundana-balijepalli/yelp-dataset-analysis/blob/main/Images/topic1.JPG)

![alt text](https://github.com/kundana-balijepalli/yelp-dataset-analysis/blob/main/Images/topic2.JPG)

![alt text](https://github.com/kundana-balijepalli/yelp-dataset-analysis/blob/main/Images/topic3.JPG)

![alt text](https://github.com/kundana-balijepalli/yelp-dataset-analysis/blob/main/Images/topic4.JPG)


## 5. Sentimental Analysis
