Course Project Code Book
========================

The original data is here: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

The orginal description is here: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

The attached R script run_analysis.R cleans up the data by:

* Merges the training and test sets to create one data set (train/X_train.txt and test/X_test.txt) the result is a 10299x561 data frame - 10299 instances and 561 attributes.

* Extracts othe measurements on the mean and standard deviation for each measurement.  After reading reading features.txt the result is a 10299x66 data frame - 66 out of 561 attributes are measurements. 

* Applies descriptive activity names to name the activities in the data set. These activities include: walking, walkingupstairs, walkingdownstairs, sitting, standing, and laying

* The script also labels the data set with descriptive names - activity labels and subject IDs.  This is saved as merged_clean_data.txt - the first column contains subject IDs, the second column activity names, and the last 66 columns are measurements. Subject IDs are integers between 1 and 30. The names of the attributes are similar to the following: tbodyacc-mean-x, tbodyacc-mean-y, tbodyacc-mean-z, tbodyacc-std-x, tgravityacc-mean-x, etc.

* The script creates a second independent tidy data set with the average of each measurement for each activity and each subject. The result is saved as data_with_averages.txt, a 180x68 data frame - There are 30 subjects and 6 activities, so we get 180 rows in this data set with averages.
