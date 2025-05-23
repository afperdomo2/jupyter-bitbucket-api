# Análisis de Proyectos en Bitbucket

Este proyecto analiza los datos de repositorios, commits y pull requests de Bitbucket para generar visualizaciones y métricas sobre el proceso de desarrollo.

## 📋 Descripción

El proyecto utiliza Jupyter Notebooks para conectarse a la API de Bitbucket, extraer datos de repositorios, pull requests y commits, y luego generar análisis visuales sobre:

- Actividad de commits
- Estados de pull requests (abiertos, fusionados, rechazados)
- Tiempos de revisión y fusión
- Patrones de comentarios en PRs
- Análisis de ramas
- Eficiencia del equipo de desarrollo

## 🚀 Instalación y uso

### Requisitos previos
- Python 3.x
- Entorno virtual (venv)
- Credenciales de Bitbucket (usuario y token)

### Configuración de credenciales

1. Crea un archivo `.env` en la raíz del proyecto con las siguientes variables:
```
BITBUCKET_USERNAME=tu_usuario
BITBUCKET_APP_PASSWORD=tu_token_app
BITBUCKET_WORKSPACE=tu_workspace
```

### Iniciar el proyecto

```sh
# Activar el entorno
venv\Scripts\activate

# Iniciar Jupyter
jupyter notebook
```

## 📊 Notebooks disponibles

- **proyectos.ipynb**: Análisis detallado de pull requests, commits y ramas.
- **archivos_estimaciones.ipynb**: Análisis de estimaciones de proyectos.

## 🔌 Dependencias

- pandas
- matplotlib
- seaborn
- python-dotenv
- requests

## 📚 Referencias

### API Bitbucket:

https://developer.atlassian.com/server/bitbucket/rest/v905/intro/#intro