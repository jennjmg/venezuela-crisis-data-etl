CAST

## Resumen

Este proyecto se centra en la creación de un sistema de procesamiento de datos para apoyar las iniciativas de respuesta ante la crisis en Venezuela.

El sistema recopila información no estructurada, como mensajes de redes sociales, informes de chats y publicaciones públicas en las que las personas solicitan ayuda, denuncian la desaparición de personas o comparten información sobre centros de ayuda.

El objetivo principal es transformar estos datos sin procesar e inconsistentes en un formato estructurado y fiable que puedan utilizar diferentes plataformas.

### Cómo funciona

El proceso sigue un flujo sencillo:

1. Entrada (datos sin procesar)
El sistema recibe datos de texto no estructurados procedentes de fuentes como redes sociales, aplicaciones de mensajería e informes manuales.
Ejemplo:
«mi hermana Ana López desaparecida en Valencia CI 12345678»

2. Procesamiento (ETL)
El sistema extrae información clave del texto:
- Nombre
- Número de identificación nacional (cédula)
- Tipo de caso (desaparición, rescate, centro de ayuda)
- Ubicación

3. Salida
Los datos procesados se convierten a un formato JSON estructurado:

```json
{
  «tipo»: «desaparecido»,
  «nombre»: «Ana López»,
  «cédula»: «12345678»,
  «ubicación»: «Valencia»
}

4.Objetivo final
El objetivo es crear una fuente de datos limpia y unificada que:

Reduzca la duplicación y los errores
Permita compartir datos entre plataformas
Facilite la creación de API y sistemas en tiempo real para la respuesta humanitaria

------------------

ENG

## Overview

This project focuses on building a data processing system to support crisis response efforts in Venezuela.

The system collects unstructured information such as social media messages, chat reports, and public posts where people request help, report missing persons, or share information about aid centers.

The main goal is to transform this raw and inconsistent data into a structured and reliable format that can be used by different platforms.

### How it works

The process follows a simple pipeline:

1. Input (raw data)  
The system receives unstructured text data from sources such as social media, messaging apps, and manual reports.  
Example:  
"mi hermana Ana Lopez desaparecida en Valencia CI 12345678"

2. Processing (ETL)  
The system extracts key information from the text:
- Name
- National ID (cédula)
- Type of case (missing, rescue, aid center)
- Location

3. Output  
The processed data is converted into a structured JSON format:

```json
{
  "tipo": "desaparecido",
  "nombre": "Ana Lopez",
  "cedula": "12345678",
  "ubicacion": "Valencia"
}

4. Final objective
The objective is to build a clean and unified data source that:

Reduces duplication and errors
Enables data sharing across platforms
Supports the creation of APIs and real-time systems for humanitarian response
