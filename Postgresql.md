# Comandos de Postgresql

## Conexion a Postgres como root
```bash
sudo -u postgres psql
```

## Crear un Usuario
```bash
CREATE USER 'nombre_usuario' WITH password 'password'
```

## Eliminar un Usuario
```bash
DROP USER 'nombre_usuario'
```

## Crear una Base de Datos
```bash
CREATE DATABASE 'nombre_db' WITH OWNER 'nombre_usuario'
```

## Eliminar una Base de Datos
```bash
DROP DATABASE 'nombre_db'
```

## Acceder a una Base de Datos con X Usuario
```bash
psql -U 'nombre_usuario' 'nombre_db' [X]
```

## Dump db a un archivo
```bash
 pg_dump -U nombre_usuario nombre_db > db.out
```

## Dump todas las Bases de Datos
```bash
sudo su - postgres
pg_dumpall > /var/lib/pgsql/backups/dumpall.sql 
```

## Restaurar db
```bash
sudo su - postgres
psql -f /var/lib/pgsql/backups/dumpall.sql 'nombre_db'

o

psql -U postgres nombredb < archivo_restauracion.sql
```


## Obtener ayuda
```bash
\h
```

## Salir de Postgres
```bash
\q
```

## Lista de Bases de Datos
```bash
\l
```

## Seleccionar una Base de Datos
```bash
\c 'nombre_db'
```

## Listar tablas 
```bash
\dt
```