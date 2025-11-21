### Descripción 
A digital ghost has breached my defenses, and my sensitive data has been stolen! 😱💻 Your mission is to uncover how this phantom intruder infiltrated my system and retrieve the hidden flag. To solve this challenge, you'll need to analyze the provided PCAP file and track down the attack method. The attacker has cleverly concealed his moves in well timely manner. Dive into the network traffic, apply the right filters and show off your forensic prowess and unmask the digital intruder! Find the PCAP file here [Network Traffic PCAP file](https://challenge-files.picoctf.net/c_verbal_sleep/586d0206891cc683bae1160ad6b0e05d7e10e7b2df122c0441ab06581038dd32/myNetworkTraffic.pcap) and try to get the flag.
### Solución 
revisé los intentos de conexión TCP y me fijé que los que tenían len=12 tenían cadenas base 64 así que las decodifiqué  y después armé la bandera
estas son las cadenas decodificadas:
nt_th4t
e1ff063
_34sy_t
{1t_w4s
picoCTF
bh_4r_2

picoCTF{1t_w4snt_th4t_34sy_tbh_4r_2e1ff063}
### Notas adicionales
### Referencias
