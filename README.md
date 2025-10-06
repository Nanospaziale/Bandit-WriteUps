Hello from NanoSpaziale!

Below you will find my solutions for the Bandit challenges from the site overthewire.org

What is Bandit?
I believe that if you're here, you already know what Bandit is and how it works. However, Bandit is a free wargame from the site [Over the wire](overthewire.org/wargames/bandit) that can help you develop hacking skills and a basic understanding of Linux.
***
**In this guide, you won’t find the best solution or the most performant, easy-to-code solution for the level; instead, you should expect something made by someone (me) who is still learning all this stuff. Enjoy!**
***
# bandit_level0
***
Level 0 is not a proper level. We should consider it an introduction to understanding how to connect to a server online through an SSH ([Secure Shell](https://en.wikipedia.org/wiki/Secure_Shell)) tunnel.
<img width="1697" height="405" alt="image" src="https://github.com/user-attachments/assets/505b9ae9-08c4-4b35-b97e-20fc0ba04139" />

As we can see in the first image, we can use the man page for a command to understand its functionality and all the various options that the command can provide us.

Of course, we can use any search engine to explore videos and tutorials on how to use something 
>Note: The man page explore every functionality of a command, but in most cases, it is not the best way to understand how a command works

The tipical use of `ssh` is `ssh login_name@server_address`. If no port is specified, the SSH command, as standard, uses port 22/TCP.
Since level 0 needs us to connect through a specific port (2220) , we can check the man page to see if there’s an option for that.

<img width="1026" height="246" alt="image" src="https://github.com/user-attachments/assets/1ac47899-31e7-42fd-b8d8-1cdb8ee5eb22" />
<img width="950" height="62" alt="image" src="https://github.com/user-attachments/assets/e51e2dd6-43e5-48d5-9dce-2433d2b36063" />

As we can see in the images above, the **-p** option can be used to specify a port.

So, our final command, will be: `ssh bandit0@bandit.labs.overthewire.org -p 2220`
>The username and password for this level are mentioned in the introduction of level 0 on the site, and they are **bandit0** and **bandit0**.

Once logged, we should see an image like this:

<img width="568" height="1183" alt="image" src="https://github.com/user-attachments/assets/6e0d41fb-089f-464c-a83d-39a68dfc1f86" />

Now that we're connected, we can dive into the challenges across all the levels!
***
# bandit_level1
***
This level tells us that the password is located in the home directory inside a file called "readme." By typing the command `ls`, we can print a list of files stored in the current directory. 
>The `pwd` command (Print Working Directory) can help us find out where we are.

<img width="163" height="48" alt="image" src="https://github.com/user-attachments/assets/998d724d-12e9-45f0-b734-a9edd7c0ff28" />


Now we can print directly the content of the file, but if we want to be sure that the file listed a moment ago is a readable file, we can check with the command `file`

<img width="211" height="47" alt="image" src="https://github.com/user-attachments/assets/04c31232-89df-442c-8584-00554daa4a75" />

As we can see, the command `file` helps us determine the file type. Since the file type is [ASCII](https://en.wikipedia.org/wiki/ASCII) we can print to the screen it's content.
There is a bunch of commans that we can use for print the content of a file, here are some:

`cat` it's the most common command to print the content of a file.

<img width="588" height="146" alt="image" src="https://github.com/user-attachments/assets/6e1b0004-c1e2-4172-8b06-7e8d314ea92d" />

`tail` print the last 10 lines of a file.
<img width="586" height="146" alt="image" src="https://github.com/user-attachments/assets/e2482cd5-a930-4394-a15c-27baad9483c8" />

`head`, do the opposite of `tail` by printing the first 10 lines of the file.

<img width="586" height="143" alt="image" src="https://github.com/user-attachments/assets/87f0202e-f828-45f2-8e3d-1314a5334e72" />

`more` is an interactive command to explore the file. It will go in interactive mode, only if the screen size is not enough to print its content. Instead, if the screen size it is enough, it print and quit.

<img width="592" height="148" alt="image" src="https://github.com/user-attachments/assets/77831840-1102-4026-9b9d-4a00db9b60ed" />

`less` is a better version of `more`, because it enter interactive mode, regardless of whether the screen size is sufficient.

<img width="591" height="132" alt="image" src="https://github.com/user-attachments/assets/7f235f10-3b38-48a8-888a-d4c401a8a23f" />






















