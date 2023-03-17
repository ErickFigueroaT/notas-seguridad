# Descripción
There is a website running at `https://jupiter.challenges.picoctf.org/problem/64649/` ([link](https://jupiter.challenges.picoctf.org/problem/64649/)). Someone has bypassed the login before, and now it's being strengthened. Try to see if you can still login! or http://jupiter.challenges.picoctf.org:64649

# Solución
```bash
Se inspecciona la página y busca una etiqueta oculta en el html, se revela y se intenta realizar un login. Basandose en la sentencia sql que aparece después de ser redireccionados, se busca una vulnerabilidad.

Esta página está protegida contra sentencias que incluyen "or" e "=", para vulnerar esta página, se busca inyectar una sentencias mediante el nombre de usuario buscando un usuario admin.

Se coloca admin'; en el campo de nombre.
```

# Bandera
picoCTF{m0R3_SQL_plz_c34df170}
# Notas Adicionales