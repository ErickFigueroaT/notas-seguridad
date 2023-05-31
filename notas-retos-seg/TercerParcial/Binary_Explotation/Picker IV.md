# Descripcion 
Can you figure out how this program works to get the flag?

Additional details will be available after launching your challenge instance.
# Pistas
- With Python, there are no binaries. With compiled languages like C, there is source code, and there are binaries. Binaries are created from source code, they are a conversion from the human-readable source code, to the highly efficient machine language, in this case: x86_64.
- How can you find the address that `win` is at?

# Solucion 
```bash
Al iniciar la instacia nos da la opcion a descargar 2 archivos de picker iv.c y picker IV al descargarlos con wget usaremos el gdb acon picker IV en la pista nos indica que busquemos el address de win entonces con gdb usamos el comando info address win y nos dara 0x40129e entonces entramos a la instancia y nos pedira una clave y es 0x40129e que previamente obtuvimos con gdb.


```
# Bandera
picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_b8de1af4}
# Notas Adicionales