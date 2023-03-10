# Descripcion 
There is a nice program that you can talk to by using this command in a shell: `$ nc mercury.picoctf.net 35652`, but it doesn't speak English...
# Pistas
- You can practice using netcat with this picoGym problem: [what's a netcat?](https://play.picoctf.org/practice/challenge/34)
- You can practice reading and writing ASCII with this picoGym problem: [Let's Warm Up](https://play.picoctf.org/practice/challenge/22)
# Solucion 
```bash
┌──(erick㉿kali)-[~/Descargas/picoCTF2021]
└─$  nc mercury.picoctf.net 35652
112 
105 
99 
111 
67 
84 
70 
123 
103 
48 
48 
100 
95 
107 
49 
116 
116 
121 
33 
95 
110 
49 
99 
51 
95 
107 
49 
116 
116 
121 
33 
95 
57 
98 
51 
98 
55 
51 
57 
50 
125 
10 
                                                    
┌──(erick㉿kali)-[~/Descargas/picoCTF2021]
└─$ 



```
# Bandera
picoCTF{g00d_k1tty!_n1c3_k1tty!_9b3b7392}

# Notas Adicionales
- nos da un codigo binario al conectarnos al servidor y en la pagina [Convert Decimal to ASCII - Online ASCII Tools](https://onlineasciitools.com/convert-decimal-to-ascii) y nos dara la llave.

