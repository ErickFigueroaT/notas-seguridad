# Descripción
Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/63090/` or http://jupiter.challenges.picoctf.org:63090

# Solución
Se inspeccionan las cookies, se copia el jwt generado.

A través de kali, se utiliza una herramienta llamada jhon y un archivo txt que contiene una lista de palabras que son las contraseñas más usadas.

Luego entramos a https://jwt.io y pegamos el jwt que nos da al principio y modificamos el usuario a admin y ponemos la clave de ilovepico para pegarla en la pagina y nos de la bandera.

```bash
┌──(erick㉿kali)-[~]
└─$ nano jawt.john 
                                                    
┌──(erick㉿kali)-[~]
└─$ john jawt.john 
Created directory: /home/erick/.john
Using default input encoding: UTF-8
Loaded 1 password hash (HMAC-SHA256 [password is key, SHA256 256/256 AVX2 8x])
ilovepico
Will run 2 OpenMP threads
Proceeding with single, rules:Single
Press 'q' or Ctrl-C to abort, almost any other key for status
Almost done: Processing the remaining buffered candidate passwords, if any.
Proceeding with wordlist:/usr/share/john/password.lst
Proceeding with incremental:ASCII

```

picoCTF{jawt_was_just_what_you_thought_44c752f5}

# Notas Adicionales
https://jwt.io