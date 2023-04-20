# Descripcion 
Run the Python script and convert the given number from decimal to binary to get the flag.[Download Python script](https://artifacts.picoctf.net/c/24/convertme.py)

# Pistas
- Look up a decimal to binary number conversion app on the web or use your computer's calculator!
- The `str_xor` function does not need to be reverse engineered for this challenge.
- If you have Python on your computer, you can download the script normally and run it. Otherwise, use the `wget` command in the webshell.
- To use `wget` in the webshell, first right click on the download link and select 'Copy Link' or 'Copy Link Address'
-  Type everything after the dollar sign in the webshell: `$ wget` , then paste the link after the space after `wget` and press enter. This will download the script for you in the webshell so you can run it!
- Finally, to run the script, type everything after the dollar sign and then press enter: `$ python3 convertme.py`
# Solucion 
```bash
erickso678-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/24/convertme.py
--2023-03-22 20:47:14--  https://artifacts.picoctf.net/c/24/convertme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.160.41.106, 18.160.41.121, 18.160.41.113, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.160.41.106|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1189 (1.2K) [application/octet-stream]
Saving to: 'convertme.py'

convertme.py                                                      100%[=============================================================================================================================================================>]   1.16K  --.-KB/s    in 0s      

2023-03-22 20:47:14 (700 MB/s) - 'convertme.py' saved [1189/1189]

erickso678-picoctf@webshell:~$ ls 
README.txt  convertme.py  runme.py
erickso678-picoctf@webshell:~$ python convertme.py 
If 85 is in decimal base, what is it in binary base?
Answer: 1010101
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_722f6b39}
erickso678-picoctf@webshell:~$ 



```
# Bandera
picoCTF{4ll_y0ur_b4535_722f6b39}
# Notas Adicionales
- descargamos la liga con wget para obtener el .py.
- lo ejecutamos con pyhton.
- hacemos la conversion de binario a decimal en [Convertidor decimal a binario (rapidtables.org)](https://www.rapidtables.org/convert/number/decimal-to-binary.html) para responder la pregunta y obtener la bandera.