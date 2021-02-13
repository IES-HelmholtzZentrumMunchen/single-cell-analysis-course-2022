---
title: Basic file operations
collapsible: true
---
How to make a new directory? Try out `mkdir`
```bash
$:~/Documents/Projects/scater/single-cell-analysis-course-2021$ cd ..
$:~/Documents/Projects/scater$ cd .
$:~/Documents/Projects/scater$ cd ../..
$:~/Documents$ cd Projects/scater/
$:~/Documents/Projects/scater$ mkdir test
$:~/Documents/Projects/scater$ ls
single-cell-analysis-course-2020  single-cell-analysis-course-2021  test
```

How to make an empty file? `touch` makes an empty file.
```bash
$:~/Documents/Projects/scater$ cd test/
$:~/Documents/Projects/scater/test$ touch testfile
$:~/Documents/Projects/scater/test$ ls
testfile
```

How to copy files? `cp` makes a copy.
```bash
$:~/Documents/Projects/scater/test$ cd ..
$:~/Documents/Projects/scater$ cd single-cell-analysis-course-2021/
$:~/Documents/Projects/scater/single-cell-analysis-course-2021$ cp README.md ../test/
$:~/Documents/Projects/scater/single-cell-analysis-course-2021$ cd ..
$:~/Documents/Projects/scater$ cd test/
$:~/Documents/Projects/scater/test$ ls
README.md
```

How to move files? `mv`, in contrast to `cp` moves files to other directories. It can also be used to rename files.
```bash
$:~/Documents/Projects/scater/test$ mv README.md ..
$:~/Documents/Projects/scater/test$ cd ..
$:~/Documents/Projects/scater$ ls
README.md  single-cell-analysis-course-2020  single-cell-analysis-course-2021  test
```

How to remove files and directories? Careful, bash will not ask for confirmation! `rm -r` recursively removes files and folders, you can wipe your hard drive if you are not careful!
```bash
$:~/Documents/Projects/scater$ rm README.md
$:~/Documents/Projects/scater$ rmdir test
$:~/Documents/Projects/scater$
```
