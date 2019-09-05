# clean_data_course_project
Course project for "Getting and Cleaning Data" Coursera course

# Overview

The objective for this project was to extract, clean, and work with data to make it tidy.  The data used for this project is data collected from Samsung Galaxy S smartphones in an experiment with 30 participants doing 6 activities (walking, walking upstairs, walking downstairs, sitting, standing, and laying).  A full description of the data is available at the site it was obtained from here:

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

The data used for this project is located here:

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

# How The Script Works

In this repository is a file called run_analysis.R.  This file contains the R code to convert the data into a tidy data set containing the average readings of each variable for each subject and each activity.  I will run over what I did to the data below in addition to the notes in the run_analysis.R file.

Step 1.  Downloading the Data

The assignment stated to build a function which would read the data assuming it was in the working directory.  I added this step to make the source code a "one-stop shop" for anyone who wanted to look at the data.  An if function checks to see if the zip file is located in the working directory.  If it is there, the code moves on to the next step.  If not, it downloads the file according the the url in the overview and unzips the file into a folder named "UCI HAR Dataset".

Step 2.  Reading the Data Tables into R

The six data tables are located in the "UCI HAR Dataset" file in the "test" and "train" folders.  The files are X_test, y_test, and subject_test with the train folders containing the same files only with "train" replacing "test".  X contains the data readings from the smartphones, y contains the activity being performed, and subject contains the subject who performed the activity.  These files were all loaded via the read.table function.

Step 3.  Assign Column Names

In all honesty, this step could've been done later, but for the sake of me being able to keeping the data straight, I did it here.
