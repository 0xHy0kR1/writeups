## web page on port 80 and 8080
1. As always it is a default Apache page.
![[gallery3.png]]

2. When we visit to port 8080, it redirects to `http://10.10.128.56/gallery/login.php` and there we find cms used by website.
![[gallery4.png]]
In this login form we can perform sql injection to get access to the admin panel and for that we are going to use "sqlmap" or we can also use the exploits from exploit-db. 

