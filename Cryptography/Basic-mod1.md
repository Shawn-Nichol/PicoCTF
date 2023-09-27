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

So, when you perform "mod 37," you're finding the value that remains after dividing a number by 37.

## Mapping
0 -> A
1 -> B
2 -> C
3 -> D
4 -> E
5 -> F
6 -> G
7 -> H
8 -> I
9 -> J
10 -> K
11 -> L
12 -> M
13 -> N
14 -> O
15 -> P
16 -> Q
17 -> R
18 -> S
19 -> T
20 -> U
21 -> V
22 -> W
23 -> X
24 -> Y
25 -> Z
26 -> 0
27 -> 1
28 -> 2
29 -> 3
30 -> 4
31 -> 5
32 -> 6
33 -> 7
34 -> 8
35 -> 9
36 -> _


Message divided: 
128 mod 37 = 17 -> R
322 mod 37 = 26 -> 0
353 mod 37 = 20 -> U
235 mod 37 = 13 -> N
336 mod 37 = 3 -> D
73 mod 37 = 36 -> _
198 mod 37 = 13 -> N
332 mod 37 = 36 -> _
202 mod 37 = 17 -> R
285 mod 37 = 26 -> 0
57 mod 37 = 20 -> U
87 mod 37 = 13 -> N
262 mod 37 = 3 -> D
221 mod 37 = 36 -> _
218 mod 37 = 33 -> 7
405 mod 37 = 35 -> 9
335 mod 37 = 2 -> C
101 mod 37 = 27 -> 1
256 mod 37 = 34 -> 8
227 mod 37 = 5 -> F
112 mod 37 = 1 -> B
140 mod 37 = 29 -> 3

R0UND_N_R0UND_79C18FB3
