![[lianyu1.png]]

## Further dir listing in /island
**Command** - 
```python
gobuster dir -u http://10.10.32.22/island -w /usr/share/wordlists/dirb/common.txt -t 64 
```

**Output** - 
```python
/.hta                 (Status: 403) [Size: 199]
/.htaccess            (Status: 403) [Size: 199]
/.htpasswd            (Status: 403) [Size: 199]
/index.html           (Status: 200) [Size: 345]
/2100                 (Status: 301) [Size: 239] [--> http://10.10.32.22/island/2100/]

```

## Further dir listing in /2100 with .ticket
**Command** - 
```python
gobuster dir -u http://10.10.32.22/island/2100 -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -t 64 -x .ticket
```

**Output** -
```python
/green_arrow.ticket   (Status: 200) [Size: 71]
```


