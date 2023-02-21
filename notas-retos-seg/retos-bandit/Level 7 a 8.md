Level 8
# Objetivo
The password for the next level is stored in the file **data.txt** next to the word **millionth**
# Datos  de Acceso 
ssh bandit7@**bandit.labs.overthewire.org** -p2220

User: bandit7 Pass: z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
# Solucion 

```bash
bandit7@bandit:~$ cat data.txt | grep millionth
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
bandit7@bandit:~$
```

# Notas Adicionales
- cat se usa para ver el contenido de un archivo.
- grep lo usamos para buscar un patron.