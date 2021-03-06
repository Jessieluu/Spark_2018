# Big Data Mining and Application 2018
Upload class implementation and homework

## Environment
* Spark
* Jupyter
* Linux (Ubuntu on vmware)

## Program Language
* Python3

## homework

### 2018/03/30 HW#1: Hadoop/Spark distributed mode setup & simple calculation in MapReduce
#### Data:
[Individual household electric power consumption dataset] from UCI Machine Learning Repository.
About 2 million instances, 20MB (compressed) in size.
Available at: https://archive.ics.uci.edu/ml/datasets/individual+household+electric+power+consumption 

#### 3 subtasks:
(1) Output the minimum, maximum, and count of the columns: ‘global active power’, ‘global reactive power’, ‘voltage’, and ‘global intensity’ 
(2) Output the mean and standard deviation of these columns
(3) Perform min-max normalization on the columns to generate normalized output

### 2018/04/13 HW#2: Statistics of various data types in MapReduce (co-occurrence)
#### Data:
[News Popularity in Multiple Social Media Platforms dataset] from UCI Machine Learning Repository.
About 100,000 news items on four different topics: economy, microsoft, Obama, and Palestine, during November 2015 and July 2016.
Available at: https://archive.ics.uci.edu/ml/datasets/News+Popularity+in+Multiple+Social+Media+Platforms 

#### 4 subtasks:
(1) In news data, count the words in two fields: ‘Title’ and ‘Headline’ respectively, and list the most frequent words according to the term frequency in descending order, in total, per day, and per topic, respectively
(2) In social feedback data, calculate the average popularity of each news by hour, and by day, respectively (for each platform)
(3) In news data, calculate the sum and average sentiment score of each topic, respectively
(4) From subtask (1), for the top-100 frequent words per topic in titles and headlines, calculate their co-occurrence matrices (100x100), respectively. Each entry in the matrix will contain the co-occurrence frequency in all news titles and headlines, respectively 

### 2018/05/03 HW#3: Similarity estimation using MapReduce (for computing minhash signatures, LSH, and KNN search) 
#### Data:
[Reuters-21578 Text Categorization Collection Data Set] from UCI Machine Learning Repository.
It contains 21,578 news articles from Reuters in 1987.
Available at: https://archive.ics.uci.edu/ml/datasets/reuters-21578+text+categorization+collection 

#### 4 Subtasks:
(1) Given the Reuters-21578 dataset, please calculate all k-shingles and output the set representation of the text dataset as a matrix.
(2) Given the set representation, compute the minhash signatures of all documents using MapReduce.
(3) Implement the LSH algorithm by MapReduce and output the resulting candidate pairs of similar documents. 
(4) Implement K-nearest neighbor (KNN) search using LSH and compare its performance with linear search.

### 2018/05/03 HW#4: Matrix multiplication using MapReduce (for dimension reduction using SVD, or CUR) 
#### Data:
[Reuters-21578 Text Categorization Collection Data Set] from UCI Machine Learning Repository.
It contains 21,578 news articles from Reuters in 1987.
Available at: https://archive.ics.uci.edu/ml/datasets/reuters-21578+text+categorization+collection 

#### 4 Subtasks:
(1) Given the Reuters-21578 dataset, please calculate the term frequencies, and output the representation of the document contents as a term-document count matrix.
(2) Implement matrix multiplication by MapReduce. Your program  should be able to output the result in appropriate dimensions. 
(3) Given the term-document matrix in (1), compute the SVD decomposition of the matrix using MapReduce. Output the resulting eigenvalues and eigenvectors.
(4) Given the term-document matrix in (1), compute the CUR decomposition of the matrix using MapReduce. Output the resulting eigenvalues and eigenvectors.

### 2018/05/17 HW#5: Analyzing web graphs in MapReduce (Connectivity, PageRank, ...) 
#### Data:
[Google web graph Data Set] from Stanford Large Network (SNAP) Dataset Collection
The data was released in 2002 by Google as a part of Google Programming Contest
Available at: http://snap.stanford.edu/data/web-Google.html 

#### 4 Subtasks:
(1) Given the Google web graph dataset, please output the list of web pages with the number of outlinks, sorted in descending order of the out-degrees.
(2) Please output the inlink distribution of the top linked web pages, sorted in descending order of the in-degrees.
(3) Design an algorithm that maintains the connectivity of two nodes in an efficient way. Given a node v, please output the list of nodes that v points to, and the list of nodes that points to v. 
(4) Compute the PageRank of the graph using MapReduce. 


## Quiz (2018/04/21)

#### Data:
[KDD Cup 1999 Data dataset] from UCI Machine Learning Repository
Available at: http://archive.ics.uci.edu/ml/datasets/kdd+cup+1999+data
Size: 18MB compressed, 743 MB uncompressed

#### Tasks:
(1) For continuous attributes ‘duration’, ‘src_bytes’, ‘dst_bytes’,
‘num_failed_logins’, please calculate their mean, median, mode, standard
deviation, respectively

(2) For symbolic attributes ‘protocol_type’, ‘service’, ‘flag’, ‘logged_in’,
‘intrusion_type’, output the list of each value and the corresponding
frequency count, sorted in descending order of the count

(3) Output the list of the most frequently used ‘service’ for each
‘intrusion_type’, sorted in descending order of the occurrence frequency

## Bonus (2018/05/02)

#### Data:
[Crime Datasets, Chicago] from US-City Open Data Census
For the city of Chicago, since 2001
Available at: https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-present/ijzp-q8t2  


#### Tasks:
(1) For the attributes  ‘Primary type’ and ‘Location description’, output the list of each value and the corresponding frequency count, sorted in descending order of the count, respectively.
(2) Output the most frequently occurred ‘Primary type‘ for each possible value of ‘Location description’, sorted in descending order of the frequency count.
(3) Output the most frequently occurred street name in the attribute ‘Block‘ for each ‘Primary type’, sorted in descending order of the frequency count. (You should remove the numbers in the ‘Block’ address of a street/avenue/boulevard) 
(4) From the attribute ‘Date’, extract the time in hours and output the most frequently occurred hour for each ‘Primary type’ and ‘Location description’, sorted in descending order of the frequency count, respectively.
