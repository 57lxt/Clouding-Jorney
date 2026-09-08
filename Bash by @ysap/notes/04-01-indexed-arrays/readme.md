# Indexed Arrays
usage:  
```var=(elements)```   
  
example:
```bash
array=(Josh Jeff Roman)
```
## Indexes
- We can go backward if we make the index negative ```${array[-1]} #last element```
- we can use variable as index ``` ${array[var]} ```
- ```${array[*]} ``` - gets us the whole array as a string
- ```${array[@]} ``` - gets us each element as separate value
- don't leave out the quotes on an array, otherwise if the array has different kind of elements, the output will be different than expected    
  example:  
   ```for i in ${array[@]}; then ... done #wrong```   
   ```for i in "${array[@]}"; then ... done #correct"```
- array can be declared by declare keyword   
  example: ```declare -a array (foo bar baz) ```


## Accessing Elements
``` echo "${array[0]}" # index 0```

## Copying Array
To copy an array we can't just do ```old_array=new_array```, because it will only assign the first element  
we can't also do ```old_array= ${new_array[@]}```, cause the new array will be string and not array  
the correct way is just like declaring a new array. if we put the string in bracket we get the array to be copied   
```old_array=( ${array[@]} )```   
example:  
```bash
old_array=(foo bar baz)
new_array=( "${array[@]}" )
```
## Adding Elements to Array
usage:  
```array+=(elements)```
example:  
```bash
array=(foo bar)
array+=(baz baf)
```
## Commands to try 
```help declare #check out -p and -a``` 
```echo "${#array[45]} #length of element```
```echo "${#array[@]} #length of array```
```echo "${#var}" #length of string```


