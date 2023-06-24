---
# These are optional elements. Feel free to remove any of them.
Estado: { accepted }
Fecha: { 2023-06-20 }
Decisores: { Juan Carlos Peñaranda, Kevin Acuña, Jorge Franco, Sergio Silva }
Consultores: { Juan Carlos Peñaranda, Kevin Acuña }
Informados: { Jorge Franco }
---

# Estilo Arquitectura PIPES AND FILTERS - Componente IoT

## Contexto y planteamiento del problema

Se pretende diseñar el software de una factoría inteligente compuesta por tres líneas de producción y más de 10 sensores IoT que proporcionan datos sobre el estado de los dispositivos físicos de una factoría inteligente 4.0. Los datos de los sensores se almacenan en una base de datos SQL.

## Drivers de decisión

Se presentan agrupados para facilitar su correlación entre los componentes de solución identificados.

    - Agrupación 1 Cockpit: 
        RF9 transmisión de información de sensores
        RF8 Captura de información IoT.
        RF10 Almacenamiento de información de sensores

## Opciones consideradas

- Estilo de la arquitectura PIPES AND FILTERS

## Decisión Final

![bluePrint de la arquitectura](/Resources/BluePrint%20Pipe%20and%20Filters.png)

- Estilo de la arquitectura PIPES AND FILTERS

Se visualiza un conjunto de interacciones entre grandes 5 grandes componentes de la solución, donde el mecanismo de comunicación es el intercambio de mensajes.

    - Agrupación 1 Cockpit, descripción de aplicación:
        - Ingesta de datos realizada por un componente especializado que permite captura de sensores IoT en tiempo real sin perdida de información.
        - Almacenamiento en base de datos relacional para garantizar durabilidad.
        - componente ETL
            - Transformación
            - Limpieza
            - completado
            - calidad
        - Almacenamiento en múltiples bases de datos relacionales con información dimensional por dominio de negocio.
        - Componentes especializados para visualización e interacción con los datos.
           

### Consecuencias

* Buenas:
    * Permite mejorar el rendimiento, la escalabilidad y la reutilización al permitir que los elementos de tarea que realizan el procesamiento se implementen y escalen por separado.
    * Facilita la flexibilidad y la adaptabilidad al permitir reordenar, eliminar, sustituir o agregar elementos de procesamiento según cambien los requisitos.
    * Favorece la modularidad y el bajo acoplamiento al encapsular cada elemento de procesamiento en un componente de filtro que solo recibe y produce datos.

* Neutrales:
    * Requiere una infraestructura de tuberías que transfiera y sincronice los datos entre los filtros.
    * Puede usar filtros pasivos o activos, dependiendo de si esperan a recibir datos o los solicitan activamente.
    * Puede usar diferentes tipos de tuberías, como archivos, memoria compartida o sockets.

* Malas:
    * Dificulta el manejo de errores y excepciones al no tener una visión global del flujo de procesamiento.
    * Complica la depuración y el seguimiento del estado de los datos al pasar por múltiples filtros.
    * Puede generar sobrecarga adicional al tener que convertir los datos a un formato estándar para cada filtro.

## Validación

Los casos de industria donde se recomienda utilizar un estilo arquitectónico Pipe and Filter son:

* Procesamiento de imágenes: se puede usar este estilo para aplicar diferentes operaciones sobre las imágenes, como filtrado, rotación, recorte o compresión.

* Compiladores: se puede usar este estilo para implementar las fases de análisis léxico, sintáctico, semántico y generación de código de un compilador.

* Análisis de texto: se puede usar este estilo para realizar tareas como tokenización, etiquetado, extracción de entidades o resumen de texto.

* Procesamiento de audio: se puede usar este estilo para modificar o mejorar el sonido mediante filtros como ecualización, reverberación o reducción de ruido.

* Cifrado y descifrado: se puede usar este estilo para aplicar algoritmos de seguridad sobre los datos, como encriptación, autenticación o firma digital.

* Transformación de datos: se puede usar este estilo para convertir los datos de un formato a otro, como XML a JSON o CSV a SQL.

* Minería de datos: se puede usar este estilo para extraer información relevante o patrones ocultos de grandes conjuntos de datos.

* Procesamiento por lotes: se puede usar este estilo para ejecutar tareas que no requieren interacción con el usuario y que pueden procesar grandes cantidades de datos en paralelo.

* Sistemas de recomendación: se puede usar este estilo para generar sugerencias personalizadas para los usuarios basadas en sus preferencias o comportamientos.

*Sistemas de streaming: se puede usar este estilo para procesar flujos continuos de datos en tiempo real, como eventos, sensores o redes sociales

##  Pros and Cons de la opción

## Mas Información

[Microsoft - Patrón Pipes and Filters](
 #https://learn.microsoft.com/es-es/azure/architecture/patterns/pipes-and-filters)


