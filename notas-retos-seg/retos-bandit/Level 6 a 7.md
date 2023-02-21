Level 7
# Objetivo
The password for the next level is stored **somewhere on the server** and has all of the following properties:

-   owned by user bandit7
-   owned by group bandit6
-   33 bytes in size
# Datos  de Acceso 
ssh bandit6@**bandit.labs.overthewire.org** -p2220

User: bandit6 Pass: P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
# Solucion 

```bash
bandit6@bandit:~$ find / -readable -user bandit7 -group bandit6 -size 33c
find: ‘/dev/mqueue’: Permission denied
find: ‘/dev/shm’: Permission denied
find: ‘/var/spool/bandit24’: Permission denied
find: ‘/var/spool/rsyslog’: Permission denied
find: ‘/var/spool/cron/crontabs’: Permission denied
find: ‘/var/crash’: Permission denied
find: ‘/var/snap/lxd/common/lxd’: Permission denied
find: ‘/var/cache/ldconfig’: Permission denied
find: ‘/var/cache/apt/archives/partial’: Permission denied
find: ‘/var/cache/apparmor/e10c1cf9.0’: Permission denied
find: ‘/var/cache/apparmor/c47eabf7.0’: Permission denied
find: ‘/var/cache/private’: Permission denied
find: ‘/var/cache/pollinate’: Permission denied
find: ‘/var/log’: Permission denied
find: ‘/var/lib/update-notifier/package-data-downloads/partial’: Permission denied
find: ‘/var/lib/polkit-1’: Permission denied
find: ‘/var/lib/chrony’: Permission denied
find: ‘/var/lib/snapd/void’: Permission denied
find: ‘/var/lib/snapd/cookie’: Permission denied
find: ‘/var/lib/amazon’: Permission denied
/var/lib/dpkg/info/bandit7.password
find: ‘/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/private’: Permission denied
find: ‘/var/tmp’: Permission denied
find: ‘/drifter/drifter14_src/axTLS’: Permission denied
find: ‘/boot/efi’: Permission denied
find: ‘/etc/polkit-1/localauthority’: Permission denied
find: ‘/etc/sudoers.d’: Permission denied
find: ‘/etc/multipath’: Permission denied
find: ‘/etc/ssl/private’: Permission denied
find: ‘/snap/core20/1778/etc/ssl/private’: Permission denied
find: ‘/snap/core20/1778/root’: Permission denied
find: ‘/snap/core20/1778/var/cache/ldconfig’: Permission denied
find: ‘/snap/core20/1778/var/cache/private’: Permission denied
find: ‘/snap/core20/1778/var/lib/private’: Permission denied
find: ‘/snap/core20/1778/var/lib/snapd/void’: Permission denied
find: ‘/snap/core18/2667/etc/ssl/private’: Permission denied
find: ‘/snap/core18/2667/root’: Permission denied
find: ‘/snap/core18/2667/var/cache/ldconfig’: Permission denied
find: ‘/snap/core18/2667/var/lib/private’: Permission denied
find: ‘/sys/kernel/tracing’: Permission denied
find: ‘/sys/kernel/debug’: Permission denied
find: ‘/sys/fs/pstore’: Permission denied
find: ‘/sys/fs/bpf’: Permission denied
find: ‘/run/chrony’: Permission denied
find: ‘/run/user/11022’: Permission denied
find: ‘/run/user/11033’: Permission denied
find: ‘/run/user/11032’: Permission denied
find: ‘/run/user/11025’: Permission denied
find: ‘/run/user/11002’: Permission denied
find: ‘/run/user/11021’: Permission denied
find: ‘/run/user/11017’: Permission denied
find: ‘/run/user/11014’: Permission denied
find: ‘/run/user/11007’: Permission denied
find: ‘/run/user/11015’: Permission denied
find: ‘/run/user/11018’: Permission denied
find: ‘/run/user/11019’: Permission denied
find: ‘/run/user/11009’: Permission denied
find: ‘/run/user/11016’: Permission denied
find: ‘/run/user/11003’: Permission denied
find: ‘/run/user/11008’: Permission denied
find: ‘/run/user/11011’: Permission denied
find: ‘/run/user/11004’: Permission denied
find: ‘/run/user/11013’: Permission denied
find: ‘/run/user/11020’: Permission denied
find: ‘/run/user/11000’: Permission denied
find: ‘/run/user/11001’: Permission denied
find: ‘/run/user/11005’: Permission denied
find: ‘/run/user/11012’: Permission denied
find: ‘/run/user/11006/systemd/inaccessible/dir’: Permission denied
find: ‘/run/user/11023’: Permission denied
find: ‘/run/sudo’: Permission denied
find: ‘/run/screen/S-bandit20’: Permission denied
find: ‘/run/multipath’: Permission denied
find: ‘/run/cryptsetup’: Permission denied
find: ‘/run/lvm’: Permission denied
find: ‘/run/credentials/systemd-sysusers.service’: Permission denied
find: ‘/run/systemd/propagate’: Permission denied
find: ‘/run/systemd/unit-root’: Permission denied
find: ‘/run/systemd/inaccessible/dir’: Permission denied
find: ‘/run/lock/lvm’: Permission denied
find: ‘/home/ubuntu’: Permission denied
find: ‘/home/drifter8/chroot’: Permission denied
find: ‘/home/bandit27-git’: Permission denied
find: ‘/home/bandit29-git’: Permission denied
find: ‘/home/bandit5/inhere’: Permission denied
find: ‘/home/bandit30-git’: Permission denied
find: ‘/home/drifter6/data’: Permission denied
find: ‘/home/bandit31-git’: Permission denied
find: ‘/home/bandit28-git’: Permission denied
find: ‘/tmp’: Permission denied
find: ‘/lost+found’: Permission denied
find: ‘/proc/tty/driver’: Permission denied
find: ‘/proc/1301526/task/1301526/fd/6’: No such file or directory
find: ‘/proc/1301526/task/1301526/fdinfo/6’: No such file or directory
find: ‘/proc/1301526/fd/5’: No such file or directory
find: ‘/proc/1301526/fdinfo/5’: No such file or directory
find: ‘/root’: Permission denied
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
bandit6@bandit:~$
```

# Notas Adicionales
- cat se usa para ver el contenido de un archivo.
- find lo usamos para filtrar archivos junto con -type para filtrar por tipo de archivo, junto con f para el tipo de archivo y con -size para poner el tamaño de archivo que deseamos buscar.