# Case Statments
Syntax:
```bash
case "$char" in
  case1)
    echo hi
    ;;
  case2)
    echo hellow
    ;;
   *) #default case
     echo error
     ;;
esac
```

example:
```bash
case "$name" in
  d* | a* ) hello "$name";; #hello is a function, | - is or
  b*) hello "$name;;
  *) goodbye "$name";;
```

notes
- Instead of ```;;```, using ```;&``` will continue to the next case and check it with the same argument.
- ```;;&``` to exec all matching cases
