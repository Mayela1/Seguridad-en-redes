### Descripción 
The Multiverse is within your grasp! Unfortunately, the server that contains the secrets of the multiverse is in a universe where keyboards only have numbers and (most) symbols.`ssh -p 64758 ctf-player@mimas.picoctf.net`Use password: `f3b61b38`
### Solución 
SansAlpha$ ls
SansAlpha: Unknown character detected
SansAlpha$ *
bash: blargh: command not found

SansAlpha$ */*
bash: blargh/flag.txt: Permission denied

SansAlpha$ /*/???
E: Invalid operation /bin/awk

SansAlpha$ /*/??????
/bin/base32: extra operand '/bin/base64'
Try '/bin/base32 --help' for more information.

SansAlpha$ /*/????64 */*
/bin/base64: extra operand '/bin/x86_64'
Try '/bin/base64 --help' for more information.

SansAlpha$ /*/???[!_]64 */*
/bin/base64: extra operand 'blargh/flag.txt'
Try '/bin/base64 --help' for more information.

SansAlpha$ /*/???[!_]64 */*
/bin/base64: extra operand 'blargh/flag.txt'
Try '/bin/base64 --help' for more information.

SansAlpha$ /*/???[!_]64 */????.*
cmV0dXJuIDAgcGljb0NURns3aDE1X211MTcxdjNyNTNfMTVfbTRkbjM1NV82NDBiNmFkZH0=

┌──(kali㉿kali)-[~]
└─$ echo cmV0dXJuIDAgcGljb0NURns3aDE1X211MTcxdjNyNTNfMTVfbTRkbjM1NV82NDBiNmFkZH0= | base64 -d

return 0 picoCTF{7h15_mu171v3r53_15_m4dn355_640b6add}
### Notas adicionales
### Referencias