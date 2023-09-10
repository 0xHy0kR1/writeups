# Enumeration - 
## Source code findings
**username** - R1ckRul3s
password - Wubbalubbadubdub --> **At robots.txt** 
## dirb findings
**Command** - 
```python
dirb http://10.10.249.128/
```

**Output** - 
```python
==> DIRECTORY: http://10.10.249.128/assets/                                                                                                            
+ http://10.10.249.128/index.html (CODE:200|SIZE:1062)                                                                    
+ http://10.10.249.128/robots.txt (CODE:200|SIZE:17)                                                                                
+ http://10.10.249.128/server-status (CODE:403|SIZE:301)       
```

### Running dirb for login.php
**Command** - 
```python
dirb http://10.10.249.128/ -X .php
```

**Output** - 
```python
+ http://10.10.249.128/denied.php (CODE:302|SIZE:0)                                                                                         
+ http://10.10.249.128/login.php (CODE:200|SIZE:882)                                                                                               
+ http://10.10.249.128/portal.php (CODE:302|SIZE:0)          
```

## nmap findings
![[temp1.png]]

## Exploitation
#### Popping a reverse shell
![[rickPickle.png]]

#### In the terminal
###### First ingredient
![[rickPickle2.png]]

###### Second ingredient
![[rickPickle3.png]]

##### Third ingredient
We need to escalate our privilege for that but we there is no password is required to get the root shell.
![[rickPickle4.png]]

