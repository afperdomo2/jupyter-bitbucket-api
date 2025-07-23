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
```sh
BITBUCKET_USERNAME=tu_usuario
BITBUCKET_APP_PASSWORD=tu_token_app
BITBUCKET_WORKSPACE=tu_workspace

# Solo para el reporte de bitbucket_incidencias_abiertas
# Se coloca el nombre del desarrollador, que aparece en el campo de Author
BITBUCKET_AUTHOR=your_name


# Estas variables son para el archivo de archivos_estimaciones
# En la lista, se deben poner los IDS de los archivos. Separar cada Id por una coma.
DESARROLLADORES=Dev1,Dev2
LISTA_IDS_ESTIMACIONES_GOOGLE_DRIVE=ID_ARCHIVO_DEV1,ID_ARCHIVO_DEV2
```

Para obtener el ID de un archivo de estimación del desarrollador, se debe abrir el archivo y ver la URL (ver ESTE_ES_TU_ID)

**Ejemplo:** https://docs.google.com/spreadsheets/d/ESTE_ES_TU_ID/edit?gid=0#gid=0

- BITBUCKET_USERNAME:
  - Ir a Bitbucket
  - Ir al botón de **settings** (La tuerca)
  - Ir a la opción de **Personal Bitbucket settings**
  - Ir a la opción de **Account settings**
  - Buscar el campo de **Username**

- BITBUCKET_APP_PASSWORD (API KEY):
  - Ir a Bitbucket
  - Ir al botón de **settings** (La tuerca)
  - Ir a la opción de **Personal Bitbucket settings**
  - Ir a la opción de **App password**
  - Dar clic en el botón de **Create app password**, se le asigna un nombre y se seleccionan solo las opciones de **READ**

- BITBUCKET_WORKSPACE:
  - Este se encuentra en la URL del proyecto:
    - **Ejemplo:** https://bitbucket.org/[ESTE ES TU WORKSPACE]/[REPOSITORIO]/pull-requests/

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