Coursera: Getting And Cleaning Data  
====================================
*Author: Sudhanshu Malik*  
*Description: Coursera project for Johns Hopkins' Getting and Cleaning Data course*  

Description
-----------
This codebook refers to the tidy data set created using run_analysis.R on the UCI HAR Dataset.  

Source Data
------------
The source data for the project can be found at:   <https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip>  

Data Set Information
---------------------
The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.  

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.  

Attribute Information
----------------------
For each record in the dataset it is provided:

- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
- Triaxial Angular velocity from the gyroscope.
- A 561-feature vector with time and frequency domain variables.
- Its activity label.
- An identifier of the subject who carried out the experiment.  

Variables
----------
`feats`          : Variable for data from the features.txt   

`test`           : Variable for data from the X_test.txt  

`train`          : Variable for data from the X_train.txt  

`data`           : Variable for binded test and train  

`activity_test`  : Variable for data from the Y_test.txt

`activity_train` : Variable for data from the Y_train.txt  

`activity`       : Variable for binded activity_test and activity_train data  

`subtest`        : Variable for data from the subject_test.txt  
 
`subtrain`       : Variable for data from the subject_train.txt  

`subject`        : Variable for binded subtest and subtrain data

`tidy_df`        : Variable for calculated average of each variable for each activity and each subject  

**The features variables were transformed as follows:**  

`tBodyAcc -> timebodyacceleration`   

`ttGravityAcc -> timegravityacceleration`   

`tBodyAccJerk -> timebodyaccelerationjerk`     

`tBodyGyro -> timebodygyro`  

`tBodyGyroJerk -> timebodygyrojerk`  

`tBodyAccMag -> timebodyaccelerationmagnitude`  

`tGravityAccMag -> timegravityaccelerationmagnitude`  

`tBodyAccJerkMag -> timebodyaccelerationjerkmagnitude`  

`tBodyGyroMag -> timebodygyromagnitude`  

`tBodyGyroJerkMag-> timebodygyrojerkmagnitude`  

`fBodyAcc -> frequencybodyacceleration`  

`fBodyAccJerk -> frequencybodyacceleration`  

`fBodyGyro -> frequencybodygyro`  

`fBodyAccMag -> frequencybodyaccelerationmagnitude`  

`fBodyAccJerkMag -> frequencybodyaccelerationjerkmagnitude`  

`fBodyGyroMag -> frequencybodygyromagnitude`  

`fBodyGyroJerkMag-> frequencygyrojerkmagnitude`  


**Activity data was transformed into descriptive names:**

1. WALKING  
2. WALKING_UPSTAIRS  
3. WALKING_DOWNSTAIRS   
4. SITTING   
5. STANDING   
6. LAYING  

Processed Data
---------------
The set of feature variables evaluated for mean and standard deviation observations were retained. The tidy data set(available as tidydat.txt) is average of these values for these measurements by subject identified by integers(1-30), and the activity identified as above. The measurements have been normalized so there are no units.
