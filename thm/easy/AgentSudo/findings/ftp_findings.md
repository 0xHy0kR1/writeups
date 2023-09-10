![[agentSudo10.png]]
By viewing the “To_agentJ.txt” file the message was login password for the chris is stored in the fake picture.

## To_agentj.txt
![[agentSudo11.png]]

## Extracting cutie.png with binwalk - 
So we use “Steghide” to retrieve some hidden info and also checked by “ExifTool” for the “cutie.png” file but nothing came up after we tried with “binwalk” and we got a zip file inside the “cutie.png” file and extracted it from “cutie.png” but it was encrypted.
![[agentSudo12.png]]

## extracting the zip file - 
We got “a” a password so we tried to extract the zip file but unzip command didn’t work so we used this command
![[agentSudo13.png]]

**After entering the password and extracting the zip file we got this message.**
![[agentSudo15.png]]

This message was from Agent R we decoded this ‘Q*******’ message using Cyberchef. Cyberchef suggests auto decoding.
--> Area51

**We got the password Now only images file left is “cute-alien.jpg” so we used the “steghide” tool to retrieve hidden info.**
![[agentSudo16.png]]
ssh credentials - 
