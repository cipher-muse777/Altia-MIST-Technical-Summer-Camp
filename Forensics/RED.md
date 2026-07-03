## RED
RED, RED, RED, RED

### SOLUTION 
- i analysed the metadata using exiftool and found a weird looking poem
```
Poem :
Crimson heart, vibrant and bold,.
Hearts flutter at your sight..
Evenings glow softly red,.
Cherries burst with sweet life..
Kisses linger with your warmth..
Love deep as merlot..
Scarlet leaves falling softly,.
Bold in every stroke.
```
- when we extract just the first letter of each line we get CHECKLSB (Least Significant Bit)
- then i used zsteg on the png file which gave me an odd looking text
```
text: "cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ=="
```
- which when i used a cipher identifier gave me base 64 as result, which after further decoding gave me the flag

### FLAG 
picoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}

### RESOURCES 
https://www.dcode.fr/cipher-identifier
