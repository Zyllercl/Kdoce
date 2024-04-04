# Conexion a la Base de Datos

## Conexion a Postgres
```bash
sudo -u postgres psql
```

## Traspasar backup a una Base de Datos
```bash
sudo -u 'nombre_usuario_db' psql 'nombre_db' < /tmp/'archivo.sql'
```