Level 11 
# Objetivo
The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions
# Datos  de Acceso 
ssh bandit11@**bandit.labs.overthewire.org** -p2220

User: bandit11 Pass: 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
# Solucion 

```bash
bandit11@bandit:~$ ls
data.txt
bandit11@bandit:~$ cat data.txt
Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi
bandit11@bandit:~$ cat data.txt | tr 'n-za-mN-ZA-M' 'a-zA-Z'
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
bandit11@bandit:~$

```

# Notas Adicionales
- cat se usa para ver el contenido de un archivo.
- ls se usa para ver el contenido del directorio.