# ProjectForGettingAndCleaningData
These files are related to the Coursera Course entitled Getting and Cleaning Data, provided by Johns Hopkins University. 

Required input files are the following:
   X_test.txt
   X_train.txt
   y_test.txt
   y_train.txt
   subject_train.txt
   subject_test.txt
   features.txt
   activity_labels.txt

Output files produced are the following:
   tidydata.txt
   proj-cleaningdata-finaldataframe.txt

This R source code assumes that all necessary data files are in the working directory.  

This R source code takes refined data (NOT the originally raw data from the experiment derived from the phones) for both text and training subjects (the X files), and merges those files together into one dataframe. Of the 561 columns of data available, it removes all the data columns except for the 86 columns that contain the text string "mean", "Mean", or "std" (short for standard deviation) in their names. The code also assigns names to the columns, based on the names in the features.txt file. It is assumed that the order found in the features.txt file is the same as found in the X data files.  In addition, this source code assigns individual subject codes based on the codes in the subject_train.txt and subject_test.txt files. The source code then assigns activity descriptions for each activity based on the assignment codes found in the activity_labels.txt file. 

Once the output file  proj-cleaningdata-finaldataframe.txt is produced, the code then attempts to calculate a mean for each of the column values for each subject, for each activity. It outputs that "tidy" data set into the tidydata.txt file.
