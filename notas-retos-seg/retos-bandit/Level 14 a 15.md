level 14
# Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.
# Datos  de Acceso 
ssh bandit14@**bandit.labs.overthewire.org** -p2220

User: bandit14 Pass: fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
# Solucion 

```bash
bandit14@bandit:~$ nc localhost 30000

Wrong! Please enter the correct current password
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
bandit14@bandit:~$ nc localhost 30000
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt


bandit14@bandit:~$


```

# Notas Adicionales
- Nos conectanos al localhost con nc.
