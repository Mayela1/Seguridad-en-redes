### Descripción 
Why search for the flag when I can make a bookmarklet to print it for me?Browse [here](http://titan.picoctf.net:63454/), and find the flag!
### Solución 
copié el siguiente código que se encontraba en la página web y lo pegué en la consola, al ejecutarlo me apareció la bandera
        javascript:(function() {
            var encryptedFlag = "àÒÆÞ¦È¬ëÙ£ÖÓÚåÛÑ¢ÕÓÓÇ¡¥Ìí";
            var key = "picoctf";
            var decryptedFlag = "";
            for (var i = 0; i < encryptedFlag.length; i++) {
                decryptedFlag += String.fromCharCode((encryptedFlag.charCodeAt(i) - key.charCodeAt(i % key.length) + 256) % 256);
            }
            alert(decryptedFlag);
        })();

### Referencias
