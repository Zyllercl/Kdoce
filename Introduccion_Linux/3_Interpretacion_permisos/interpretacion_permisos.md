# Lectura e Interpretacion de Permisos

### Formato en Decimal

|   Permiso   |     Numero      |   Descripcion   |
|-------------|-----------------|-----------------|
|    --X      |      **1**      | **Permiso de Ejecucicion** |
|    -W-      |        2        | Permiso de Escritura | 
|    -WX      |        3        | Permido de Estricura y Ejecucion |
|    R--      |      **4**      | **Permiso de Lectura** |
|    R-X      |        5        | Permiso de Lectura y Ejecucion |
|    RW-      |        6        | Permiso de Lectura y Escritura |
|    RWX      |      **7**      | **Permiso de Lectura, Escritura y Ejecucion** |

### Asignacion de permisos
```bash
# Propietarios
u | Owner
g | Group
o | Others

# Permisos
r | Permido de Lectura
w | Permiso de Escritura
x | Permiso de Ejecucion

# Definicion del Primer Caracter de los Archivos
d | Directorio
b | Archivo Especiales
c | Archivo de caracteres especiales (Dispositivo TTY, impresora)
l | Archivo de vinculo o enlace (enlace simbolico)
p | Archivo especial de canal (pipe o tuberia)
s | Socket de dominio para comunicacion entre procesos
```

### Interpretacion
```bash
-rw-    r--     r--  1   zyller       zyller   19 oct 23 19:23 file.txt
Owner  Grupo   Otros	Propietario   Grupo
```

### Ejemplos
```bash
# Ejemplo en modo Simbolico o Caracter
$ chmod u+x example.txt -> Asignacion de permiso de ejecucion al propietario (Owner) del archivo

# Ejemplo en modo Octal
$ chmod 100 example.txt -> Asignacion unicamente al permiso de ejecucion SOLO al propietario (Owner) del archivo
```