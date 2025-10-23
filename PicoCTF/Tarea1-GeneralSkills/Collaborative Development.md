### Descripción 
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/179/challenge.zip)
### Solución 
┌──(kali㉿kali)-[~/PicoCTF/drop-in]
└─$ git branch -a
  feature/part-1
  feature/part-2
  feature/part-3
* main

┌──(kali㉿kali)-[~/PicoCTF/drop-in]
└─$ git checkout feature/part-1
Switched to branch 'feature/part-1'

┌──(kali㉿kali)-[~/PicoCTF/drop-in]
└─$ cat flag.py             
print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='')                                                                                                                                                    
┌──(kali㉿kali)-[~/PicoCTF/drop-in]
└─$ git checkout feature/part-2
Switched to branch 'feature/part-2'
                                    
┌──(kali㉿kali)-[~/PicoCTF/drop-in]
└─$ cat flag.py
print("Printing the flag...")

print("m@k3s_th3_dr3@m_", end='')                                                                                                                                                    
┌──(kali㉿kali)-[~/PicoCTF/drop-in]
└─$ git checkout feature/part-3
Switched to branch 'feature/part-3'

┌──(kali㉿kali)-[~/PicoCTF/drop-in]
└─$ cat flag.py
print("Printing the flag...")

print("w0rk_798f9981}")

flag: picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_798f9981}

descargué y descomprimí el archivo e ingresé an la carpeta drop-in, utilicé el comando git branch -a para ver las ramas y luego utilicé git checkout para ingresar a las ramas y ver el contenido del archivo flag

### Notas adicionales
### Referencias