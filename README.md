# Our own simple shell

This is our self owned simple shell in C language.

### About

Shell is a user interface to use the services of a computer. It can be a command-line interface –the one we will build- or graphical user interface, like regular software such as Windows Office.

### Compilation
This simple shell is compiled with:
```
gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh
```

### Output
This program have exact same output as ```sh``` as well as the exact same error output. The only difference is when it prints an error, the name of the program is equivalent to ```argv[0]```.

#### Example of error with ```sh```:
```
$ echo "qwerty" | /bin/sh
/bin/sh: 1: qwerty: not found
$ echo "qwerty" | /bin/../bin/sh
/bin/../bin/sh: 1: qwerty: not found
$
```

#### Error with our program:

```
$ echo "qwerty" | ./hsh
./hsh: 1: qwerty: not found
$ echo "qwerty" | ./././hsh
./././hsh: 1: qwerty: not found
$
```
### Testing
#### Our shell work like this in interactive mode:
```
$ ./hsh
($) /bin/ls
hsh main.c shell.c
($)
($) exit
$
```

#### But also in non-interactive mode:
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

```
$ ls -la
total 108
-rw-r--r-- 1 abina 197609  361 Oct 25 11:21 _getpath.c
-rw-r--r-- 1 abina 197609  154 Oct 25 11:26 AUTHORS
-rw-r--r-- 1 abina 197609  345 Oct 25 11:21 check_type.c
-rw-r--r-- 1 abina 197609  193 Oct 25 11:20 checkC.c
-rw-r--r-- 1 abina 197609  376 Oct 25 11:21 checkD.c
-rw-r--r-- 1 abina 197609  425 Oct 25 11:21 exec_cmd.c
-rw-r--r-- 1 abina 197609  218 Oct 25 11:22 exiter.c
-rw-r--r-- 1 abina 197609  232 Oct 25 11:21 free_args.c
-rw-r--r-- 1 abina 197609  203 Oct 25 11:22 init_shell.c
-rw-r--r-- 1 abina 197609  502 Oct 25 11:22 is_builtin.c
-rw-r--r-- 1 abina 197609 1083 Oct 25 11:21 main.c
-rw-r--r-- 1 abina 197609 1521 Oct 25 12:10 man_1_simple_shell
-rw-r--r-- 1 abina 197609  611 Oct 25 11:25 pathcat.c
-rw-r--r-- 1 abina 197609  273 Oct 25 11:24 print_env.c
-rw-r--r-- 1 abina 197609 2891 Oct 30 09:46 README.md
-rw-r--r-- 1 abina 197609 1379 Oct 25 11:23 shell.h
-rw-r--r-- 1 abina 197609 1613 Oct 25 11:23 strings.c
-rw-r--r-- 1 abina 197609  841 Oct 25 11:24 token_maker.c
-rw-r--r-- 1 abina 197609  383 Oct 25 11:24 ver_paths.c
```

```
$ Ethio
./hsh: No such file or directory
```

### Authors
[Abinet Tesfu](https://github.com/Abinet508)
[Melat Samuel](https://github.com/melatsam)
