# Scripting with bash

## variables

```bash

  myvariable = value

  echo $mavariable
  #display value

  echo The value of \$varname is \"$varname\".
```

The double quotes circumvent this part of the process (by making the shell think that the whole quoted string is a single word if you want to conserve space

## display date

```bash
  echo $(date +%d/%m/%y-%H:%M:%S)
```

## functions

### simple function

```bash
  function myFunction {
    #instructions
  }

  myFunction() {
    #instructions
  }
```

### explain arguments

```bash
  function alice {

    echo "alice: $@"
    # print all arguments

    echo "$0: $1 $2 $3 $4"
    # print arguments which are defined and replace other by empty (or null) strings

    echo "$# arguments"
    #print number of arguments
  }
```

```bash
  ${#varname}
  #length value
```

## Patterns

|     Operator    |                        Meaning                          |
| --------------- | ------------------------------------------------------- |
| *(patternlist)  |  Matches zero or more occurrences of the given patterns.|
| +(patternlist)  |  Matches one or more occurrences  of the given patterns.|
| ?(patternlist)  |  Matches zero or one occurrences of the given patterns. |
| @(patternlist)  |  Matches exactly one of the given patterns.             |
| !(patternlist)  |  Matches anything except one of the given patterns.     |

## Arithmetic test operators

| Test  |               Comparison                |
| ----- | --------------------------------------- |
| -lt   | Less than                               |
| -le   | Less than or equal -eq Equal            |
| -ge   | Greater than or equal -gt Greater than  |
| -ne   | Not equal                               |

## flox control

```bash
  if [condition]; then
    statements
  elif [condition]; then
    statements
  else
    statements
  fi
```

| Operator|                                       True if...                                            |
| ------- | ------------------------------------------------------------------------------------------- |
| -a file |   file exists                                                                               |
| -d file |   file exists and is a directory                                                            |
| -e file |   file exists; same as -a                                                                   |
| -f file |   file exists and is a regular file (i.e., not a directory or other special type of file)   |
| -r file |   You have read permission on file                                                          |
| -s file |   file exists and is not empty                                                              |
| -w file |   You have write permission on file                                                         |
| -x file |   You have execute permission on file, or directory search permission if it is a directory  |
| -N file |   file was modified since it was last read                                                  |
| -O file |   You own file                                                                              |
| -G file |   file’s group ID matches yours (or one of yours, if you are in multiple groups)            |

## Loops

### for

```bash
  for x := 1 to 10 do
  begin
    statements...
  end

  for name [in list]
  do
    statements that can use $name...
  done

  for (( initialisation ; ending condition ; update ))
  do
    statements...
  done
```

### while

```bash
  while condition; do
    statements
  done
```

### until

```bash
  until condition; do
    statements
  done  
```

### case

```bash
  case expression in
    pattern1 )
      statements ;;
    pattern2 )
      statements ;;
    ...
  esac
```

### select

```bash
  select name [in list] do
    statements that can use $name...
   done
```

## Arrays

```bash
  names[2]=alice
  names[0]=hatter
  names[1]=duchess

  names=(hatter duchess alice)

  names=([2]=alice [0]=hatter [1]=duchess)
```
