---
# These are optional elements. Feel free to remove any of them.
Estado: { deprecated }
Fecha: { 2023-06-18 }
Decisores: { Juan Carlos Peñaranda, Kevin Acuña, Jorge Franco, Sergio Silva }
Consultores: { Juan Carlos Peñaranda, Kevin Acuña }
Informados: { Jesús Barrios }
---

# Fabrica 4.0: Selección de base de datos

## Contexto y planteamiento del problema

Se pretende diseñar el software de una factoría inteligente compuesta por tres líneas de producción y más de 10 sensores IoT que proporcionan datos sobre el estado de los dispositivos físicos de una factoría inteligente 4.0. Los datos de los sensores se almacenan en una base de datos SQL. Además, se desea tener el inventario de la fábrica almacenado.

## Drivers de decisión

- RF3 - Almacenar inventario
- RF10 - Almacenamiento de informacion de sensores

## Opciones consideradas

- Cassandra

## Decision final

Opción seleccionada: Cassandre

### Consecuencias

- Bueno, porque permite almacenar y consultar con un mejor performance que SQL
- Neutral, porque permite datos desestructurados
- Malo, porque no cuida la integridad de los datos
- Malo, porque no cumple el deseo de que sea una base de datos SQL

## Validación

Benchmarks

## Pros and Cons de la opción

### Cassandra

- Bueno, porque es un motor de base de datos de codigo abierto lo que aumenta la seguridad
- Malo, porque al ser codigo abierto no hay soporte más que el que presta la comunidad
- Neutral, porque permite estructuras flexibles
- Bueno, porque tiene mejor performance de lectura y escritura que SQL
- Malo, porque no cuida la integridad de la información
