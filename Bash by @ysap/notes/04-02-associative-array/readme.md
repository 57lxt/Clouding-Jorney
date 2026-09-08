# Associative Array
just like dictionary in python

### Declaration
```declare -A array```
Associatve array works for bash v4.0 and above  
to test if it works on system
```bash
declare -A arr
echo $?
```
or 
```bash
if ! declare -A arr; then
  echo "couldn't make associative array" >&2 # redirected to stderr
  exit 1
fi
```

## Setting Elements
we do this by using the key as index and assigning value 
```bash
declare -A arr
arr[one]=1
arr[foo]=2
arr[baz]="one"
```
## Accessing Elements
```bash
echo "${arr[one]}"
echo "${arr[foo]}"
echo "${arr[baz]}"
```
- to loop over the values we can use ```*``` or ```@``` just like we used in indexed array
- to loop over keys ```${!arr[*]}```. we use ```!```

## connecting the whole thing 
   
```bash
declare -A arr
arr[one]=1
arr[foo]=2
arr[baz]="one"

for key in ${!arr[@]}; do
  value=${arr[$key]} # we have to use $ before the key variable here, otherwise bash will think key is literal and not variable
  echo "KEY: $key, value: $value"
done

```
