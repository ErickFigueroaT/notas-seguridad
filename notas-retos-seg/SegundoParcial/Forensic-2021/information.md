# Descripcion 
Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://mercury.picoctf.net/static/a614a27d4cb251d04c7d2f3f3f76a965/cat.jpg)
# Pistas
- Look at the details of the file
- Make sure to submit the flag as picoCTF{XXXXX}
# Solucion 
```bash
Descargamos la imagen con wget y despues la inspeccionamos con exiftool para ver el contenido y notamos que la licencia esta en base 64 entonces con el mismo comando de exiftool lo usamos con grep en la licencia con base 64 y nos dara la bandera de este

```
# Bandera
picoCTF{the_m3tadata_1s_modified}
# Notas Adicionales