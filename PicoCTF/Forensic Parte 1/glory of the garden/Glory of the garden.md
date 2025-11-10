### Descripción 
This [garden](https://jupiter.challenges.picoctf.org/static/d0e1ffb10fc0017c6a82c57900f3ffe3/garden.jpg) contains more than it seems.
### Solución 
┌──(kali㉿kali)-[~/picoCTF/glory_of_the_garden]
└─$ wget https://jupiter.challenges.picoctf.org/static/d0e1ffb10fc0017c6a82c57900f3ffe3/garden.jpg
┌──(kali㉿kali)-[~/picoCTF/glory_of_the_garden]
└─$ ls
garden.jpg
          
┌──(kali㉿kali)-[~/picoCTF/glory_of_the_garden]
└─$ hexeditor garden.jpg 

┌──(kali㉿kali)-[~/picoCTF/glory_of_the_garden]
└─$ strings garden.jpg | grep "pico"        
Here is a flag "picoCTF{more_than_m33ts_the_3y3eBdBd2cc}"


### Notas adicionales
### Referencias