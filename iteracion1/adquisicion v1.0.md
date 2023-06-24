---
# These are optional elements. Feel free to remove any of them.
Estado: { Rejected }
Fecha: { 2023-06-20 }
Decisores: { Juan Carlos Peñaranda, Kevin Acuña, Jorge Franco, Sergio Silva }
Consultores: { Juan Carlos Peñaranda, Kevin Acuña }
Informados: { Jesús Barrios }
---

# Fabrica 4.0: Adquisición de datos

## Contexto y planteamiento del problema

Para poder conocer el estado de la fabrica con tres líneas de producción es necesario tener la capacidad de adquirir los datos de más de 10 sensores IoT. Se debe poder capturar información de diferentes sensores y hacer el tratamiento de su información de tal forma que se pueda observar la información de los sensores, con sus analiticas y que esto refleje la realidad de la fabrica.

## Drivers de decisión

- RF8 - Captura de información IoT
- RF9 - Transmision de información de sensores

## Opciones consideradas

- Event driven

## Decisión final

No se acepta event driven ya que a pesar que es una buena forma de trasmitir datos requiere que los emisores tengan una forma de conectarse a un broker lo cual no es cierto en muchas circunstancias.

### Consecuencias

- Bueno, porque permite conocer que event driven funciona parcialmente para la adquisición de los datos de sensores
- Malo, porque requiere un estilo más complejo que permita adaptar muchos tipos de sensores IoT diferentes

## Validación

Se observó las arquitecturas de referencia de azure para adquisición de datos de Azure y de Google cloud.

## Pros and Cons de la opción

### Event Driven

- Bueno, porque permite escalar en fuentes y en subscirptores
- Malo, porque no permite adaptar multiples tipos de sensores cada uno con su protocolo
- Bueno, porque es inter operable con muchos sistemas
- Bueno, porque es desacoplado
- Neutral, porque permite portabilidad
