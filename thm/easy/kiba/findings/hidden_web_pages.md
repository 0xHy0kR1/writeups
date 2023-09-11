## Default web page on port 80
![[kiba4.png]]
Enumerating port 80, we get a screen which looks like this, this screen has a clue which will be uncover at the later part.

further enumerating on port **80** for sub-directories did not yield any desired results, so let’s try our hands on other ports as well.

## Default web page on port 5601
![[kiba5.png]]
When enumerating the port **5601** on the browser leads us to an attractive UI which seems to be a data visualization dashboard called **Kibana**.

**The management tab from the dashboard leads us to the management page which discloses the version of Kibana**
![[kiba6.png]]
Now that we know the version of the software, a google search for exploits would lead us to the exploit.
[[user_own_with_RCE_on_kibana]]