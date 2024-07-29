![Banner](./img/portainer-server.png)

# 🖥️ Portainer Server

Portainer Server es un repositorio que facilita la configuración de un servidor Portainer utilizando Docker Compose.

## 📝 Descripción

Este repositorio contiene un archivo Docker Compose que configura un entorno completo para gestionar tus contenedores Docker a través de Portainer. Incluye la configuración básica necesaria para poner en marcha el servidor de Portainer.

## 🛠️ Instalación

### Requisitos

- Docker
- Docker Compose

### Pasos

1. Clona este repositorio:

```bash
git clone https://github.com/JSisques/portainer-server.git
```

2. Navega hasta el directorio del repositorio:

```bash
cd portainer-server
```

3. Ejecuta Docker Compose para iniciar el servicio:

```bash
docker-compose up -d
```

Esto iniciará el contenedor del servidor de Portainer en segundo plano.

## 🚀 Uso

Una vez que el contenedor esté en ejecución, puedes acceder a la interfaz de Portainer en:

- **Portainer:** https://localhost:9443

## 👨‍💻 Autor

- Nombre: Javier Plaza Sisqués
- GitHub: [JSisques](https://github.com/JSisques)

## 📄 Archivos de Configuración

En este repositorio se incluye el archivo de configuración necesario para personalizar el comportamiento del servidor de Portainer:

- **docker-compose.yml:** Configuración principal para desplegar el servidor de Portainer.

## 🧾 Ejemplo de docker-compose.yml

Aquí está el archivo docker-compose.yml utilizado para esta configuración:

```yaml
version: "3"
services:
  portainer-server:
    image: portainer/portainer-ce:latest
    container_name: portainer-server
    hostname: portainer-server
    volumes:
      - ./data:/data
    ports:
      - 9443:9443
    restart: unless-stopped
```
