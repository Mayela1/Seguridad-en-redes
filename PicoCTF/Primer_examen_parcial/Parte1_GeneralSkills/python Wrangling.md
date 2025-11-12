### Descripción 
Python scripts are invoked kind of like programs in the Terminal... Can you run [this Python script](https://mercury.picoctf.net/static/2ac2139344d2e734d5d638ac928f1a8d/ende.py) using [this password](https://mercury.picoctf.net/static/2ac2139344d2e734d5d638ac928f1a8d/pw.txt) to get [the flag](https://mercury.picoctf.net/static/2ac2139344d2e734d5d638ac928f1a8d/flag.txt.en)?
### Solución 
┌──(kali㉿kali)-[~/picoCTF]
└─$ python3 ende.py 
Usage: ende.py (-e/-d) [file]

┌──(kali㉿kali)-[~/picoCTF]
└─$ python3 ende.py -h
Usage: ende.py (-e/-d) [file]
Examples:
  To decrypt a file named 'pole.txt', do: '$ python ende.py -d pole.txt'

┌──(kali㉿kali)-[~/picoCTF]
└─$ python ende.py -d flag.txt.en
Please enter the password:68f88f9368f88f9368f88f9368f88f93
picoCTF{4p0110_1n_7h3_h0us3_68f88f93}


### Notas adicionales
### Referencias