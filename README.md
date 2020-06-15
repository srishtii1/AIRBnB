# AIRBnB
Analyses the Seattle AirBnB dataset (source: Kaggle) to find out what can hosts do to become Super-Hosts (dataset in the zip folder 'Datasets.zip')

The project uses the listing.csv to analyse the numerical and categorical data using Logistic Regression and Random Forest Classifier. 
Further, I have used the textual reviews in reviews.csv to analyse the sentiments. I have performed Sentiment Analysis using VADER package. After analysing the sentiments, I separated positive and negative sentiments into two different dataframes. I then analysed which factors are more important for positive reviews and what should hosts avoid doing by analysing negative reviews. this involved finding the most frequently occuring words in the dataframe. To achieve this, the following strategy was adopted:

1. Data preparation: 

   1.1. Language identification. Followed by removal of all language comments except English
   
   1.2. Tokenizing 
   
   1.3. Lemmatization 
   
   1.4. Using POS Tagging to keep just nouns
   
   1.5. Removal of Stopwords
   
 
 
 2. Analysed comments using three different models
 
    2.1. WordCloud Method: Looks artsy but is a poor method of visualization of data
    
    2.2. Frequency Chart: Used Yellowbrick library to draw a frequency table of the 30 most frequently used words in data
    
    2.3. Latent Dirichlet Allocation Model (LDA): This is a bag of words model. It takes the number of topics as a parameter let’s say 3. It then picks three topics from the dataset and assigns a topic to each word such that the entire data is clustered into 3 topics like you can see in the image. This clustering is done based on how close a particular word is to that specific topic. 
The output is a sorted list of words with their probability of occurring. 


From the above model the following conclusions were drawn:


Reviews and ratings have a huge role in determining whether a host is eligible to be a superhost. After analysing the positive and negative reviews, we can conclude that customers have a strong preference for apartments with:
1. An accessible location that is central 
2. Good kitchen and bed
3. Clean interior
4. Hassle-free transaction/ check-in and check-out 
5. Available parking
-----
With the above pointers in mind, we have the following suggestion for hosts:

1. Since it is impossible for host to physically change the location of the listing, they can give directions to places of interest that are nearby. This allows customers to get around easily.
2. Invest in good amenities so that their customers can have an enjoyable stay.
3. Hire professional cleaners that can maintain the cleanliness of the apartment.
4. Communicate and clarify with the customers about the procedures to avoid confusion and issues down the road.
