# Module Name
Practicing Piping 
## Challenge Name                                                   
1. Redirecting Output
### Solve

#### Commands run: 

```sh
$ echo PWN > COLLEGE
```
## Flag: 

```
pwn.college{4RjxI_KYM39eqb6D9Zm2U88yt7E.QX0YTN0wSM1AzNzEzW}
```
### New Learnings

### References 
Took Reference from the pwn.college site 


## Challenge Name                                                   
2. Redirecting more output
### Solve


#### Commands run: 

```sh
$ /challenge/run > myflag
$ cat myflag
```
## Flag: 

```
pwn.college{kBHTF8ZyGqpG-i5Z5JxO5IYCnJv.QX1YTN0wSM1AzNzEzW}
```
### New Learnings

### References 
Took Reference from the pwn.college site 


## Challenge Name                                                   
3. Appending output
### Solve


#### Commands run: 

```sh
$ /challenge/run >> /home/hacker/the-flag
$  cat /home/hacker/the-flag
```
## Flag: 

```
pwn.college{skIeXe4BUpxnRTZ16pZKMYJKgcG.QX3ATO0wSM1AzNzEzW}
```
### New Learnings

### References 
Took Reference from the pwn.college site 

## Challenge Name                                                   
4. Redirecting errors
### Solve

#### Commands run: 

```sh
$ /challenge/run > myflag 2> instructions
$ cat myflag
```
## Flag: 

```
 pwn.college{IK6H9ep98MTuIl82IkdAqpS-35v.QX3YTN0wSM1AzNzEzW}
```
### New Learnings

### References 
Took Reference from the pwn.college site 


## Challenge Name                                                   
5. Redirecting input 
### Solve

#### Commands run: 

```sh
$ echo COLLEGE > PWN
$ /challenge/run < PWN
```
## Flag: 

```
pwn.college{4bmd5N83nf5gceLRxyVsYBYe19T.QXwcTN0wSM1AzNzEzW}
 ```
### New Learnings

### References 
Took Reference from the pwn.college site 

## Challenge Name                                                   
6. Grepping stored results 
### Solve

#### Commands run: 

```sh
$ /challenge/run > /tmp/data.txt
$ grep "pwn.college"* /tmp/data.txt

```
## Flag: 

```
pwn.college{sklK8Ves6pwBE2aWiWWrZ2xzvUp.QX4EDO0wSM1AzNzEzW}
 ```
### New Learnings

### References 
Took Reference from the pwn.college site 



## Challenge Name                                                   
7. Grepping live output
### Solve

#### Commands run: 

```sh
$  /challenge/run | grep "pwn.college"*
```
## Flag: 

```
 pwn.college{8kHejHEahQfZK--42PqrTJYGiea.QX5EDO0wSM1AzNzEzW}
 ```
### New Learnings

### References 
Took Reference from the pwn.college site 


## Challenge Name                                                   
8. Grepping errors   
### Solve

#### Commands run: 

```sh
$ /challenge/run 2>&1 | grep 'pwn.college{'

```
## Flag: 

```
 pwn.college{U-QajXMlWMEmL95_pgGTgQb7KNO.QX1ATO0wSM1AzNzEzW}
 ```
### New Learnings

### References 
Took Reference from the pwn.college site 



## Challenge Nameo                                                   
9. Filtering with grep-v 
### Solve

#### Commands run: 

```sh
$ /challenge/run | grep -v DECOY
```
## Flag: 

```
pwn.college{YsBjxAIMgN1S-0Q0cmAAf0vzfG6.0FOxEzNxwSM1AzNzEzW}
 ```
### New Learnings

### References 
Took Reference from the pwn.college site 


## Challenge Name                                                   
10. Duplicating piped data with tee 
### Solve

#### Commands run: 

```sh
$ /challenge/pwn | tee /dev/tty | /challenge/college
$ /challenge/pwn --secret ovwKd94k | tee /dev/tty | /challenge/college


```
## Flag: 

```
pwn.college{ovwKd94kjRgeN7slkCtamoDvqdi.QXxITO0wSM1AzNzEzW}
```
### New Learnings

### References 
Took Reference from the pwn.college site 


## Challenge Name                                                   
11. Process substitution for input 
### Solve
usse diff command between the command outputs and get the flags
#### Commands run: 

```sh
$ diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)

```
## Flag: 

```
 pwn.college{0-_AeTHv1tBTglQrMXpBAnf8U6E.0lNwMDOxwSM1AzNzEzW}
 ```
### New Learnings 

Took Reference from the pwn.college site 




## Challenge Name                                                   
12. Writing to multiple programs 
### Solve

#### Commands run: 

```sh
$  /challenge/hack | tee >(/challenge/the) | /challenge/planet


```
## Flag: 

```
pwn.college{w9cypGGglu1A3H6WwWJNf2cjW0H.QXwgDN1wSM1AzNzEzW}
 ```
### New Learnings

### References 
Took Reference from the pwn.college site 


## Challenge Name                                                   
13. Split piping stderr and stdout
### Solve
 
#### Commands run: 

```sh
$   /challenge/hack 2> >(/challenge/the) | /challenge/planet

```
## Flag: 

```
pwn.college{If5O0_OB9YdOyXV5TFoeQVJdFuI.QXxQDM2wSM1AzNzEzW}
 ```
### New Learnings


## Challenge Name                                                   
14. Named pipes
### Solve

#### Commands run: 

```sh
$  mkfifo /tmp/flag_fifo (Terminal 1)
$ cat /tmp/flag_fifo (Terminal 1)
$ /challenge/run > /tmp/flag_fifo (Terminal 2)


```
## Flag: 

```
pwn.college{I8HlQ3iarAYsgNlZIG_B_cDFuI2.01MzMDOxwSM1AzNzEzW}
 
 ```
### New Learnings

### References 
Took Reference from the pwn.college site 





