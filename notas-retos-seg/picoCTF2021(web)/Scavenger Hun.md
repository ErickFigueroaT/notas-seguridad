# Descripcion 
There is some interesting information hidden around this site [http://mercury.picoctf.net:27278/](http://mercury.picoctf.net:27278/). Can you find it?

# Pistas
- You should have enough hints to find the files, don't run a brute forcer.
# Solucion 
```bash
1.-La primer parte de la llave esta en el html en un comentario.
2.-La segunda llave esta en el .css en la parte final.
3.- La tercera parte de la llave esta en el robos.txt 
4.- La cuarta parte se encuentra en /.htaccess ya que nos dice una pista en el robots que nos idica que es un servidor apache y Access esta en mayuscula lo cual al investigar en google es es un archivo de configuración instalado en servidores con apache que permite al administrador que lo gestiona restringir el acceso a los directorios o archivos que se incluyen en el servidor y nos dara la cuarta parte de la llave.
5.- La pista nos indica que esta en la tienda mac pero lo que es tienda esta en mayuscula entonces en google nos dice que la DS_Store es donde se almacena la informacion en mac entonces al buscador agregamos el DS_Store y nos llevara a otra pagina con la quinta y ultima parte de la llave.

```
# Bandera
picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_a69684fd}        
# Notas Adicionales