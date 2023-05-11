# Descripcion 
The name of the game is [speed](https://www.youtube.com/watch?v=8piqd2BWeGI). Are you quick enough to solve this problem and keep it above 50 mph? [need-for-speed](https://jupiter.challenges.picoctf.org/static/27dd5548b14661f65ce3ac6a8a8f575b/need-for-speed).
# Pistas
- What is the final key?
# Solucion 
```bash
1.- Primero cambiamos con chmod el archivo de need for speed para poder ejecutarlo.
2.- Usamos gdb para abrir el archivo need for speed.
3.- dentro de gdb ignoramos el signalrm y usamos r para ejecuaar el archivo y nos dara la bandera.


```
# Bandera
PICOCTF{Good job keeping bus #1f2ac4ec speeding along!}
# Notas Adicionales
