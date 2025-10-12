### Descripción 
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/cfea736820f329083dab9558c3932ada/warm) has extraordinarily helpful information...
### Solución 
┌──(kali㉿kali)-[~]
└─$ ./warm -h
zsh: permission denied: ./warm

┌──(kali㉿kali)-[~]
└─$ chmod +x warm

┌──(kali㉿kali)-[~]
└─$ ./warm -h    
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_30e77291}
intenté ejecutar el archivo pero como no dejó agregué el permiso de ejecución para este archivo
![[Pasted image 20251011145508.png]]
### Notas adicionales
### Referencias