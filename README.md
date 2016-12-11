Last login: Tue Nov 29 18:44:30 on console
MacBook-Pro:~ chenthilramasamy$ cd Coursera/
  MacBook-Pro:Coursera chenthilramasamy$ ls
Complete.R	corr.R		pollutantmean.R	week4
cachematrix.R	data.csv	specdata
MacBook-Pro:Coursera chenthilramasamy$ ls -ltr
total 8328
drwxr-xr-x@ 334 chenthilramasamy  staff    11356 Sep 21  2012 specdata
-rw-r--r--@   1 chenthilramasamy  staff      367 Oct 28 17:57 pollutantmean.R
-rw-r--r--@   1 chenthilramasamy  staff      806 Oct 28 18:07 corr.R
-rw-r--r--@   1 chenthilramasamy  staff      279 Oct 31 21:54 Complete.R
-rwxr-xr-x@   1 chenthilramasamy  staff     2188 Nov  5 14:08 cachematrix.R
-rw-r--r--    1 chenthilramasamy  staff  4246554 Nov 17 10:42 data.csv
drwx------@   9 chenthilramasamy  staff      306 Dec  8 14:58 week4
MacBook-Pro:Coursera chenthilramasamy$ cd week4/
  MacBook-Pro:week4 chenthilramasamy$ ls -ltr
total 122184
-rw-r--r--@ 1 chenthilramasamy  staff  62556944 Dec  8 14:32 getdata%2Fprojectfiles%2FUCI HAR Dataset.zip
drwxr-xr-x@ 9 chenthilramasamy  staff       306 Dec  8 14:58 UCI HAR Dataset
MacBook-Pro:week4 chenthilramasamy$ cd UCI\ HAR\ Dataset/
  MacBook-Pro:UCI HAR Dataset chenthilramasamy$ ls -ltr
total 64
-rwxr-xr-x@ 1 chenthilramasamy  staff     80 Oct 10  2012 activity_labels.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff  15785 Oct 11  2012 features.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff   2809 Oct 15  2012 features_info.txt
drwxr-xr-x@ 6 chenthilramasamy  staff    204 Nov 29  2012 test
drwxr-xr-x@ 6 chenthilramasamy  staff    204 Nov 29  2012 train
-rwxr-xr-x@ 1 chenthilramasamy  staff   4453 Dec 10  2012 README.txt
drwxr-xr-x  3 chenthilramasamy  staff    102 Dec  8 14:58 week4
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ vi CodeBook.md
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
  MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
  MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
  MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
  MacBook-Pro:UCI HAR Dataset chenthilramasamy$ ls -ltr
total 80
-rwxr-xr-x@ 1 chenthilramasamy  staff     80 Oct 10  2012 activity_labels.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff  15785 Oct 11  2012 features.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff   2809 Oct 15  2012 features_info.txt
drwxr-xr-x@ 6 chenthilramasamy  staff    204 Nov 29  2012 test
drwxr-xr-x@ 6 chenthilramasamy  staff    204 Nov 29  2012 train
-rwxr-xr-x@ 1 chenthilramasamy  staff   4453 Dec 10  2012 README.txt
drwxr-xr-x  3 chenthilramasamy  staff    102 Dec  8 14:58 week4
-rw-r--r--  1 chenthilramasamy  staff   7163 Dec  8 15:45 CodeBook.md
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ more CodeBook.md 
Code Book

generated 2014-07-10 11:04:30 during sourcing of run_analysis.R

Actions performed on data:
  
  create data dir ./data
downloading zip file: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip to ./data
extracting zip file: ./data/data.zip to ./data/UCI HAR Dataset
merging all *_test.txt and *_train.txt files into one dataset: mergedData
mergedData loaded in memory, dimensions: 10299 x 563
subsetted mergedData into subSetMergedData keeping only the key columns and features containing std or mean, dimensions : 10299 x 68
merged ./data/UCI HAR Dataset/activity_labels.txt contents with correct activity_num column, effectivly appending activity_name to subSetMergedData, dimensions : 10299 x 69
melt subSetMergedData into reshapedData, based on key columns, dimensions : 679734 x 5
split feature column variable into 7 seperate colums (for each sub feature), and added it to reshapedData, dimensions : 679734 x 12
renamed reshapedData to resultData
cast resultData into tidyData with the average of each variable for each activity and each subject dimensions :180 x 68
write tidyData to file ./data/tidy_data.txt
resultData variable

key columns

Variable name   Description
subject ID of subject, int (1-30)
activity_num    ID of activity, int (1-6)
activity_name   Label of activity, Factor w/ 6 levels
non-key columns

Variable name   Description
variable        comlete name of the feature, Factor w/ 66 levels (eg. tBodyAcc-mean()-X)
value   the actual value, num (range: -1:1)
dimension       dimension of measurement, Factor w/ 2 levels: t (Time) or f (Frequency)
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ vi CodeBook.md 
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
  MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
  MacBook-Pro:UCI HAR Dataset chenthilramasamy$ ls -ltr
total 192
-rwxr-xr-x@ 1 chenthilramasamy  staff     80 Oct 10  2012 activity_labels.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff  15785 Oct 11  2012 features.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff   2809 Oct 15  2012 features_info.txt
drwxr-xr-x@ 6 chenthilramasamy  staff    204 Nov 29  2012 test
drwxr-xr-x@ 6 chenthilramasamy  staff    204 Nov 29  2012 train
-rwxr-xr-x@ 1 chenthilramasamy  staff   4453 Dec 10  2012 README.txt
drwxr-xr-x  3 chenthilramasamy  staff    102 Dec  8 14:58 week4
-rw-r--r--@ 1 chenthilramasamy  staff  63226 Dec  8 15:50 CodeBook.md
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
  MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
  MacBook-Pro:UCI HAR Dataset chenthilramasamy$ more CodeBook.md 




<!DOCTYPE html>
  <html lang="en" class=" is-u2f-enabled">
  <head prefix="og: http://ogp.me/ns# fb: http://ogp.me/ns/fb# object: http://ogp.me/ns/object# article: http://ogp.me/ns/article# profile: http://ogp.me/ns/profile#">
  <meta charset='utf-8'>
  
  
  <link crossorigin="anonymous" href="https://assets-cdn.github.com/assets/frameworks-c64b206fb6104fd10a7b4f7460f970885149c62649a7414df084683d7a0f7bf3.css" integrity="sha256-xksgb7YQT9EKe090YPlwiFFJxiZJp0FN8IRoPXoPe/M=" media="all" rel="stylesheet" />
  <link crossorigin="anonymous" href="https://assets-cdn.github.com/assets/github-de2c179df8aa1e18b73cde40af9856d4238b40e33c49a57f8924af619e670688.css" integrity="sha256-3iwXnfiqHhi3PN5Ar5hW1COLQOM8SaV/iSSvYZ5nBog=" media="all" rel="stylesheet" />
  
  
  
  
  
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta http-equiv="Content-Language" content="en">
  <meta name="viewport" content="width=device-width">
  
  <title>coursera-getting-cleaning-data-project/CodeBook.md at master · TomLous/coursera-getting-cleaning-data-project</title>
  <link rel="search" type="application/opensearchdescription+xml" href="/opensearch.xml" title="GitHub">
  <link rel="fluid-icon" href="https://github.com/fluidicon.png" title="GitHub">
  <link rel="apple-touch-icon" href="/apple-touch-icon.png">
  <link rel="apple-touch-icon" sizes="57x57" href="/apple-touch-icon-57x57.png">
  <link rel="apple-touch-icon" sizes="60x60" href="/apple-touch-icon-60x60.png">
  <link rel="apple-touch-icon" sizes="72x72" href="/apple-touch-icon-72x72.png">
  <link rel="apple-touch-icon" sizes="76x76" href="/apple-touch-icon-76x76.png">
  <link rel="apple-touch-icon" sizes="114x114" href="/apple-touch-icon-114x114.png">
  <link rel="apple-touch-icon" sizes="120x120" href="/apple-touch-icon-120x120.png">
  <link rel="apple-touch-icon" sizes="144x144" href="/apple-touch-icon-144x144.png">
  <link rel="apple-touch-icon" sizes="152x152" href="/apple-touch-icon-152x152.png">
  <link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon-180x180.png">
  <meta property="fb:app_id" content="1401488693436528">
  
  <meta content="https://avatars3.githubusercontent.com/u/2259971?v=3&amp;s=400" name="twitter:image:src" /><meta content="@github" name="twitter:site" /><meta content="summary" name="twitter:card" /><meta content="TomLous/coursera-getting-cleaning-data-project" name="twitter:title" /><meta content="coursera-getting-cleaning-data-project - Coursera Project for class Getting &amp; Cleaning data" name="twitter:description" />
  <meta content="https://avatars3.githubusercontent.com/u/2259971?v=3&amp;s=400" property="og:image" /><meta content="GitHub" property="og:site_name" /><meta content="object" property="og:type" /><meta content="TomLous/coursera-getting-cleaning-data-project" property="og:title" /><meta content="https://github.com/TomLous/coursera-getting-cleaning-data-project" property="og:url" /><meta content="coursera-getting-cleaning-data-project - Coursera Project for class Getting &amp; Cleaning data" property="og:description" />
  <meta name="browser-stats-url" content="https://api.github.com/_private/browser/stats">
  <meta name="browser-errors-url" content="https://api.github.com/_private/browser/errors">
  <link rel="assets" href="https://assets-cdn.github.com/">
  <link rel="web-socket" href="wss://live.github.com/_sockets/MjI0ODUxNjc6ZDliNjg1ZjQyZTAxMGNmOGE2NWFlOWJkM2Y0NTgwMGE6OGEzYzdjMmY1MTFkMzUxYjIzYmYwZDgxMWRjZGM0MGNhMzU2NmQzOWMwMmNiMTcyMjliN2RiZDg0ZDI0ZmZhMw==--315eb7891bfc0a9e9292d96f7fcd778587b56bba">
  <meta name="pjax-timeout" content="1000">
  <link rel="sudo-modal" href="/sessions/sudo_modal">
  <meta name="request-id" content="6C3583AC:610C:163EE29:5849C78C" data-pjax-transient>
  
  <meta name="msapplication-TileImage" content="/windows-tile.png">
  <meta name="msapplication-TileColor" content="#ffffff">
  <meta name="selected-link" value="repo_source" data-pjax-transient>
  
  <meta name="google-site-verification" content="KT5gs8h0wvaagLKAVWq8bbeNwnZZK1r1XQysX3xurLU">
  <meta name="google-site-verification" content="ZzhVyEFwb7w3e0-uOTltm8Jsck2F5StVihD0exw2fsA">
  <meta name="google-analytics" content="UA-3769691-2">
  
  <meta content="collector.githubapp.com" name="octolytics-host" /><meta content="github" name="octolytics-app-id" /><meta content="6C3583AC:610C:163EE29:5849C78C" name="octolytics-dimension-request_id" /><meta content="22485167" name="octolytics-actor-id" /><meta content="chenthil1023" name="octolytics-actor-login" /><meta content="061c25dc522fb230a2385ccd9016f115d504ff8367d145883a129e7a3a1387f1" name="octolytics-actor-hash" />
  <meta content="/&lt;user-name&gt;/&lt;repo-name&gt;/blob/show" data-pjax-transient="true" name="analytics-location" />
  
  
  
  <meta class="js-ga-set" name="dimension1" content="Logged In">
  
  
  
  <meta name="hostname" content="github.com">
  <meta name="user-login" content="chenthil1023">
  
  <meta name="expected-hostname" content="github.com">
  <meta name="js-proxy-site-detection-payload" content="ZjgzZWFkYmVkNjU0M2JkNTQwMTI1ODk0YTNiMmFlOWZmMzQyNmY4ZGFhN2VmYzMwM2MyMjE4ZmE1MTgxYjE3N3x7InJlbW90ZV9hZGRyZXNzIjoiMTA4LjUzLjEzMS4xNzIiLCJyZXF1ZXN0X2lkIjoiNkMzNTgzQUM6NjEwQzoxNjNFRTI5OjU4NDlDNzhDIiwidGltZXN0YW1wIjoxNDgxMjMwMjIwLCJob3N0IjoiZ2l0aHViLmNvbSJ9">
  
  
  <link rel="mask-icon" href="https://assets-cdn.github.com/pinned-octocat.svg" color="#000000">
  <link rel="icon" type="image/x-icon" href="https://assets-cdn.github.com/favicon.ico">
  
  <meta name="html-safe-nonce" content="f2ec5e92e534356d78d04c91c96c4dba7e712a4d">
  <meta content="94cba512faa459ecb278e5c95ada666696af8d25" name="form-nonce" />
  
  <meta http-equiv="x-pjax-version" content="565d2f0453cce72d5bb102c5693de179">
  MacBook-Pro:UCI HAR Dataset chenthilramasamy$ !
  -bash: syntax error near unexpected token `newline'
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ ls -ltr
total 424
-rwxr-xr-x@ 1 chenthilramasamy  staff      80 Oct 10  2012 activity_labels.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff   15785 Oct 11  2012 features.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff    2809 Oct 15  2012 features_info.txt
drwxr-xr-x@ 6 chenthilramasamy  staff     204 Nov 29  2012 test
drwxr-xr-x@ 6 chenthilramasamy  staff     204 Nov 29  2012 train
-rwxr-xr-x@ 1 chenthilramasamy  staff    4453 Dec 10  2012 README.txt
drwxr-xr-x  3 chenthilramasamy  staff     102 Dec  8 14:58 week4
-rw-r--r--@ 1 chenthilramasamy  staff   63226 Dec  8 15:50 CodeBook.md
-rw-------@ 1 chenthilramasamy  staff     162 Dec  8 15:58 ~$odeBook.md".docx
-rw-------@ 1 chenthilramasamy  staff  113261 Dec  8 15:58 "CodeBook.md".docx
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ ls -ltr
total 416
-rwxr-xr-x@ 1 chenthilramasamy  staff      80 Oct 10  2012 activity_labels.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff   15785 Oct 11  2012 features.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff    2809 Oct 15  2012 features_info.txt
drwxr-xr-x@ 6 chenthilramasamy  staff     204 Nov 29  2012 test
drwxr-xr-x@ 6 chenthilramasamy  staff     204 Nov 29  2012 train
-rwxr-xr-x@ 1 chenthilramasamy  staff    4453 Dec 10  2012 README.txt
drwxr-xr-x  3 chenthilramasamy  staff     102 Dec  8 14:58 week4
-rw-r--r--@ 1 chenthilramasamy  staff   63226 Dec  8 15:50 CodeBook.md
-rw-------@ 1 chenthilramasamy  staff  113261 Dec  8 15:58 "CodeBook.md".docx
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ mv "CodeBook.md".docx CodeBook.md
mv: CodeBook.md.docx: No such file or directory
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ mv "CodeBook.md".docx CodeBook.md
mv: CodeBook.md.docx: No such file or directory
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ mv "
"CodeBook.md".docx   README.txt           features.txt         test/                week4/
CodeBook.md          activity_labels.txt  features_info.txt    train/               
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ mv "CodeBook.md" 
"CodeBook.md".docx   README.txt           features.txt         test/                week4/
CodeBook.md          activity_labels.txt  features_info.txt    train/               
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ mv "CodeBook.md".docx CodeBook.md
mv: CodeBook.md.docx: No such file or directory
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ mv "CodeBook.md" .docx CodeBook.md
usage: mv [-f | -i | -n] [-v] source target
mv [-f | -i | -n] [-v] source ... directory
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ ls -ltr
total 416
-rwxr-xr-x@ 1 chenthilramasamy  staff      80 Oct 10  2012 activity_labels.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff   15785 Oct 11  2012 features.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff    2809 Oct 15  2012 features_info.txt
drwxr-xr-x@ 6 chenthilramasamy  staff     204 Nov 29  2012 test
drwxr-xr-x@ 6 chenthilramasamy  staff     204 Nov 29  2012 train
-rwxr-xr-x@ 1 chenthilramasamy  staff    4453 Dec 10  2012 README.txt
drwxr-xr-x  3 chenthilramasamy  staff     102 Dec  8 14:58 week4
-rw-r--r--@ 1 chenthilramasamy  staff   63226 Dec  8 15:50 CodeBook.md
-rw-------@ 1 chenthilramasamy  staff  113261 Dec  8 15:58 "CodeBook.md".docx
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ ls -ltr
total 648
-rwxr-xr-x@ 1 chenthilramasamy  staff      80 Oct 10  2012 activity_labels.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff   15785 Oct 11  2012 features.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff    2809 Oct 15  2012 features_info.txt
drwxr-xr-x@ 6 chenthilramasamy  staff     204 Nov 29  2012 test
drwxr-xr-x@ 6 chenthilramasamy  staff     204 Nov 29  2012 train
-rwxr-xr-x@ 1 chenthilramasamy  staff    4453 Dec 10  2012 README.txt
drwxr-xr-x  3 chenthilramasamy  staff     102 Dec  8 14:58 week4
-rw-r--r--@ 1 chenthilramasamy  staff   63226 Dec  8 15:50 CodeBook.md
-rw-------@ 1 chenthilramasamy  staff  113261 Dec  8 15:58 "CodeBook.md".docx
-rw-------@ 1 chenthilramasamy  staff     162 Dec  8 16:10 ~$deBook.docx
-rw-------@ 1 chenthilramasamy  staff  112599 Dec  8 16:10 CodeBook.docx
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ ls -lr
total 640
drwxr-xr-x  3 chenthilramasamy  staff     102 Dec  8 14:58 week4
drwxr-xr-x@ 6 chenthilramasamy  staff     204 Nov 29  2012 train
drwxr-xr-x@ 6 chenthilramasamy  staff     204 Nov 29  2012 test
-rwxr-xr-x@ 1 chenthilramasamy  staff    2809 Oct 15  2012 features_info.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff   15785 Oct 11  2012 features.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff      80 Oct 10  2012 activity_labels.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff    4453 Dec 10  2012 README.txt
-rw-r--r--@ 1 chenthilramasamy  staff   63226 Dec  8 15:50 CodeBook.md
-rw-------@ 1 chenthilramasamy  staff  112599 Dec  8 16:10 CodeBook.docx
-rw-------@ 1 chenthilramasamy  staff  113261 Dec  8 15:58 "CodeBook.md".docx
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ ls -ltr
total 640
-rwxr-xr-x@ 1 chenthilramasamy  staff      80 Oct 10  2012 activity_labels.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff   15785 Oct 11  2012 features.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff    2809 Oct 15  2012 features_info.txt
drwxr-xr-x@ 6 chenthilramasamy  staff     204 Nov 29  2012 test
drwxr-xr-x@ 6 chenthilramasamy  staff     204 Nov 29  2012 train
-rwxr-xr-x@ 1 chenthilramasamy  staff    4453 Dec 10  2012 README.txt
drwxr-xr-x  3 chenthilramasamy  staff     102 Dec  8 14:58 week4
-rw-r--r--@ 1 chenthilramasamy  staff   63226 Dec  8 15:50 CodeBook.md
-rw-------@ 1 chenthilramasamy  staff  113261 Dec  8 15:58 "CodeBook.md".docx
-rw-------@ 1 chenthilramasamy  staff  112599 Dec  8 16:10 CodeBook.docx
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ mv CodeBook.docx CodeBook.md
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ ls -ltr
total 512
-rwxr-xr-x@ 1 chenthilramasamy  staff      80 Oct 10  2012 activity_labels.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff   15785 Oct 11  2012 features.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff    2809 Oct 15  2012 features_info.txt
drwxr-xr-x@ 6 chenthilramasamy  staff     204 Nov 29  2012 test
drwxr-xr-x@ 6 chenthilramasamy  staff     204 Nov 29  2012 train
-rwxr-xr-x@ 1 chenthilramasamy  staff    4453 Dec 10  2012 README.txt
drwxr-xr-x  3 chenthilramasamy  staff     102 Dec  8 14:58 week4
-rw-------@ 1 chenthilramasamy  staff  113261 Dec  8 15:58 "CodeBook.md".docx
-rw-------@ 1 chenthilramasamy  staff  112599 Dec  8 16:10 CodeBook.md
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ ls -ltr
total 512
-rwxr-xr-x@ 1 chenthilramasamy  staff      80 Oct 10  2012 activity_labels.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff   15785 Oct 11  2012 features.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff    2809 Oct 15  2012 features_info.txt
drwxr-xr-x@ 6 chenthilramasamy  staff     204 Nov 29  2012 test
drwxr-xr-x@ 6 chenthilramasamy  staff     204 Nov 29  2012 train
-rwxr-xr-x@ 1 chenthilramasamy  staff    4453 Dec 10  2012 README.txt
drwxr-xr-x  3 chenthilramasamy  staff     102 Dec  8 14:58 week4
-rw-------@ 1 chenthilramasamy  staff  113261 Dec  8 15:58 "CodeBook.md".docx
-rw-------@ 1 chenthilramasamy  staff  112599 Dec  8 16:10 CodeBook.md
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ mv README.txt README.md
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ more README.md 
==================================================================
Human Activity Recognition Using Smartphones Dataset
Version 1.0
==================================================================
Jorge L. Reyes-Ortiz, Davide Anguita, Alessandro Ghio, Luca Oneto.
Smartlab - Non Linear Complex Systems Laboratory
DITEN - Universit<E0> degli Studi di Genova.
Via Opera Pia 11A, I-16145, Genoa, Italy.
activityrecognition@smartlab.ws
www.smartlab.ws
==================================================================

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. See 'features_info.txt' for more details. 

For each record it is provided:
======================================

- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
- Triaxial Angular velocity from the gyroscope. 
- A 561-feature vector with time and frequency domain variables. 
- Its activity label. 
- An identifier of the subject who carried out the experiment.

The dataset includes the following files:
=========================================

- 'README.txt'

- 'features_info.txt': Shows information about the variables used on the feature vector.

- 'features.txt': List of all features.

- 'activity_labels.txt': Links the class labels with their activity name.

- 'train/X_train.txt': Training set.

- 'train/y_train.txt': Training labels.

- 'test/X_test.txt': Test set.

- 'test/y_test.txt': Test labels.

The following files are available for the train and test data. Their descriptions are equivalent. 

- 'train/subject_train.txt': Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30. 

- 'train/Inertial Signals/total_acc_x_train.txt': The acceleration signal from the smartphone accelerometer X axis in standard gravity units 'g'. Every row shows a 128 element vector. The same description applies for the 'total_acc_x_train.txt' and 'total_acc_z_train.txt' files for the Y and Z axis. 

- 'train/Inertial Signals/body_acc_x_train.txt': The body acceleration signal obtained by subtracting the gravity from the total acceleration. 

- 'train/Inertial Signals/body_gyro_x_train.txt': The angular velocity vector measured by the gyroscope for each window sample. The units are radians/second. 

Notes: 
======
- Features are normalized and bounded within [-1,1].
- Each feature vector is a row on the text file.

For more information about this dataset contact: activityrecognition@smartlab.ws

License:
========
Use of this dataset in publications must be acknowledged by referencing the following publication [1] 

[1] Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012

This dataset is distributed AS-IS and no responsibility implied or explicit can be addressed to the authors or their institutions for its use or misuse. Any commercial use is prohibited.

Jorge L. Reyes-Ortiz, Alessandro Ghio, Luca Oneto, Davide Anguita. November 2012.
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ ls -ltr
total 512
-rwxr-xr-x@ 1 chenthilramasamy  staff      80 Oct 10  2012 activity_labels.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff   15785 Oct 11  2012 features.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff    2809 Oct 15  2012 features_info.txt
drwxr-xr-x@ 6 chenthilramasamy  staff     204 Nov 29  2012 test
drwxr-xr-x@ 6 chenthilramasamy  staff     204 Nov 29  2012 train
-rwxr-xr-x@ 1 chenthilramasamy  staff    4453 Dec 10  2012 README.md
drwxr-xr-x  3 chenthilramasamy  staff     102 Dec  8 14:58 week4
-rw-------@ 1 chenthilramasamy  staff  113261 Dec  8 15:58 "CodeBook.md".docx
-rw-------@ 1 chenthilramasamy  staff  112599 Dec  8 16:10 CodeBook.md
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ ls -ltr
total 512
-rwxr-xr-x@ 1 chenthilramasamy  staff      80 Oct 10  2012 activity_labels.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff   15785 Oct 11  2012 features.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff    2809 Oct 15  2012 features_info.txt
drwxr-xr-x@ 6 chenthilramasamy  staff     204 Nov 29  2012 test
drwxr-xr-x@ 6 chenthilramasamy  staff     204 Nov 29  2012 train
-rwxr-xr-x@ 1 chenthilramasamy  staff    4453 Dec 10  2012 README.md
drwxr-xr-x  3 chenthilramasamy  staff     102 Dec  8 14:58 week4
-rw-------@ 1 chenthilramasamy  staff  113261 Dec  8 15:58 "CodeBook.md".docx
-rw-------@ 1 chenthilramasamy  staff  112599 Dec  8 16:10 CodeBook.md
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ ls -ltr
total 648
-rwxr-xr-x@ 1 chenthilramasamy  staff      80 Oct 10  2012 activity_labels.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff   15785 Oct 11  2012 features.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff    2809 Oct 15  2012 features_info.txt
drwxr-xr-x@ 6 chenthilramasamy  staff     204 Nov 29  2012 test
drwxr-xr-x@ 6 chenthilramasamy  staff     204 Nov 29  2012 train
-rwxr-xr-x@ 1 chenthilramasamy  staff    4453 Dec 10  2012 README.md
drwxr-xr-x  3 chenthilramasamy  staff     102 Dec  8 14:58 week4
-rw-------@ 1 chenthilramasamy  staff  113261 Dec  8 15:58 "CodeBook.md".docx
-rw-------@ 1 chenthilramasamy  staff  112599 Dec  8 16:10 CodeBook.md
-rw-------@ 1 chenthilramasamy  staff     162 Dec 11 13:07 ~$n_analysis.docx
-rw-------@ 1 chenthilramasamy  staff   65106 Dec 11 13:07 run_analysis.docx
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ ls -ltr
total 640
-rwxr-xr-x@ 1 chenthilramasamy  staff      80 Oct 10  2012 activity_labels.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff   15785 Oct 11  2012 features.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff    2809 Oct 15  2012 features_info.txt
drwxr-xr-x@ 6 chenthilramasamy  staff     204 Nov 29  2012 test
drwxr-xr-x@ 6 chenthilramasamy  staff     204 Nov 29  2012 train
-rwxr-xr-x@ 1 chenthilramasamy  staff    4453 Dec 10  2012 README.md
drwxr-xr-x  3 chenthilramasamy  staff     102 Dec  8 14:58 week4
-rw-------@ 1 chenthilramasamy  staff  113261 Dec  8 15:58 "CodeBook.md".docx
-rw-------@ 1 chenthilramasamy  staff  112599 Dec  8 16:10 CodeBook.md
-rw-------@ 1 chenthilramasamy  staff   65106 Dec 11 13:07 run_analysis.docx
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ mv run_analysis.docx run_analysis.R
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ 
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ cd ..
MacBook-Pro:week4 chenthilramasamy$ ls -ltr
total 122184
-rw-r--r--@  1 chenthilramasamy  staff  62556944 Dec  8 14:32 getdata%2Fprojectfiles%2FUCI HAR Dataset.zip
drwxr-xr-x@ 12 chenthilramasamy  staff       408 Dec 11 13:07 UCI HAR Dataset
MacBook-Pro:week4 chenthilramasamy$ 
MacBook-Pro:week4 chenthilramasamy$ 
MacBook-Pro:week4 chenthilramasamy$ cd ..
MacBook-Pro:Coursera chenthilramasamy$ ls -ltr
total 8328
drwxr-xr-x@ 334 chenthilramasamy  staff    11356 Sep 21  2012 specdata
-rw-r--r--@   1 chenthilramasamy  staff      367 Oct 28 17:57 pollutantmean.R
-rw-r--r--@   1 chenthilramasamy  staff      806 Oct 28 18:07 corr.R
-rw-r--r--@   1 chenthilramasamy  staff      279 Oct 31 21:54 Complete.R
-rwxr-xr-x@   1 chenthilramasamy  staff     2188 Nov  5 14:08 cachematrix.R
-rw-r--r--    1 chenthilramasamy  staff  4246554 Nov 17 10:42 data.csv
drwx------@   9 chenthilramasamy  staff      306 Dec  8 14:58 week4
MacBook-Pro:Coursera chenthilramasamy$ cd week4/
MacBook-Pro:week4 chenthilramasamy$ ls -ltr
total 122184
-rw-r--r--@  1 chenthilramasamy  staff  62556944 Dec  8 14:32 getdata%2Fprojectfiles%2FUCI HAR Dataset.zip
drwxr-xr-x@ 12 chenthilramasamy  staff       408 Dec 11 13:07 UCI HAR Dataset
MacBook-Pro:week4 chenthilramasamy$ cd UCI\ HAR\ Dataset/
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ ls -ltr
total 640
-rwxr-xr-x@ 1 chenthilramasamy  staff      80 Oct 10  2012 activity_labels.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff   15785 Oct 11  2012 features.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff    2809 Oct 15  2012 features_info.txt
drwxr-xr-x@ 6 chenthilramasamy  staff     204 Nov 29  2012 test
drwxr-xr-x@ 6 chenthilramasamy  staff     204 Nov 29  2012 train
-rwxr-xr-x@ 1 chenthilramasamy  staff    4453 Dec 10  2012 README.md
drwxr-xr-x  3 chenthilramasamy  staff     102 Dec  8 14:58 week4
-rw-------@ 1 chenthilramasamy  staff  113261 Dec  8 15:58 "CodeBook.md".docx
-rw-------@ 1 chenthilramasamy  staff  112599 Dec  8 16:10 CodeBook.md
-rw-------@ 1 chenthilramasamy  staff   65106 Dec 11 13:07 run_analysis.R
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ mv run_analysis.R ../.
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ mv CodeBook.md ../.
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ mv README.md ../.
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ ls -ltr
total 272
-rwxr-xr-x@ 1 chenthilramasamy  staff      80 Oct 10  2012 activity_labels.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff   15785 Oct 11  2012 features.txt
-rwxr-xr-x@ 1 chenthilramasamy  staff    2809 Oct 15  2012 features_info.txt
drwxr-xr-x@ 6 chenthilramasamy  staff     204 Nov 29  2012 test
drwxr-xr-x@ 6 chenthilramasamy  staff     204 Nov 29  2012 train
drwxr-xr-x  3 chenthilramasamy  staff     102 Dec  8 14:58 week4
-rw-------@ 1 chenthilramasamy  staff  113261 Dec  8 15:58 "CodeBook.md".docx
MacBook-Pro:UCI HAR Dataset chenthilramasamy$ cd ..
MacBook-Pro:week4 chenthilramasamy$ ls -ltr
total 122552
-rwxr-xr-x@ 1 chenthilramasamy  staff      4453 Dec 10  2012 README.md
-rw-r--r--@ 1 chenthilramasamy  staff  62556944 Dec  8 14:32 getdata%2Fprojectfiles%2FUCI HAR Dataset.zip
-rw-------@ 1 chenthilramasamy  staff    112599 Dec  8 16:10 CodeBook.md
-rw-------@ 1 chenthilramasamy  staff     65106 Dec 11 13:07 run_analysis.R
drwxr-xr-x@ 9 chenthilramasamy  staff       306 Dec 11 13:08 UCI HAR Dataset
MacBook-Pro:week4 chenthilramasamy$ mv UCI\ HAR\ Dataset/ ../.
MacBook-Pro:week4 chenthilramasamy$ mv getdata%2Fprojectfiles%2FUCI\ HAR\ Dataset.zip ../.
MacBook-Pro:week4 chenthilramasamy$ ls -ltr
total 368
-rwxr-xr-x@ 1 chenthilramasamy  staff    4453 Dec 10  2012 README.md
-rw-------@ 1 chenthilramasamy  staff  112599 Dec  8 16:10 CodeBook.md
-rw-------@ 1 chenthilramasamy  staff   65106 Dec 11 13:07 run_analysis.R
MacBook-Pro:week4 chenthilramasamy$ vi run_analysis.R 
MacBook-Pro:week4 chenthilramasamy$ 
MacBook-Pro:week4 chenthilramasamy$ 
MacBook-Pro:week4 chenthilramasamy$ 
MacBook-Pro:week4 chenthilramasamy$ 
MacBook-Pro:week4 chenthilramasamy$ ls -ltr
total 160
-rwxr-xr-x@ 1 chenthilramasamy  staff   4453 Dec 10  2012 README.md
-rw-------@ 1 chenthilramasamy  staff  65106 Dec 11 13:07 run_analysis.R
-rw-------@ 1 chenthilramasamy  staff   7206 Dec 11 18:36 CodeBook.md
MacBook-Pro:week4 chenthilramasamy$ 
MacBook-Pro:week4 chenthilramasamy$ 
MacBook-Pro:week4 chenthilramasamy$ more CodeBook.md 
Code Book
Actions performed on data:
•     create data dir ./week4
•       downloading zip file: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip to ./week4
•       extracting zip file: ./week4/data.zip to ./data/UCI HAR Dataset
•       merging all *_test.txt and *_train.txt files into one dataset: mergedData
•       mergedData loaded in memory, dimensions: 10299 x 563
•       subsetted mergedData into subSetMergedData keeping only the key columns and features containing std or mean, dimensions : 10299 x 68
•       merged ./data/UCI HAR Dataset/activity_labels.txt contents with correct activity_num column, effectivly appending activity_name to subSetMergedData, dimensions : 10299 x 69
•       melt subSetMergedData into reshapedData, based on key columns, dimensions : 679734 x 5
•       split feature column variable into 7 seperate colums (for each sub feature), and added it to reshapedData, dimensions : 679734 x 12
•       renamed reshapedData to resultData
•       cast resultData into tidyData with the average of each variable for each activity and each subject dimensions :180 x 68
•       write tidyData to file ./week4/tidy_data.txt
resultData variable
key columns
Variable name
Description
subject
ID of subject, int (1-30)
activity_num
ID of activity, int (1-6)
activity_name
Label of activity, Factor w/ 6 levels
non-key columns
Variable name
Description
variable
comlete name of the feature, Factor w/ 66 levels (eg. tBodyAcc-mean()-X)
value
the actual value, num (range: -1:1)
dimension
MacBook-Pro:week4 chenthilramasamy$ 
MacBook-Pro:week4 chenthilramasamy$ 
MacBook-Pro:week4 chenthilramasamy$ ls -ltr
total 160
-rwxr-xr-x@ 1 chenthilramasamy  staff   4453 Dec 10  2012 README.md
-rw-------@ 1 chenthilramasamy  staff  65106 Dec 11 13:07 run_analysis.R
-rw-------@ 1 chenthilramasamy  staff   7206 Dec 11 18:36 CodeBook.md
MacBook-Pro:week4 chenthilramasamy$ more README.md 
==================================================================
Human Activity Recognition Using Smartphones Dataset
Version 1.0
==================================================================
Jorge L. Reyes-Ortiz, Davide Anguita, Alessandro Ghio, Luca Oneto.
Smartlab - Non Linear Complex Systems Laboratory
DITEN - Universit<E0> degli Studi di Genova.
Via Opera Pia 11A, I-16145, Genoa, Italy.
activityrecognition@smartlab.ws
www.smartlab.ws
==================================================================

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. See 'features_info.txt' for more details. 

For each record it is provided:
======================================

- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
- Triaxial Angular velocity from the gyroscope. 
- A 561-feature vector with time and frequency domain variables. 
- Its activity label. 
- An identifier of the subject who carried out the experiment.

The dataset includes the following files:
=========================================
MacBook-Pro:week4 chenthilramasamy$ vi README.md 

Human Activity Recognition Using Smartphones Dataset
Version 1.0
==================================================================
Jorge L. Reyes-Ortiz, Davide Anguita, Alessandro Ghio, Luca Oneto.
Smartlab - Non Linear Complex Systems Laboratory
DITEN - Università degli Studi di Genova.
Via Opera Pia 11A, I-16145, Genoa, Italy.
activityrecognition@smartlab.ws
www.smartlab.ws
==================================================================

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. See 'features_info.txt' for more details.

For each record it is provided:
======================================

- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
- Triaxial Angular velocity from the gyroscope.
- A 561-feature vector with time and frequency domain variables.
- Its activity label.
- An identifier of the subject who carried out the experiment.

The dataset includes the following files:
=========================================


