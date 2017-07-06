# Assignment-7-collaboration-on-repository-and-data-cleanup
# Remove special characters, padding from Street 1 and Street 2 variables,etc.
DataClean<-read.csv("~/Downloads/DataClean.csv")
clean<-read.csv("~/Downloads/DataClean.csv")
View(clean)
clean$Street <- gsub("[^A-Za-z ]", " ", clean$Street)
clean$Street <- gsub("(?<=[\\s])\\s*|^\\s+|\\s+$", "", clean$Street, perl=TRUE)


clean$Street.2 <- gsub("[^A-Za-z ]", " ", clean$Street.2)
clean$Street.2 <- gsub("(?<=[\\s])\\s*|^\\s+|\\s+$", "", clean$Street.2, perl=TRUE)
View(clean)
