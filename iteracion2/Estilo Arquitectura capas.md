---
# These are optional elements. Feel free to remove any of them.
Estado: { accepted }
Fecha: { 2023-06-20 }
Decisores: { Juan Carlos Peñaranda, Kevin Acuña, Jorge Franco, Sergio Silva }
Consultores: { Juan Carlos Peñaranda, Kevin Acuña }
Informados: { Jorge Franco }
---

# Estilo Arquitectura Capas

## Contexto y planteamiento del problema

Luego que se han adquirido y procesado los datos de los sensores, el sistema debe ser capaz de mostrarle a los operarios en un modulo de administración de ordenes cuales son las tareas que tienen asignadas y en caso de una alerta con algún sensor, en la interfaz se debe visualizar las notificaciones de los eventos. 
Se debe seleccionar las tecnologías y estinos para la construcción o adquisición de tecnologías para obtener un modulo de administración de ordenes.

La solución debe contar con una solución de software que permita al usuario interactuar con el sistema, ofreciendo una interfaz grafica para:

    - Ordenes
    - Personal : (roles) : Operaciones, Coordinadores, Jefes de producción.. etc
    - Maquinas
    - Inventario
    - Sensores
    - Correlación entre sensores
    - Suscripciones a evento


## Drivers de decisión

Se presentan agrupados para facilitar su correlación entre los componentes de solución identificados.

    - Agrupación 3 Solución Web
        RF1 Panel de control.
        RF2 Ordenes asignadas.
        RF11 configuración de secuencia
        RF12 Interfaz configurable

## Opciones consideradas

Estilo de la arquitectura para el módulo de administración de ordenes de trabajo; CAPAS
-Pasar de un estilo de 3 capas a tener 4 capas.

## Decisión Final

![bluePrint de la arquitectura](/Resources/Capas.png)

Opción seleccionada: Pasar de un estilo de 3 capas a tener 4 capas para el módulo de ordenes de trabajo.

    La solución de software con la que interactuará el usuario tendrá una arquitectura de 4 capas:

    * Front: Capa dedicada a realizar representaciones gráficas en navegadores web para interacción directa con el usuario.

    * Backend: Capa que contendrá toda la lógica de negocio requerida para el cumplir el objetivo de la solución.

    * Integraciones: Capa que se servirá de disponibilizar la lógica de negocio e interactuar con el mediador de comunicación con el resto de la solución "Broker de Mensajeria"

    * Base de datos: Repositorio de información
        
            
### Consecuencias

* Buenas:
    * Permite mejorar la modularidad, el mantenimiento y la reutilización al encapsular la lógica y los datos de cada capa.
    * Facilita la adaptabilidad y la escalabilidad al permitir cambiar o reemplazar las implementaciones de cada capa según las necesidades.
    * Favorece la seguridad y el rendimiento al distribuir las capas en diferentes niveles físicos y controlar el acceso a cada una.
    * Al separar la capa de integración del backend, crea una clara separación de preocupaciones entre los diferentes componentes del sistema. 
    * El backend puede enfocarse en el procesamiento de datos y la funcionalidad principal, mientras que la capa de integración puede manejar la comunicación con sistemas externos.

* Neutrales:
    * Requiere una infraestructura de comunicación que permita el intercambio de datos entre las capas.
    * Puede usar diferentes tipos de capas, como presentación, negocio, persistencia o integraciones.
    * Puede usar diferentes tipos de arquitecturas, como monolítica, cliente-servidor o n-niveles.

* Malas:
    * Dificulta el diseño y la implementación al tener que definir las interfaces, las responsabilidades y las dependencias de cada capa.
    * Complica la depuración y el seguimiento al tener que analizar múltiples capas y componentes.
    * Puede generar sobrecarga adicional al tener que transformar o serializar los datos para cada capa.

## Validación

Los casos de industria donde se recomienda utilizar un estilo arquitectónico "Capas" son:

* Aplicaciones web: se puede usar este estilo para separar la interfaz de usuario, la lógica de negocio y el acceso a datos en una aplicación web.
* Aplicaciones móviles: se puede usar este estilo para organizar la aplicación móvil en capas como presentación, servicios, dominio y datos.
* Aplicaciones empresariales: se puede usar este estilo para implementar sistemas complejos que involucran múltiples procesos de negocio, reglas y validaciones.
* Aplicaciones de escritorio: se puede usar este estilo para crear interfaces de usuario ricas y funcionales que se comuniquen con una capa de negocio y una capa de datos.
* Aplicaciones cliente-servidor: se puede usar este estilo para distribuir la aplicación en dos capas: una capa cliente que se ejecuta en el dispositivo del usuario y una capa servidor que se ejecuta en un equipo remoto.
* Aplicaciones n-niveles: se puede usar este estilo para dividir la aplicación en más de dos capas, como una capa de presentación, una capa de aplicación, una capa de servicios y una capa de datos.

##  Pros and Cons de la opción

    * Bueno, dividir la capa de integración permite una clara separación de preocupaciones entre el backend y los componentes de integración.
    * Bueno, el desacoplamiento de la capa de integración del backend permite la escalabilidad independiente de cada capa.
    * Malo, ividir la capa de integración agrega complejidad a la arquitectura general. Introduce componentes adicionales, interfaces y posibles puntos de falla.
    * Malo, la implementación de una capa de integración separada requiere un esfuerzo y experiencia de desarrollo adicionales.


## Mas Información

[Microsoft - Estilo de arquitectura de n niveles](
 #https://learn.microsoft.com/es-es/azure/architecture/guide/architecture-styles/n-tier)