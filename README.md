Getting And Cleaning Data - 'run_analysis.R' script and data transformation
===================

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
The data linked to from the course website represent data collected from the accelerometers from the Samsung Galaxy S smartphone. A full description is available at the site where the data was obtained: 

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones 

Data for the project was obtained from the follwoing link:

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 



**To read morea about data transformations please refer to the codebook**
