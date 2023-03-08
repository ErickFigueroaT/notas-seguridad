
# Descripcion 
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings) without running it?
# Pistas
[strings](https://linux.die.net/man/1/strings)
# Solucion 
```bash
┌──(erick㉿kali)-[~/Descargas]
└─$ strings strings | grep picoCTF 
picoCTF{5tRIng5_1T_d66c7bb7}
                                                     
┌──(erick㉿kali)-[~/Descargas]
└─$ 



```
# Bandera
picoCTF{5tRIng5_1T_d66c7bb7}
# Notas Adicionales
- Usamos grep que filtra expresiones específicas en texto sin formato. Como sabemos que el formato de las banderas de picoCTF es picoCTF{ }, podemos hacer grep para picoCTF. El comando entonces sería strings strings | grep picoCTF.

