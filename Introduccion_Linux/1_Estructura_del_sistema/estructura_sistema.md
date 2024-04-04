# Estructura del Sistema

*Se agregara informacion respecto a la Estructura del Sistema en Linux*

|         Directorio            |            Descripción         |
|-------------------------------|--------------------------------|
| Directorio **Raíz**           | Símbolo **"/"** , directorio principal a partir del cual se ramifican todos los demás directorios. |
| Directorio **/bin**           | Directorio **estático y compartible** en el que se **almacenan archivos binarios/ejecutables** necesarios para el funcionamiento del sistema.<br />*Los archivos binarios los pueden ocupar todos los usuarios del SO.* |
| Directorio **/boot**          | Directorio **estático NO compartible** que contiene la totalidad de los archivos necesarios para el arranque del PC **excepto los archivos de configuración.** | 
|                               | *Archivos de arranque automático: <br />- Kernel <br />- Gestor de arranque GRUB* |
| Directorio **/dev**           | Linux trata a los dispositivos de Hardware como si fueran un archivo. Estos archivos que representan nuestros dispositivos de Hardware se hallan almacenados en el directorio * **/dev.** * |
|                               | * Archivos básicos en la carpeta **/dev:**  <br />- **CDROM** -> Representa el dispositivo CDROM <br />- **SDA** -> Representa el Disco duro SATA <br />- **AUDIO** -> Representa la tarjeta de sonido <br />- **PSAUX** -> Representa el puerto PS/2 <br />- **LPX** -> Representa la impresora <br />- **FD0** -> Representa disquetera * |
| Directorio **/etc**           | Directorio **estático** que contiene los **archivos de configuración del SO**. También contiene archivos de configuración para controlar el funcionamiento de diversos programas. |
|                               | * Algunos archivos de configuración en **/etc** pueden ser sustituidos o complementados por archivos de configuración ubicados en el directorio principal **/home**. * |
| Directorio **/home**          | Directorio **variable y compartible**. Esta destinado a alojar la totalidad de los archivos personales de los distintos usuarios del SO a excepción del usuario * **ROOT**. * |
|                               | * Algunos archivos son: <br />- Fotos <br />- Docs <br />- Videos <br />- etc * |
| Directorio **/lib**           | Directorio **estático y que PUEDE ser compartible**. Contiene bibliotecas compartidas que son necesarias para arrancar los ejecutables que se almacenan en los directorios **/bin** y **/sbin**. |
| Directorio **/mnt**           | Finalidad de albergar los puntos de montaje de los distintos dispositivos de almacenamiento. |
|                               | * Ejemplo: <br />- Discos duros externos <br />- Particiones de unidades externas <br />- etc * |
| Directorio **/media**         | Similar al directorio **/mnt**. Contiene los puntos de montaje de los medios extraibles de almacenamiento.
|                               | * Ejemplo: <br />- Memorias USB <br />- Lectores de CD-ROM <br />- Unidades de disquete * |
| Directorio **/opt**           | El contenido almacenado en **/opt** es **estático y compartible**. Su función es almacenar programas que no vienen con el SO. |
|                               | * Ejemplo: <br />- Spotify <br />-Google Chrome <br />- etc * |
| Directorio **/proc**          | Se trata de un sistema de archivos virtual. Este nos proporciona información acerca de los distintos procesos y aplicaciones que se están ejecutando en el SO. |
| Directorio **/root**          | Directorio **variable NO compartible**. Es el directorio * **/home** * del administrador del sistema (usuario **ROOT**). |
| Directorio **/sbin**          | Directorios **estático y compartible**. Su función es similar al directorio * **/bin** *, con la diferencia de que el directorio **/sbin almacena archivos binarios/ejecutables que solo ejecuta el usuario root**. |
| Directorio **/srv**           | Se usa para almacenar directorios y datos que usan ciertos servidores que podamos tener instalados en el pc. |
| Directorio **/tmp**           | Se crean y se almacenan los archivos temporales y las variables para que los programas puedan funcionar de forma adecuada. |
| Directorio **/usr**           | Directorio **compartido y estático**. Contiene la gran mayoría de programas instalados en el SO. |
| Directorio **/var**           | Contiene archivos de datos **variables y temporables**.
|                               | * Ejemplo: <br />- Registros del sistema **(logs)** <br />- REgistros de programas instalados en el SO <br />- Archivos spool <br />- etc * |
| Directorio **/sys**           | Contiene información similar al directorio * **/proc** *. Dentro de **/sys** se encuentra información: |
|                               | * - Estructurada y jerárquica acerca del Kernel del equipo. <br />- Nuestras particiones y sistemas de archivo <br />- Nuestros drivers <br />- etc  * |
| Directorio **/lost-found**    | Directorio que se crea en las particiones del disco con un sistema de archivos **‘ext’** de ejecutar herramientas para restaurar y recuperar el SO, por ejemplo: **fsch**. <br /> * Si el SO no ha presentado problemas, el directorio permanente vacío. En caso contrario, tendrá ficheros y directorios que han sido recuperados tras la caída del SO. * |
