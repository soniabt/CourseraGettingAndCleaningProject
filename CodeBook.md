---
title: 'Codebook: Activity Recognition (tidy dataset)'
output: html_document
---

# Data Source    
Human Activity Recognition Using Smartphones Dataset      
Published reference:    
[1] Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz.     
Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine.  International Workshop of Ambient Assisted Living (IWAAL 2012).  Vitoria-Gasteiz, Spain. Dec 2012    
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 

# Variables of Subsetted Data

The Human Activity Recognition Using Smartphones Dataset are subesetted to include only the mean and standard deviation data (already pre-processed from the research team).  The final processed data presented here include the means of these variables for each subject (1-30) and one of six activities (laying, sitting, standing, walking, walkingdownstairs, walkingupstairs).

Other than the variables subject and activity, the list of variables are referred to as "features" in the original work -  561 variables and 10299 observations divided into "training" and "test" data.  The authors of the publication describe the features of the smartphones from which the data are collected:  acelerometer and gyroscope which provide 3-axial raw signals tAcc-XYZ, tGyro-XYZ, ..., where "t" denotes time.  The data are then filtered and separated into body and gravity acceleration signals (prefixed with "t" or "f" e.g. tBodyAcc-XYZ, tGravityAcc-XYZ).  Body linear acceleration and angular velocity were derived in time to obtain Jerk signals (Jerk or GyroJerk).  The Magnitude of these 3-D signals were calculated (eg. tBodyAccMag).  Finally, a Fast Fourier Transform was applied to the signals.  The variable names were then prepended with an "f" to denote the FFT processing.   (Refer to publication [1] and website for details.)  

The post-processing conducted to prepare this dataset includes merging the training and test datasets, extracting the variables already processed as mean and standard deviation values (designated mean() or std()  e.g. tBodyAcc-mean()-X).  The final tidy dataset retains only the average of each variable for each activity and each subject.   

Variables of the tidy dataset are averages of each standard deviation and mean variables.   
Each row  identifies the subject (1-30) and the activity performed by the subject with values of the feature measurements standardized between [-1,1].  The naming convention matches the original naming convention:  t-time domain; f-FFT domain; etc.    
* subject   
* activity   
* tbodyaccmeanx   
* tbodyaccmeany   
* tbodyaccmeanz   
* tgravityaccmeanx   
* tgravityaccmeany   
* tgravityaccmeanz   
* tbodyaccjerkmeanx     
* tbodyaccjerkmeany    
* tbodyaccjerkmeanz    
* tbodygyromeanx     
* tbodygyromeany    
* tbodygyromeanz    
* tbodygyrojerkmeanx      
* tbodygyrojerkmeany    
* tbodygyrojerkmeanz    
* tbodyaccmagmean    
* tgravityaccmagmean    
* tbodyaccjerkmagmean    
* tbodygyromagmean    
* tbodygyrojerkmagmean    
* fbodyaccmeanx    
* fbodyaccmeany     
* fbodyaccmeanz    
* fbodyaccjerkmeanx   
* bodyaccjerkmeany   
* fbodyaccjerkmeanz    
* fbodygyromeanx    
* fbodygyromeany    
* fbodygyromeanz    
* fbodyaccmagmean     
* fbodybodyaccjerkmagmean    
* fbodybodygyromagmean   
* fbodybodygyrojerkmagmean   
* tbodyaccstdx   
* tbodyaccstdy   
* tbodyaccstdz   
* tgravityaccstdx   
* tgravityaccstdy    
* tgravityaccstdz    
* tbodyaccjerkstdx    
* tbodyaccjerkstdy    
* tbodyaccjerkstdz    
* tbodygyrostdx   
* tbodygyrostdy    
* tbodygyrostdz    
* tbodygyrojerkstdx    
* tbodygyrojerkstdy    
* tbodygyrojerkstdz   
* tbodyaccmagstd    
* tgravityaccmagstd   
* tbodyaccjerkmagstd    
* tbodygyromagstd    
* tbodygyrojerkmagstd    
* fbodyaccstdx    
* fbodyaccstdy    
* fbodyaccstdz    
* fbodyaccjerkstdx    
* fbodyaccjerkstdy    
* fbodyaccjerkstdz    
* fbodygyrostdx    
* fbodygyrostdy    
* fbodygyrostdz    
* fbodyaccmagstd    
* fbodybodyaccjerkmagstd    
* fbodybodygyromagstd    
* fbodybodygyrojerkmagstd   



Refer to published paper [1], website or activityregognition@smartlab.ws for more detailed information about the original research and datasets.

```{r, include=FALSE}
   # add this chunk to end of mycode.rmd
   file.rename(from="Codebook.Rmd", 
               to="CodeBook.md")
```