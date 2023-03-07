Level 21
# Objetivo

# Datos  de Acceso 
ssh bandit21@**bandit.labs.overthewire.org** -p2220

User: bandit21 Pass: NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
# Solucion 

```bash
bandit21@bandit:~$ ls - la
ls: cannot access '-': No such file or directory
ls: cannot access 'la': No such file or directory
bandit21@bandit:~$ ls -la
total 24
drwxr-xr-x  2 root     root     4096 Feb 21 22:03 .
drwxr-xr-x 70 root     root     4096 Feb 21 22:04 ..
-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
-r--------  1 bandit21 bandit21   33 Feb 21 22:03 .prevpass
-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
bandit21@bandit:~$ cat /etc/cron.d/cronjob_bandit22
@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
bandit21@bandit:~$ cat /usr/bin/cronjob_bandit22.sh
#!/bin/bash
chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
bandit21@bandit:~$ cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff
bandit21@bandit:~$
```

# Notas Adicionales
- cat se usa para ver el contenido de un archivo.
-  chmod cambia los permisos del archivo.