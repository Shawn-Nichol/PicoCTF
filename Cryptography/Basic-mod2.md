AUTHOR: WILL HONG

Description
A new modular challenge!
Download the message here.
Take each number **mod 41** and find the modular inverse for the result. Then, map to the following character set: 1-26 are the alphabet, 27-36 are the decimal digits, and 37 is an underscore.
Wrap your decrypted message in the picoCTF flag format.

message
```
432 331 192 108 180 50 231 188 105 51 364 168 344 195 297 342 292 198 448 62 236 342 63 
```
``` python
# Define the character set mapping
char_set = "_ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789_"
message = "432 331 192 108 180 50 231 188 105 51 364 168 344 195 297 342 292 198 448 62 236 342 63  "

# split the message into individual numbers
numbers = message.split()
result_string = ""

for num in numbers:
    # Pow is a function that stands for power and is used to raise a number to a specific exponent.
    mod = pow(int(num), -1, 41)
    result_string += char_set[mod]

print (result_string)
```

flag: 1NV3R53LY_H4RD_C680BDC1
