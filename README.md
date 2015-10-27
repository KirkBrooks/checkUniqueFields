# checkUniqueFields
Method for checking a v13+ 4D database for any fields designated as unique that have duplicate records. 

Here's a method I made to check unique fields in v13 databases in prep for converting to version 14 or 15. v13 will tolerate existing duplicates in a unique field. The newer versions will simply refuse to open the datafile so be sure to fix this in the v13 version. 

The method **4D_find_uniqueFieldsWithDupes** checks all the fields of your database and steps through all records in unique fields. If any dupes are found they are reported at the end of the run. 

Just copy the methods to your database to run. The 4D_alert component is an alternative to the regular ALERT command and is nice for displaying large text varables. It also allows you to copy the contents directly. If you prefer not to use it simply modify the method to return the text report. 
