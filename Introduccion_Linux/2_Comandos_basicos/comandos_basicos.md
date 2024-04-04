# Comandos Básicos

*Se agregara informacion respecto a los comandos basicos Linux*

### Cómo saber en qué usuario me encuentro
```bash
$ whoami
```

### Cómo leer un directorio o archivo
```bash
$ cat

Ejemplo: $ cat example.txt
```
### Moverse de Directorio
```bash
$ cd 'nombre-directorio'

# Devolverse a un directorio
$ cd ..
```
### Buscar texto en ficheros
```bash
$ grep

Ejemplo: $ cat /etc/group | grep 'tu-usuario'
```

### Conocer la ruta absoluta
```bash
$ which 

Ejemplo: $ which whoami [return -> /usr/bin/whoami]

$ command -v

Ejemplo: $ command -v whoami
```

### Cómo saber en qué ruta me encuentro
```bash
$ pwd
```

### Mostrar de manera detallada los archivos o directorios
```bash
$ ls -l

$ ll
```