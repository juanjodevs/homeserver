
# Configuración servidor cloud en casa

Según vimos en los directos de [twitch.tv](https://twitch.tv/juanjodevs), probamos varias plataformas para almacenar nuestros datos y nos quedamos finalmente con NextCloud para los datos y Immich para las imágenes y vídeos.

A pesar de que la app Memories de NextCloud cumple bien la función de sincronización, Immich me gustó mucho más para almacenar las fotos y vídeos como remplazo de Google Photos / iCloud. Todo funciona perfectamente con la configuración por defecto.

Además también he configurado algunas aplicaciones más que quedan explicadas en los vídeos de [Youtube](https://youtube.com/juanjodevs).

## NextCloud

Sustituto de Dropbox / Google Drive / iCloud

## Immich

Sustituto de Google Photos / iCloud Photos

## Yacht

Aplicación para ver los contenedores que están funcionando actualmente además de algunos datos como el consumo de CPU o RAM.

## NginxProxyManager


Servidor Nginx con extras para redirigir el tráfico según la URL por la que acceden a nuestro a servidor, además de propocionar una fácil gestión para los certificados.
## PiHole

Al no poder acceder con nuestro dominio desde dentro de la red a nuestro servidor, tendremos que usar PiHole para sobreescribir las direcciones de DNS que querramos. Además sirve como bloqueador de anuncios.

## Monitoring
Consiste en 3 aplicaciones que unidas sirven para tener un panel de administrador donde poder ver todas las estadísticas de nuestro servidor como CPU, RAM, Uso de los discos, estado de la red, etc...
## Lanzar servicios

Para lanzar los servicios lo único que hay que hacer (tras modificar a nuestro gusto las rutas los archivos de configuración) es lanzar este comando en la carpeta del proyecto que queramos iniciar:

```bash
docker-compose up -d
```

## Configuración ssh

En la carpeta ssh hay un ejemplo de archivo de configuración para entrar en nuestro servidor sin tener que poner ni el usuario ni la contraseña, una vez hayamos puesto nuestra clave pública como se mostró en el directo de [twitch.tv](https://twitch.tv/juanjodevs).

Este archivo debería ir en nuestra carpeta de usuario:

```bash
/home/juanjo/.ssh/config
```
