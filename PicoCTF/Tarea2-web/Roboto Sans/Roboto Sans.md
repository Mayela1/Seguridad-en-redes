### Descripción 
The flag is somewhere on this web application not necessarily on the website. Find it. Check [this](http://saturn.picoctf.net:57231/) out.
### Solución 
agregué al link de la página robots.txt 
http://saturn.picoctf.net:55410/robots.txt
y me apareció el siguiente texto: ZmxhZzEudHh0;anMvbXlmaW
anMvbXlmaWxlLnR4dA
utilicé burpsuite para decodificarlo y me dió esto: flag1.txt;js/myfi
js/myfile.txt
así que busqué ese archivo
http://saturn.picoctf.net:55410/js/myfile.txt
picoCTF{Who_D03sN7_L1k5_90B0T5_718c9043}
### Notas adicionales
### Referencias