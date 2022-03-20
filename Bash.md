### Running Several Commands in Sequence

1. We need to run them in that order, but don’t want to wait around for `long` to finish before starting the other commands. We could use a shell script (aka batch file). Here’s a primitive way to do that:

```
$ cat > simple.script
  long
  medium
  short
  ^D                      # Ctrl-D, not visible
$ bash ./simple.script
```

2. Another solution is to run each command in sequence. If you want to run each program, regardless if the preceding ones fail, separate them with semicolons.
```
$ long ; medium ; short
```
Or
```
$ long
  medium
  short
```

3. If you only want to run the next program if the preceding program worked, and all the programs correctly set exit codes, separate them with double-ampersands.
```
$ long && medium && short
```
Or
```
$ long && 
  medium && 
  short
```



# Reference
- https://www.oreilly.com/library/view/bash-cookbook/0596526784/ch04s03.html
