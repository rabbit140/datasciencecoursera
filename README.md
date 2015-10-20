Getting And Cleaning Data - 'run_analysis.R' script and data transformation
===================

The data which 'run_analysis.R' operates on is available under https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 

----------


Script
-------------

The **'run_analysis.R** script does the following:

1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement. 
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive variable names. 
5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

> **Note:**

> -The unzipped folder with data ('UCI HAR Dataset') should be present in the working directory as given by getwd() function

> -Only variables containing 'mean()' and 'std()' are used

####  Running the script

To run the script on data, source it from within the R console.

#### Output

The output file is created in the working directory and is called 'tidy.txt'.



Data
--------


#### Variable names


**Left column - in dataset, right clumn - original:**

|              Dataset              |           Original          |
|:---------------------------------:|:---------------------------:|
|       BodyAccelerationmeanX       |      tBodyAcc.mean...X      |
|       BodyAccelerationmeanY       |      tBodyAcc.mean...Y      |
|       BodyAccelerationmeanZ       |      tBodyAcc.mean...Z      |
|        BodyAccelerationstdX       |       tBodyAcc.std...X      |
|        BodyAccelerationstdY       |       tBodyAcc.std...Y      |
|        BodyAccelerationstdZ       |       tBodyAcc.std...Z      |
|      GravityAccelerationmeanX     |     tGravityAcc.mean...X    |
|      GravityAccelerationmeanY     |     tGravityAcc.mean...Y    |
|      GravityAccelerationmeanZ     |     tGravityAcc.mean...Z    |
|      GravityAccelerationstdX      |     tGravityAcc.std...X     |
|      GravityAccelerationstdY      |     tGravityAcc.std...Y     |
|      GravityAccelerationstdZ      |     tGravityAcc.std...Z     |
|     BodyAccelerationJerkmeanX     |    tBodyAccJerk.mean...X    |
|     BodyAccelerationJerkmeanY     |    tBodyAccJerk.mean...Y    |
|     BodyAccelerationJerkmeanZ     |    tBodyAccJerk.mean...Z    |
|      BodyAccelerationJerkstdX     |     tBodyAccJerk.std...X    |
|      BodyAccelerationJerkstdY     |     tBodyAccJerk.std...Y    |
|      BodyAccelerationJerkstdZ     |     tBodyAccJerk.std...Z    |
|         BodyGyroscopemeanX        |      tBodyGyro.mean...X     |
|         BodyGyroscopemeanY        |      tBodyGyro.mean...Y     |
|         BodyGyroscopemeanZ        |      tBodyGyro.mean...Z     |
|         BodyGyroscopestdX         |      tBodyGyro.std...X      |
|         BodyGyroscopestdY         |      tBodyGyro.std...Y      |
|         BodyGyroscopestdZ         |      tBodyGyro.std...Z      |
|       BodyGyroscopeJerkmeanX      |    tBodyGyroJerk.mean...X   |
|       BodyGyroscopeJerkmeanY      |    tBodyGyroJerk.mean...Y   |
|       BodyGyroscopeJerkmeanZ      |    tBodyGyroJerk.mean...Z   |
|       BodyGyroscopeJerkstdX       |    tBodyGyroJerk.std...X    |
|       BodyGyroscopeJerkstdY       |    tBodyGyroJerk.std...Y    |
|       BodyGyroscopeJerkstdZ       |    tBodyGyroJerk.std...Z    |
|   BodyAccelerationMagnitudemean   |      tBodyAccMag.mean..     |
|    BodyAccelerationMagnitudestd   |      tBodyAccMag.std..      |
|  GravityAccelerationMagnitudemean |    tGravityAccMag.mean..    |
|  GravityAccelerationMagnitudestd  |     tGravityAccMag.std..    |
| BodyAccelerationJerkMagnitudemean |    tBodyAccJerkMag.mean..   |
|  BodyAccelerationJerkMagnitudestd |    tBodyAccJerkMag.std..    |
|     BodyGyroscopeMagnitudemean    |     tBodyGyroMag.mean..     |
|     BodyGyroscopeMagnitudestd     |      tBodyGyroMag.std..     |
|   BodyGyroscopeJerkMagnitudemean  |   tBodyGyroJerkMag.mean..   |
|   BodyGyroscopeJerkMagnitudestd   |    tBodyGyroJerkMag.std..   |
|       BodyAccelerationmeanX       |      fBodyAcc.mean...X      |
|       BodyAccelerationmeanY       |      fBodyAcc.mean...Y      |
|       BodyAccelerationmeanZ       |      fBodyAcc.mean...Z      |
|        BodyAccelerationstdX       |       fBodyAcc.std...X      |
|        BodyAccelerationstdY       |       fBodyAcc.std...Y      |
|        BodyAccelerationstdZ       |       fBodyAcc.std...Z      |
|     BodyAccelerationJerkmeanX     |    fBodyAccJerk.mean...X    |
|     BodyAccelerationJerkmeanY     |    fBodyAccJerk.mean...Y    |
|     BodyAccelerationJerkmeanZ     |    fBodyAccJerk.mean...Z    |
|      BodyAccelerationJerkstdX     |     fBodyAccJerk.std...X    |
|      BodyAccelerationJerkstdY     |     fBodyAccJerk.std...Y    |
|      BodyAccelerationJerkstdZ     |     fBodyAccJerk.std...Z    |
|         BodyGyroscopemeanX        |      fBodyGyro.mean...X     |
|         BodyGyroscopemeanY        |      fBodyGyro.mean...Y     |
|         BodyGyroscopemeanZ        |      fBodyGyro.mean...Z     |
|         BodyGyroscopestdX         |      fBodyGyro.std...X      |
|         BodyGyroscopestdY         |      fBodyGyro.std...Y      |
|         BodyGyroscopestdZ         |      fBodyGyro.std...Z      |
|   BodyAccelerationMagnitudemean   |      fBodyAccMag.mean..     |
|    BodyAccelerationMagnitudestd   |      fBodyAccMag.std..      |
| BodyAccelerationJerkMagnitudemean |  fBodyBodyAccJerkMag.mean.. |
|  BodyAccelerationJerkMagnitudestd |  fBodyBodyAccJerkMag.std..  |
|     BodyGyroscopeMagnitudemean    |   fBodyBodyGyroMag.mean..   |
|     BodyGyroscopeMagnitudestd     |    fBodyBodyGyroMag.std..   |
|   BodyGyroscopeJerkMagnitudemean  | fBodyBodyGyroJerkMag.mean.. |
|   BodyGyroscopeJerkMagnitudestd   |  fBodyBodyGyroJerkMag.std.. |
|             subject_id            |                             |
|              activity             |                             |

**To read morea about data transformations please refer to the codebook**
