---
# These are optional elements. Feel free to remove any of them.
Estado: { accepted }
Fecha: { 2023-06-20 }
Decisores: { Juan Carlos Peñaranda, Kevin Acuña, Jorge Franco, Sergio Silva }
Consultores: { Juan Carlos Peñaranda, Kevin Acuña }
Informados: { Jorge Franco }
---

# Estilo Arquitectura - Event-Diven

## Contexto y planteamiento del problema

El problema abordado con esta arquitectura requiere grupos de componentes funcionales que generan, transforman, visualizan y/o publican información e intercambian datos entre ellos de forma asíncrona para la realización de acciones ante eventos programados.

## Drivers de decisión

Se presentan agrupados para facilitar su correlación entre los componentes de solución identificados.

    - Agrupación 1 Cockpit: 
        RF9 transmisión de información de sensores
        RF8 Captura de información IoT.
        RF10 Almacenamiento de información de sensores

    - Agrupación 3 Solución Web
        RF1 Panel de control.
        RF2 Ordenes asignadas.

    - Agrupación 2 analítica Avanzada: 
        RF4 Optimización de órdenes.
        RF5 Predicción de fallos . 

    - Agrupación 4 Boker de mensajería:
        RF6 Notificaciones.
        RF7 Subscripciones.
        RF11 Aplicación de la configuración de secuencia para componentes IoT   

## Opciones consideradas

- Estilo de la arquitectura EVENT-DRIVEN
- Estilo de la arquitectura PIPES AND FILTERS

## Decisión Final

![bluePrint de la arquitectura](/Resources/BluePrint.png)

- Estilo de la arquitectura EVENT-DRIVEN

Se visualiza un conjunto de interacciones entre grandes 5 grandes componentes de la solución, donde el mecanismo de comunicación es el intercambio de mensajes.

    - Agrupación 1 Cockpit: 
        Interacción directa con dispositivos IoT, para la captura, almacenamiento, transformación y visualización de datos.
    - Agrupación 2 analítica Avanzada: 
        - Preparación de datos, 
        - Validación de modelos de ML, entrenamiento y selección de modelo.
        - Aplicación de modelo. 
        - Generación de datos para toma de decisiones 
    - Agrupación 3 Solución Web:
        - Solución de Software que permita la interacción con usuario final.
        - almacén de datos paramétricas, inventario y configuración de la plataforma.
    - Agrupación 4 Boker de mensajería:
        - Componente para intercambio de información entre las componentes actuales y futuros de la solución.
    - Agrupación 5 Notificación:
        - Componente para generación de notificaciones.

### Consecuencias

* Buenas:
    * Permite desacoplar los componentes del sistema y hacerlos más autónomos.
    * Facilita la entrega de eventos en tiempo real y la respuesta inmediata a los cambios de estado.
    * Mejora el rendimiento y la escalabilidad del sistema al distribuir el procesamiento de eventos entre varios consumidores.

* Neutrales:
    * Requiere una infraestructura de mensajería que administre los eventos, las suscripciones y los canales.
    * Puede usar un modelo de publicar/subscribir o un modelo de streaming de eventos, dependiendo de las necesidades del sistema.
    * Puede tener diferentes tipos de procesamiento de eventos, como simple, complejo o de flujo

* Malas:
    * Dificulta mantener la atomicidad y la consistencia de las transacciones en una serie de eventos.
    * Complica el seguimiento y la depuración del flujo de eventos y las posibles fallas.
    * Puede generar complejidad adicional al diseñar e implementar los componentes del sistema.

## Validación

Los casos de industria donde se recomienda utilizar un estilo arquitectónico event-driven son:

* Internet de las cosas (IoT): se puede usar este estilo para ingerir, procesar y reaccionar a los eventos generados por dispositivos físicos, como sensores, cámaras o wearables

* Aplicaciones en tiempo real: se puede usar este estilo para entregar información actualizada a los usuarios, como notificaciones, alertas o recomendaciones.

* Integración de sistemas heterogéneos: se puede usar este estilo para proporcionar interoperabilidad entre diferentes tecnologías y plataformas, manteniendo la independencia de cada una.

* Big data y analítica: se puede usar este estilo para procesar grandes volúmenes de datos y extraer información valiosa mediante técnicas como el procesamiento de eventos complejos o el streaming de eventos.

* Arquitecturas reactivas: se puede usar este estilo para crear sistemas que respondan a los cambios del entorno, sean resilientes ante las fallas y escalen según la demanda.

* Automatización de procesos de negocio: se puede usar este estilo para modelar y ejecutar flujos de trabajo basados en eventos, que involucren a diferentes actores y sistemas.

* Gestión de inventario: se puede usar este estilo para monitorear y actualizar el estado del inventario en función de los eventos relacionados con la compra, venta o devolución de productos.

##  Pros and Cons de la opción

###  Estilo de la arquitectura PIPES AND FILTERS

- Esta opción por si sola no cumple con todas las necesidades del caso de negocio.

## Mas Información

[Microsoft - Patrón Pipes and Filters](
 #https://learn.microsoft.com/es-es/azure/architecture/patterns/pipes-and-filters)

