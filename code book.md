# Getting and Cleaning Data Course Project

## Data Source
The original data is downloaded from
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

## R script `run_analysis.R` introduction
1. Merges the training and the test sets to create one data set.
  1.1 Download zip file and Unzip files
  1.2 Read training, test, features and activity_labels data
  1.3 Merge train and test data
2. Extracts only the measurements on the mean and standard deviation for each measurement
  - use `grep()`to find the indexes with measurements on the mean and standard deviation
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive variable names
  - use `gsub()` to replace the variable names with appropriate labels
5. creates a second, independent tidy data set `TidyMeanData.txt` with the average of each variable for each activity and each subject.

## Introduction of data sets
- `X_train.txt`: Training data set
- `y_train.txt`: Training labels
- `X_test.txt`: Test data set
- `y_test.txt`: Test labels
- `subject_train.txt`: Each row identifies the subject who performed the activity for each window sample.
- `features.txt`: List of all features.
- `activity_labels.txt`: Links the class labels with their activity name.
