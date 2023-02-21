Level 5
# Objetivo
The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.
# Datos  de Acceso 
ssh bandit4@**bandit.labs.overthewire.org** -p2220

User: bandit4 Pass: 2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
# Solucion 

```bash
bandit4@bandit:~$ ls
inhere
bandit4@bandit:~$ cd inhere/
bandit4@bandit:~/inhere$ ls
-file00  -file01  -file02  -file03  -file04  -file05  -file06  -file07  -file08  -file09
bandit4@bandit:~/inhere$ cat ./-file00
T߼B#6Kt36Xt��)bandit4@bandit:~/inhere$ cd ../
bandit4@bandit:~$ cd inhere/
bandit4@bandit:~/inhere$ ls
-file00  -file01  -file02  -file03  -file04  -file05  -file06  -file07  -file08  -file09
bandit4@bandit:~/inhere$ cat ./file07
cat: ./file07: No such file or directory
bandit4@bandit:~/inhere$ cat ./-file07
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
bandit4@bandit:~/inhere$
```

# Notas Adicionales
- ls se usa para ver el contenido del directorio.
- cat se usa para ver el contenido de readme.
- cd se usa para ingresar a un directorio.