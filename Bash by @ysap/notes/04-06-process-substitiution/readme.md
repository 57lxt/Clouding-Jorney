## Process Substitution 
```<(...)``` & ```>(...)```

### messy way to count words
```bash
words=$(grep d ./words)
i=0
for word in words;do
  echo $word
  ((i++))
done
echo "found $i words"
```
### Better way to do it 

```bash
while read -r word;do
  echo "$word"
  ((i++))
done < ./words #redirecting the file to read
# or we can redirect variable by <<< $words
```
### piping to while 
```bash
i=0
grep d ./words | while read -r word;do
  echo "$word"
  ((i++)) 
done
echo " found $i words"
# the output is 'found 0 words' because as mentioned in notes under
# the while loop is being executed on subs# the output is 'found 0 words' because as mentioned in notes under
# the while loop is being executed on sub shell and it is not modifying the i in parent shell
# this is where process substitution comeshell and it is not modifying the i in parent shell
# this is where process substitution comes
```
## Process Sub
Using ```<(...)``` to substitute process 
```bash
i=0
while read -r word;do
  echo "$word"
  ((i++)) 
done < <(grep d ./words)
echo " found $i words"

# this code works fine because the process is substituted and it runs on parent shell
# what ever the output of grep is it will be redirected to the while loop ```
```
## Notes
- ```here string``` - lets us pipe data to variable
-```grep -c d ./words``` #counts the occurrence of d in the file
-```<<<```
- Anything that is to the right of pipe ```|``` is being executed on a new shell

## Commands to try
- ``` echo <(uname) #returns file descriptor```
- ```cat <(uname) #returns the normal command output```
