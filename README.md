---
title: "README"
output: html_document
---

# Getting and Cleaning Data: Course Project Week 3   


Create a tidy dataset from activity recognition observations obtained from wearable computing devices.    
Published reference for research and dataset:    
Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. 
Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support 
Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). 
Vitoria-Gasteiz, Spain. Dec 2012      

run_analysis.R - R script to download, merge and clean data     
* download file from URL and unzip if data are not already available    
* read in datasets, subject id, activity id's and names, and variable names (features) from text files (using read.table())    
* merge training and test files together     
* remove underscores and make activities all lowercase, then replace activity id's with activity names    
* bind subject id's and activity names to corresponding data    
* extract only -mean() and -std() variables      
* create a first version of the tidy dataset by averaging each variable for each activity and each subject using group\_by() and summarise\_each()    
* remove dashes and lower case variable names (features) to finalize the tidy dataset
* write the tidy dataset as a text file to be uploaded for review     

```{r, include=FALSE}
   # add this chunk to end of mycode.rmd
   file.rename(from="README.Rmd", 
               to="README.md")
```
# CourseraGettingAndCleaningProject
