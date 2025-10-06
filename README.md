***
Command to connect to this level:
`sudo ssh bandit0@bandit.labs.overthewire.org -p 2220`  - This let you connect to overthewire server
*Password*: " bandit0 " - Needed for authentication
***
Solution for wargame Bandit hosted on overthewire.org

![43449268fcc1c000b095f5e4808134d6.png](:/7bbb9b17aa884a0cb3c7a1fa22d83aca)
***
Commands needed to solve this level:
`ls` - Needed to list what files are stored in the current location
`file filename` - Needed to determine the filetype of files
![e89fc84a3dc645670f71e3ae0c972cbf.png](:/de9960b554214e3dbc79c9f97696c6cf)
Since 'readme' is an ASCII text file, we can read his content with these commands:
`more filename` - Shows one at time the lines of a file
![d7054e8989db484493b2e47cd3daf7b8.png](:/32910df2f9e04ad5847c5c41f2b1c0fa)
`less filename` - Shows one at time the lines of a file (Unlike the command `more` it's interactive)
![e8ecdc02da142b7721a53ae21defd8cf.png](:/c1090f71150d4ca997800b1861da8414)
`head filename` - Shows the first 10 lines of a file
![51c635a0cb2dee6c9883267dc7ac46da.png](:/b890525c1e0d4d99975141d89a2cdedd)
`tail filename` - Shows the last 10 lines of a file
![8110386a1465a1cca6090b07bf75f764.png](:/a3906a24d24f4f2e8cd2114f5b4a00f6)
`cat filename` - Shows the content of a file
![1bf962f403e7c1f3f83d4a4cd96110b9.png](:/3f889e5e5ca64be783b122a6a9d05160)
