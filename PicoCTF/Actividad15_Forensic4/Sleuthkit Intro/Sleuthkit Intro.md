### Descripción 
Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag. Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory. [Download disk image](https://artifacts.picoctf.net/c/164/disk.img.gz) Access checker program: `nc saturn.picoctf.net 49374`
### Solución 
┌──(kali㉿kali)-[~/picoCTF/Sleuthkit_Intro]
└─$ gzip disk.img.gz 
gzip: disk.img.gz already has .gz suffix -- unchanged
                                                                                      
┌──(kali㉿kali)-[~/picoCTF/Sleuthkit_Intro]
└─$ gzip -d disk.img.gz
                                                                                      
┌──(kali㉿kali)-[~/picoCTF/Sleuthkit_Intro]
└─$ ls    
disk.img

┌──(kali㉿kali)-[~/picoCTF/Sleuthkit_Intro]
└─$ ls -la
total 102408
drwxrwxr-x  2 kali kali      4096 Nov 23 00:06 .
drwxrwxr-x 45 kali kali      4096 Nov 22 23:32 ..
-rw-rw-r--  1 kali kali 104857600 Aug  4  2023 disk.img

┌──(kali㉿kali)-[~/picoCTF/Sleuthkit_Intro]
└─$ mmls disk.img 
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000204799   0000202752   Linux (0x83)
                                                                                      
┌──(kali㉿kali)-[~/picoCTF/Sleuthkit_Intro]
└─$ nc saturn.picoctf.net 49374
What is the size of the Linux partition in the given disk image?
Length in sectors: 202752
202752
Great work!
picoCTF{mm15_f7w!}

### Notas adicionales
### Referencias
