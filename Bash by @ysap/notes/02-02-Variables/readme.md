# Basic Variables
## System Variables
1. USER  - username of current user
2. PATH  - environment variable of the system
3. SHELL - current shell
4. HOSTNAME - hostname of the sys
5. PWD - same output as the cmd pwd - print working dir
6. MACHTYPE - machine type - example: aarch64-apple-linux-gnu

usage: ```$ + variable name```

example:
```bash
echo $PATH
```

## User Defined 
usage: ```variable name + = + value```
example: 
```bash
country=US && echo $country
```

## Note: 

### use of <" "> (quotation)
```bash
foo='hello      world'
echo $foo #outputs with only one space
echo "$foo #outputs the spaces too
```

### aliases
usage: variable name = \` + command + \`
```bash
ls=$(ls --color) #or ls = `ls --color` 
echo "$ls"
```

### unset
usage: ```unset + variable name```

### export
we can also use export to use the var throughout the shell and sub shells
example: 
```bash
export name=Levan && echo $name
```

### Commands to try
```uname -a ``` 




