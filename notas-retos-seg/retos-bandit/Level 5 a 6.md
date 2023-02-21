Level 6
# Objetivo
The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:

-   human-readable
-   1033 bytes in size
-   not executable
# Datos  de Acceso 
ssh bandit5@**bandit.labs.overthewire.org** -p2220

User: bandit5 Pass: lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
# Solucion 

```bash
bandit5@bandit:~$ ls
inhere
bandit5@bandit:~$ cd inhere/
bandit5@bandit:~/inhere$ ls
maybehere00  maybehere03  maybehere06  maybehere09  maybehere12  maybehere15  maybehere18
maybehere01  maybehere04  maybehere07  maybehere10  maybehere13  maybehere16  maybehere19
maybehere02  maybehere05  maybehere08  maybehere11  maybehere14  maybehere17
bandit5@bandit:~/inhere$ find -type -size 1033c
find: Unknown argument to -type: -
bandit5@bandit:~/inhere$ find -type f -size 1033c
./maybehere07/.file2
bandit5@bandit:~/inhere$ cd maybehere07
bandit5@bandit:~/inhere/maybehere07$ ls
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3
bandit5@bandit:~/inhere/maybehere07$ cat ./.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        bandit5@bandit:~/inhere/maybehere07$
```

# Notas Adicionales
- ls se usa para ver el contenido del directorio.
- cat se usa para ver el contenido.
- cd se usa para ingresar a un directorio.
- find lo usamos para filtrar archivos junto con -type para filtrar por tipo de archivo, junto con f para el tipo de archivo y con -size para poner el tamaño de archivo que deseamos buscar.