# Descripcion 
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/7495259e963bd5b67d0fb8b616652618/static)? This [BASH script](https://mercury.picoctf.net/static/7495259e963bd5b67d0fb8b616652618/ltdis.sh) might help!
# Pistas
no hay pistas
# Solucion 
```bash
┌──(erick㉿kali)-[~/Descargas/picoCTF2021]
└─$ strings static | grep pico
picoCTF{d15a5m_t34s3r_f6c48608}
                                                    
┌──(erick㉿kali)-[~/Descargas/picoCTF2021]
└─$ 


```
# Bandera
picoCTF{d15a5m_t34s3r_f6c48608}
# Notas Adicionales
- usamos strings con el archivo static para filtrarlo con grep con pico y nos de la llave.
