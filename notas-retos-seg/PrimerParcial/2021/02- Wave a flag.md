# Descripcion 
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/cfea736820f329083dab9558c3932ada/warm) has extraordinarily helpful information...

# Pistas
- This program will only work in the webshell or another Linux computer.
- To get the file accessible in your shell, enter the following in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/cfea736820f329083dab9558c3932ada/warm`
- Run this program by entering the following in the Terminal prompt: `$ ./warm`, but you'll first have to make it executable with `$ chmod +x warm`
- -h and --help are the most common arguments to give to programs to get more information from them!
- Not every program implements help features like -h and --help.
# Solucion 
```bash
┌──(erick㉿kali)-[~/Descargas/picoCTF2021]
└─$ ./warm         
zsh: permiso denegado: ./warm
                                                    
┌──(erick㉿kali)-[~/Descargas/picoCTF2021]
└─$ ./warm -h 
zsh: permiso denegado: ./warm
                                                    
┌──(erick㉿kali)-[~/Descargas/picoCTF2021]
└─$ chmod +x warm             
                                                    
┌──(erick㉿kali)-[~/Descargas/picoCTF2021]
└─$ ./warm        
Hello user! Pass me a -h to learn what I can do!
                                                    
┌──(erick㉿kali)-[~/Descargas/picoCTF2021]
└─$ ./warm -h     
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_30e77291}
                                                    
┌──(eri


```
# Bandera
picoCTF{b1scu1ts_4nd_gr4vy_30e77291}

# Notas Adicionales
- siguiendo las pistas nos dice que el archivo se ejecuta con ./warm junto con un -h pero no nos dara acceso entonces hay que usar chmod para cambiar el acceso y a si nos de la llave.
