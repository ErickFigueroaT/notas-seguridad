# Descripcion 
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 14291`.
# Pistas
- Remember the flag format is picoCTF{XXXX}
- What's a pipe? No not that kind of pipe... This [kind](http://www.linfo.org/pipes.html)
# Solucion 
```bash
┌──(erick㉿kali)-[~/Descargas]
└─$ nc jupiter.challenges.picoctf.org 14291 | grep picoCTF
picoCTF{digital_plumb3r_ea8bfec7}
                                                     
┌──(erick㉿kali)-[~/Descargas]
└─$ 



```
# Bandera
picoCTF{digital_plumb3r_ea8bfec7}
# Notas Adicionales
- las pistas nos indican que al momento de que nos conectemos tengas en cuenta el formato de la solucion en picoCTF y  | entonces nos da entender que usemos grep para filtar con picoCTF y a si nos de la solucion al momento de conectarnos. 