## Hidden in plainsight
You’re given a seemingly ordinary JPG image. Something is tucked away out of sight inside the file. Your task is to discover the hidden payload and extract the flag.

### SOLUTION 
- i first inspected the file using exiftool whcih displayed all the metadata and found suspicious data in comments that is ```Comment : c3RlZ2hpZGU6Y0VGNmVuZHZjbVE9```
- i analyzed this in cipher identifer to under that this is base 64 encoding and decoded it to obatin ```steghide:cEF6endvcmQ=```
- which i once again analysed using cipher identifer to find out that its once again base 64 and decoded it to obtain ```pAzzword```
- then i steghide extracted the file using the command ``steghide extract -sf img.jpg`` and when they prompted for a password i provided with the decoded comment
- this created a flag.txt file with the flag

### FLAG 
picoCTF{h1dd3n_1n_1m4g3_5d4cba73}

### RESOURCES 
https://www.dcode.fr/cipher-identifier
