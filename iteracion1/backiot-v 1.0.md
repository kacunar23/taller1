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

- Clase IoTBack
Atributos: Familia, ID, Topología, Secuencia. 
Metodos: AsignarFamiliar, AsignarSecuencia. 

## Decisión final

Opción seleccionada: Clase IoTBack porque brinda mayor flexibilidad teniendo en cuenta que se cuenta con una variedad de sensores que tienen diferentes modelos de configuracion. 

### Consecuencias

- Bueno, porque es una nueva clase totalmente flexible.
- Malo, porque todo se debe desarrollar desde 0. 


## Validación

Se hizo una revisión de la capacidad de la clase a construir. 

## Pros and Cons de la opción

### Clase IoTBack

- Bueno, porque es una clase totalmente configurable de acuerdo a los intereses del negocio. 
- Malo, porque al ser una nueva clase toca desarrollarla desde 0. 
- Bueno, porque permite flexibilidad en la comunicacion con componentes externos. 

