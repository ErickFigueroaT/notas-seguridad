Level 32 
# Objetivo
After all this `git` stuff its time for another escape. Good luck!
# Datos  de Acceso 
ssh bandit32@**bandit.labs.overthewire.org** -p2220

User: bandit32 Pass: rmCBvG56y58BXzv98yZGdO7ATVL5dW8y
# Solucion 

```bash
WELCOME TO THE UPPERCASE SHELL
>> $0
$ ls
uppershell
$ ls -la
total 36
drwxr-xr-x  2 root     root      4096 Feb 21 22:03 .
drwxr-xr-x 70 root     root      4096 Feb 21 22:04 ..
-rw-r--r--  1 root     root       220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root      3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root     root       807 Jan  6  2022 .profile
-rwsr-x---  1 bandit33 bandit32 15128 Feb 21 22:03 uppershell
$ whoami
bandit33
$ man /etc/bandit_pass/bandit33
odHo63fHiFqcWWJG9rLiLDtPm45KzUKy
Manual page bandit33 line 1/2 (END) (press h for help or q to quit)
$ $
```

# Notas Adicionales
- ls se usa para ver el contenido del directorio.
- man proporciona informacion de un comando o archivo.
- usamos $0 para ingresar al shell porque es necsario usar un parametro posicional que son del 1 al n , pero en este caso usamos 0 que es el valor del script que se invoco.
- whoami nos dice el usuario que esta en la sesion.

