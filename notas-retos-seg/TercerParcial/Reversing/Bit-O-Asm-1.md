# Descripcion 
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.Download the assembly dump [here](https://artifacts.picoctf.net/c/509/disassembler-dump0_a.txt).
# Pistas
As with most assembly, there is a lot of noise in the instruction dump. Find the one line that pertains to this question and don't second guess yourself!
# Solucion 
```bash
El reto nos indica que una parte del ensamble en hexadecimal es la bandera entnces convertimos cada una y probamos para ver cual es la correcta que en este caso fue 0x30=48

```
# Bandera
picoCTF{48}
# Notas Adicionales