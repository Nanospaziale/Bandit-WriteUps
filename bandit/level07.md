rssh***
# bandit_level6->7
***
<img width="733" height="234" alt="image" src="https://github.com/user-attachments/assets/0271756d-6352-44f5-99b6-905675f57372" />  
  
This level is very similar to the previous one, except for the proprerties of the file we are searching for.    
- Owned by user bandit7  
- Owned by group bandit6  
- 33 bytes in size  

If we try running `ls`, we can see that there are no files or directories.  
Indeed, as mentioned in the level description, we need to search for the file across the entire server.  
<img width="211" height="60" alt="image" src="https://github.com/user-attachments/assets/eb108f4d-62dd-4cc1-b825-109cef99266f" />  

In this particular case, we have to search in the root folder **/** (Root directory by default in most unix system, but it can be changed. [Unix filesystem](https://en.wikipedia.org/wiki/Unix_filesystem)).

We can use `find` again, but in this case we need to change some options.
If we look through the man page of `find` we can see that to search for our file we can use 2 particular oprions:
- **group gname** - In this case gname is bandit6 (gname stands for group-name)  
<img width="652" height="63" alt="image" src="https://github.com/user-attachments/assets/aa629f4a-023f-449c-a84c-8a29b3a953a2" />  

- **user uname** - In this case uname is bandit7 (uname stands for user-name)  
<img width="625" height="68" alt="image" src="https://github.com/user-attachments/assets/675bb342-fc68-4360-bec8-920253254aab" />  





<img width="600" height="1349" alt="image" src="https://github.com/user-attachments/assets/fcf32e85-5d9e-45e2-b5b7-dba2ae57138a" />





