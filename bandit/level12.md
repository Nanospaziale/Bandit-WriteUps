***
# bandit_level11->12
***  
<img width="994" height="158" alt="image" src="https://github.com/user-attachments/assets/725742e9-a41d-427f-9da5-0d4e976e26cd" />
  
We can do the usual:  
  
<img width="492" height="174" alt="image" src="https://github.com/user-attachments/assets/557b2020-594b-4c15-8fea-d6e7eb73acd6" />  
  
As we can see, we have another encrypted message. In this case [ROT13](https://en.wikipedia.org/wiki/ROT13) has been used to encrypt.  
  
***  
  
<details>
  <summary> Understanding ROT13 </summary>

> ROT13 is pretty easy to understand.  
> Basically, we need to shift each letter forward to the 13th position after it.  
> Following this table, we can understand how ROT13 works.
>   
> <img width="598" height="81" alt="image" src="https://github.com/user-attachments/assets/f2efcd85-04e9-4ab5-8e56-45b393b504d6" />  
>  
> Capital ***A*** became a capital ***N***.  
>     
> In fact, if we create a table with numbers, we can see it more clearly.  
> |1|2|3|4|5|6|7|8|9|10|11|12|13|14|15|16|17|18|19|20|21|22|23|24|25|26|  
> |-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|  
> |A|B|C|D|E|F|G|H|I|J|K|L|M|N|O|P|Q|R|S|T|U|V|W|X|Y|Z|
>
> So, if we take the letter ***A*** and shift its position by 13 places, we land in the position 14 or letter ***N***.

</details>
  
***  
  
Now that we understand how ROT13 works, we need to figure out how to shift each letter of our phrase 13 positions forward.  
If we look at the Wikipedia page for ROT13, in the *Implementation* section, we can read about two methods:  
- `tr` command  
- `vi` (or `vim`) text editor  
  
Of course, there are many other methods available, I just chose the two simplest ones for me.  
  
***  
  
Let's analyze the first: `tr`
`tr` helps us to translate characters.  
  
<img width="440" height="146" alt="image" src="https://github.com/user-attachments/assets/675984da-e3bf-458e-bf46-790c2d06a8df" />  
  
In this case, we can use this command to translate the char on our ***data.txt***:
- `tr 'A-Za-z' 'N-ZA-Mn-za-m' < data.txt`  
In fact, executing this command in our command line should give back this:  
  
<img width="572" height="79" alt="image" src="https://github.com/user-attachments/assets/2ceeadfa-f50b-4854-9884-38574c4c4d3c" />  
  
Let’s break down the code.  
  
- `tr` is obviously the command we want to run.
- `'A-Za-z'` defines the first set of characters (STRING1), all uppercase and lowercase letters in the English alphabet (from A to Z and from a to z).
- `'N-ZA-Mn-za-m'` defines the second set (STRING2), which shifts the first set by 13 positions.

<details>
  <summary>Dive into 'tr'</summary>

> ***For this example i will take only the uppercase letters.***
> So imagine the command as `tr 'A-Z' 'N-ZA-M'`.  
> - The first set (`A-Z`) defines all uppercase letters.  
> - The second set (`N-ZA-M`) defines how to transform them using ROT13. We can't write `N-M` because `tr` only accepts intervals that go forward according to the ASCII table.
>   
> So we split it into two growing intervals: `N-Z` for the second half of the alphabet, followed by `A-M` for the first half.  
> In this way, every letter is correctly mapped 13 positions forward.  
</details>
  
***  

Now, let's analyze the second: `vi` or `vim`.  
What is vi?  
Vi or Vim it's a text editor that allows you do things, a lot of things.










































