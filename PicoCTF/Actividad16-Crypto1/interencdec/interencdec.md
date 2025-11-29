### Descripción 
Can you get the real meaning from this file. Download the file [here](https://artifacts.picoctf.net/c_titan/109/enc_flag).

HINTS: Engaging in various decoding processes is of utmost importance
### Solución
┌──(kali㉿kali)-[~/picoCTF]
└─$ mkdir interencdec  
                                                                                     
┌──(kali㉿kali)-[~/picoCTF]
└─$ cd interencdec 
                                                                                     
┌──(kali㉿kali)-[~/picoCTF/interencdec]
└─$ wget https://artifacts.picoctf.net/c_titan/109/enc_flag
--2025-11-28 18:25:19--  https://artifacts.picoctf.net/c_titan/109/enc_flag
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.100, 3.161.55.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 73 [application/octet-stream]
Saving to: ‘enc_flag’

enc_flag              100%[======================>]      73  --.-KB/s    in 0s      

2025-11-28 18:25:19 (21.8 MB/s) - ‘enc_flag’ saved [73/73]

                                                                                     
┌──(kali㉿kali)-[~/picoCTF/interencdec]
└─$ ls
enc_flag
                                                                                     
┌──(kali㉿kali)-[~/picoCTF/interencdec]
└─$ file enc_flag     
enc_flag: ASCII text
                                                                                     
┌──(kali㉿kali)-[~/picoCTF/interencdec]
└─$ cat enc_flag     
YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclgyMHdNakV5TnpVNGZRPT0nCg==
                                                                                     
┌──(kali㉿kali)-[~/picoCTF/interencdec]
└─$ echo YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclgyMHdNakV5TnpVNGZRPT0nCg== | base64 --decode
b'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX20wMjEyNzU4fQ=='
                                                                                     
┌──(kali㉿kali)-[~/picoCTF/interencdec]
└─$ echo d3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX20wMjEyNzU4fQ== | base64 --decode
wpjvJAM{jhlzhy_k3jy9wa3k_m0212758}

utilicé la herramienta dcode para desencriptar:  wpjvJAM{jhlzhy_k3jy9wa3k_m0212758}

picoCTF{caesar_d3cr9pt3d_f0212758}
### Notas adicionales
### Referencias
https://www.dcode.fr/caesar-cipher