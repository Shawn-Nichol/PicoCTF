Description
We found this weird message being passed around on the servers; we think we have a working decryption scheme.
Download the message here.
Take each number **mod 37** and map it to the following character **set: 0-25** is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore.
Wrap your decrypted message in the picoCTF flag format.

message
```
128 322 353 235 336 73 198 332 202 285 57 87 262 221 218 405 335 101 256 227 112 140 
```

## Mod 37
"mod 37" refers to the operation of taking the remainder when a number is divided by 37. This operation is commonly denoted by the percent symbol (%). 

For example, if you have the expression "x mod 37," it means you're finding the remainder when x is divided by 37. Mathematically, you can express this as:

x mod 37 = x % 37

1. 45 mod 37 = 45 % 37 = 8
2. 100 mod 37 = 100 % 37 = 26
3. 20 mod 37 = 20 % 37 = 20

```python
# Define the character set mapping
char_set = "ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789_"
message = "128 322 353 235 336 73 198 332 202 285 57 87 262 221 218 405 335 101 256 227 112 140 "

# split the message into individual numbers
numbers = message.split()
result_string = ""

for num in numbers:
    num = int(num)
    mod_37 = num % 37
    char = char_set[mod_37]
    result_string += char

print (result_string)
```
flag R0UND_N_R0UND_79C18FB3
