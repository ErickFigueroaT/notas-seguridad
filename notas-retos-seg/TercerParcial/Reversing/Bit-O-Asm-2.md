# Descripcion 
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.Download the assembly dump [here](https://artifacts.picoctf.net/c/510/disassembler-dump0_b.txt).
# Pistas
`PTR`'s or 'pointers', reference a location in memory where values can be stored.
# Solucion 
```bash
En este caso por la pista nos indica que en el ensamble la bandera esta en donde se almacenan los valores entonces en este caso esta en 0x9fe1a que ya haciendo la conversion nos da 654874 y al probar es la llave correcta 
```
# Bandera
picoCTF{654874}
# Notas Adicionales