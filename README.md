# HAPT_auto_viz

Using the wildly popular HAPT dataset, the goal is to simply visualise it.

This task is difficult for a few reasons. Primarily the complex nature of the features and difficulty in understanding the features after applying PCA to reduce the
features to 3.


The train and test folders contain three files each which are connected such that the first file called X_train.txt (or X_test.txt) contains the feature data. 
It contains 7767 rows of data and 561 columns for the training data. Each row is a measurement made of one of the 30 subjects.
The file y_train.txt (or y_test.txt) contains labels for the data. Here row 1 contains the label for row 1 of X_train.txt (or X_test.txt),
row 50 of y_train.txt contains the label for row 50 of X_train.txt (or X_test.txt), and so on.
The file subject_id_train.txt contains data describing which volunteer each row refers to. For example, rows 1 – 368 of X_train.txt (or X_test.txt)
were recorded by volunteer number 1.



The following steps were applied to attempt visualising the data. --ONLY TRAINING DATA IS USED FOR THIS TASK BUT TEST IS INCLUDED AS WELL--

1. Standardise the data
2. Get rid of outliers using winsorisation or get rid of those records altogether (This step was not implemented yet)
3. Exclude readings with blanks
4. Reduce dimensionality using PCA
5. Partition data by subject id and then label
6. Use partitioned data and get average readings for all users taking a particular action (falling under a certain label)
7. Plot the readings in the most appropriate chart. Probably scatter

After the above was implemented, there was still very little meaning in the visualisation. The entire data set was then plotted on an interactive chart where each line represented a single label's readings of a single pca component.