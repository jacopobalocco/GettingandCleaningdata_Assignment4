Getting and Cleaning Data Assignment 4 README.txt
==================================================

Author: Emily Smenderovac 

The data utilized to create this tidy dataset were files from the 
UCI HAR data set retrieved from 
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip on April 8th, 2016.

## The files used in the analysis were in the UCI HAR Dataset directory

- 'features.txt': List of all features.

- 'activity_labels.txt': Links the class labels with their activity name.

- 'train/X_train.txt': Training set.

- 'train/y_train.txt': Training labels.

- 'test/X_test.txt': Test set.

- 'test/y_test.txt': Test labels.

- 'train/subject_train.txt'

- 'test/subject_test.txt'

Details on these datasets can be found in the UCI HAR Dataset README.txt file as well as the features_info.txt file found in the unzipped directory downloaded from the link above. 

Data from train and test subjects were merged and averages by subject id and type of activity were used to summarize the data.

## The files included for the production of the tidy dataset are:

README.md

CodeBook.Rmd

CodeBook.md

run_analysis.R

###The tidy data set created with the run_analysis.R script summarizes the mean of select variables for each subject for different activities.
###The script is annotated to inform readers on the data download, merger, relabeling and tidying.
The main steps of the run_analysis.R script are: 

1. download data into R from the UCI HAR Dataset

2.Merges the training and the test sets to create one data set

3.Extracts only the measurements on the mean and standard deviation for each measurement. 

4.Uses descriptive activity names to name the activities in the data set add descriptive activities to the activities column

5.Appropriately labels the data set with descriptive variable names.

6.Create a tidy dataset.


##The variables in the tiny dataset produced from the script are as follows:

[1] "subject" - subject id  

 [2] "activity" - physical activity being conducted one of 6 variables (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING)                                                 
 [3] "datset" - whether the data came from the test or training dataset   
 
The remaining data are means of different measures derived from Gyroscope and Accelerometer data for either body acceleration or gravity acceleration.
 
 [4] "timeBodyAccelerationAccelerometer-mean()-X"  
 
 [5] "timeBodyAccelerationAccelerometer-mean()-Y"
 
 [6] "timeBodyAccelerationAccelerometer-mean()-Z"
 
 [7] "timeBodyAccelerationAccelerometer-std()-X"    
 
 [8] "timeBodyAccelerationAccelerometer-std()-Y"  
 
 [9] "timeBodyAccelerationAccelerometer-std()-Z"     
 
[10] "timeGravityAccelerometer-mean()-X"           

[11] "timeGravityAccelerometer-mean()-Y"        

[12] "timeGravityAccelerometer-mean()-Z"        

[13] "timeGravityAccelerometer-std()-X"         

 as follows for the remaining variables... 
 
 A full list of original variables included in the dataset is availiable in the 
 CodeBook.md and can be regenerated from CodeBook.Rmd if the dataset should change. Data was renamed to be more informative.
 
 

