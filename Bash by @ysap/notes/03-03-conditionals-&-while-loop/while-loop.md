# While loop
iterates until the condition is false 
syntax:  
```bash
while [[ condition ]]; do  
.  
.  
done
```  
### Example

```bash
while [[ -f file.txt ]]; do
  echo "file exists"
  sleep 1 # pauses the program for 1 sec
done
echo "file not found"
```

# Until loop
opposite of while loop.
rewriting the above code

```bash
until [[ -f file.txt ]]; do
  echo "file not found"
  sleep 1 # pauses the program for 1 sec
done
echo "file exists"
```
the code runs until the file is created 
```touch file.txt```
then it will stop printing "file exists"

# Note 

1. we can use use any command as conditions in if and loop statments  
example:
```bash
if ls;then
  echo 'ls worked'
fi
```

2. we can use the keyword true and false   
   example:
```bash
  if true; then
     echo 'always true'
  fi
```
3. checking exit code of the previous command with ```echo $?```
