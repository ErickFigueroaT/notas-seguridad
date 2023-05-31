# Descripcion 
Can you solve this?

Additional details will be available after launching your challenge instance.
`n1 > n1 + n2 OR n2 > n1 + n2`Enter them here `nc saturn.picoctf.net 61807`. [Source](https://artifacts.picoctf.net/c/454/flag.c)
# Pistas
- Integer overflow
- Not necessarily a math problem
# Solucion 
```bash
erickso678-picoctf@webshell:~$ echo -e "2147483647\n1" | nc saturn.picoctf.net 61807
n1 > n1 + n2 OR n2 > n1 + n2 
What two positive numbers can make this possible: 
You entered 2147483647 and 1
You have an integer overflow
YOUR FLAG IS: picoCTF{Tw0_Sum_Integer_Bu773R_0v3rfl0w_f6ed8057}

erickso678-picoctf@webshell:~$ 

```
# Bandera
picoCTF{Tw0_Sum_Integer_Bu773R_0v3rfl0w_f6ed8057}
# Notas Adicionales
