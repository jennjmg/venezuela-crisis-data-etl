CAST 

# Venezuela Crisis Data ETL
Este proyecto tiene como objetivo construir un sistema de procesamiento de datos para apoyar la respuesta ante situaciones de crisis en Venezuela.

El sistema recoge información no estructurada (redes sociales, mensajería, reportes manuales), la procesa y la transforma en un formato estructurado.

### Objetivo

Crear una fuente de datos unificada que:
- Reduzca errores y duplicados
- Permita compartir información entre plataformas
- Sirva como base para APIs y herramientas de ayuda

### Estructura de datos

```json
{
  "id_caso": "",
  "cedula": "",
  "tipo": "",
  "nombre": "",
  "ubicacion": "",
  "fecha_registro": ""
}
```

### Qué hace este sistema

- Procesa mensajes de redes sociales
- Extrae:
  - nombres
  - cédulas
  - ubicaciones
- Clasifica en categorías críticas:
  - rescate
  - desaparecido
  - ayuda
  - infraestructura
- Genera outputs estructurados (JSON / Excel)

---------

ENG

# Venezuela Crisis Data ETL
This project aims to build a data processing system to support crisis response efforts in Venezuela.
The system collects unstructured data (social media, messaging, manual reports), processes it, and transforms it into structured datasets.

### Objective
Create a unified data source that:

Reduces errors and duplication
Enables data sharing across platforms
Serves as a base for APIs and response tools

### Data structure

```json
{
  "id_caso": "",
  "cedula": "",
  "tipo": "",
  "nombre": "",
  "ubicacion": "",
  "fecha_registro": ""
}
```

### What This System Does

- Processes social media messages
- Extracts:
  - names
  - ID numbers
  - locations
- Classifies into critical categories:
  - rescue
  - missing persons
  - assistance
  - infrastructure
- Generates structured outputs (JSON / Excel)

