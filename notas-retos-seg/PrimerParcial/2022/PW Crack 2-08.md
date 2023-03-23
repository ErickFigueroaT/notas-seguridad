# Descripcion
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/13/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/13/level2.flag.txt.enc) in the same directory too.
# Pistas
- Does that encoding look familiar?
- The `str_xor` function does not need to be reverse engineered for this challenge.
# Solucion 
```bash
erickso678-picoctf@webshell:~$ python 
Python 3.10.6 (main, Aug 10 2022, 11:40:04) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36)
'de76'
>>> 
erickso678-picoctf@webshell:~$ python level
level1.py  level2.py  
erickso678-picoctf@webshell:~$ python level2.py 
Please enter correct password for flag: de76
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_489dea9a}
erickso678-picoctf@webshell:~$ 


```
# Bandera
picoCTF{tr45h_51ng1ng_489dea9a}
# Notas Adicionales
- en un if hay un codigo ASCII entonces ejecutamos python y lo pegamos para que nos de la contraseña y nos de la llave