# Input & Output
## read cmd options 
* -p - prompt - usage ```read -p "..." var```
* -r - don't allow \ to escape character

## While read
using read cmd inside while condition to read multiple lines  
example: 
```bash
while read -r line; then
  #true - since bash doesn't allow while loop without body we can use true keyword or : which does nothing
  :
done
```
### problems:
for the above code 
echo -n hello | ./script - this will not have output because it doesn't have newline 
  
possible solutions
  
```while read -r line || [[ -n $line ]]; do ...``` - this means true when sucessfully read or if line variable has something in it 



## notes
1. echo -n "..." - the option removes the hidden new line
2. 

## commands to try
xxd - not sure but he used it to get he ascii value of string
```echo hellow | xxd```
```echo -n hellow | xxd```

