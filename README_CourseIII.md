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
## XLSX
* install.packages("xlsx") - install library to load xlsx files
* library(xlsl) - library to read Excel files
* read.xlsx("./CourseIII/data/cameras.xlsx", sheetIndex = 1, header = TRUE) - reads in xlsx files
* write.xlsx - writes down xlsx files
* download.file(fileUrl, destfile = "./data/cameras2.xlsx", mode = "wb") - add mode="wb" in order to have not corrupted xls files
## XML
* fileUrl <- "http://www.w3schools.com/xml/simple.xml" - url to xml file
* doc <- xmlTreeParse(fileUrl, useInternalNodes = TRUE) - parses xml file
* rootNode <- xmlRoot(doc) - wrapper element for entire structure
* xmlName(rootNode) - gets name of the root node
* names(rootNode)
* rootNode[[1]] - access first component of the root node
* rootNode[[1]][[1]] - access first component of first component
* xmlSApply(rootNode, xmlValue) - gets values of all xml variables
* xpathSApply(rootNode, "//name",xmlValue) - more convenient way of getting values
##JSON
* library(jsonlite)
* jsonData <- fromJSON("https://api.github.com/users/jtleek/repos") - downloads data in json format
* myjson <- toJSON(dataset, pretty=TRUE) - converts data set to JSON format
* dataset2 <- fromJSON(myjson) - converts json formatted data to dataframe
##Data tables
* data.table() - creates data table
* tables() - shows table in memory
* DT[, list(mean(x))] <- calculates mean of x columns i data table DT
* DT[,w:=z^2] - adds new column to data table
* DT[, .N, by=x] - groups by x with respect to number of elements
* setkey(x, DT) - sets key of DT to be x, works like in primary key in sql
* merge(DT1, DT2) - merges two data frames
* file <- tempfile() - sets up a temporary file
* fread(file) - reads files much faster than read.table()
## dplyr
* library("dplyr")
* tbl_df(df) <- creates "data frame tbl" (object from dplyr package) from a data frame. 
* rm("variable") <- removes variavle from workspace
* select(), filter(), arrange(), mutate(), summarize() - core functions of dplyr package
* select(obj, col1, col2, ...) - selects columns
* select(obj, col1: col5) - also selects columns
* select(obj, -(col1:col4)) - omits columns from col1 to col4
* filter(obj, col1=="value", col2=="value2") - selects rows with value "value" in col1 and "value2" in col2
* filter(obj, col1=="value" | col1=="value2") - selects rows with value "value" in col1 and "value2" in col1
* filter(obj, !is.na(col)) - selects values in col which are not NA
* arrange(obj, col) - arrange data from obj in ascending order according to col
* group_by(obj, col) <- groups data by col, any applied operation will take place on groups of data
* arrange(obj, desc(col)) - arrange data from obj in descending order according to col
* mutate(obj, newcol = col1+col2) - createsa new column which is a sum of col1 and col2, it can be any other operation
* summarize(obj, count = n(), unique = n_distinct(col1), countries = n_distinct(col2), avg_bytes = mean(col3)) - summarizes tbf, creates cols with countes, unique counts, unique counts, and average for each group if obj is grouped
* quantile(obj$col, probs = 0.99) - selects 0.99 sampl equantile of obj according to col
* View(obj) - views all the data, creates w new workbook with tables!
* %>%  - chaining operator in dplyr, sends left side to right side as an argument
## MySQL
* database <- dbConnect(MySQL(), user="genome", host="genome-mysql.cse.ucsc.edu") - connects with a database server with multiple databases
* result <- dbGetQuery(ucscDb,"showdatabases;"); dbDisconnect(uscDb); - sends a query to database and closes the connection, always do that
* hg19 <- dbConnect(MySQL(), user="genome", db="hg19", host="genome-mysql.cse.ucsc.edu") - connects with a specific databse
* allTalbes <- dbListTables(hg19) - lists tables in hg19 database
* length(allTables) - prints the nimber of tables
* dbListFields(hg19, "affyU133Plus2") - lists fields in table affy...
* dbGetQuery(hg19, "select count(*) from affyU133Plus2") - sends a query to database
* affyData <- dbReadTable(hg19, "affyU133Plus2") - reads databse table
* query <- dbSendQuery(hg19, "select * from affyU133Plus2 where misMatches between 1 and 3") - sends a more complicated query
* fetch(query) - executes query
* affyMisSmall <- fetch(query, n=10); dbClearResult(query) - sends a query and clears query, must do this
* dbDisconnect(hg19) - closes the connection
## HDF5
* source("http://bioconductor.org/biocLite.R") - containts hdf5 package
* biocLite("rhdf5") - installs package
* library(rhdf5) - loads package
* created = h5createFile("file.h5") - creates hdf5 file, created checks if operation works
* created = h5createGroup("example.h5", "foo") - creates group
* created = h5createGroup("example.h5", "baa") - creates group
* created = h5createGroup("example.h5", "foo/foobaa") - creates subgroup
* h5ls("file.h5") - list content of h5 file
* h5write(elem, "file.h5", "group") - writes elem into the specific group of h5 file
* h5read("file.h5", "group/data") - reads data from h5 file from a specific group
* h5write(c(12,13,14), "example.h5", "foo/A", index=list(1:3,1)) - writes data in chunks, works the same with read
## Reading from web, webscraping
* con <- url("http://...") - open a connection to url
* htmlCode <- readLines(con) - read html code
* clones(con) - closes connection
* library(httr) - package for reading from html
* html2 <- GET(url) - gets the url
* content2 <- content(html2, as="text") - reads content of page
* parsedhtml <- htmlParse(content2, asTest=TRUE) - parsees webpage
* xpathSApply(parsedhtml, "//title", xmlValue) - gets specific elements from web
* google <- handle("http://google.com") - when handlig don't have to authenticate every time
## tidyr
* library(tidyr)
* gather(data, col1, col2, newcol, -col) - collapses columns
* separate(data=res, col=sex_class, into = c("sex", "class")) - separates columns
* students2 %>% gather( sex_class, count, -grade) %>% separate(sex_class ,c("sex", "class")) %>% print - example of chaining
* select(data, -contains("text")) - select all columns without those with "text" string
* library(lubridate)
* today() - prints date in y m d format
* now() - pints date and h m s
* ymd(), dmy(), ymd_hms(), ... - functions to parse data
* update(depart, hours=17, minutes=34) - updates date