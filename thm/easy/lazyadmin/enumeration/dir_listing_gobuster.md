### gobuster command - 
```python
gobuster dir -u http://10.10.76.177/ -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -t 50
```

### gobuster output - 
```python
/content              (Status: 301) [Size: 314] [-->http://10.10.76.177/content/]
```

![[lazyadmin5.png]]
I think it has CMS panel called sweet rice lets check further form the content endpoint. For that we are going to use again gobuster tool to find out

### gobuster command - 
```python
gobuster dir -u http://10.10.76.177/content -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -t 50
```

### gobuster output - 
```python
/images       (Status: 301) [Size: 321] [-->http://10.10.76.177/content/images/]
/js           (Status: 301) [Size: 317] [--> http://10.10.76.177/content/js/]
/inc          (Status: 301) [Size: 318] [--> http://10.10.76.177/content/inc/]
/as           (Status: 301) [Size: 317] [--> http://10.10.76.177/content/as/]
/_themes     (Status: 301) [Size: 322] [--> http://10.10.76.177/content/_themes/]
/attachment (Status: 301) [Size: 325] [->http://10.10.76.177/content/attachment/]

```
