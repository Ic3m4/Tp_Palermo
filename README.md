 ██╗ ██████╗███████╗███╗   ███╗ █████╗ ███╗   ██╗
███║██╔════╝██╔════╝████╗ ████║██╔══██╗████╗  ██║
╚██║██║     █████╗  ██╔████╔██║███████║██╔██╗ ██║
 ██║██║     ██╔══╝  ██║╚██╔╝██║██╔══██║██║╚██╗██║
 ██║╚██████╗███████╗██║ ╚═╝ ██║██║  ██║██║ ╚████║
 ╚═╝ ╚═════╝╚══════╝╚═╝     ╚═╝╚═╝  ╚═╝╚═╝  ╚═══╝

Trabajo practico integrador grupal – VM en Debian – Junio 2025
###################################################################################################
########
Universidad de Palermo
Autor = Jonatan Rios 

#######
####################################################################################################
## Objetivo

El proyecto consiste en preparar un entorno Linux con las siguientes tareas:

- Agregar un nuevo disco de 10 GB a la máquina virtual.
- Crear dos particiones estándar:
  - `/www_dir` de 3 GB para alojar archivos web.
  - `/backup_dir` de 6 GB para almacenar backups.
- Configurar Apache para utilizar `/www_dir` como raíz del sitio.
- Asegurar el montaje automático de ambas particiones al iniciar el sistema.
- Crear un archivo persistente `/proc/particion` con el contenido de `/proc/partitions`.
- Desarrollar un script de backup (`backup_full.sh`) ubicado en `/opt/scripts`.

## Script `backup_full.sh`

- Realiza un backup comprimido del directorio de origen indicado por argumento.
- El archivo generado incluye la fecha en formato `YYYYMMDD`.
- El destino del backup también se pasa como argumento.
- El script valida la existencia de los directorios antes de ejecutar.
- Se incluye opción `-help` para mostrar uso básico.

