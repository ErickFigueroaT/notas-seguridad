Level 9
# Objetivo
The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once
# Datos  de Acceso 
ssh bandit8@**bandit.labs.overthewire.org** -p2220

User: bandit8 Pass: TESKZC0XvTetK0S9xNwm25STk5iWrBvP
# Solucion 

```bash
bandit8@bandit:~$ cat data.txt | sort | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
bandit8@bandit:~$
```

# Notas Adicionales
- cat se usa para ver el contenido de un archivo.
- sort lo usamos para ordenar el texto y poder usar uniq.
- uniq sirve para encontrar cadenas de texto duplicado.