# Functions

use:
* code reuse


### Functions are mini programs 

example:  
```hello.sh```
```bash
#!/usr/bin/env bash
echo hello $1
```
```greeter.sh```
```bash
#!/usr/bin/env bash
for name in $@; do
  ./hello.sh "$name"
done
```

### Writing functions
```bash
greet(){
  echo "hello $1"
  return 0 #signals the functions exec correctly
}
for name in $@; do
  greet "$name"
done
```

## Things to study 
* scope of variable
