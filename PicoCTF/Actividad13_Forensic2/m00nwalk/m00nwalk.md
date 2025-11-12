### Descripción
Decode this [message](https://jupiter.challenges.picoctf.org/static/d6fcea5e3c6433680ea4f914e24fab61/message.wav) from the moon.
### Solución 
┌──(kali㉿kali)-[~/picoCTF/m00nwalk]
└─$ cd /opt    

┌──(kali㉿kali)-[/opt]
└─$ git clone https://github.com/colaclanth/sstv.git
fatal: could not create work tree dir 'sstv': Permission denied

┌──(kali㉿kali)-[/opt]
└─$ sudo git clone https://github.com/colaclanth/sstv.git
[sudo] password for kali: 
Cloning into 'sstv'...
remote: Enumerating objects: 221, done.
remote: Counting objects: 100% (59/59), done.
remote: Compressing objects: 100% (10/10), done.
remote: Total 221 (delta 51), reused 49 (delta 49), pack-reused 162 (from 1)
Receiving objects: 100% (221/221), 1.01 MiB | 2.45 MiB/s, done.
Resolving deltas: 100% (139/139), done.

┌──(kali㉿kali)-[/opt]
└─$ cd sstv 

┌──(kali㉿kali)-[/opt/sstv]
└─$ sudo python3 setup.py install

┌──(kali㉿kali)-[~/picoCTF/m00nwalk]
└─$ sstv -d message.wav -o result.png
[sstv] Searching for calibration header... Found!    
[sstv] Detected SSTV mode Scottie 1
[sstv] Decoding image...   [############################################] 100%
[sstv] Drawing image data...
[sstv] ...Done!


picoCTF{beep_boop_im_in_space}
### Notas adicionales
### Referencias
https://github.com/colaclanth/sstv
