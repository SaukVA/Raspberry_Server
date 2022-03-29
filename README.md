# Servidor Raspberry

Este repositorio contiene la estructura que se necesita para generar una servidor con una Raspberry-pi. Este repositorio se divide en las siguientes partes:

* [Requisito](#Requisitos)
* [Set Up](#Set-Up)

## Requisitos

...

## Set Up
En esta sección se indicara los pasos que se deben de seguir para desplegar la infraestructura del servidor.

Primero deberemos de descargar el repositorio en nuestra Raspberry:

```
git clone https://github.com/SaukVA/raspberry_server.git
```
Con el servidor descargado nos deberemos de registrar en [DuckDns](https://www.duckdns.org/)🦆 y registrar el el subdominio que nosotros queramos.

Después debemos de crear eberemos crear es archivo `.env` el cual contendrá todos los datos sensibles(contraseñas, dominios ...). La estructura de este fichero debe ser:

```
SUBDOMAINS= # Subdominio registrado(seguido de coma): ejemplo, 
DOMINIO= # Dominio completo registrado: ejemplo.duckdns.org
TOKEN= # Token de cuenta de duckduck
```

Una vez hecho esto ya podemos montar la infraestructura para ello deberemos ejecutar: 

```
docker-compose up -d
docker-compose restart swag
```

Si todo ha salido bien podremos acceder al panel de administrador de Portainer🐋 a través del dominio de DuckDns que se ha configurado seguido por la subcarpeta de portainer(https://ejemplo.duckdns.org/portainer/).