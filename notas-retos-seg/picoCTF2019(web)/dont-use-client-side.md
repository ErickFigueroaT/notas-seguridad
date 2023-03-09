# Descripcion 
Can you break into this super secure portal? `https://jupiter.challenges.picoctf.org/problem/29835/` ([link](https://jupiter.challenges.picoctf.org/problem/29835/)) or http://jupiter.challenges.picoctf.org:29835

# Pistas
Never trust the client
# Solucion 
```bash
1.- inspeccionamos la pagina.
2.- como validan la contraseña desde el html en los ifs 
de split viene la contraseña de split a split 8 y solo hay
que juntar los pedazos.

```
# Bandera
picoCTF{no_clients_plz_7723ce}
# Notas Adicionales