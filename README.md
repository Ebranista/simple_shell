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

```
$ ls -la
total 108
drwxr-xr-x 4 root root  4096 Oct 25 09:15 .
drwx------ 1 root root  4096 Oct 25 09:15 ..
drwxr-xr-x 2 root root    28 Oct 25 08:54 authors
-rw-r--r-- 1 root root   256 Oct 25 08:55 AUTHORS
-rwxr-xr-x 1 root root   436 Oct 25 21:46 check_type.c
-rw-r--r-- 1 root root   431 Oct 25 20:02 exec_cmd.c
-rwxr-xr-x 1 root root   239 Oct 25 21:46 exiter.c
-rw-r--r-- 1 root root   232 Oct 25 22:16 free_args.c
-rw-r--r-- 1 root root 12288 Oct 25 23:29 .free_args.c.swp
-rwxr-xr-x 1 root root   627 Oct 25 21:13 _getpath.c
drwxr-xr-x 8 root root   220 Oct 25 08:56 .git
-rwxr-xr-x 1 root root 18448 Oct 25 23:18 hsh
-rwxr-xr-x 1 root root   382 Oct 25 21:46 init_shell.c
-rw-r--r-- 1 root root   504 Oct 25 20:10 is_builtin.c
-rw-r--r-- 1 root root  1378 Oct 25 08:27 main.c
-rw-r--r-- 1 root root  1657 Oct 25 08:56 man_1_simple_shell
-rwxr-xr-x 1 root root   856 Oct 25 21:12 pathcat.c
-rwxr-xr-x 1 root root   350 Oct 25 21:12 print_env.c
-rw-r--r-- 1 root root   603 Oct 25 09:15 README.md
-rw-r--r-- 1 root root  1326 Oct 25 22:03 shell.h
-rwxr-xr-x 1 root root  2040 Oct 25 23:15 strings.c
-rw-r--r-- 1 root root   855 Oct 25 23:18 token_maker.c
-rw-r--r-- 1 root root   383 Oct 25 20:20 ver_paths.c
```

```
$ Ethio
./hsh: No such file or directory
```

### Authors
[Abinet Tesfu](https://github.com/Abinet508)
[Melat Samuel](https://github.com/melatsam)
