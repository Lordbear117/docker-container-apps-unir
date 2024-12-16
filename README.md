# Docker Container Apps - UNIR DevOps

Este repositorio contiene la documentación, los proyectos y los Dockerfiles necesarios para la actividad de la **maestría en DevOps** en la **Universidad Internacional de La Rioja (UNIR)**. En este proyecto se utilizaron tecnologías como **Docker**, **Docker Hub** y **Docker Compose** para crear y gestionar aplicaciones contenedorizadas en diferentes lenguajes de programación.

## 📂 Estructura del Repositorio

El repositorio está dividido en tres principales carpetas:

- **`docs/`**: Contiene toda la documentación relacionada con el proceso de creación, configuración y despliegue de las aplicaciones en contenedores.
- **`projects/`**: Incluye los proyectos de las aplicaciones creadas en diferentes lenguajes de programación (Node.js, Python, Java, etc.), que se ejecutan dentro de contenedores Docker.
- **`dockerfiles/`**: Contiene los Dockerfiles utilizados para construir las imágenes de Docker para cada uno de los proyectos.

## 🛠 Tecnologías Utilizadas

- **Docker**: Para crear, administrar y ejecutar contenedores con las aplicaciones
- **Docker Hub**: Para almacenar y compartir las imágenes de Docker creadas
- **Docker Compose**: Para gestionar múltiples contenedores y facilitar el despliegue de aplicaciones con dependencias entre contenedores

## 🚀 Pasos para Ejecutar los Proyectos

### 1. Clonar el Repositorio

```bash
git clone https://github.com/Lordbear117/docker-container-apps-unir.git
cd docker-container-apps-unir
```

### 2. Ejecutar Proyectos con Docker Compose

```bash
cd projects/express-api-docker-compose
docker-compose up --build
```

### 3. Construcción de Dockerfiles Individuales

Construir la imagen Docker:

```bash
docker build -t nombre-de-la-imagen .
```

Ejecutar el contenedor:

```bash
docker run -p 3000:3000 nombre-de-la-imagen
```

## 🌐 Acceso a Aplicaciones

Una vez levantados los contenedores, accede a las aplicaciones:

- Express API: `http://localhost:3000`
- FastAPI: `http://localhost:8000`

## 📄 Documentación

Toda la documentación detallada se encuentra en la carpeta `docs/`, que incluye:

- Procedimientos de construcción
- Configuración de Dockerfiles
- Explicaciones técnicas de contenedores e interacciones

## 🐳 Imágenes en Docker Hub

Accede a las imágenes en: `lordbears117/unir-cesar-castro`

Obtener imagen:

```bash
docker pull lordbears117/unir-cesar-castro/nombre-de-la-imagen
```

Ejecutar imagen:

```bash
docker run -p puerto-local:puerto-contenedor lordbears117/unir-cesar-castro/nombre-de-la-imagen
```

## 🤝 Contribuciones

1. Haz un fork del repositorio
2. Crea tu rama de características
3. Realiza tus cambios
4. Abre un pull request

## 📝 Licencia

Proyecto de uso educativo para la maestría en DevOps de la Universidad Internacional de La Rioja (UNIR).

---

**Desarrollado con ❤️ para la maestría en DevOps - UNIR**
