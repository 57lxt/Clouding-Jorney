# User Input
usage: read + [option] + 'string' + variable

example:
```bash
read -p 'Enter number:' num
```

### greeting script

```bash
#!/usr/bin/env bash

read -p 'Enter Name:' name
echo "hello $name"
```
## arguments
passed when running the script like ```script arg1 arg2```  
usage: $ + n-th argument
example:
```bash
first_name=$1 #first argument assigned to variable
last_name=$2 #second argument
echo "hi $1 $2"
```

#### arguments in loop
```bash
for i in "$1" "$2" "$3"; do
  echo $i
done
```

## if statment
usage:
if [[expression]]; then 
.
else 
.
fi

example:
```bash
if [[ -n $1 ]]; then
    name=$1
else
    read -p 'Enter Name:' name
fi
echo name
```
## things to study 
difference between single and double quote in bash
  
## Commands to try
```help '[['```
```help '['```
```help test```
