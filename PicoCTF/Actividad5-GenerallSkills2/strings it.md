### Descripción 
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/5bd86036f013ac3b9c958499adf3e2e2/strings) without running it?
### Solución 
┌──(kali㉿kali)-[~]
└─$ file strings 
strings: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=047a5079a5f563cd0e540d28f42a37161093ffda, not stripped
       
┌──(kali㉿kali)-[~]
└─$ strings strings | grep pico
picoCTF{5tRIng5_1T_827aee91}

descargué el archivo y utilicé el comando strings y grep para recuperar la cadena de texto que tuviera la bandera
![[Pasted image 20251008114303.png]]
### Notas adicionales
### Referencias