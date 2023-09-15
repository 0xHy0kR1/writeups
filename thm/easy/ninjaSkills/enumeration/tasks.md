
## Answer the questions about the following files:

- 8V2L
- bny0
- c4ZX
- D8B3
- FHl1
- oiMO
- PFbD
- rmfX
- SRSq
- uqyw
- v2Vb
- X1Uy

##### 1. Which of the above files are owned by the best-group group(enter the answer separated by spaces in alphabetical order)
**Command** - 
```python
find / -type f -group best-group 2>/dev/null
```

![[ninjaskills1.png]]

##### 2. Which of these files contain an IP address?
**Command** - 
```python
find / -type f \( -name "8V2L" -o -name "bny0"  -o -name "c4ZX"  -o -name "D8B3" -o -name "FHl1" -o -name "oiMO" -o -name "PFbD" -o -name "rmfX" -o -name "SRSq" -o -name "uqyw" -o -name "v2Vb" -o -name "X1Uy" \) -exec grep -EH '[0-9{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}' {} \; 2>/dev/null
```

![[ninjaskills2.png]]

- `-exec`: This is an option that tells `find` to execute another command on each file that matches the criteria specified earlier.
    
- `grep -E '[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}' {} \;`: This part of the command is executed for each file that matches the criteria. Here's what it does:
    
    - `grep`: This is a command used for searching text patterns in files.
    - `-E`: This option tells `grep` to use extended regular expressions, which allow for more complex pattern matching.
    - `'[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}'`: This is the regular expression pattern that `grep` is looking for. It matches sequences of numbers separated by periods (dot), which is how IP addresses are typically formatted. Each `[0-9]{1,3}` part means 1 to 3 digits (0-9).
    - `{}`: This is a placeholder where `find` will substitute the name of each matching file when executing the `grep` command.
    - `\;`: This marks the end of the `-exec` command.
- `2>/dev/null`: This part of the command redirects error messages (specifically, the standard error stream, which is represented as "2") to a special device file called `/dev/null`. This effectively suppresses any error messages, so you don't see them on the screen.

##### 3. Which file has the SHA1 hash of 9d54da7584015647ba052173b84d45e8007eba94?
Similar to the previous question, but instead we will calculate the hash of each file and compare it with the one given
**Command** - 
```python
find / -type f -exec sha1sum {} \; 2>/dev/null | grep 9d54da7584015647ba052173b84d45e8007eba94
```


##### 4. Which file contains 230 lines?
To get number of lines for a file in Linux, we can use “wc” command, there are many ways but this is the easier, so let’s construct the command

**Searching among all files** - 
```python
find / -type f -exec wc -l {} \; 2>/dev/null | grep -w 230
```
- wc -l (small L) to count the lines of each file
- grep -w is to search for a specific word, not a sub string ( 230 will show but 2303 won’t)

**Searching among specific files** - 
```python
find / -type f \( -name "8V2L" -o -name "bny0"  -o -name "c4ZX"  -o -name "D8B3" -o -name "FHl1" -o -name "oiMO" -o -name "PFbD" -o -name "rmfX" -o -name "SRSq" -o -name "uqyw" -o -name "v2Vb" -o -name "X1Uy" \) -exec wc -l  {} \; 2>/dev/null
```

![[ninjaskills3.png]]
all of them are 209, but there’s one file missing which is “bny0”, s i tried it and luckily that was the answer

##### 5. Which file's owner has an ID of 502?
**Command** - 
```python
find / -type f \( -name "8V2L" -o -name "bny0"  -o -name "c4ZX"  -o -name "D8B3" -o -name "FHl1" -o -name "oiMO" -o -name "PFbD" -o -name "rmfX" -o -name "SRSq" -o -name "uqyw" -o -name "v2Vb" -o -name "X1Uy" \) -exec ls -ln {} \;  2>/dev/null
```
ls -ln , l is to print it as a list, and n is to display numeric user ID and group ID

![[ninjaskills4.png]]

##### 6. Which file is executable by everyone?
Previous one also solve this question
![[ninjaskills5.png]]
answer is 8V2L