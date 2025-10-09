# Module Name
File Globbing 

## Challenge Name                                                   
1.Matching with *
### Solve
First we need to chane the directory and use use /challenge/run to get the flag
#### Commands run: 

```sh
$cd /ch*
$/challenge/run
```
## Flag: 

```
 pwn.college{kNbpcpcJsUtQ4q6AUX_8mVEsz6d.QXxIDO0wSM1AzNzEzW}   
```
### New Learnings

### References 
Took reference fromn the pwn.collenge site 


## Challenge 2
2.Matching with ?
### Solve
First we need to change the directry using ? and then we need to input the required command to get the flag

#### Commands run: 

```sh
$ cd /?ha??enge
$ /challenge/run
```
## Flag: 

```
pwn.college{MTV8MtY1r4mN1q7aVJvMq9Yj6Wi.QXyIDO0wSM1AzNzEzW}
```
### New Learnings

### References 
Took reference fromn the pwn.collenge site 

## Challenge 
3. Matching with []

### Solve
We need to change into the required directory and then from there we need to use `[]` to catch the flag
#### Commands run: 

```sh
$cd /challenge/files
$ /challenge/run file_[bash]
```
## Flag: 

```
pwn.college{UtpupSgtxF50kNaiK2SS9CoPcKo.QXzIDO0wSM1AzNzEzW}
```
### New Learnings

### References 
Took reference fromn the pwn.collenge site 



## Challenge 
4. Matching paths with []

### Solve
we need to mention the path of the file with [] to get the flag 

#### Commands run: 

```sh
$ /challenge/run /challenge/files/file_[bash]

```
## Flag: 

```
pwn.college{0GW3BZ9KP3APRmBr2O3MzlP-DZr.QX0IDO0wSM1AzNzEzW}
```
### New Learnings

### References 
Took reference fromn the pwn.collenge site 




## Challenge 
5. Multiple globs

### Solve
In this first you have to change to the required directory then write using the conditions given in the question use globs and get the flag
#### Commands run: 

```sh
$ cd /challenge/files
$ /challenge/run *p*
```
## Flag: 

```
pwn.college{Iiq5NWYlrLX20Exzri-yktCsrCo.0lM3kjNxwSM1AzNzEzW}
```
### New Learnings

### References 
Took reference fromn the pwn.collenge site 





## Challenge 
6. Mixing globs

### Solve

#### Commands run: 

```sh
$  cd /challenge/files
$ /challenge/run [cep]*
```
## Flag: 

```
pwn.college{UELqMgoTTFT_8-u16CwhrP5Nn7R.QX1IDO0wSM1AzNzEzW}
```
### New Learnings
Learnt exactly how the globs * work 
### References 
Took reference fromn the pwn.collenge site 



## Challenge 
7. Exclusionary globbing 

### Solve
You need to first change the directory and then you have to use ! or ^ to get the flag
#### Commands run: 

```sh
$ cd /challenge/files
$ /challenge/run [^pwn]*
```
## Flag: 

```
pwn.college{wtscsZb9vqUhiseGycS2CMcsTxw.QX2IDO0wSM1AzNzEzW}
```
### New Learnings

### References 
Took reference fromn the pwn.collenge site 


## Challenge 
8. Tab completion 

### Solve
go through the hints in the question and solve the question 
#### Commands run: 

```sh
$ cat /challenge/pwn<TAB>
$ cat /challenge/pwncollege<TAB>
$ and then enter 
```
## Flag: 

```
pwn.college{MEwHNd6LDXl6IT252Vk7a3L43kn.0FN0EzNxwSM1AzNzEzW}
```
### New Learnings

### References 
Took reference fromn the pwn.collenge site


## Challenge 
9. Multiple options for tab completionn

### Solve
go through the hints in the question and solve the question 
#### Commands run: 

```sh
$ cat /challenge/files/pwn<TAB>
$ cat /challenge/files/pwncollege-flag<tab>
$  cat /challenge/files/pwncollege-flag<ENTER>
```
## Flag: 

```
pwn.college{81atbJ_7LPYDuEOD4n-j4y3Zdmj.0lN0EzNxwSM1AzNzEzW}
```
### New Learnings

### References 
Took reference fromn the pwn.collenge site




## Challenge 
10. Tab completion on commands

### Solve
Type the comman pwncollege and press tab and then press enter
#### Commands run: 

```sh
$ pwmcollege<TAB>
$ pwncollege-16144<enter>
```
## Flag: 

```
pwn.college{8tmiTJh9BMO6Wp2OJhXx203JSq7.0VN0EzNxwSM1AzNzEzW}
```
### New Learnings

### References 
Took reference fromn the pwn.collenge site





