***
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

In this particular case, we have to search in the root folder **/** ( **/** is the root directory by default, but it can be changed. [Unix filesystem](https://en.wikipedia.org/wiki/Unix_filesystem)).





