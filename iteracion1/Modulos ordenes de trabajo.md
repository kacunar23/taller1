---
# These are optional elements. Feel free to remove any of them.
Estado: { Deprecated }
Fecha: { 2023-06-20 }
Decisores: { Juan Carlos Peñaranda, Kevin Acuña, Jorge Franco, Sergio Silva }
Consultores: { Juan Carlos Peñaranda, Kevin Acuña }
Informados: { Jorge Franco }
---

# Estilo Arquitectura Capas

## Contexto y planteamiento del problema

Luego que se han adquirido y procesado los datos de los sensores, el sistema debe ser capaz de mostrarle a los operarios en un modulo de administración de ordenes cuales son las tareas que tienen asignadas y en caso de una alerta con algún sensor, en la interfaz se debe visualizar las notificaciones de los eventos. 
Se debe seleccionar las tecnologías y estinos para la construcción o adquisición de tecnologías para obtener un modulo de administración de ordenes.

## Drivers de decisión

Se presentan agrupados para facilitar su correlación entre los componentes de solución identificados.

    - Agrupación 3 Solución Web
        RF1 Panel de control.
        RF2 Ordenes asignadas.
        RF11 configuración de secuencia
        RF12 Interfaz configurable

## Opciones consideradas

- integración con SAP para ordenes de trabajo

## Decisión Final

Opción considerada: Creación de el módulo de administración utilizando una arquitectura de capas.

### Consecuencias

Bueno, SAP incorpora las mejores prácticas de la industria y los procesos estándar en sus módulos, incluido el módulo de órdenes de trabajo.
Malo, La implementación y el mantenimiento de SAP pueden ser una inversión significativa, ya que implica tarifas de licencia, infraestructura de hardware y recursos calificados para la implementación y el soporte continuo.

## Validación

Se hizo una revisión con benchmarks

##  Pros and Cons de la opción

Bueno, SAP ofrece una amplia gama de características y funcionalidades diseñadas específicamente para la gestión de órdenes de trabajo.
Bueno, SAP está diseñado para manejar operaciones a gran escala y puede adaptarse al crecimiento de las órdenes de trabajo.
Malo, Los sistemas SAP pueden ser complejos y tener una curva de aprendizaje pronunciada. Capacitar a los usuarios para que utilicen de manera efectiva el módulo de órdenes de trabajo puede requerir recursos, tiempo y esfuerzo dedicados.
Malo, Implementar SAP significa confiar en un proveedor externo para actualizaciones de software, corrección de errores y soporte continuo.

