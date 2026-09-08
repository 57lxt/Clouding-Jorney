# Command Substitution
we use backticks to store the command to variable
usage:  
```var=`command` ```  
example
```bash
user=`whoami`
echo "hi $user "
```
### Nested backticks
if we wanna do ```echo `echo `whoami`` ```, bash thinks the first backtick is closed after echo.  
the correct way of doing it is to escape the second backtick.  
  ```echo `echo \`whoami\`` ```  
  ```echo `echo \`echo \\\`whoami\\\`\`` ``` - crazy backtick escape :)
#### Better way to do it 
echo "$(echo $(echo $(whoami)))"

## Parameter expansion
This method has side effect on global vars and runs on parent shell

```var={ cmd; }``` - the space is important after curly brace   
example:   
```bash
user={ whoami; }
echo $user
```

## Notes
- when running command with $(cmd) it runs on subshell which means if its a function it can't affect global variables   
  ```func=$(my-func)```- my-func exec on subshell and doesn't have side effect on global variables   
  ```my-func ``` - execs on parent shell and has side effect on global vars
  __SUGGESTION__: use local keyword for variables

## Things I found out
```bash
name=""
echo "${name:-unknown}" # :- means use unknown if name is empty
```

## Things to study
- parameter expansion ${ } and how to manipulate the vars

prompt: what is parameter expansion shortly, and how to use it with example
