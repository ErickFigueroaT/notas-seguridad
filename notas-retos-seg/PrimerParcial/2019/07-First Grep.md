# Descripcion 
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/315d3325dc668ab7f1af9194f2de7e7a/file)? This would be really tedious to look through manually, something tells me there is a better way.
# Pistas
grep [tutorial](https://ryanstutorials.net/linuxtutorial/grep.php)
# Solucion 
```bash
┌──(erick㉿kali)-[~/Descargas]
└─$ cat file | grep picoCTF        
picoCTF{grep_is_good_to_find_things_f77e0797}
                                                     
┌──(erick㉿kali)-[~/Descargas]
└─$ 

```
# Bandera
picoCTF{grep_is_good_to_find_things_f77e0797}
# Notas Adicionales
- Filtramos con grep el contenido del archivo con una expresion especifica de picoCTF  que seria lo logico al guardar la solucion y usamos cat para ver el contenido del file y filtrarlo con grep.