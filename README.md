# Daniel-Roberts

Once the vagrant machines were up and running I used the Vagrant SSH command to log into my machine and get the ip address to attack
[SSH with IP](https://imgur.com/3bNg8pZ)
- I was able to use that IP to run my wpscan ( https://github.com/danielroberts000/Daniel-Roberts/blob/master/wpscan_wordpress.txt ) Image( https://imgur.com/1UL1z4M )
- Next was going to use searchsploit to find some potential vulnerabilities (https://github.com/danielroberts000/Daniel-Roberts/blob/master/searchsploit.txt) Image(https://imgur.com/LxdYrmS)

I figured a good place to start would be to attack the Admin password of Word press to determine what kind of access I could get

1.) Admin Password Attack
   - First step was to change the Admin Password. I didn't want to change it to something crazy complicated since this was for testing but I pulled a random password form the rockyou.txt repo on Kali. In this case I used "scorpio"
   - From there I setup burp as a proxy, opened up the Admin page and logged in with the new password. I was successfully able to capture the login information through burp, which surprisingly was sent in plain text.(https://imgur.com/A8pdOFv)
  

2.) p0wny script
- Next I wanted to see if i could get a Shell from the browswer and I figured the easiest way would be to find a section of the site that would allow me to upload php script
- I was able to find a section under Appearance and Editor. The easiest one to remember in here was the 404.php templte. i removed the default script and added the p0wny script there instead. (https://imgur.com/owDHwiO)
- From there it was a matter of navigating to that php page to get my shell. didn't even have to be logged in as admin to get to it. (https://imgur.com/Ifc4pNT) Shell (https://imgur.com/kk2FfHu)
- Running 'ls' command from shell (https://imgur.com/FyMyCup)

3.) Attacking the Core
- Next I wanted see if i could exploit vulnerabilities that was found with metasploit. The one that stood out to me the most was the Persistent Cross-Site Scripting which was number 36844 in the exploitdb
- so the first step was to go to exploitdb.com to see if I could get any information about that particular exploit and it turns out it had a lot of information on the expoit as well as a usefull script. (https://imgur.com/L1eIrfc)
- So I took that script and filled in the number of characaters that were needed and posted that in the comments section of the webpage..Script looked like this (https://github.com/danielroberts000/Daniel-Roberts/blob/master/message.txt) things happened pretty quick from there and the end result was this popup whenever anyone tried to click on anything (https://imgur.com/Hb9g6Op)
