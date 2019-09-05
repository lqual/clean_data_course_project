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

The six data tables are located in the "UCI HAR Dataset" file in the "test" and "train" folders.  The files are "X_test", "y_test", and "subject_test" with the train folders containing the same files only with "train" replacing "test".  "X" contains the data readings from the smartphones, "y" contains the activity being performed, and "subject" contains the subject who performed the activity.  These files were all loaded via the read.table function.

Step 3.  Assign Column Names

In all honesty, this step could've been done later, but for the sake of me being able to keeping the data straight, I did it here.  The column names for the "X_test" and "X_train" files were located in the "UCI HAR Dataset" folder in the "features.txt" file.  I read them into R using read.table and pulled out the column names which were located in the second column of the dataframe.  I then assigned these as the names for both X_test and X_train columns.  For y_test and y_train, I assigned the column name as "activity std()", and for the subject_test and subject_train, I assigned the column name as "subject std()".  Note: I added "std ()" to the end of the column names to make it easier (for me at least) to keep the columns in place down the road when I got rid of the columns which didn't contain mean or std.

Step 4.  Combine Dataframes Into One

Cbind the test variables together (subject, activity, and readings) and did the same for the train variables.  Then rbind the two new dataframes together to create one dataframe.

Step 5.  Remove Column Variables Which Don't Contain Mean or Std

I built a dataframe with 4 columns.  The first column was a numeric vector from 1:563 (563 is the total number of columns in the large dataframe) to hold the location of the columns.  The second column was an integer vector which was the number 1 if "mean" was located in that column name and 0 if it wasn't.  The third column was an integer vector which was the number 1 if "std" was located in that column name and 0 if it wasn't.  The fourth column was the sum of the mean and std columns.  This resulted in the fourth column equalling 1 if it contained a mean or std reading and a 0 if it didn't.  I then subsetted out the 0's, and used the first column in the dataframe which contained the location of the columns to subset out the column variables in the large dataframe which weren't a reading of mean or std.  By adding the std to the activity and subject variables, this kept those columns from being removed.

Step 6.  Descriptive Column Names

This step should come after step 7 according to the assignment, but I did it first to make the coding less wordy for step 7.  I renamed the initial two columns to "subject" and "activity" (getting rid of the "std()").  Then I changed all "f"'s and "t"'s at the beginning of any column names to "freq" and "time" respectively to make the names more descriptive.  Then I removed all parentheses in any column name and replaced "-" with "." (some people view "." as cleaner than any other symbol).  I didn't make any other changes to the column names because although they may still be confusing to look at, they are descriptive of the data collected and didn't want to make things anymore confusing.

Step 7.  Changing Activity Variable from Numbers to Description

I made a vector of the activity column data to find the length of the column and created a new character vector of the activity names.  Then I made a for loop which went through every value in the vector, determined what the descriptive name should be for that particular instance (1 == "walking, 2 == "walk_upstairs", 3 == "walk_downstairs", 4 == "sitting", 5 == "standing", and 6 == "laying") and assigning that value to the same place in the new character vector.  Then I reassigned the variables in the activity column to be the newly made character vector.
