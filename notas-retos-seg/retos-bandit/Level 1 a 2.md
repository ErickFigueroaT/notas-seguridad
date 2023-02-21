Level 2
# Objetivo
The password for the next level is stored in a file called **-** located in the home directory
# Datos  de Acceso 
ssh bandit1@**bandit.labs.overthewire.org** -p2220

User: bandit1 Pass: NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
# Solucion 

```bash
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$
```

# Notas Adicionales
- ls se usa para ver el contenido.
- cat se usa para ver el contenido de -.

