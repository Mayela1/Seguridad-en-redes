### Descripción
[🥛](http://mercury.picoctf.net:16940/)
### Solución 
┌──(kali㉿kali)-[~/picoCTF/milkslap]
└─$ ls
concat_v.png
  
┌──(kali㉿kali)-[~/picoCTF/milkslap]
└─$ file concat_v.png        
concat_v.png: PNG image data, 1280 x 47520, 8-bit/color RGB, non-interlaced
 
┌──(kali㉿kali)-[~]
└─$ sudo apt install ruby ruby-dev build-essential

┌──(kali㉿kali)-[~/picoCTF/milkslap]
└─$ sudo gem install zsteg -v 0.2.11

Fetching zsteg-0.2.11.gem
Successfully installed zsteg-0.2.11
Parsing documentation for zsteg-0.2.11
Installing ri documentation for zsteg-0.2.11
Done installing documentation for zsteg after 1 seconds
1 gem installed

┌──(kali㉿kali)-[~/picoCTF/milkslap]
└─$ zsteg concat_v.png              
imagedata           .. text: "\n\n\n\n\n\n\t\t"
b1,b,lsb,xy         .. text: "picoCTF{imag3_m4n1pul4t10n_sl4p5}\n"
b1,bgr,lsb,xy       .. /var/lib/gems/3.3.0/gems/iostruct-0.5.0/lib/iostruct.rb:180:in `inspect': stack level too deep (SystemStackError)
        from /var/lib/gems/3.3.0/gems/zsteg-0.2.11/lib/zsteg/checker/wbstego.rb:41:in `to_s'
        from /var/lib/gems/3.3.0/gems/iostruct-0.5.0/lib/iostruct.rb:180:in `inspect'
        from /var/lib/gems/3.3.0/gems/zsteg-0.2.11/lib/zsteg/checker/wbstego.rb:41:in `to_s'
        from /var/lib/gems/3.3.0/gems/iostruct-0.5.0/lib/iostruct.rb:180:in `inspect'
        from /var/lib/gems/3.3.0/gems/zsteg-0.2.11/lib/zsteg/checker/wbstego.rb:41:in `to_s'
        from /var/lib/gems/3.3.0/gems/iostruct-0.5.0/lib/iostruct.rb:180:in `inspect'
        from /var/lib/gems/3.3.0/gems/zsteg-0.2.11/lib/zsteg/checker/wbstego.rb:41:in `to_s'
        from /var/lib/gems/3.3.0/gems/iostruct-0.5.0/lib/iostruct.rb:180:in `inspect'
         ... 10906 levels...
        from /var/lib/gems/3.3.0/gems/zsteg-0.2.11/lib/zsteg.rb:30:in `run'
        from /var/lib/gems/3.3.0/gems/zsteg-0.2.11/bin/zsteg:8:in `<top (required)>'
        from /usr/local/bin/zsteg:25:in `load'
        from /usr/local/bin/zsteg:25:in `<main>'

### Notas adicionales
### Referencias

