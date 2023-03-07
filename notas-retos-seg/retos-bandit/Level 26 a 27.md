Level 26
# Objetivo
Good job getting a shell! Now hurry and grab the password for bandit27!
# Datos  de Acceso 
ssh bandit26@**bandit.labs.overthewire.org** -p2220

User: bandit26 Pass: c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1
# Solucion 

```bash
 _                     _ _ _   ___   __
  _                     _ _ _   ___   __
 | |                   | (_) | |__ \ / /
 | |__   __ _ _ __   __| |_| |_   ) / /_
 | '_ \ / _` | '_ \ / _` | | __| / / '_ \
 | |_) | (_| | | | | (_| | | |_ / /| (_) |
 |_.__/ \__,_|_| |_|\__,_|_|\__|____\___/
~                                                                                                                                                     
~                                                                                                                                                     
~                                                                                                                                                                                                                                                                                                        
~                                                                                                                                                     
~                                                                                                                                                     
~                                                                                                                                                     
~                                                                                                                                                     
~                                                                                                                                                     
:set shell=/bin/bash
:shell                                                                                                                    
bandit26@bandit:~$ ls
bandit27-do  text.txt
bandit26@bandit:~$ ./bandit27-do cat /etc/bandit_pass/bandit27
YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
```

# Notas Adicionales
- nuevamente nos aprovechamos de more, para poner  la ventana muy chica luego accedemos a al vim para poder ver la ventana se pone /bin/bash para poder acceder a la terminal y se usa ls para ver que arhivos hay y cat para ver la constraseña del proximo reto.