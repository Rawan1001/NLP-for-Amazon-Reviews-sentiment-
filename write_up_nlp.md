## NLP for Amazon Reviews sentiment:
> In this project our task was to get a dataset to build an NLP model. We chose to analyze a dataset obtained from a website that collects amazon customers reviews of different products they bought.


> -  We used the CountVectorizer tool to convetr the reviews into document-term matrix as unigram.
> -  Then, we used Svd to extract and reduce the featutes we will use in the classification. 
> -  clustering.
> -  We used a number of classifiction algorithms to pridect if the reviews will be negative or positive.

## Data Collection :

>**We chose the Luxury Beauty products dataset for this project:**
>- The dataset was obtained from  this website https://nijianmo.github.io/amazon/index.html# 
>- The dataset contains 34278 reviews (rows) and 12 columns in total.


>**Our EDA steps :**

>- Dropping all the duplicated values and removing all the uneeded columns such as: reivewers names and IDs.
>- Stripped all spaces and unwanted characters form the columns.
>- Cleaning the outliers.
>- Converting categorical data to numeric ones.

>**After cleaning the dataset the remainning rows are 25911.**

## EDA graph:

>This graph shows the number of reviews for each month during the perioed of 14 years. the dataset we have are during thr period form 2005 to 2018.

<img width="450" alt="Screen Shot 2021-11-15 at 7 19 52 PM" src="https://github.com/nisreenabdullah6/NLP-Project/blob/main/EDA-4.png">

## cluster graph
> This graph shows the distrbution of words in customers reviwes in the dataset, and the number of colors represent the number of clusters.

<img width="450" alt="Screen Shot 2021-11-15 at 7 19 52 PM" src="https://github.com/nisreenabdullah6/NLP-Project/blob/main/cluster.png">



## Future work:

>- Convetrting the reviews into document-term matrix as bigram.
>- Using other liberies such as Spacy.




```python

```
