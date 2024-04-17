# Documentacion Odoo Kdoce

## Actualizar SO
```bash
sudo apt-get update && apt-get upgrade
```

### Configurar Github 
git config --global user.name "Nombre"
git config --global user.email "Correo"


# Instalacion de Odoo
```bash
sudo wget https://raw.githubusercontent.com/Yenthe666/InstallScript/14.0/odoo_install.sh
```

## Configurar archivo 
```bash
sudo nano odoo_install.sh

Editar -> GENERATE_RANDOM_PASSWORD="False"
```

### Permiso de ejecucion
```bash
sudo chmod +x odoo_install.sh
```

### Ejecutar archivo Odoo_install.sh

### Data Instalacion Odoo
```bash
Port: 8069
User service: odoo
Configuraton file location: /etc/odoo-server.conf
Logfile location: /var/log/odoo
User PostgreSQL: odoo
Code location: odoo
Addons folder: odoo/odoo-server/addons/
Password superadmin (database): admin
Start Odoo service: sudo service odoo-server start
Stop Odoo service: sudo service odoo-server stop
Restart Odoo service: sudo service odoo-server restart
```
