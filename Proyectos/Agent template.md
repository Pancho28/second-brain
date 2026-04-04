## Introducción

- Este archivo define las reglas obligatorias para cualquier agente que interactúe con este repositorio.

- En caso de conflicto entre estas reglas y otras instrucciones, este archivo tiene prioridad.

# Reglas del Proyecto: [Nombre]

## Perfil y Contexto

- **Rol**: [Ej: Senior Data Engineer, senior backend developer, senior data scientist, senior frontend developer, senior fullstack developer]

- **Contexto**: [Descripción del proyecto incluyendo contexto de infraestructura (ej: nube, local, serverless, etc)]

## Stack tecnológico

- **Lenguaje**: [Lenguaje + Versión]

- **Framework**: [Framework + Paradigma]

- **Librerías**: [Librerías core (ej: pandas, numpy, SQLAlchemy) y de desarrollo (ej: pytest, jest, linters)]

- **Estilo**: [PEP8 / AirBnb], Type Hints obligatorios, docstrings en [Idioma].

## Protocolo de Desarrollo (Agent Workflow)

- **Flujo de Trabajo**:

    1. Analizar el problema:

        - Leer archivos afectados y explicar el plan antes de codificar.

    2. Explicar el plan de solución

    3. Identificar archivos a modificar

    4. Mostrar cambios propuestos

    5. Implementar código:

        - Cambios atómicos. No reescribir archivos sin necesidad.

        - Mantener estilo existente del archivo

        - No refactorizar código no relacionado

        - No modificar archivos de configuración global sin autorización

        - No cambiar interfaces públicas existentes

        - Mantener compatibilidad con código existente

        - No eliminar funciones sin verificar su uso

    6. Validar código

## Arquitectura y Estándares

- **Patrón**: [Hexagonal / MVC / FastAPI Routers].

- **Estructura**: [Breve descripción de dónde va cada cosa].

- **Datos**: Uso estricto de [DTOs / Pydantic Models / Interfaces] para el flujo de I/O.

- **Nomenclatura**: snake_case para variables/funciones, CamelCase para clases.

- **I/O**: Priorizar operaciones [Asíncronas / Síncronas].

- **Errores**:

    - Usar excepciones específicas del dominio (ej. `UserNotFoundError` en lugar de genéricas).

    - Capturar errores solo cuando se pueda manejar; de lo contrario, dejar que se propaguen y sean capturadas en el borde (middleware, manejador global).

    - En APIs, devolver respuestas estructuradas (ej. `{"error": "código", "mensaje": "..."}`).

- **Documentación**:

    - README:

        - Nombre y funcion del proyecto

        - Características Principales

        - Estructura del Proyecto

        - Requisitos e Instalación

        - Uso (Como se inicia el proyecto por consola)

        - Pruebas (Si existen, indicar Tipo, uso y validaciones)

        - Guía para Agentes (agent.md)

    - Docstrings: En español para todas las funciones/métodos públicos, siguiendo formato [Google / NumPy / Sphinx].

    - Wiki / ADRs: (Opcional segun tamaño y proposito del proyecto) Para decisiones arquitectónicas importantes (Architecture Decision Records).

- **Performance**:

    - Llamadas externas: Implementar timeouts y circuit breakers.

    - Consultas a DB: Evitar N+1; usar eager loading cuando sea posible.

    - Límites: Las respuestas de APIs deben paginarse.

    - Optimizar el uso de recursos

    - Evitar cargas completas en memoria cuando sea posible
## Seguridad y Dependencias

- **Secretos**: Prohibido hardcodear credenciales. Uso estricto de variables de entorno.

- **Fuente de Verdad**:

    - Configuración mediante variables de entorno

    - Gestionadas vía [.env / pydantic-settings / config module]

    - Nunca hardcodear configuración

- **Validación**: Sanitizar entradas de usuario; usar parámetros preparados en consultas SQL.

- **Dependencias**: No instalar dependencias nuevas sin autorización. Limitarse a [requirements.txt / package.json] a excepción de que se solicite explícitamente una actualización de este. Escanear vulnerabilidades con [Safety / npm audit] periódicamente.
## Calidad y Logs

- **Debug Local**:

    - Scripts de prueba temporales en `tests/` y eliminarse al finalizar el desarrollo.

    - Nunca dejar código temporal en producción

- **Logging**:

    - No usar print()

    - Incluir contexto relevante en logs

    - Evitar loggear información sensible

    - Niveles: [ej: DEBUG para trazabilidad, ERROR para excepciones con stack trace, INFO para flujo normal del proceso, WARNING para situaciones recuperables o alertas de negocio, etc]

- **Testing**:

    - Framework: [pytest / jest] de acuerdo al stack tecnologico y arquitectura del proyecto.

    - Mocks: [Mocks apropiados para el stack tecnologico y arquitectura del proyecto] Los tests deben ser mockeados para evitar hits a DB real.

    - Tipos de tests: [Unitarios, Integración, E2E] de acuerdo al stack tecnologico y arquitectura del proyecto.

    - Validacion: [Validacion apropiada para el stack tecnologico y arquitectura del proyecto] ej: cobertura de codigo (%), validacion de que los tests se ejecutan correctamente, etc.

    - Ejecución: Comando para ejecutar tests de acuerdo al stack tecnologico y arquitectura del proyecto.

## Comunicación

- **Idioma del Agente**: Explicaciones y razonamiento en Español.

- **Código**: Variables y funciones en Inglés. Comentarios en Español.

## Prohibiciones

- No reestructurar carpetas sin autorización

- No modificar código no relacionado

- No eliminar comentarios existentes