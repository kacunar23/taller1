---
# These are optional elements. Feel free to remove any of them.
Estado: { accepted }
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

- Pipe and Filter
  Un hub que reciba los datos de diferentes sensores y los almacene en la base de datos. Se incluye un modulo de extracción, transformación y carga de datos de la base en la que los sensores guardan su datos crudos a una base de información. Además se incluye un componente dataMart en el cual se puedan tener estructuras analíticas diferentes como cubos, y diagramas dimensionales que permitan conseguir insights de los datos de los sensores.

## Decisión final

Se acepta el estilo ya que permite adaptar muchos tipos de sensores y acoplarlos a un sistema en el cual se utilice la información. Es un estilo que permite escalabilidad, es desacoplado y portable. El nuevo modulo de ETL permite hacer adaptaciones, analiticas y reportes sobre los datos de los sensores. Para conseguir la solución completa se decide adquirir la solución IoT ofrecida por Azure.

### Consecuencias

- Bueno, porque permite adaptar tantos tipos de sensores como se desee en el futuro.
- Bueno, porque escala facilmente y al permitir insertar filtros intermedios es adaptable
- Malo, porque es una solución compleja que requiere dinero
- Bueno, porque permite hacer adaptación de los datos según las necesidades y analíticas
- Bueno, porque permite realizar y almacenar analíticas en estructuras de datos diferentes
- Malo, porque no tiene portabilidad
- Bueno, porque reduce tiempos de implementación

## Validación

Se observó las arquitecturas de referencia de azure para adquisición de datos de Azure y de Google cloud.

## Pros and Cons de la opción

### Pipe & filter

- Bueno, porque permite escalar en cantidad de sensores y filtros
- Malo, por su complejidad
- Bueno, porque es inter operable con muchos sistemas y estilos (Event driven ncluido)
- Bueno, porque es desacoplado
- Malo, porque al escoger la opción de Azure no es portable.
