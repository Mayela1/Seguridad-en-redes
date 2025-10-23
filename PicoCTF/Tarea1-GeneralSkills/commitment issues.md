### Descripción 
I accidentally wrote the flag down. Good thing I deleted it!You download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/137/challenge.zip)
### Solución 
┌──(kali㉿kali)-[~/PicoCTF/drop-in]
└─$ git log            
commit ef0b7cc6b98367fa168573c931e0f7098ef59182 (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:06:20 2024 +0000

    remove sensitive info

commit ea859bf3b5d94ee74ce5ee1afa3edd7d4d6b35f0
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:06:20 2024 +0000

    create flag
┌──(kali㉿kali)-[~/PicoCTF/drop-in]
└─$ git checkout ea859bf3b5d94ee74ce5ee1afa3edd7d4d6b35f0  
Previous HEAD position was ef0b7cc remove sensitive info
HEAD is now at ea859bf create flag
 
┌──(kali㉿kali)-[~/PicoCTF/drop-in]
└─$ cat message.txt
picoCTF{s@n1t1z3_cf09a485}

### Notas adicionales
### Referencias