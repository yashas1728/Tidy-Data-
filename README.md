# TidyData
Extracting Tidy data (Getting and cleaning data Coursera)


Coursera Getting and Cleaning Data course project

System Info (exectuting the script on my machine)

R version 4.1.2 (2021-11-01)
Platform: x86_64-w64-mingw32/x64 (64-bit)
Running under: Windows 11 x64 (build 22000)

Matrix products: default

locale:
[1] LC_COLLATE=English_United States.1252  LC_CTYPE=English_United States.1252   
[3] LC_MONETARY=English_United States.1252 LC_NUMERIC=C                          
[5] LC_TIME=English_United States.1252    
system code page: 65001

attached base packages:
[1] stats     graphics  grDevices utils     datasets  methods   base     

other attached packages:
[1] dplyr_1.0.8

loaded via a namespace (and not attached):
 [1] rstudioapi_0.13  knitr_1.38       magrittr_2.0.3   tidyselect_1.1.1 R6_2.5.1        
 [6] rlang_1.0.1      fastmap_1.1.0    fansi_1.0.2      tools_4.1.2      xfun_0.30       
[11] utf8_1.2.2       cli_3.1.1        DBI_1.1.2        htmltools_0.5.2  ellipsis_0.3.2  
[16] yaml_2.2.2       digest_0.6.29    assertthat_0.2.1 tibble_3.1.6     lifecycle_1.0.1 
[21] crayon_1.4.2     purrr_0.3.4      vctrs_0.3.8      glue_1.6.1       evaluate_0.15   
[26] rmarkdown_2.13   compiler_4.1.2   pillar_1.7.0     generics_0.1.2   pkgconfig_2.0.3 



One of the most exciting areas in all of data science right now is wearable computing - see for example this article. Companies like Fitbit, Nike, and Jawbone Up are racing to develop the most advanced algorithms to attract new users.

In this project, data collected from the accelerometer and gyroscope of the Samsung Galaxy S smartphone was retrieved, worked with, and cleaned, to prepare a tidy data that can be used for later analysis.

This repository contains the following files:

README.md, this file, which provides an overview of the data set and how it was created. tidy_data.txt, which contains the data set. CodeBook.md, the code book, which describes the contents of the data set (data, variables and transformations used to generate the data). run_analysis.R, the R script that was used to create the data set (see the Creating the data set section below) Study design

The source data set that this project was based on was obtained from the Human Activity Recognition Using Smartphones Data Set, which describes how the data was initially collected as follows:

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. Training and test data were first merged together to create one data set, then the measurements on the mean and standard deviation were extracted for each measurement (79 variables extracted from the original 561), and then the measurements were averaged for each subject and activity, resulting in the final data set.

Creating the data set

The R script run_analysis.R can be used to create the data set. It retrieves the source data set and transforms it to produce the final data set by implementing the following steps (see the Code book for details, as well as the comments in the script itself):

Download and unzip source data if it doesn't exist. Read data. Merge the training and the test sets to create one data set. Extract only the measurements on the mean and standard deviation for each measurement. Use descriptive activity names to name the activities in the data set. Appropriately label the data set with descriptive variable names. Create a second, independent tidy set with the average of each variable for each activity and each subject. Write the data set to the tidy_data.txt file. The tidy_data.txt in this repository was created by running the run_analysis.R script using R version 3.2.2 (2015-08-14) on Windows 8.1 64-bit edition.

This script requires the dplyr package (version 0.4.3 was used).