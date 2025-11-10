### Descripción 
Find the flag in this [picture](https://jupiter.challenges.picoctf.org/static/89b371a46702a31aa9931a2a2b12f8bf/pico_img.png).
### Solución 
┌──(kali㉿kali)-[~/picoCTF/so_meta]
└─$ wget 'https://jupiter.challenges.picoctf.org/static/89b371a46702a31aa9931a2a2b12f8bf/pico_img.png'

┌──(kali㉿kali)-[~/picoCTF/so_meta]
└─$ exiftool pico_img.png | grep "picoCTF"
Artist                          : picoCTF{s0_m3ta_eb36bf44}

### Notas adicionales
### Referencias