# Permisos Especiales

### Permiso Sticky bit

Consiste en darle a un Directorio/Carpeta el atributo **Sticky bit** con la finalidad de que un usuario que no pertenezca al grupo 'pepe' no pueda eliminar los archivos creados.

* **Objetivo Principal**: * Solo el usuario creador puede eliminar o renombrar un archivo en sistemas donde todos los usuarios tengan permiso de Lectura y Escritura *

```bash
[ROOT]
$ cd /home/Desktop

$ mkdir test_pepe

$ chown pepe:pepe test_pepe

$ chmod 777 test_pepe

$ cd test_pepe

$ echo Esto es una prueba > file.txt
```

```bash
[PEPE]
$ su pepe

$ chmod +t test_pepe

$ exit
```

Ahora cualquier usuario que NO sea pepe solo podra leer el archivo pero NO tendra permiso para ELIMINAR el archivo.

### Permisos SUID & SGID

**SUID** -> Permite que un archivo se ejecute como si fuese el **propietario**, independiente del usuario que lo ejecute. El archivo se ejecutara como el propietario.

```bash
# Asignar privilegio SUID a 'python3.9'
$ chmod 4755 /usr/bin/python3.9

$ chmod u+s /usr/bin/python3.9

# Encontrar archivos que tengan SUID
$ find / -type f -perm 4000 2>/dev/null
    -> Esto puede ser un problema. ya que cualquier usuario que inicie Python3.9 lo iniciara como ROOT, permitiendo escalar privilegios.
```

**SGID** -> Permite que cualquier usuario ejecute el archivo como si fuese el **miembro del grupo** al que pertenece el archivo.

```bash
# Asignar privilegio GUID a 'python3.9'
$ chmod 2755 /usr/bin/python3.9

$ chmod g+s /usr/bin/python3.9

# ENcontrar archivos que tengan GUID
$ find / -perm -2000 2>/dev/null
    
-> Si se establece en un Directorio/Carpeta, cualquier archivo creado dentro de esa carpeta se le asignara como grupo perteneciente al grupo del directorio.
```