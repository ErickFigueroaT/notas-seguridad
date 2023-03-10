# Descripcion 
This file has a flag in plain sight (aka "in-the-clear"). [Download flag](https://mercury.picoctf.net/static/33996e32dce022205a6a36f69aba56f0/flag).

# Pistas
- Any hints about entering a command into the Terminal (such as the next one), will start with a '$'... everything after the dollar sign will be typed (or copy and pasted) into your Terminal.
- To get the file accessible in your shell, enter the following in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/33996e32dce022205a6a36f69aba56f0/flag`
- $ man cat
# Solucion 
```bash
┌──(erick㉿kali)-[~/Descargas]
└─$ wget https://mercury.picoctf.net/static/33996e32dce022205a6a36f69aba56f0/flag  
--2023-03-09 23:36:03--  https://mercury.picoctf.net/static/33996e32dce022205a6a36f69aba56f0/flag
Resolviendo mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Conectando con mercury.picoctf.net (mercury.picoctf.net)[18.189.209.142]:443... conectado.
Petición HTTP enviada, esperando respuesta... 200 OK
Longitud: 34 [application/octet-stream]
Grabando a: «flag»

flag         100%      34  --.-KB/s    en 0s       

2023-03-09 23:36:06 (9.40 MB/s) - «flag» guardado [34/34]

                                                    
┌──(erick㉿kali)-[~/Descargas]
└─$ cat lyrics(1).txt 
Completing file
apache-tomcat-8.5.84.tar.gz            
area.txt                               
emacs_1%3a27.1+1-3.1_all.deb           
emacs-common_1%3a27.1+1-3.1_all.deb    
emacs-gtk_1%3a27.1+1-3.1+b1_amd64.deb  
emacs-lucid_1%3a27.1+1-3.1+b1_amd64.deb
emacs-nox_1%3a27.1+1-3.1+b1_amd64.deb  
file                                   
file1                                  
file2                                  
file3                                  
file5                                  
flag                                   
hard-link                              
hola\ /                                
lyrics\(1\).txt                        
lyrics.txt                             
salida                                 
salida2                                
salida3                                
store.c                                
strings                                
sublime-text_build-3211_amd64.deb      
zacatecas.txt                          
┌──(erick㉿kali)-[~/Descargas]
└─$ cat flag 
picoCTF{s4n1ty_v3r1f13d_2aa22101}
                                                    
┌──(erick㉿kali)-[~/Descargas]
└─$ 



```
# Bandera
picoCTF{s4n1ty_v3r1f13d_2aa22101}

# Notas Adicionales
- descargamos el archivo con wget 
- vemos el contenido con cat.