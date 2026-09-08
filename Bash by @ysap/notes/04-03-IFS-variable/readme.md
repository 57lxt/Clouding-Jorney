# IFS Variable
built in variable used to split characters or strings. by default it is set to space
usage 
```bash
array=(foo bar baz)
IFS=,
echo "array: ${array[*]}"
```
we can also __unset__ the IFS var with ```unset IFS```
