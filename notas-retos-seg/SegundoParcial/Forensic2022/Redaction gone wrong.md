# Descripcion 
Now you DON’T see me.This [report](https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf) has some critical data in it, some of which have been redacted correctly, while some were not. Can you find an important key that was not redacted properly?
# Pistas
- How can you be sure of the redaction?
# Solucion 
```bash
Descargamos la herramineta de pdftotext y una vez descargada convertimos a texto el pdf y usamos un cat para ver el texto generado y nos saldra visible la bandera.

```
# Bandera
picoCTF{C4n_Y0u_S33_m3_fully}

# Notas Adicionales