## Morse-code
AUTHOR: WILL HONG

Description
Morse code is well known. Can you decrypt this?
Download the file here.
Wrap your answer with picoCTF{}, put underscores instead of pauses, and use all lowercase.

## Download file. 
It is an audio file with Morse code. 

## Hint
Audicty is a really good program to analyze morse code audio. 

## Enumeration
Image of Audio file
![image](https://github.com/Shawn-Nichol/PicoCTF/assets/30714313/b83bf253-b88d-4fd5-b3dc-d719c38e3788)

short burst are . and long burst are -, big gapes are spaces /

.-- .... ....- --... / .... ....- --... .... / ----. ----- -.. / .-- ..--- ----- ..- ----. .... --...

Translated on [Morese Code Translator](https://morsecode.world/international/translator.html)
WH47 H47H 90D W20U9H7

Replace spaces with underscores:
WH47_H47H_90D_W20U9H7

## Flag
Tag: picoCTF{WH47_H47H_90D_W20U9H7}
