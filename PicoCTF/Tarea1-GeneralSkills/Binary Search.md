### Descripción 
¿Quieres jugar? A medida que uses más el shell, ¡quizás te interese saber cómo funcionan! La búsqueda binaria es un algoritmo clásico para encontrar rápidamente un elemento en una lista ordenada. ¿Puedes encontrar la bandera? Tendrás 1000 posibilidades y solo 10 intentos.La ciberseguridad suele requerir una gran cantidad de datos que analizar, desde registros e informes de vulnerabilidad hasta análisis forense. Practicar los fundamentos manualmente podría ayudarte en el futuro cuando tengas que desarrollar tus propias herramientas.Puedes descargar los archivos del desafío aquí:

- [desafío.zip](https://artifacts.picoctf.net/c_atlas/5/challenge.zip)

`ssh -p 63027 ctf-player@atlas.picoctf.net`Usando la contraseña `1ad5be0d`. Acepta la huella digital con `yes`y, `ls`una vez conectado, comienza. Recuerda: en un shell, las contraseñas están ocultas.
### Solución 
┌──(kali㉿kali)-[~/PicoCTF/home/ctf-player/drop-in]
└─$ ssh -p 64035 ctf-player@atlas.picoctf.net
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500
Higher! Try again.
Enter your guess: 750
Higher! Try again.
Enter your guess: 800
Lower! Try again.
Enter your guess: 775
Higher! Try again.
Enter your guess: 790
Lower! Try again.
Enter your guess: 780
Lower! Try again.
Enter your guess: 776
Higher! Try again.
Enter your guess: 777
Higher! Try again.
Enter your guess: 778
Higher! Try again.
Enter your guess: 779
Congratulations! You guessed the correct number: 779
Here's your flag: picoCTF{g00d_gu355_3af33d18}
Connection to atlas.picoctf.net closed.

### Notas adicionales
### Referencias