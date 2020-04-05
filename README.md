# Daniel-Roberts

Once the vagrant machines were up and running I used the Vagrant SSH command to log into my machine and get the ip address to attack(https://imgur.com/3bNg8pZ)
- I was able to use that IP to run my wpscan (https://github.com/danielroberts000/Daniel-Roberts/blob/master/wpscan_wordpress.txt) Image(https://imgur.com/1UL1z4M)
- Next was going to use searchsploit to find some potential vulnerabilities (Image(https://imgur.com/LxdYrmS)



1.) Admin Password Attack
   - First step was to change the Admin Password. I didn't want to change it to something crazy complicated since this was for testing but I pulled a random password form the rockyou.txt repo on Kali. In this case I used "scorpio"
   - From there I setup burp as a proxy, opened up the Admin page and logged in with the new password. I was successfully able to capture the login information through burp, which surprisingly was sent in plain text.(https://imgur.com/A8pdOFv)
  
2.) 
