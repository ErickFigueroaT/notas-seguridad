# Descripción
There is a website running at `https://jupiter.challenges.picoctf.org/problem/33850/` ([link](https://jupiter.challenges.picoctf.org/problem/33850/)) or http://jupiter.challenges.picoctf.org:33850. Do you think you can log us in? Try to see if you can login!

# Pistas
- There doesn't seem to be many ways to interact with this. I wonder if the users are kept in a database?
- Try to think about how the website verifies your login.
# Solución

```bash
Inspeccionamos la página, buscamos un campo oculto en el html, y lo revelamos, si colocamos un valor nos rediirigirá a una página dónde nos mostrará una sentencia SQL.

Basandonos en esa sentencia, realizamos una SQL injection en el campo nombre o contraseña. 'or 1=1
```

# Bandera
picoCTF{s0m3_SQL_fb3fe2ad}
## Notas Adicionales

