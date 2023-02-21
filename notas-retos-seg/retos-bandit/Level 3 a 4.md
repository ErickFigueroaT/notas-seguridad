Level 4
# Objetivo
The password for the next level is stored in a hidden file in the **inhere** directory.
# Datos  de Acceso 
ssh bandit3@**bandit.labs.overthewire.org** -p2220

User: bandit3 Pass: aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
# Solucion 

```bash
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere/
bandit3@bandit:~/inhere$ ls -a
.  ..  .hidden
bandit3@bandit:~/inhere$ cat ./.hidden
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
bandit3@bandit:~/inhere$
```

# Notas Adicionales
- ls se usa para ver el contenido.
- ls -a para ver los archivos ocultos.
- cat se usa para ver el contenido de un archivo.
- cd se usa para ingresar a un directorio.