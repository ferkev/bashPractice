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
