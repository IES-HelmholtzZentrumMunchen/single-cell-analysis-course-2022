---
title: Command line basics
---
If you've already done some programming, or are aspiring to learn it, you will sooner or later encounter that most scientific software requires some degree of proficiency with the command line. On different operating systems, there are different command language interpreters, for example:
  * On Windows, the [shell](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/windows-commands)
  * On Linux/Unix, [bash](https://www.gnu.org/software/bash/manual/bash.html)
  * Also, Mac OS runs a variant of [bash](https://developer.apple.com/library/archive/documentation/OpenSource/Conceptual/ShellScripting/CommandLInePrimer/CommandLine.html)

Especially on Unix, you can also install other command line interpreters, for instance [ksh](https://en.wikipedia.org/wiki/KornShell) or [zsh](https://en.wikipedia.org/wiki/Z_shell).

For our course, you will need only the most basic commands which you may already be familiar with. If you know any bash tricks, we'd love to know, so feel free to share them with the whole course!

Some commands are also directly accessible trough the Jupyter [magic fucntions](https://ipython.readthedocs.io/en/stable/interactive/magics.html) that start with `%`. We'll focus on bash, because that's what is integrated into Jupyter; but if you work on a Windows or Mac system, it will be good if you get familiar with the commands specific for you operating system.

### Navigationg the file system

How to change the directory?
```bash
andreas@Ceto:~$ cd ~/Documents/
andreas@Ceto:~/Documents$ cd Projects/scater/single-cell-analysis-course-2021
```

Sometimes it is good to know where we are:
```bash
andreas@Ceto:~/Documents/Projects/scater/single-cell-analysis-course-2021$ pwd
~/Documents/Projects/scater/single-cell-analysis-course-2021
```

Which files and folders are in the current directory?
```bash
andreas@Ceto:~/Documents/Projects/scater/single-cell-analysis-course-2021$ ls
README.md  docs  nn_models  notebooks  sample_data  test_folder
```

Most commands take options, starting with `-` for example the `ls` command can show more details by adding the `-l` option. `ls -al` shows more details and also hidden files.
```bash
andreas@Ceto:~/Documents/Projects/scater/single-cell-analysis-course-2021$ ls -l
total 0
-rwxrwxrwx 1 andreas andreas  374 Feb 10 09:12 README.md
drwxrwxrwx 1 andreas andreas 4096 Feb 10 18:59 docs
drwxrwxrwx 1 andreas andreas 4096 Feb 10 11:04 nn_models
drwxrwxrwx 1 andreas andreas 4096 Feb 11 09:47 notebooks
drwxrwxrwx 1 andreas andreas 4096 Feb 10 11:00 sample_data
drwxrwxrwx 1 andreas andreas 4096 Feb 11 09:44 test_folder
```

```bash
andreas@Ceto:~/Documents/Projects/scater/single-cell-analysis-course-2021$ ls -al
total 0
drwxrwxrwx 1 andreas andreas 4096 Feb 11 09:44 .
drwxrwxrwx 1 andreas andreas 4096 Feb  9 15:41 ..
drwxrwxrwx 1 andreas andreas 4096 Feb 10 22:53 .git
-rwxrwxrwx 1 andreas andreas  374 Feb 10 09:12 README.md
drwxrwxrwx 1 andreas andreas 4096 Feb 10 18:59 docs
drwxrwxrwx 1 andreas andreas 4096 Feb 10 11:04 nn_models
drwxrwxrwx 1 andreas andreas 4096 Feb 11 09:47 notebooks
drwxrwxrwx 1 andreas andreas 4096 Feb 10 11:00 sample_data
```

How to make a new directory?
```bash
andreas@Ceto:~/Documents/Projects/scater/single-cell-analysis-course-2021$ cd ..
andreas@Ceto:~/Documents/Projects/scater$ cd .
andreas@Ceto:~/Documents/Projects/scater$ cd ../..
andreas@Ceto:~/Documents$ cd Projects/scater/
andreas@Ceto:~/Documents/Projects/scater$ mkdir test
andreas@Ceto:~/Documents/Projects/scater$ ls
single-cell-analysis-course-2020  single-cell-analysis-course-2021  test
```

How to make an empty file?
```bash
andreas@Ceto:~/Documents/Projects/scater$ cd test/
andreas@Ceto:~/Documents/Projects/scater/test$ touch testfile
andreas@Ceto:~/Documents/Projects/scater/test$ ls
testfile
```

How to copy files?
```bash
andreas@Ceto:~/Documents/Projects/scater/test$ cd ..
andreas@Ceto:~/Documents/Projects/scater$ cd single-cell-analysis-course-2021/
andreas@Ceto:~/Documents/Projects/scater/single-cell-analysis-course-2021$ cp README.md ../test/
andreas@Ceto:~/Documents/Projects/scater/single-cell-analysis-course-2021$ cd ..
andreas@Ceto:~/Documents/Projects/scater$ cd test/
andreas@Ceto:~/Documents/Projects/scater/test$ ls
README.md
```

How to move files?
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
