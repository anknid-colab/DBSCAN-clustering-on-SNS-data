# Unsupervised Learning: DBSCAN (Destiny Based Spatial Clusters with Applicaion of Noise)
## Project: Build an unsupervised model on Social Networking Services dataset for the Marketing teams to target specific clusters of students with certain interests or beliefs.
## Project Overview:
The dataset collected used for clustering analysis with DBSCAN contains social networking service (SNS) information of 30000 anonymous U.S. high school students who had SNS profile in 2006. This dataset was compiled by Brett Lantz while conducting his sociological research on the teenage identities at the University of Notre Dame, and was used again as example in his book: Machine Learning with R (second edition) published by PACKT.
The SNS dataset contains 30000 observations (rows) each preresents a high school student and 40 features (columns) that provides information for the student. The 40 features includes graduation year, the gender, age and number of friends one has connected throught the SNS for each student, and the remaining 36 columns are word/s terms such as football, shopping, hot, church etc. that describes the student interest and beliefs with value of 1 indicates a belonging to the group, and 0 otherwise. Information like this can help to group individuals into clusters with similar interest, and provide help for companies’ marketing teams to advertise appropriate products online targeting students with certain interest or belief.
## Software requirements 
This project uses the following softwares and libraries:
- RStudio (https://rstudio.com/)
- KMeans (https://www.jstor.org/stable/2346830?origin=crossref)

## Data Munging  
After collecting and reading the data, I have treated the missing values. As the "Gender" has more number of Female counts, we have replaced the missing values with Female in that column. Missing values in "Age" column are repalced with the mean of the same column. 
## Normalize the data.
To apply DBSCAN algorithm, we need to normalize our data, so that all the records have same range, that is 0-1. Also, by normalizing the data, we make the dataset uniteless.  And hence, we would be able to apply minimum distance while implementing the DBSCAN algorithm. The formula for normalization is as follows: 

![alt text](https://github.com/NikhilSalv/DBSCAN-clustering-on-SNS-data/blob/main/Normalization-Formula.jpg) 

## Hyperparameter Optimizing.

After data munging part, we come to Hyperparameter optimizing part. Here, we try different values of eps (Minimum distance) and Minimum points. 
As we increase the minimum distance between two data points, the noise decreases, and as we increase the minimum points of a cluster, the noise increases. 
We choose the valaues of eps (minimum distance) and minimum points to be 0.5 and 5 respectively.  

# Running the model on the dataset.
After predicting the value of eps and minimum points, we run the DBSCAN Clustering algorithm on the SNS dataset. The output denotes the 2 clusters. The output column is row-wise combined with the original dataset. And we can see that which record belongs to which cluster. 
