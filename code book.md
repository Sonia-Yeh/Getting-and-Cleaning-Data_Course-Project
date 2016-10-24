# Getting and Cleaning Data Course Project

## Data Source
The data for the project is downloaded from
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

A full data description is at
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

## Introduction of variables
- `x_train`, `y_train`, `subject_train`: the train data from the downloaded files
- `x_test`, `y_test`, `subject_test`: the test data from the downloaded files
- `features`: names of all measurements
- `activityName`: the data set linking the class labels with their activity name.

## `run_analysis.R` Introduction of the code submitted
1. Merges the training and the test sets to create one data set.
  - 1.1 Download zip file and Unzip files
  - 1.2 Read training, test, features and activity_labels data
  - 1.3 Merge train and test data
2. Extracts only the measurements on the mean and standard deviation for each measurement
  - use `grep()`to find the indexes with measurements on the mean and standard deviation
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive variable names
  - use `gsub()` to replace the variable names with appropriate labels
5. creates a second, independent tidy data set `TidyMeanData.txt` with the average of each variable for each activity and each subject
  - use `group_by()` and `summarise_each()` in `library(dplyr)` to calculate the average of each variable for each activity and each subject 


