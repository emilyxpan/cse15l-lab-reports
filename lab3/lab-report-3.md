# Lab Report 3
## find -name
**Example 1**
```
(base) MacBook-Pro-172:technical emilypan$ find 911report -name chapter-1.txt
911report/chapter-1.txt
```
This command searches for a file called "chapter-1.txt" in the /911report directory.
**Example 2**
```
(base) MacBook-Pro-172:technical emilypan$ find government -name commission_report.txt
government/About_LSC/commission_report.txt
```
This command searches for a file called "comission_report.txt" in the /government directory. Note that it's still able to find the file even though the file is in a subdirectory called /About_LSC within the /government directory.
**Example 3**
```
(base) MacBook-Pro-172:technical emilypan$ find government/Media -name Annual_Fee.txt
government/Media/Annual_Fee.txt
```
This command searches for a file called "Annual_Fee.txt" in the /government/Media directory. This allows you to search for a file that's not directly in the specified directory, but is nested within subdirectories.
## find -path pattern
**Example 1**
**Example 2**
**Example 3**
## find -links n
**Example 1**
**Example 2**
**Example 3**