# Getting and Cleaning Data

* setwd("./data") - moves to /data in current directory
* setwd("../") - moves to upper directory
* setwd("C:/Users/Documents and settings/") - absolute path
* file.exists("directoryName") - checks if file exists
* dir.create("directoryName") - creates directory if it does not exist
* downloa.file() - download files
* if(!file.exists("./data")) dir.create("./data") - checks if file exists, if not creates it
* fileUrl <- "https://data.baltimorecity.gov/api/views/dz54-2aru/rows.csv?accessType=DOWNLOAD" - Baltimore cameras data
* download.file(fileUrl, destfile = "destinationDir") - downloads data from url to destination directory
* dateDownloaded <- date() - alsways save the date of downloading the file
* install.packages("xlsx") - install library to load xlsx files
* library(xlsl) - library to read Excel files
* read.xlsx("./CourseIII/data/cameras.xlsx", sheetIndex = 1, header = TRUE) - reads in xlsx files
* write.xlsx - writes down xlsx files