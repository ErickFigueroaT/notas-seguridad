# Descripción
I found this cipher in an old book. Can you figure out what it says? Connect with `nc jupiter.challenges.picoctf.org 58295`.

# Pistas
- There are tools that make this easy.
- Perhaps looking at history will help

# Solución


```bash
1.- Al conectarnos al servidor nos da todo un texto encriptado
2.- Se deduce que se resulve por vignere entonces nos vamos a cyberchef 
pero no tenemos la llave para poder traducir entonces nos vamos a https://www.boxentriq.com/code-breaking/vigenere-cipher
para ver que llave es una vez que nos da la llave la usamos en cyberchef y nos da la bandera.

```

# Bandera
picoCTF{b311a50_0r_v1gn3r3_c1ph3ra966878a}
# Notas Adicionales