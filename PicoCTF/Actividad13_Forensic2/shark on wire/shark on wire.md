### Descripción 
We found this [packet capture](https://challenge-files.picoctf.net/c_fickle_tempest/07bf5ee832c595a6de406476b6c07f164d2951fbcfcf9cf3739c25dea26e5f0b/capture.pcap). Recover the flag.
### Solución 
abrí el archivo con wireshark y observé los puertos
┌──(kali㉿kali)-[~/picoCTF/sharkOnWire2]
└─$ wireshark capture.pcap &
[1] 38714

utilicé el siguiente código para ayudarme a solucionar el reto:
from scapy.all import *

packets =rdpcap('capture.pcap')

flag = ' '
for p in packets:
        if UDP in p and p[UDP].dport == 22:
                if p[UDP].sport > 5000:
                        flag += chr(p[UDP].sport - 5000)
print(flag)

┌──(kali㉿kali)-[~/picoCTF/sharkOnWire2]
└─$ python3 exp.py
 picoCTF{p1LLf3r3d_data_v1a_st3g0}
                                   
### Notas adicionales
### Referencias
