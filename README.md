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
-rw-r--r-- 1 abina 197609  487 Oct 30 11:10 _dollar_special.c
-rw-r--r-- 1 abina 197609  824 Oct 30 11:10 _get_history_lines_count.c
-rw-r--r-- 1 abina 197609  363 Oct 30 11:10 _getenv.c
-rw-r--r-- 1 abina 197609  818 Oct 30 11:11 _handle_var_replacement.c
-rw-r--r-- 1 abina 197609 1745 Oct 30 11:11 _help.c
-rw-r--r-- 1 abina 197609 1587 Oct 30 11:09 _history.c
-rw-r--r-- 1 abina 197609  750 Oct 30 11:11 _own_memory.c
-rw-r--r-- 1 abina 197609  232 Oct 30 11:13 _puts.c
-rw-r--r-- 1 abina 197609  351 Oct 30 11:11 _strcpy.c
-rw-r--r-- 1 abina 197609  448 Oct 30 11:12 _strncpy.c
-rw-r--r-- 1 abina 197609 1327 Oct 30 11:12 _strtok.c
-rw-r--r-- 1 abina 197609  491 Oct 30 11:12 _write_history.c
-rw-r--r-- 1 abina 197609  158 Oct 30 11:37 AUTHORS
-rw-r--r-- 1 abina 197609 3978 Oct 30 11:15 builtins.c
-rw-r--r-- 1 abina 197609 3934 Oct 30 11:16 f_alias_list.c
-rw-r--r-- 1 abina 197609 1083 Oct 30 11:16 f_builtin_utils.c
-rw-r--r-- 1 abina 197609 3018 Oct 30 11:16 f_command_handlers.c
-rw-r--r-- 1 abina 197609  754 Oct 30 11:14 f_error.c
-rw-r--r-- 1 abina 197609 1372 Oct 30 11:15 f_exit.c
-rw-r--r-- 1 abina 197609 1910 Oct 30 11:15 f_handle_builtins.c
-rw-r--r-- 1 abina 197609  502 Oct 30 11:14 f_handle_comment.c
-rw-r--r-- 1 abina 197609  316 Oct 30 11:16 f_handle_enter.c
-rw-r--r-- 1 abina 197609 4138 Oct 30 11:21 f_handle_shell_logical_operators.c
-rw-r--r-- 1 abina 197609 1271 Oct 30 11:21 f_linked_lists.c
-rw-r--r-- 1 abina 197609 1399 Oct 30 11:19 f_memory.c
-rw-r--r-- 1 abina 197609  727 Oct 30 11:17 f_special.c
-rw-r--r-- 1 abina 197609 1809 Oct 30 11:17 f_strings.c
-rw-r--r-- 1 abina 197609 1238 Oct 30 11:17 f_strings_creations.c
-rw-r--r-- 1 abina 197609 1002 Oct 30 11:18 f_strings2.c
-rw-r--r-- 1 abina 197609 2156 Oct 30 11:18 main.c
-rw-r--r-- 1 abina 197609 1752 Oct 30 11:37 man_1_simple_shell
-rw-r--r-- 1 abina 197609 2657 Oct 30 11:37 README.md
-rw-r--r-- 1 abina 197609 4088 Oct 30 11:25 shell.h
```

```
$ Ethio
./hsh: No such file or directory
```

### Authors
[Abinet Tesfu](https://github.com/Abinet508)
[Melat Samuel](https://github.com/melatsam)
