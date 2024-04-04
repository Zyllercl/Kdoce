# Asignacion de Permisos

### Ejemplo de CHMOD
```bash
# Crear 2 carpetas: Una con Usuario Normal y otra con ROOT
$ mkdir test1 [ROOT] 
$ mkdir test2 [NO ROOT]

# Migrar al usuario normal
$ cd test 1
$ touch example
    -> Mostrara un ERROR ya que el propietario y el grupo asociado es ROOT
        ERROR [!]touch: cannot touch 'example': Permission denied
    -> No dejara crear el archivo 'example' ya que el usuario ('Username') no pertenece al grupo ROOT

# Cambio de privilegios de un Archivo/Directorio
$ chmod o+w test1 -> Otros usuarios podrán escribir en el directorio 'test1'

$ chmod o-w test1 -> Elimina el privilegio de escritura para el directorio 'test1'

# Cambiar grupo de un Archivo/Directorio
$ chgrp 'username' test1

# Permitir que los grupos puedan escribir en 'test1'
$ chmod g+w test1

# Ejercicio: Cambiar permiso del directorio test1 a rw-|-w-|rw-
[Permiso actual] drwx rwx r-x 1 root   zyller 0 oct 25 13:45 test1

Instruccion:
$ chmod u-x,g-rx,o+w,o-x test1

# Eliminar todos los Archivos/Directorios de forma recursiva
[!] $ rm -r *
```

### Creacion de Usuarios
```bash
# Dirigirse a /home
$ cd /home

# Crear una carpeta con el nombre del nuevo usuario
$ mkdir pepe

# Crear Usuario
$ useradd pepe -s /bin/bash -d /home/pepe
    # Parametros:
    -s -> Indica tipo de shell
    -d -> Directorio personal del usuario

# Eliminar un usuario
$ userdel pepe

# Corroborar si el usuario fue creado
$ cat /etc/passwd | grep 'pepe'

[return] pepe:x:1001:1004::/home/pepe:/bin/bash

# Identificador de grupo
$ cat /etc/group | grep 'pepe'

# Crear una Password al usuario pepe
$ passwd pepe

# Asignar al usuario pepe como grupo al directorio de trabajo 'pepe'
$ chgrp pepe pepe

# Asignar al usuario pepe como propietario al directorio de trabajo 'pepe'
$ chown pepe pepe

# Otra forma de asignar propietario y grupo
$ chown pepe:pepe pepe

# Creacion de Grupos
$ usermod -a -G Alumnos pepe

# Corroborar si el usuario esta asignado al grupo Alumnos

# Migrar al directorio 'pepe'
$ su pepe

# Mostrar grupos asociados
$ id

[return] uid=1001(pepe) gid=1004(pepe) groups=1004(pepe),1005(Alumnos)

# Eliminar grupo
$ groupdel Alumnos
```