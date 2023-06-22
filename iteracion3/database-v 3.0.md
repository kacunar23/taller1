---
# These are optional elements. Feel free to remove any of them.
Estado: { accepted }
Fecha: { 2023-06-18 }
Decisores: { Juan Carlos Peñaranda, Kevin Acuña, Jorge Franco, Sergio Silva }
Consultores: { Juan Carlos Peñaranda, Kevin Acuña }
Informados: { Jesús Barrios }
---

# Fabrica 4.0: Selección de base de datos

## Contexto y planteamiento del problema

Se pretende diseñar el software de una factoría inteligente compuesta por tres líneas de producción y más de 10 sensores IoT que proporcionan datos sobre el estado de los dispositivos físicos de una factoría inteligente 4.0. Los datos de los sensores se almacenan en una base de datos SQL. Además, se desea tener el inventario de la fábrica almacenado.

## Decision Drivers

- RF3 - Almacenar inventario
- RF10 - Almacenamiento de informacion de sensores

## Opciones consideradas

- Cassandra
- MySQL

## Decision final

Opción seleccionada:(MySQL + Cassandra) La opción seleccionada es una base de datos cassandra para la adquisición de datos y las consultas analiticas de IoT, con un respaldo estructurado en MySQL que también se encargará de llevar los inventarios.

### Consecuencias

- Bueno, porque permite almacenar y consultar con un buen performance
- Bueno, porque permite datos desestructurados y estructurados
- Neutral (Petoencialmente malo), porque esta atado a un servidor
- Bueno, porque cumple el deseo de que sea una base de datos SQL

## Validación

Benchmarks

## Pros and Cons de la opción

### Cassandra

- Bueno, porque es un motor de base de datos de codigo abierto lo que aumenta la seguridad
- Malo, porque al ser codigo abierto no hay soporte más que el que presta la comunidad
- Neutral, porque permite estructuras flexibles
- Bueno, porque tiene mejor performance de lectura y escritura que SQL
- Malo, porque no cuida la integridad de la información

### MySQL

- Bueno, porque es un motor de base de datos abierto lo que aumenta la seguridad
- Malo, porque al ser codigo abierto no hay soporte más que el que presta la comunidad
- Neutral, porque permite estructuras bidimensionales
- Bueno, porque permite integridad de la información
- malo, porque no permite flexibilidad de la información
- Neutral, porque se puede implementar en el servidor
