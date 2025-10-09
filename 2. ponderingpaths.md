# Challenge 1 The Root

In this challenge, you will learn to navigate to the root directory. The root directory is the top-level directory in the Linux filesystem, represented by a single forward slash `/`.

## Solution:

The user needs to navigate to the root directory and run the challenge.

#### Commands run: 

```sh
$ /pwn
```

## Flag: 

```
pwn.college{8BM0b4YQwOFFUrBGxukp913MCru.QX4cTO0wSM1AzNzEzW}
```

### Notes:

- The root directory is accessed using `/`
- Absolute paths start from the root directory

# Challenge 2 Program and Absolute Paths

In this challenge, you will learn to run programs using their absolute paths. An absolute path specifies the complete path from the root directory to the target file.

## Solution:

The user needs to run the challenge program using its absolute path.

#### Commands run: 

```sh
$ /challenge/run
```

## Flag: 

```
pwn.college{IvHPDczlERP72OTdqkENwhsjloX.QX1QTN0wSM1AzNzEzW}
```

### Notes:

- Absolute paths always start with `/`
- You can run programs by specifying their full path

# Challenge 3 Position Me

In this challenge, you will learn to change directories using the `cd` command and then run programs from different locations.

## Solution:

The user needs to change directory to `/etc` and then run the challenge.

#### Commands run: 

```sh
$ /challenge/run
$ cd /usr/share/zoneinfo/posix/Asia
$ /usr/share/zoneinfo/posix/Asia$ /challenge/run
```

## Flag: 

```
pwn.college{k741Q-xC8FapkfiNvo27UUTg_R5.QX2QTN0wSM1AzNzEzW}
```

### Notes:

- `cd` command is used to change directories
- You can run programs from any directory using absolute paths
- used the course material and the sensai for help 
# Challenge 4 Position Elsewhere

In this challenge, you will navigate to a more complex directory path and run the challenge from there.

## Solution:

The user needs to change to a specific process directory and run the challenge.

#### Commands run: 

```sh
$ /challenge/run
$ cd /usr/share/doc/fontconfig
$ /challenge/run
```

## Flag: 

```
pwn.college{0yrohpYtyn_tpM6uiaLrJIPD3lq.QX3QTN0wSM1AzNzEzW}
```

### Notes:


- You can navigate to deeply nested directories

# Challenge 5 Position Yet Elsewhere

In this challenge, you will practice navigating to the root directory and running the challenge.

## Solution:

The user needs to change to the root directory and run the challenge.

#### Commands run: 

```sh
$ /challenge/run
$ cd /var
$ /challenge/run
```

## Flag: 

```
pwn.college{EmE6Z_LXwzpTbBtSUxtIzHMZiZp.QX4QTN0wSM1AzNzEzW}
```

### Notes:


- All absolute paths start from the root directory

# Challenge 6 Implicit Relative Paths from Root

In this challenge, you will learn about relative paths and how they work from different directories.

## Solution:

The user needs to navigate to root and use a relative path to run the challenge.

#### Commands run: 

```sh
$ cd  /
$ chellenge/run
```

## Flag: 

```
pwn.college{cPcWktaS-ET4OZk9qOpHXCvfVPP.QX5QTN0wSM1AzNzEzW}
```

### Notes:

- Relative paths are relative to your current working directory

# Challenge 7 Explicit Relative Paths from Root

In this challenge, you will learn to use explicit relative paths and change directories in a single operation.

## Solution:

The user needs to change to the challenge directory and run the program relatively.

#### Commands run: 

```sh
$ cd /
$ ./challenge/run
```

## Flag: 

```

pwn.college{cjZ1HUXddFIb11hw9sxelfb1AcR.QXwUTN0wSM1AzNzEzW}
```

### Notes:

- 

# Challenge 8 IMPLICIT RELATIVE PATH
In this level, we'll practice referring to paths using . a bit more. This challenge will need you to run it from the /challenge directory. Here, things get slightly tricky.

Linux explicitly avoids automatically looking in the current directory when you provide a "naked" path. Consider the following:
```
hacker@dojo:~$ cd /challenge
hacker@dojo:/challenge$ run
```
This will not invoke /challenge/run. This is actually a safety measure: if Linux searched the current directory for programs every time you entered a naked path, you could accidentally execute programs in your current directory that happened to have the same names as core system utilities! As a result, the above commands will yield the following error:
```
bash: run: command not found
```

We'll explore the mechanisms behind this concept later, but in this challenge, we'll learn how to explicitly use relative paths to launch run in this scenario. 
## SOLUTION
The way to do this is to tell Linux that you explicitly want to execute a program in the current directory, using . like in the previous levels. Give it a try now!
###COMMANDS RUN
```
$ cd /challenge
$ run
$ ./run
```
###FLAG
```
pwn.college{AlqTYWiMLMQMKu56ebGRerWXNgf.QXxUTN0wSM1AzNzEzW}
```
###NOTES
Linux doesnt run some files whose names sometimes are same as that of some system programs, therefore to run them we have to implicitly 'tell' linux to run.

# Challenge 9 HOME SWEET HOME

In this challenge, you will use implicit relative paths with arguments to run the challenge program.

## Solution:

The user needs to run the challenge program with a specific argument using a relative path.

#### Commands run: 

```sh
$ /challenge/run ~/
$ /challenge/run ~/x
```

## Flag: 

```
pwn.college{AbHDfgosMmle4pae_VUfWug-fBO.QXzMDO0wSM1AzNzEzW}
```

### Notes:

- `~` represents the home directory
- Arguments can be paths to files or directories
- You can pass arguments to programs when running them
