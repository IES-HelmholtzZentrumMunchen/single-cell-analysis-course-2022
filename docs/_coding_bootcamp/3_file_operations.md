---
title: Basic file operations
collapsible: yes
---
How to make a new directory? Try out `mkdir`
```bash
andreas@Ceto:~/Documents/Projects/scater/single-cell-analysis-course-2021$ cd ..
andreas@Ceto:~/Documents/Projects/scater$ cd .
andreas@Ceto:~/Documents/Projects/scater$ cd ../..
andreas@Ceto:~/Documents$ cd Projects/scater/
andreas@Ceto:~/Documents/Projects/scater$ mkdir test
andreas@Ceto:~/Documents/Projects/scater$ ls
single-cell-analysis-course-2020  single-cell-analysis-course-2021  test
```

How to make an empty file? `touch` makes an empty file.
```bash
andreas@Ceto:~/Documents/Projects/scater$ cd test/
andreas@Ceto:~/Documents/Projects/scater/test$ touch testfile
andreas@Ceto:~/Documents/Projects/scater/test$ ls
testfile
```

How to copy files? `cp` makes a copy.
```bash
andreas@Ceto:~/Documents/Projects/scater/test$ cd ..
andreas@Ceto:~/Documents/Projects/scater$ cd single-cell-analysis-course-2021/
andreas@Ceto:~/Documents/Projects/scater/single-cell-analysis-course-2021$ cp README.md ../test/
andreas@Ceto:~/Documents/Projects/scater/single-cell-analysis-course-2021$ cd ..
andreas@Ceto:~/Documents/Projects/scater$ cd test/
andreas@Ceto:~/Documents/Projects/scater/test$ ls
README.md
```

How to move files? `mv`, in contrast to `cp` moves files to other directories. It can also be used to rename files.
```bash
andreas@Ceto:~/Documents/Projects/scater/test$ mv README.md ..
andreas@Ceto:~/Documents/Projects/scater/test$ cd ..
andreas@Ceto:~/Documents/Projects/scater$ ls
README.md  single-cell-analysis-course-2020  single-cell-analysis-course-2021  test
```

How to remove files and directories? Careful, bash will not ask for confirmation! `rm -r` recursively removes files and folders, you can wipe your hard drive if you are not careful!
```bash
andreas@Ceto:~/Documents/Projects/scater$ rm README.md
andreas@Ceto:~/Documents/Projects/scater$ rmdir test
andreas@Ceto:~/Documents/Projects/scater$
```
