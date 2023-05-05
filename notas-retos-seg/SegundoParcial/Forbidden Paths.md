# Descripcion 
Can you get the flag?Here's the [website](http://saturn.picoctf.net:52021/).We know that the website files live in `/usr/share/nginx/html/` and the flag is at `/flag.txt` but the website is filtering absolute file paths. Can you get past the filter to read the flag?
# Pistas
NONE
# Solucion 
```bash
Al ingresar a la pagina al poner /flag.txt nos indica que no estamos autorizados pero si ponemos ../../../../../flag.txt nos dara la bandera de este.

```
# Bandera
# Notas Adicionales
