---
# These are optional elements. Feel free to remove any of them.
status: { accepted }
date: { 2023-06-18 }
deciders: { Juan Carlos Peñaranda, Kevin Acuña, Jorge Franco, Sergio Silva }
consulted: { Juan Carlos Peñaranda, Kevin Acuña }
informed: { Jesús Barrios }
---

# Fabrica 4.0: Selección de base de datos

## Contexto y planteamiento del problema

Se pretende diseñar el software de una factoría inteligente compuesta por tres líneas de producción y más de 10 sensores IoT que proporcionan datos sobre el estado de los dispositivos físicos de una factoría inteligente 4.0. Los datos de los sensores se almacenan en una base de datos SQL. Además, se desea tener el inventario de la fábrica almacenado.

## Decision Drivers

- RF3 - Almacenar inventario
- RF10 - Almacenamiento de informacion de sensores

## Considered Options

- MySQL

## Decision final

Opción seleccionada: "Kassandra", porque ...
{justification. e.g., only option, which meets k.o. criterion decision driver | which resolves force {force} | … | comes out best (see below)}.

### Consequences

- Good, because {positive consequence, e.g., improvement of one or more desired qualities, …}
- Bad, because {negative consequence, e.g., compromising one or more desired qualities, …}

## Validation

{describe how the implementation of/compliance with the ADR is validated. E.g., by a review or an ArchUnit test}

## Pros and Cons of the Options

### MySQL

- Good, because {argument a}
- Good, because {argument b}
- Neutral, because {argument c}
- Bad, because {argument d}
