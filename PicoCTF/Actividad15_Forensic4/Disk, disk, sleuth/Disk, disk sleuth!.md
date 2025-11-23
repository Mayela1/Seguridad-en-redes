### Descripción 
Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image: [dds1-alpine.flag.img.gz](https://mercury.picoctf.net/static/4f3df7052b4121aff89af1a3f517afb1/dds1-alpine.flag.img.gz)
### Solución 
┌──(kali㉿kali)-[~/picoCTF/disk]
└─$ ls
dds1-alpine.flag.img.gz
 
┌──(kali㉿kali)-[~/picoCTF/disk]
└─$ gunzip dds1-alpine.flag.img.gz 
  
┌──(kali㉿kali)-[~/picoCTF/disk]
└─$ ls
dds1-alpine.flag.img

┌──(kali㉿kali)-[~/picoCTF/disk]
└─$ file dds1-alpine.flag.img 
dds1-alpine.flag.img: DOS/MBR boot sector; partition 1 : ID=0x83, active, start-CHS (0x0,32,33), end-CHS (0x10,81,1), startsector 2048, 260096 sectors

┌──(kali㉿kali)-[~/picoCTF/disk]
└─$ srch_strings dds1-alpine.flag.img | grep picoCTF

  SAY picoCTF{f0r3ns1c4t0r_n30phyt3_a011c142}
   
### Notas adicionales
### Referencias

