# Chatbot de Simulación de Entrevista en el Consulado Americano

**Link:** [Link a este design doc](#)

**Author(s):** Oziel Valenzuela, Hector Sanchez

**Status:** Draft

**Última actualización:** 2025-03-10

## Contenido
- Objetivo
- Goals
- Non-Goals
- Background
- Overview
- Detailed Design
  - Arquitectura del Sistema
  - Flujo de la Entrevista
  - Tecnologías y APIs Utilizadas
  - Infraestructura y Despliegue
- Consideraciones
- Métricas

## Objetivo
Crear un chatbot que simule una entrevista en el consulado americano para que los usuarios puedan practicar y mejorar sus respuestas antes de la entrevista real.

## Goals
- Desarrollar un chatbot que realice preguntas basadas en entrevistas reales del consulado.
- Permitir que el usuario reciba retroalimentación sobre sus respuestas.
- Integrar el chatbot en Telegram

## Non-Goals
- No se pretende que el chatbot garantice la aprobación de la visa.
- No se usará reconocimiento de voz en esta versión inicial.

## Background
Muchas personas enfrentan nervios y falta de preparación al asistir a una entrevista en el consulado americano. Un chatbot puede ayudarles a practicar mediante una simulación interactiva, mejorando su confianza y desempeño.

## Overview
El chatbot interactuará con los usuarios a través de una interfaz conversacional en la que les hará preguntas basadas en entrevistas reales. Usará NLP para interpretar las respuestas y proporcionar retroalimentación. Dependiendo de la respuesta del usuario, podrá hacer preguntas de seguimiento o dar consejos sobre cómo mejorar.

## Detailed Design

### Arquitectura del Sistema
- **Frontend :** Chat de Telegram.
- **Backend:** API REST con Flask/FastAPI para manejar la lógica de la conversación.
- **Procesamiento de Lenguaje Natural (NLP):** Se puede usar Dialogflow, OpenAI GPT o Rasa para interpretar respuestas.
- **Base de Datos:** Para almacenar respuestas de usuarios y evaluar su progreso.
- **Plataforma de Integración:** Telegram Bot API.

### Flujo de la Entrevista
1. El usuario inicia la conversación con el bot.
2. El bot hace preguntas basadas en entrevistas reales del consulado.
3. El usuario responde y el bot analiza la respuesta.
4. El bot proporciona retroalimentación y hace preguntas de seguimiento.
5. Al finalizar, el bot da un resumen con recomendaciones para mejorar.

### Tecnologías y APIs Utilizadas
- **Backend:** Flask/FastAPI
- **Procesamiento de Texto:** OpenAI GPT, Dialogflow o Rasa
- **Base de Datos:** Firebase, PostgreSQL o MongoDB
- **Integraciones:** Telegram Bot API

### Infraestructura y Despliegue
- **Hosting:** AWS Lambda, Google Cloud Functions o un VPS con Docker
- **Base de Datos:** Firebase Firestore o PostgreSQL en AWS RDS
- **Manejo de Versiones:** GitHub

## Consideraciones
- La privacidad de los datos debe ser prioritaria.
- Las respuestas del bot deben ser realistas y alineadas con entrevistas reales.
- Se deben evitar sesgos en las respuestas para garantizar equidad en la práctica.

## Métricas
- Número de usuarios que completan la simulación.
- Porcentaje de respuestas bien calificadas.
- Tiempo promedio por entrevista.
