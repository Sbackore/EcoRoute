# Taller de Arquitectura: Ecoroute

## 1. ***Cohesión de datos***

## *¿Por que no ponemos el nombre del condutor dentro de la tabla vehiculos?*

 ### El aspecto mas importante es de la redundancia que se generaría en ese contexto, si el conductor llegase a cmabiar de algo (como por ejemplo numero de telefono) se tendria que rastrear cada registro en el que ese conductor aparce y cambiar el dato manualmente, lo que lo hace un prátcia muy anticuada.

## *¿Que pasasaría con la cohesión de la tabla si mezclamos datos del motor con datos del humano?*

### Sencillamente la cohesión desaparecería casi por completo. Recordemos que la cohesión nos habla de que un aspecto debe enfocarse en un solo concepto, mezclar técnicas de motor y de humanos rompería el principio de responsabilidad única.

## 2. ***Reflexión del ejercicio***

## *Si en un futuro el módulo de 'Entregas' crece tanto que se convierte en una empresa aparte. ¿Que tan dificil sería separar esas tablas de otra base de deatos?.*

### Gracias a la modulariad del diseño, se puede decir que sería un cambio bastante manejable, mas especificamente porque la tabla de "Entregas" tiene un bajo nivel de acoplamiento. El proceso de separación a una base de datos externa solo conllevaría eliminar la tabla y las llaves foráneas presenten como relacion en otras tablas y mas bien, realizar la comunicacion a travez de una API por ejemplo.