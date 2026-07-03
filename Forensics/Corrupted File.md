## Corrupted File
This file seems broken... or is it? Maybe a couple of bytes could make all the difference. Can you figure out how to bring it back to life?

### SOLUTION 
- i opened the file in hex editor and noticed how the header was kinda similar to jpeg
<img width="1418" height="547" alt="Screenshot from 2026-07-03 21-24-05" src="https://github.com/user-attachments/assets/1de73964-a65e-43d2-bfbf-f8637466959d" />
- so i changed the first 2 bytes of the header from 5c to ff and 78 to d8 and saved the file to obatin the flag
<img width="823" height="526" alt="image" src="https://github.com/user-attachments/assets/9e4e4a69-a077-49db-be5c-6c28560fe37c" />

### FLAG
picoCTF{r3st0r1ng_th3_by73s_939a65f5}
