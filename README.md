# Our own simple shell

This is a simple shell we made for our final project in C

### About

The program recreates the basic functionality found in the traditional Unix shell.

### Compilation
Our simple shell is compiled this way:
```
gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh
```

### Output
The program should have the exact same output as `sh` as well as the exact same error output. The only difference is when it prints an error, the name of the program must be equivalent the `argv[0]`.

Example of error with `sh`:
```
$ echo "qwerty" | /bin/sh
/bin/sh: 1: qwerty: not found
$ echo "qwerty" | /bin/../bin/sh
/bin/../bin/sh: 1: qwerty: not found
$
```

Same error with our program:
```
$ echo "qwerty" | ./hsh
./hsh: 1: qwerty: not found
$ echo "qwerty" | ./././hsh
./././hsh: 1: qwerty: not found
$
```
### Testing
Our shell should work like this in interactive mode:
```
$ ./hsh
($) /bin/ls
hsh main.c shell.c
($)
($) exit
$
```

But also in non-interactive mode:
```
$ echo "/bin/ls" | ./hsh
hsh main.c shell.c test_ls_2
$
$ cat test_ls_2
/bin/ls
/bin/ls
$
$ cat test_ls_2 | ./hsh
hsh main.c shell.c test_ls_2
hsh main.c shell.c test_ls_2
$
```

### Examples
```
$ /bin/pwd
/home/vagrant/shell
```


### Authors
[Abinet Tesfu](https://github.com/Abinet508)
[Melat Samuel](https://github.com/melatsam)
