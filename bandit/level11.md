***
# bandit_level10->11
***
<img width="661" height="145" alt="image" src="https://github.com/user-attachments/assets/a9571a53-e435-40e4-97dd-a62653a8a621" />

In this level, the password is stored in the usual file ***data.txt***, which contains Base64-encoded data.
Executing `ls` as usual show the file in the home directory.  
  
<img width="223" height="79" alt="image" src="https://github.com/user-attachments/assets/7827e83f-84b9-44e1-af51-1f1949717343" />  

We can run `file` on ***data.txt*** to confirm its type before decoding the Base64 content. (This part isn’t strictly necessary, but it’s a habit of mine to do it.)
  
<img width="332" height="78" alt="image" src="https://github.com/user-attachments/assets/d856e3ca-bbfb-461b-b111-f458a65681fa" />  

Now, if we print the file's contents to the screen, we can see some readable characters, but they don’t make sense. At this point, we need to understand what Base64 is and how it works.
  
<img width="695" height="99" alt="image" src="https://github.com/user-attachments/assets/44614b1e-497c-4bbd-bf70-e5adad340434" />  

<details>
  <summary> What is Base64 Encoding?  </summary>

> Understanding what Base64 is and how it works isn’t essential to retrieve the password for this level.  
> However, it can be useful for future levels or challenges that involve Base64.  
> **Base64** has the purpose to encode binary data or simply text into printable charachters.  
> But how does it encode the data?  
> Let's take as example the word MAN  
> The first thing to do it's to take it's binary code in ASCII, that is M=0100 1101, A=0100 0001,N=0100 1110.  
> It is important to represent the letter in 8 bits and not 7. (Look at [ASCII's story](https://en.wikipedia.org/wiki/ASCII) to understand why the first ASCII characters were represented with 7 bits instead of 8.)
> 
</details>
<img width="810" height="396" alt="image" src="https://github.com/user-attachments/assets/a3f8f9b1-4506-45a3-8f4e-f35f5d028527" />  
<img width="490" height="82" alt="image" src="https://github.com/user-attachments/assets/83b15e6b-bd24-4897-9dae-47b415cc44cd" />   

  













