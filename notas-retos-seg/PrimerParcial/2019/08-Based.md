# Descripcion 
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with `nc jupiter.challenges.picoctf.org 15130`.
# Pistas
- I hear python can convert things.
- It might help to have multiple windows open.
# Solucion 
```bash
┌──(erick㉿kali)-[~/Descargas]
└─$ nc jupiter.challenges.picoctf.org 15130
Let us see how data is stored
pear
Please give the 01110000 01100101 01100001 01110010 as a word.
...
you have 45 seconds.....

Input:
pear 
Please give me the  156 165 162 163 145 as a word.
Input:
nurse 
Please give me the 636f6c6f7261646f as a word.
Input:
colorado 
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_02167de8}


```
# Bandera
picoCTF{learning_about_converting_values_02167de8}
# Notas Adicionales
- usamos la pagina https://www.rapidtables.com/convert/number/hex-to-ascii.html para en el primer acertijo para convertir de binario a ACII, en el segundo de octal a ACII y el ultimo de hexadecimal a ACII.
