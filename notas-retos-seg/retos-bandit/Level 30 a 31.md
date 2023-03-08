Level 30
# Objetivo
There is a git repository at `ssh://bandit30-git@localhost/home/bandit30-git/repo`. The password for the user `bandit30-git` is the same as for the user `bandit30`.

Clone the repository and find the password for the next level.
# Datos  de Acceso 
ssh bandit30@**bandit.labs.overthewire.org** -p2220

User: bandit30 Pass: xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS
# Solucion 

```bash
bandit30@bandit:/tmp/tmp.X0b44vxUoy$ cd repo/

bandit30@bandit:/tmp/tmp.X0b44vxUoy/repo$ ls
README.md
bandit30@bandit:/tmp/tmp.X0b44vxUoy/repo$ cat README.md 
just an epmty file... muahaha

bandit30@bandit:/tmp/tmp.X0b44vxUoy/repo$ git log
commit cf552c166d78421e64ddf52f850e680075d216e1 (HEAD -> master, origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:13 2023 +0000
    initial commit of README.md
    
bandit30@bandit:/tmp/tmp.X0b44vxUoy/repo$ git branch
* master
bandit30@bandit:/tmp/tmp.X0b44vxUoy/repo$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
  
bandit30@bandit:/tmp/tmp.X0b44vxUoy/repo$ git show-ref
cf552c166d78421e64ddf52f850e680075d216e1 refs/heads/master
cf552c166d78421e64ddf52f850e680075d216e1 refs/remotes/origin/HEAD
cf552c166d78421e64ddf52f850e680075d216e1 refs/remotes/origin/master
831aac2e2341f009e40e46392a4f5dd318483019 refs/tags/secret
bandit30@bandit:/tmp/tmp.X0b44vxUoy/repo$ git show 831aac2e2341f009e40e46392a4f5dd318483019
OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt



```

# Notas Adicionales
- cd se usa para ingresar a un directorio.
- mktemp permite a los usuarios crear un archivo o directorio temporal.
- ls se usa para ver el contenido del directorio.
