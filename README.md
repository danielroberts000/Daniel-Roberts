# Daniel-Roberts

Admin Password Attack
  1. First step was to change the Admin Password. I didn't want to change it to something crazy complicated since this was for testing but I pulled a random password form the rockyou.txt repo on Kali. In this case I used "scorpio"
  2. From there I setup burp as a proxy, opened up the Admin page and logged in with the new password. I was successfully able to capture the login information through burp, which surprisingly was sent in plain text.(https://i.imgur.com/A8pdOFv.png)
  
