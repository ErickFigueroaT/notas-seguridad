# Descripcion 
Run the Python script `code.py` in the same directory as `codebook.txt`.

-   [Download code.py](https://artifacts.picoctf.net/c/1/code.py)
-   [Download codebook.txt](https://artifacts.picoctf.net/c/1/codebook.txt)
# Pistas
- On the webshell, use `ls` to see if both files are in the directory you are in
- The `str_xor` function does not need to be reverse engineered for this challenge.
# Solucion 
```bash
erickso678-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/1/code.py
--2023-03-22 20:54:32--  https://artifacts.picoctf.net/c/1/code.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.160.41.106, 18.160.41.121, 18.160.41.113, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.160.41.106|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1278 (1.2K) [application/octet-stream]
Saving to: 'code.py'

code.py                                                           100%[=============================================================================================================================================================>]   1.25K  --.-KB/s    in 0s      

2023-03-22 20:54:32 (1.06 GB/s) - 'code.py' saved [1278/1278]

erickso678-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/1/codebook.txt
--2023-03-22 20:54:42--  https://artifacts.picoctf.net/c/1/codebook.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 52.84.18.125, 52.84.18.29, 52.84.18.20, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|52.84.18.125|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 27 [application/octet-stream]
Saving to: 'codebook.txt'

codebook.txt                                                      100%[=============================================================================================================================================================>]      27  --.-KB/s    in 0s      

2023-03-22 20:54:42 (16.5 MB/s) - 'codebook.txt' saved [27/27]

erickso678-picoctf@webshell:~$ python code.py 
picoCTF{c0d3b00k_455157_d9aa2df2}
erickso678-picoctf@webshell:~$ 



```
# Bandera
picoCTF{c0d3b00k_455157_d9aa2df2}
# Notas Adicionales
- descargamos los archivos con wget al mismo directorio 
- ejecutamos el code.py y nos da la llave
