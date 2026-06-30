CAST

## Resumen

Este proyecto tiene como objetivo construir un sistema de procesamiento de datos para apoyar iniciativas de respuesta ante emergencias en Venezuela.

El sistema recopila información no estructurada proveniente de redes sociales, aplicaciones de mensajería y reportes manuales, donde las personas solicitan ayuda, reportan desapariciones o comparten información sobre centros de apoyo.

El objetivo principal es transformar estos datos inconsistentes en un formato estructurado, fiable y reutilizable por diferentes plataformas.

### Cómo funciona

El sistema sigue un pipeline sencillo de tipo ETL:

1. Entrada (datos sin procesar)  
Se reciben textos no estructurados desde diversas fuentes.  
Ejemplo:  
"mi hermana Ana López desaparecida en Valencia CI 12345678"

2. Procesamiento (ETL)  
Se extrae información relevante del texto:
- Nombre (informativo, no confiable como identificador)
- Número de identificación (cédula, cuando esté disponible)
- Tipo de caso (desaparición, rescate, centro de acopio)
- Ubicación

Además:
- La cédula funciona como identificador principal cuando existe
- Se genera un identificador de caso (`id_caso`) para cada registro

3. Salida  
Los datos se transforman en un formato JSON estructurado:

```json
{
  "id_caso": "",
  "cedula": "",
  "tipo": "desaparecido",
  "nombre": "Ana Lopez",
  "ubicacion": "Valencia",
  "fecha_registro": "2026-06-30"
}
```

### Consideraciones del sistema

La cédula es el identificador más fiable
Los nombres pueden contener errores y no se usan como clave
En ausencia de cédula, se genera un identificador de caso único
Se prioriza no perder información sobre eliminar duplicados
El sistema trabaja bajo incertidumbre (datos incompletos o inconsistentes)

### Objetivo final
Construir una fuente de datos unificada que:

Reduzca la duplicación y los errores
Permita compartir información entre plataformas
Sirva como base para APIs y sistemas en tiempo real


------------------

ENG

## Overview

This project aims to build a data processing system to support emergency response efforts in Venezuela.

The system collects unstructured information from social media, messaging platforms, and manual reports where people request help, report missing persons, or share information about aid centers.

The main goal is to transform inconsistent raw data into a structured, reliable format that can be used across multiple platforms.

### How it works

The system follows a simple ETL pipeline:

1. Input (raw data)  
Unstructured text is collected from different sources.  
Example:  
"mi hermana Ana Lopez desaparecida en Valencia CI 12345678"

2. Processing (ETL)  
Relevant information is extracted:
- Name (informational, not reliable as an identifier)
- National ID (cédula, when available)
- Case type (missing, rescue, aid center)
- Location

Additionally:
- The cédula is used as the primary identifier when available
- A case identifier (`id_caso`) is generated for each record

3. Output  
Data is converted into structured JSON format:

```json
{
  "id_caso": "",
  "cedula": "",
  "tipo": "desaparecido",
  "nombre": "Ana Lopez",
  "ubicacion": "Valencia",
  "fecha_registro": "2026-06-30"
}
```
### System considerations

The cédula is the most reliable identifier
Names may contain errors and are not used as keys
When no cédula is available, a unique case identifier is generated
The system prioritizes not losing information over removing duplicates
It operates under uncertainty (incomplete and inconsistent data)

### Final objective
To build a unified data source that:

Reduces duplication and errors
Enables data sharing across platforms
Serves as a base for APIs and real-time systems
