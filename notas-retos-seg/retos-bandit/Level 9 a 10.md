Level 9
# Objetivo
The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.
# Datos  de Acceso 
ssh bandit9@**bandit.labs.overthewire.org** -p2220

User: bandit9 Pass: EN632PlfYiZbn3PhVK3XOGSlNInNE00t
# Solucion 

```bash
bandit9@bandit:~$ cat  data.txt  | strings | grep ==
c========== the
h;========== password
========== isT
n.E========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
bandit9@bandit:~$
```

# Notas Adicionales
- cat se usa para ver el contenido de un archivo.
-  grep lo usamos para buscar un patron.