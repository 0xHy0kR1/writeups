## Surface level dir listing 
**Command** - 
```python
gobuster dir -u http://10.10.44.27 -w /usr/share/wordlists/dirb/small.txt -t 64
```

**Output** - 
```python
/archive              (Status: 301) [Size: 118] [--> /]
/blog                 (Status: 200) [Size: 5389]
/install              (Status: 302) [Size: 126] [--> /umbraco/]
/sitemap              (Status: 200) [Size: 1035]
/search               (Status: 200) [Size: 3464]
```