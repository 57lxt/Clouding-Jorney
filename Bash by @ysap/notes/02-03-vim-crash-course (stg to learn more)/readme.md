# Vim Crash Course
usage: vim + filename

## modes 
* normal
* insert
* visual

## Shortcuts on visual mode
- [ ] i - insert mode
- [ ] dd  - cut line
- [ ] u -undo 
- [ ] yy - copy
- [ ] p - paste 
- [ ] . - plays last command 
- [ ] o - add new line under, or with 'shift + o' above

## Commands (:)
usage-  ':'  + command letters  
:w - write  
:q - quit  
!- force  

## First Bash Script
```bash
vim script.sh
name='jackson'
age=29
system=$(uname)
echo "$name is $age years old"
echo "your system is $system" #save file by :wq!
```
