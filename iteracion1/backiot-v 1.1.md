---
# These are optional elements. Feel free to remove any of them.
Estado: { deprecated }
Fecha: { 2023-06-18 }
Decisores: { Juan Carlos Peñaranda, Kevin Acuña, Jorge Franco, Sergio Silva }
Consultores: { Juan Carlos Peñaranda, Kevin Acuña }
Informados: { Jesús Barrios }
---

# Back End IoT

## Contexto y planteamiento del problema

Se pretende diseñar el software de una factoría inteligente compuesta por tres líneas de producción y más de 10 sensores IoT que proporcionan datos sobre el estado de los dispositivos físicos de una factoría inteligente 4.0. Los datos de los sensores se almacenan en una base de datos SQL. Los sensores IoT se clasifican en dos familias (sensores A y B), cada una de las cuales comparte cierta funconalidad, pero dispone de ciertas características diferentes entre una familia y otra. La familia se sensores A, está compuesta por tres sensores en los que el primero envía información al segundo y éste al tercero.

## Drivers de decisión

- RF11 - Configuracion de secuencia

## Opciones consideradas

- Azure IoT Central

## Decisión final

Opción seleccionada: Clase IoTBack porque brinda mayor flexibilidad teniendo en cuenta que se cuenta con una variedad de sensores que tienen diferentes modelos de configuracion. 

### Consecuencias

- Bueno, porque es una nueva clase totalmente flexible.
- Malo, porque todo se debe desarrollar desde 0. 
- Malo, porque no se podrian utilizar las herramientas de calidad que ya trae de por si IoT Central. 

## Validación

Se hizo una revisión con benchmarks

## Pros and Cons de la opción

### Azure IoT Central

- Bueno, es un componente con alto nivel de seguridad. 
- Malo, porque solo se puede utilizar plantillas de dispositivos ya configuradas. 
- Bueno, porque permite una capacidad para analisis y visualizacion de datos rapida. 
- Malo, porque no permite flexibilidad en la comunicacion con componentes externos de MS. 

