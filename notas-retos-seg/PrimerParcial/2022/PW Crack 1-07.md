# Descripcion 
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/11/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/11/level1.flag.txt.enc) in the same directory too.
# Pistas
- To view the file in the webshell, do: `$ nano level1.py`
- To exit `nano`, press Ctrl and x and follow the on-screen prompts.
- The `str_xor` function does not need to be reverse engineered for this challenge.
# Solucion 
```bash

erickso678-picoctf@webshell:~$ pyhton level1.py 
-bash: pyhton: command not found
erickso678-picoctf@webshell:~$ python level1.py 
Please enter correct password for flag: 1e1a
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_fa343060}
erickso678-picoctf@webshell:~$ 

```
# Bandera
picoCTF{545h_r1ng1ng_fa343060}
# Notas Adicionales
- abrimos el codigo y encontramos la clave de acceso en un if donde esta la clave y la usamos al ejecutar el archivo y nos da la llave
