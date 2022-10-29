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
## find -iname
**Example 1**
```
(base) MacBook-Pro-172:technical emilypan$ find government -iname proGRESS_report.txt
government/About_LSC/Progress_report.txt
```
This command finds files using name while ignoring case. For this example, the command searches for a file called "proGRESS_report.txt" (case does NOT matter) in the /government directory.

**Example 2**
```
(base) MacBook-Pro-172:technical emilypan$ find government -iname config_standards.txt
government/About_LSC/CONFIG_STANDARDS.txt
```
This command searches for a file called "config_standards.txt" (case does NOT matter) in the /government directory.

**Example 3**
```
(base) MacBook-Pro-172:technical emilypan$ find government -iname CONFIG_STANDARDS.txt
government/About_LSC/CONFIG_STANDARDS.txt
```
This command searches for a file called "CONFIG_STANDARDS.txt" (case does NOT matter) in the /government directory.
## find -type d
**Example 1**
```
(base) MacBook-Pro-172:technical emilypan$ find government -type d
government
government/About_LSC
government/Env_Prot_Agen
government/Alcohol_Problems
government/Gen_Account_Office
government/Post_Rate_Comm
government/Media
```
This command finds all directories in the /government directory.

**Example 2**
```
(base) MacBook-Pro-172:technical emilypan$ find government -type d -name About_LSC
government/About_LSC
```
This command finds a directory named "About_LSC" in the /government directory.

**Example 3**
```
(base) MacBook-Pro-172:technical emilypan$ find biomed -type d
biomed
```
This command finds all directories in the /biomed directory, and since /biomed has no subdirectories, the command just returns biomed itself.