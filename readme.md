# Principles commands linux

## basic commands

```bash
  touch <file>
  # create a file
  mkdir <folder>
  # create a folder
```

list all files and directories

```bash
  ls
  # list files and folders
  ls -a
  # list all even hidden files
  ls -l
  # list to list the file’s owner, size, time of last modification...
```

move into directories

```bash
  cd <path>
  # go to a destination

  cd ..
  cd -
   # go to parent directory

  cd --
  cd ~
   # go to home directory
```

display directories

```bash
  which <folder>
  where <folder>
```

copy a file

```bash
 cp SOURCE DESTINATION
 #copy a file with a destination
```

remove a file

```bash
  rm <file>
  #remove file
```

command clear

```bash
  clear
  # to clear terminal
```

use echo

```bash
 echo $PATH
 # show a value of a variable
```

print history commands

```bash
  history
  #print history commands

  !188
  # print the 188nth command
```

kill process

```bash
  kill [process ID]
  
  killall [process name]
```

## command chmod

### chmod options

* -f
* -v
* -c
* -R
* --help
* --version

### permissions

* 7 rwx read, write, execute
* 6 rw- read and write
* 5 r-x read and execute
* 4 r-- read only
* 3 -wx write and execute
* 2 -w- write only
* 1 --x execute only
* 0 --- none

```bash
  chmod
```

## command find

### find options

* -name

* -size

* -print

* -empty

```bash
  find ./folder -empty
  # find an empty file in a ./[folder] directory
```
