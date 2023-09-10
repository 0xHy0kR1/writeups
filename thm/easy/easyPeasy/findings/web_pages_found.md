## hidden directory contents
![[easyPeasy3.png]]
The /hidden directory pops up. Upon visiting this page, we see nothing but a picture. The “view source” doesn't bring us any further… Could there be another directory hidden after this one? I run the same gobuster command but this time on the /hidden directory:

[[easyPeasy/enumeration/dir_list_gobuster|dir_list_gobuster]]

## Flag1 found in /whatever - 
![[easyPeasy5.png]]
After decrypting it, we get the first flag --> 
![[easyPeasy6.png]]

## Found another hashed text on 65524 of robots.txt - 
![[easyPeasy14.png]]
### flag2 in above md5 hash
![[easyPeasy15.png]]
## flag3 found 65524 port of source code - 
![[easyPeasy7.png]]

## Hidden directory hashed in 65524 port of source code 
![[easyPeasy8.png]]
It is base62 encoded. 

### Decoding base62 encoded text with cyberchef - 
![[easyPeasy9.png]]

## After visiting /n0th1ng3ls3m4tt3r
![[easyPeasy10.png]]
After decrypting this hashed text, we get another text and I guess this may be the passphrase for the image.
![[easyPeasy11.png]]

## Extracting data from image 
![[easyPeasy12.png]]
username must be ssh username and binary encoded text must be password.

### Cracking the binary encoded text
![[easyPeasy13.png]]
ssh username - boring
ssh password - iconvertedmypasswordtobinary