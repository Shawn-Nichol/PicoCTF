AUTHOR: WILL HONG / LT 'SYREAL' JONES

## Description
We found a leak of a blackmarket website's login credentials. Can you find the password of the user cultiris and successfully decrypt it?
Download the leak here.
The first user in usernames.txt corresponds to the first password in passwords.txt. The second user corresponds to the second password, and so on.

## Enumeration

The file is a tar, which is short for **Tape Archive**. unzip the folder and we get the following contents. 
![image](https://github.com/Shawn-Nichol/PicoCTF/assets/30714313/7583211d-db7d-4c54-8500-63987e152b17)

- open up the username file and CRTL+F to find user "cultriris" line 378
- open the password file and scroll down to line 378, here you will find the hashed password "cvpbPGS{P7e1S_54I35_71Z3}". 

- I entered this password into chatGPT to see if it had any thoughts on what type of cipher was being used. ChatGPT identifies this a simple Caesar cipher, which is a type of cipher in which each letter in the plain text is shifted a certain number of places. 


- Know you can head over to https://www.dcode.fr/caesar-cipher enter the password in the text box, and bruteforce Decypt. Scroll through the list of results on the left until you can find one that is readable. D

![image](https://github.com/Shawn-Nichol/PicoCTF/assets/30714313/9c72398a-05a4-4ef0-8e88-0e2e83a435b2)

## Answer
Tag is picoCTF{C7r1F_54V35_71Me}
