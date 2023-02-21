Level 3
# Objetivo
The password for the next level is stored in a file called **spaces in this filename**
located in the home directory
# Datos  de Acceso 
ssh bandit2@**bandit.labs.overthewire.org** -p2220

User: bandit2 Pass: rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
# Solucion 

```bash
bandit2@bandit:~$ nano 'spaces in this filename'
Unable to create directory /home/bandit2/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.
 
 
 GNU nano 6.2                                     spaces in this filename *                                            aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG

                           [ Error writing spaces in this filename: Operation not permitted ]
^G Help        ^O Write Out   ^W Where Is    ^K Cut         ^T Execute     ^C Location    M-U Undo       M-A Set Mark
^X Exit        ^R Read File   ^\ Replace     ^U Paste       ^J Justify     ^/ Go To Line  M-E Redo       M-6 Copy


```

# Notas Adicionales
- usamos nano para abrir el archivo.


