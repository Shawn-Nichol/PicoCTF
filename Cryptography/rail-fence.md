AUTHOR: WILL HONG

Description
A type of transposition cipher is the rail fence cipher, which is described here. Here is one such cipher encrypted using the rail fence with four rails. Can you decrypt it?
Download the message here.
Put the decoded message in the picoCTF flag format, picoCTF{decoded_message}.

## Download message
Ta _7N6DDDhlg:W3D_H3C31N__0D3ef sHR053F38N43D0F i33___NA

## Enumeration
In the rail fence cipher, the plaintext is written downwards diagonally on successive rails of an imaginary fence, then moving up when the bottom rail is reached, down again when the top rail is reached and so on until the whole plaintext is written out.
For example, to encrypt the message 'WE ARE DISCOVERED. RUN AT ONCE.' With 3 "rails," write the text as:

W . . . E . . . C . . . R . . . U . . . O . . . 
. E . R . D . S . O . E . E . R . N . T . N . E 
. . A . . . I . . . V . . . D . . . A . . . C . 


python script encrypt
```
message = "WE ARE DISCOVERED. RUN AT ONCE."

rail1 = ""
rail2 = ""
rail3 = ""
rail4 = ""

rail = 1
position = 0
direction = 0 

for char in message:
    if char.isalpha():
        if direction == 0: 
            position += 1
            if position == 3:
                direction = 1
        else:
            position -= 1
            if position == 1:
                direction = 0
        print(position, "and", char)

        if position == 1:
            rail1 += char
        elif position == 2:
            rail2 += char
        elif position == 3:
            rail3 += char
        elif position == 4:
            rail4 += char

print(rail1, rail2, rail3)


WECRUO ERDSOEERNTNE AIVDAC
```
## Flag
