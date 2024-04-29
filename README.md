# Kdoce
Documentacion Kdoce

## Instalacion 'pgadmin4'
```bash
- Instalar Postgresql
> sudo apt install postgresql
> sudo apt install postgresql postgresql-contrib -y

- Instalar curl
> sudo apt install curl

- Obtener KEY de pgadmin4
> sudo curl https://www.pgadmin.org/static/packages_pgadmin_org.pub | sudo apt-key add

- Agregar KEY publica de pgadmin4 al sistema operativo
> echo "deb https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/$(lsb_release -cs) pgadmin4 main" | sudo tee /etc/apt/sources.list.d/pgadmin4.list

- Update del sistema
> sudo apt update

- Instalacion de pgadmin4
> sudo apt install pgadmin4
```
