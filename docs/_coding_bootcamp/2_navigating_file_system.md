---
title: Navigating the file system
collapsible: true
---
How to change the directory? Use `cd` to navigate the file system.
```bash
$:~$ cd ~/Documents/
$:~/Documents$ cd Projects/scater/single-cell-analysis-course-2021
```

Sometimes it is good to know where we are.  `pwd` prints the working directory.
```bash
$:~/Documents/Projects/scater/single-cell-analysis-course-2021$ pwd
~/Documents/Projects/scater/single-cell-analysis-course-2021
```

Which files and folders are in the current directory? `ls` is your friend.
```bash
$:~/Documents/Projects/scater/single-cell-analysis-course-2021$ ls
README.md  docs  nn_models  notebooks  sample_data  test_folder
```

Most commands take options, starting with `-` for example the `ls` command can show more details by adding the `-l` option. `ls -al` shows more details and also hidden files.
```bash
$:~/Documents/Projects/scater/single-cell-analysis-course-2021$ ls -l
total 0
-rwxrwxrwx 1 root root  374 Feb 10 09:12 README.md
drwxrwxrwx 1 root root 4096 Feb 10 18:59 docs
drwxrwxrwx 1 root root 4096 Feb 10 11:04 nn_models
drwxrwxrwx 1 root root 4096 Feb 11 09:47 notebooks
drwxrwxrwx 1 root root 4096 Feb 10 11:00 sample_data
drwxrwxrwx 1 root root 4096 Feb 11 09:44 test_folder
```

```bash
$:~/Documents/Projects/scater/single-cell-analysis-course-2021$ ls -al
total 0
drwxrwxrwx 1 root root 4096 Feb 11 09:44 .
drwxrwxrwx 1 root root 4096 Feb  9 15:41 ..
drwxrwxrwx 1 root root 4096 Feb 10 22:53 .git
-rwxrwxrwx 1 root root  374 Feb 10 09:12 README.md
drwxrwxrwx 1 root root 4096 Feb 10 18:59 docs
drwxrwxrwx 1 root root 4096 Feb 10 11:04 nn_models
drwxrwxrwx 1 root root 4096 Feb 11 09:47 notebooks
drwxrwxrwx 1 root root 4096 Feb 10 11:00 sample_data
```
