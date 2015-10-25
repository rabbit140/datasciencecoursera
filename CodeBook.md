Project description
===================
The purpose of this project is to demonstrate your ability to collect, work with, and clean a data set. The goal is to prepare tidy data that can be used for later analysis. You will be graded by your peers on a series of yes/no questions related to the project. You will be required to submit: 1) a tidy data set as described below, 2) a link to a Github repository with your script for performing the analysis, and 3) a code book that describes the variables, the data, and any transformations or work that you performed to clean up the data called CodeBook.md. You should also include a README.md in the repo with your scripts. This repo explains how all of the scripts work and how they are connected.

> Description taken from Coursera's Getting and Cleaning Data assignment page

Study design and data processing
===============================

Collection of the raw data
--------------------------
The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.

##### For each record it is provided:
* A 561-feature vector with time and frequency domain variables. 
* Its activity label. 
* An identifier of the subject who carried out the experiment. 


##### The dataset includes the following files:


* 'README.txt'

* 'features_info.txt': Shows information about the variables used on the feature vector.

* 'features.txt': List of all features.

* 'activity_labels.txt': Links the class labels with their activity name.

* 'train/X_train.txt': Training set.

* 'train/y_train.txt': Training labels.

* 'test/X_test.txt': Test set.

* 'test/y_test.txt': Test labels.

##### The following files are available for the train and test data. Their descriptions are equivalent. 

* 'train/subject_train.txt': Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30. 

* 'train/Inertial Signals/total_acc_x_train.txt': The acceleration signal from the smartphone accelerometer X axis in standard gravity units 'g'. Every row shows a 128 element vector. The same description applies for the 'total_acc_x_train.txt' and 'total_acc_z_train.txt' files for the Y and Z axis. 

* 'train/Inertial Signals/body_acc_x_train.txt': The body acceleration signal obtained by subtracting the gravity from the total acceleration. (NOT USED FOR ANALYSIS PURPOSES)

* 'train/Inertial Signals/body_gyro_x_train.txt': The angular velocity vector measured by the gyroscope for each window sample. The units are radians/second. (NOT USED FOR ANALYSIS PURPOSES)

Creating the tidy datafile
==========================

Guide to create the tidy data file
----------------------------------

1. Download the data (https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip)
2. Unzip the archive into the working directory of RStudio
3. Source and run the "run_analysis.R" file
4. View the "tidy.txt" file that was created in your working directory

Cleaning of the data
--------------------

#####Data preparation

1. Extract features names and create "X_test" and "X_train" datasets
2. Merge the training and the test sets to create one data set

#####Data manipulation

3. Extracts only the measurements on the mean and standard deviation (string "-mean()" or "-std()") for each measurement
4. Merge "y_test" and "y_train"
5. Use descriptive activity names to name the activities in the data set
6. Appropriately labels the data set with descriptive variable names
7. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject

#####Data summary

8. Computes mean by subject id and activity
9. Removes unecessary columns and makes column names more readable

#####Data write

10. Writes the result to a "tidy.txt" file in the user's working directory

Variables
=========

#### Variable names


**Left column - in dataset, right clumn - original:**

|              Dataset              |           Original          |
|:---------------------------------:|:---------------------------:|
|       BodyAccelerationMeanX       |      tBodyAcc.mean...X      |
|       BodyAccelerationMeanY       |      tBodyAcc.mean...Y      |
|       BodyAccelerationMeanZ       |      tBodyAcc.mean...Z      |
|        BodyAccelerationStdX       |       tBodyAcc.std...X      |
|        BodyAccelerationStdY       |       tBodyAcc.std...Y      |
|        BodyAccelerationStdZ       |       tBodyAcc.std...Z      |
|      GravityAccelerationMeanX     |     tGravityAcc.mean...X    |
|      GravityAccelerationMeanY     |     tGravityAcc.mean...Y    |
|      GravityAccelerationMeanZ     |     tGravityAcc.mean...Z    |
|      GravityAccelerationStdX      |     tGravityAcc.std...X     |
|      GravityAccelerationStdY      |     tGravityAcc.std...Y     |
|      GravityAccelerationStdZ      |     tGravityAcc.std...Z     |
|     BodyAccelerationJerkMeanX     |    tBodyAccJerk.mean...X    |
|     BodyAccelerationJerkMeanY     |    tBodyAccJerk.mean...Y    |
|     BodyAccelerationJerkMeanZ     |    tBodyAccJerk.mean...Z    |
|      BodyAccelerationJerkStdX     |     tBodyAccJerk.std...X    |
|      BodyAccelerationJerkStdY     |     tBodyAccJerk.std...Y    |
|      BodyAccelerationJerkStdZ     |     tBodyAccJerk.std...Z    |
|         BodyGyroscopeMeanX        |      tBodyGyro.mean...X     |
|         BodyGyroscopeMeanY        |      tBodyGyro.mean...Y     |
|         BodyGyroscopeMeanZ        |      tBodyGyro.mean...Z     |
|         BodyGyroscopeStdX         |      tBodyGyro.std...X      |
|         BodyGyroscopeStdY         |      tBodyGyro.std...Y      |
|         BodyGyroscopeStdZ         |      tBodyGyro.std...Z      |
|       BodyGyroscopeJerkMeanX      |    tBodyGyroJerk.mean...X   |
|       BodyGyroscopeJerkMeanY      |    tBodyGyroJerk.mean...Y   |
|       BodyGyroscopeJerkMeanZ      |    tBodyGyroJerk.mean...Z   |
|       BodyGyroscopeJerkStdX       |    tBodyGyroJerk.std...X    |
|       BodyGyroscopeJerkStdY       |    tBodyGyroJerk.std...Y    |
|       BodyGyroscopeJerkStdZ       |    tBodyGyroJerk.std...Z    |
|   BodyAccelerationMagnitudeMean   |      tBodyAccMag.mean..     |
|    BodyAccelerationMagnitudeStd   |      tBodyAccMag.std..      |
|  GravityAccelerationMagnitudeMean |    tGravityAccMag.mean..    |
|  GravityAccelerationMagnitudeStd  |     tGravityAccMag.std..    |
| BodyAccelerationJerkMagnitudeMean |    tBodyAccJerkMag.mean..   |
|  BodyAccelerationJerkMagnitudeStd |    tBodyAccJerkMag.std..    |
|     BodyGyroscopeMagnitudeMean    |     tBodyGyroMag.mean..     |
|     BodyGyroscopeMagnitudeStd     |      tBodyGyroMag.std..     |
|   BodyGyroscopeJerkMagnitudeMean  |   tBodyGyroJerkMag.mean..   |
|   BodyGyroscopeJerkMagnitudeStd   |    tBodyGyroJerkMag.std..   |
|       BodyAccelerationMeanX       |      fBodyAcc.mean...X      |
|       BodyAccelerationMeanY       |      fBodyAcc.mean...Y      |
|       BodyAccelerationMeanZ       |      fBodyAcc.mean...Z      |
|        BodyAccelerationStdX       |       fBodyAcc.std...X      |
|        BodyAccelerationStdY       |       fBodyAcc.std...Y      |
|        BodyAccelerationStdZ       |       fBodyAcc.std...Z      |
|     BodyAccelerationJerkMeanX     |    fBodyAccJerk.mean...X    |
|     BodyAccelerationJerkMeanY     |    fBodyAccJerk.mean...Y    |
|     BodyAccelerationJerkMeanZ     |    fBodyAccJerk.mean...Z    |
|      BodyAccelerationJerkStdX     |     fBodyAccJerk.std...X    |
|      BodyAccelerationJerkStdY     |     fBodyAccJerk.std...Y    |
|      BodyAccelerationJerkStdZ     |     fBodyAccJerk.std...Z    |
|         BodyGyroscopeMeanX        |      fBodyGyro.mean...X     |
|         BodyGyroscopeMeanY        |      fBodyGyro.mean...Y     |
|         BodyGyroscopeMeanZ        |      fBodyGyro.mean...Z     |
|         BodyGyroscopeStdX         |      fBodyGyro.std...X      |
|         BodyGyroscopeStdY         |      fBodyGyro.std...Y      |
|         BodyGyroscopeStdZ         |      fBodyGyro.std...Z      |
|   BodyAccelerationMagnitudeMean   |      fBodyAccMag.mean..     |
|    BodyAccelerationMagnitudeStd   |      fBodyAccMag.std..      |
| BodyAccelerationJerkMagnitudeMean |  fBodyBodyAccJerkMag.mean.. |
|  BodyAccelerationJerkMagnitudeStd |  fBodyBodyAccJerkMag.std..  |
|     BodyGyroscopeMagnitudeMean    |   fBodyBodyGyroMag.mean..   |
|     BodyGyroscopeMagnitudeStd     |    fBodyBodyGyroMag.std..   |
|   BodyGyroscopeJerkMagnitudeMean  | fBodyBodyGyroJerkMag.mean.. |
|   BodyGyroscopeJerkMagnitudeStd   |  fBodyBodyGyroJerkMag.std.. |
|             subject_id            |           N/A               |
|              activity             |           N/A               |

> **Notes:**
> * All variables, except for 'subject_id' and 'activity' (type: character) are of type numeric.
> * "Std" appearing in variable names is standard deviation of measurements


License
-------
[1] Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012
