# Conditionals

* equals ```==```
* negation ```!```
* -f - checks if file exists
*  

### Example
```bash
read "Enter 1st num: " num1
read "Enter 2nd num: " num2
if [[ $num1==$num2 ]]; then
  echo 'the numbers are equal'
else
  echo 'the numbers are not equal'
fi
```

## Commands to try 
* ```help test```

## My findings
__Bash needs space around operators__  
example:  
```bash
crx@DESKTOP-6OFM6RC:~/bash_ysap$ cat 03-03-conditionals
if [[ $1==$2 ]];then
  echo "they are equal"
else
  echo "they are not equal"
fi
crx@DESKTOP-6OFM6RC:~/bash_ysap$ chmod +x 03-03-conditionals
crx@DESKTOP-6OFM6RC:~/bash_ysap$ ./03-03-conditionals 2 3
they are equal
```
it should be 

```bash
crx@DESKTOP-6OFM6RC:~/bash_ysap$ cat 03-03-conditionals
if [[ $1 == $2 ]];then
  echo "they are equal"
else
  echo "they are not equal"
fi
crx@DESKTOP-6OFM6RC:~/bash_ysap$ ./03-03-conditionals 2 3
they are not equal
crx@DESKTOP-6OFM6RC:~/bash_ysap$
```
