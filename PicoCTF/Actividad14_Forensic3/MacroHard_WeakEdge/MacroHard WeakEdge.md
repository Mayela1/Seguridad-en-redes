### Descripción 
I've hidden a flag in this file. Can you find it? [Forensics is fun.pptm](https://mercury.picoctf.net/static/d3dd8cd51524d9fafcccd1b7d55f85e7/Forensics%20is%20fun.pptm)
### Solución 
┌──(kali㉿kali)-[~/picoCTF/MacroHard_Weakedge]
└─$ file Forensics\ is\ fun.pptm 
Forensics is fun.pptm: Microsoft PowerPoint 2007+
   
┌──(kali㉿kali)-[~/picoCTF/MacroHard_Weakedge]
└─$ unzip Forensics\ is\ fun.pptm 
┌──(kali㉿kali)-[~/picoCTF/MacroHard_Weakedge]
└─$ grep -r pico

┌──(kali㉿kali)-[~/picoCTF/MacroHard_Weakedge]
└─$ ls
'[Content_Types].xml'   docProps  'Forensics is fun.pptm'   ppt   _rels
 
┌──(kali㉿kali)-[~/picoCTF/MacroHard_Weakedge]
└─$ cd ppt               
  
┌──(kali㉿kali)-[~/picoCTF/MacroHard_Weakedge/ppt]
└─$ ls    
presentation.xml  _rels         slideMasters  tableStyles.xml  vbaProject.bin
presProps.xml     slideLayouts  slides        theme            viewProps.xml
 
┌──(kali㉿kali)-[~/picoCTF/MacroHard_Weakedge/ppt]
└─$ cd slideMasters 

┌──(kali㉿kali)-[~/picoCTF/MacroHard_Weakedge/ppt/slideMasters]
└─$ ls               
hidden  _rels  slideMaster1.xml
 
┌──(kali㉿kali)-[~/picoCTF/MacroHard_Weakedge/ppt/slideMasters]
└─$ cat hidden       
Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q                                                                                     

┌──(kali㉿kali)-[~/picoCTF/MacroHard_Weakedge/ppt/slideMasters]
└─$ echo "Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q " | tr -d " " | base64 -d
flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}  
### Notas adicionales
### Referencias
