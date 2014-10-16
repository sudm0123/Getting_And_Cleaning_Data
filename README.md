Coursera: Getting And Cleaning Data  
=========================
*Author: Sudhanshu Malik*  
*Description: Coursera project for Johns Hopkins' Getting and Cleaning Data course*

Overview  
---------
**Human Activity Recognition Using Smartphones**  
One of the most exciting areas in all of data science right now is wearable computing. Companies like Fitbit, Nike, and Jawbone Up are racing to develop the most advanced algorithms to attract new users. The data used in this project is the data collected from the accelerometers of the Samsung Galaxy S smartphone. A full description is available at the site where the data was obtained:  
<http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones>

Here is the data for the project:
<https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip>

*The purpose of this project is to demonstrate the ability to collect, work with, and clean a data set.*

Files Included
--------------------------
The following files are included:  
- run_analysis.R (R code for this project)  
- CodeBook.md (A description of the code used)  
- tidydata.txt (The data transformed to a more suitable form) 

Project Summary
---------------
The aim of the project is to create one R script called run_analysis.R that does the following:  
1. Merges the training and the test sets to create one data set.   
2. Extracts only the measurements on the mean and standard deviation for each measurement.  
3. Uses descriptive activity names to name the activities in the data set.   
4. Appropriately labels the data set with descriptive activity names.  
5. Creates a second, independent tidy data set with the average of each variable for each activity and each subject.  

Steps Involved
--------
###Step 1: Read these files from UCI HAR dataset directory :
**From the test directory:**  
- X_test.tx (measurement data)  
- y_test.txt (activity data)  
- subject_test.txt (subject data)  

**From the train directory:**  
- X_train.txt (measurement data)  
- y_train.txt (activity data)  
- subject_train.txt (subject data)  

###Step 2: Combining data:   
- Data from X-train is added to X-test to form data frame named "data".  
- Data y-train is added to y-test to form data frame "activity".  
- Training subject data is added to test subject data to form data frame "subject".  
- Test and training data frames are removed from environment to leave only combined data sets.   

###Step 3: Load and manipulate features data:  
- The file features.txt is read from the UCI HAR Dataset directory to create "feats" data set.  
- The feats data set is filtered to retain only the mean[mean()] and standard deviation[std()] variables.  
- The names of the retained features are changed to improve uniformity, remove confusing symbols, and make them more descriptive.  

###Step 4: Manipulate measurement data and attach descriptive variable names:    
- Columns of measurement data frame(called "data") are selected using the index variable(feats$V1) retained from filtering the features data frame.
- Variable names are attached using the features variable(feats$V2).  

###Step 5: Attach variables for activity and subject data to measurement data:  
- Activity and subject data are given descriptive variable names.  
- Activity and subject columns are added to the measurement data to create one unified data frame(data).  
- Activity, subject, and feats data frames are removed from environment leaving only unified data frame.  
- Numerical identifiers are replace with descriptive activity names in activity column.  

###Final Step:
- New data set is is created from unified data frame that takes mean values for all measurements by subject and activity called "tidydata".  
- Tidy data frame is saved as tidydata.txt in working directory.  
