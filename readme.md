
# Configuración servidor cloud en casa

Según vimos en los directos de [twitch.tv](https://twitch.tv/juanjodevs), probamos varias plataformas para almacenar nuestros datos y nos quedamos finalmente con NextCloud para los datos y Immich para las imágenes y vídeos.

A pesar de que la app Memories de NextCloud cumple bien la función de sincronización, Immich me gustó mucho más para almacenar las fotos y vídeos como remplazo de Google Photos / iCloud. Todo funciona perfectamente con la configuración por defecto.

## NextCloud

En la carpeta nextcloud encontraremos el docker compose que tiene tanto el servidor con la aplicación de nextcloud como un mysql.

## Immich

En la carpeta de immich encontraremos el docker-compose y el archivo .env que es el que modificaremos para las rutas y contraseñas.

## Lanzar servicios

Para lanzar ambos servicios lo único que hay que hacer (tras modificar a nuestro gusto las rutas los archivos de configuración) es lanzar este comando en ambas carpetas:

```bash
docker-compose up -d
```

## Configuración ssh

En la carpeta ssh hay un ejemplo de archivo de configuración para entrar en nuestro servidor sin tener que poner ni el usuario ni la contraseña, una vez hayamos puesto nuestra clave pública como se mostró en el directo de [twitch.tv](https://twitch.tv/juanjodevs).

Este archivo debería ir en nuestra carpeta de usuario:

```bash
/home/juanjo/.ssh/config
```
