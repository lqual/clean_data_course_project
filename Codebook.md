# Codebook

# Acknowledgements

This codebook builds off the original codebook in the dataset (https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip, file name = features_info.txt).

# Feature Selection

The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 

Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag). 

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals). 

These signals were used to estimate variables of the feature vector for each pattern:  
'-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.

# Variables and Meanings

"subject": subject id number ranging from 1:30 

"activity": 1 of 6 activities including walking, walk_upstairs, walk_downstairs, standing, sitting, and laying

"timeBodyAcc.mean.X"

"timeBodyAcc.mean.Y"

"timeBodyAcc.mean.Z"

"timeBodyAcc.std.X"

"timeBodyAcc.std.Y"

"timeBodyAcc.std.Z"

The above variables are the average and standard deviation time readings of the body acceleration signals.  The values in the table are the average for the subject and activity.

"timeGravityAcc.mean.X"

"timeGravityAcc.mean.Y"

"timeGravityAcc.mean.Z"

"timeGravityAcc.std.X"

"timeGravityAcc.std.Y"

"timeGravityAcc.std.Z"

The above variables are the average and standard deviation time readings of the gravity acceleration signals.  The values in the table are the average for the subject and activity.

"timeBodyAccJerk.mean.X"

"timeBodyAccJerk.mean.Y"

"timeBodyAccJerk.mean.Z"

"timeBodyAccJerk.std.X"

"timeBodyAccJerk.std.Y"

"timeBodyAccJerk.std.Z"

The above variables are the average and standard deviation time readings of the body acceleration Jerk signals.  The values in the table are the average for the subject and activity.

"timeBodyGyro.mean.X"

"timeBodyGyro.mean.Y"

"timeBodyGyro.mean.Z"

"timeBodyGyro.std.X"

"timeBodyGyro.std.Y"

"timeBodyGyro.std.Z"

The above variables are the average and standard deviation time readings of the body angular velocity signals.  The values in the table are the average for the subject and activity.

"timeBodyGyroJerk.mean.X"

"timeBodyGyroJerk.mean.Y"

"timeBodyGyroJerk.mean.Z"

"timeBodyGyroJerk.std.X"

"timeBodyGyroJerk.std.Y"

"timeBodyGyroJerk.std.Z"

The above variables are the average and standard deviation time readings of the body angular velocity Jerk signals.  The values in the table are the average for the subject and activity.

"timeBodyAccMag.mean"

"timeBodyAccMag.std"

The above variables are the average and standard deviation time readings of the magnitude of the body acceleration signals.  The values in the table are the average for the subject and activity.

"timeGravityAccMag.mean"

"timeGravityAccMag.std"

The above variables are the average and standard deviation time readings of the magnitude of the gravity acceleration signals.  The values in the table are the average for the subject and activity.

"timeBodyAccJerkMag.mean"

"timeBodyAccJerkMag.std"

The above variables are the average and standard deviation time readings of the body acceleration Jerk signals.  The values in the table are the average for the subject and activity.

"timeBodyGyroMag.mean"

"timeBodyGyroMag.std"

The above variables are the average and standard deviation time readings of the magnitude of the body angular velocity signals.  The values in the table are the average for the subject and activity.

"timeBodyGyroJerkMag.mean"

"timeBodyGyroJerkMag.std"

The above variables are the average and standard deviation time readings of the magnitude of the body angular velocity Jerk signals.  The values in the table are the average for the subject and activity.

"freqBodyAcc.mean.X"

"freqBodyAcc.mean.Y"

"freqBodyAcc.mean.Z"

"freqBodyAcc.std.X"

"freqBodyAcc.std.Y"

"freqBodyAcc.std.Z"

The above variables are the average and standard deviation frequency readings of the body acceleration signals.  The values in the table are the average for the subject and activity.

"freqBodyAcc.meanFreq.X"

"freqBodyAcc.meanFreq.Y"

"freqBodyAcc.meanFreq.Z"

The above variables are the average frequency readings of the body acceleration signals for each occurence.  The values in the table are the average for the subject and activity.

"freqBodyAccJerk.mean.X"

"freqBodyAccJerk.mean.Y"

"freqBodyAccJerk.mean.Z"

"freqBodyAccJerk.std.X"

"freqBodyAccJerk.std.Y"

"freqBodyAccJerk.std.Z"

The above variables are the average and standard deviation frequency readings of the body acceleration Jerk signals.  The values in the table are the average for the subject and activity.

"freqBodyAccJerk.meanFreq.X"

"freqBodyAccJerk.meanFreq.Y"

"freqBodyAccJerk.meanFreq.Z"

The above variables are the average frequency readings of the body acceleration Jerk signals for each occurence.  The values in the table are the average for the subject and activity.

"freqBodyGyro.mean.X"

"freqBodyGyro.mean.Y"

"freqBodyGyro.mean.Z"

"freqBodyGyro.std.X"

"freqBodyGyro.std.Y"

"freqBodyGyro.std.Z"

The above variables are the average and standard deviation frequency readings of the body angular velocity signals.  The values in the table are the average for the subject and activity.

"freqBodyGyro.meanFreq.X"

"freqBodyGyro.meanFreq.Y"

"freqBodyGyro.meanFreq.Z"

The above variables are the average frequency readings of the body angular velocity signals for each occurence.  The values in the table are the average for the subject and activity.

"freqBodyAccMag.mean"

"freqBodyAccMag.std"

"freqBodyAccMag.meanFreq"

The above variables are the average and standard deviation frequency readings of the magnitude of the body acceleration signals (over each occurence for the meanFreq).  The values in the table are the average for the subject and activity.

"freqBodyBodyAccJerkMag.mean"

"freqBodyBodyAccJerkMag.std"

"freqBodyBodyAccJerkMag.meanFreq"

The above variables are the average and standard deviation frequency readings of the magnitude of the body acceleration Jerk signals (over each occurence for the meanFreq).  The values in the table are the average for the subject and activity.

"freqBodyBodyGyroMag.mean"

"freqBodyBodyGyroMag.std"

"freqBodyBodyGyroMag.meanFreq"

The above variables are the average and standard deviation frequency readings of the magnitude of the body angular velocity signals (over each occurence for the meanFreq).  The values in the table are the average for the subject and activity.

"freqBodyBodyGyroJerkMag.mean"

"freqBodyBodyGyroJerkMag.std"

"freqBodyBodyGyroJerkMag.meanFreq"

The above variables are the average and standard deviation frequency readings of the magnitude of the body angular velocity Jerk signals (over each occurence for the meanFreq).  The values in the table are the average for the subject and activity.
