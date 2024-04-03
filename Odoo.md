# Estructura de archivos Odoo
Addons = Plugins -> Modulos del Sistema

## Ruta de Modulos
```bash
/opt/odoo/addons/
```

## Ruta de Modulos Personalizados
```bash
/opt/odoo/custom_addons/
```

## Definicion de rutas de un Modulo Personalizado
```python
/models/    -> Archivos Python donde se define cada objeto o clase
/views/     -> Archivos XML de las vistas Web de los modelos
/reports/   -> Todo archivo generados por un XML se guardan com PDF 
/security/  -> Dos tipos de archivos:
                    - XML
                    - CSV
                
            Se debe definir quien puede leer y escribir en mi modelo
/static/    -> Todos los documentos estaticos que no van a cambiar con el tiempo. Ej: Imagenes

/wizards/   -> Modelos especiales (Paso a Paso), aqui se encuentran archivos.py y archivos.xml


__init__.py     -> Indica como se debe iniciar la app o modelo

    Dentro del archivo:
        from . import models
        from . import wizards

__manifest__.py -> Es un JSON con la configuracion del plugin

            Dentro del campo 'data:[]' se encuentran todos los archivos XML y CSV que se van a usar en el plugin personalizado
```

### Creacion de un Modelo en '/models/'
```python
Cuando se crea un archivo dentro de la carpeta '/Models/', por ejempplo: 'nombre_archivo.py' se debe agregar al __init__.py de la siguiente forma:

    from . import 'nombre_archivo'
```
