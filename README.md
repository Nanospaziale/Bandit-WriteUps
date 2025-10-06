Hello from NanoSpaziale!

Below you will find my solutions for the Bandit challenges from the site overthewire.org

<img width="1658" height="526" alt="image" src="https://github.com/user-attachments/assets/cb9b3d65-34af-4a68-8fc9-063f1d5221dd" />

***
In this guide, you won’t find the best solution or the most performant, easy-to-code solution for the level; instead, you should expect something made by someone (me) who is still learning all this stuff. Enjoy!
***
# Bandit level 0
Level 0 is not a proper level. We should consider it an introduction to understanding how to connect to a server online through an SSH ([Secure Shell](https://en.wikipedia.org/wiki/Secure_Shell))tunnel.
<img width="1697" height="405" alt="image" src="https://github.com/user-attachments/assets/505b9ae9-08c4-4b35-b97e-20fc0ba04139" />

As we can see in the first image, we can use the man page for a command to understand its functionality and all the various options that the command can provide us.
Of course, we can use any search engine to explore videos and tutorials on how to use something 
>Note: The man page explore every functionality of a command, but in most cases, it is not the best way to understand how a command works

The tipical use of `ssh` is `ssh login_name@server_address`. If no port is specified, the SSH command, as standard, uses port 22/TCP.

