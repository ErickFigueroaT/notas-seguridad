# Descripcion 
Our data got corrupted on the way here. Luckily, nothing got replaced, but every block of 3 got scrambled around! The first word seems to be three letters long, maybe you can use that to recover the rest of the message.Download the corrupted message [here](https://artifacts.picoctf.net/c/191/message.txt).
# Pistas
Split the message up into blocks of 3 and see how the first block is scrambled
# Solucion 
```bash
Al descargar el archivo y hacer un cat viene un texto cifrado y en la pista nos dice que hay que dividir entre 3 el bloque y ver que sale entonces creamos un codigo en python que nos decifre el texto en utf8 recorriendo el texto en 3 para que nos de la bandera.


```
# Bandera
picoCTF{7R4N5P051N6_15_3XP3N51V3_56E6924A}
# Notas Adicionales