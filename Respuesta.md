Gabriel Corobo
2do A informatica


¿Por qué un sistema de delivery usa Queue para los pedidos pero Stack para la bitácora? ¿Qué problema operativo surgiría si invertimos las estructuras?

R:En un sistema de delivery el concepto de Queue se vuelve vital debido a que su funcionamiento, que pertenece a la estructura FIFO, cumple con todo lo que todo restaurante debe respetar: atender por orden de llegada. 
En cambio, para la bitácora (registro), es impensable el uso de la estructura LIFO; en una sistema de bitácoras, el ultimo pedido es el primer registro que se ve. El ultimo es el mas antiguo. Esa es su estructura. Se lee de abajo hacia arriba; esa lectura es tradicional. Por lo tanto, el sistema LIFO respeta ello, y su uso es impensable en un sistema de delivery.
Si se revierte las estructuras, sería un caos. No se puede atender al ultimo que llega (generaría problemas con los pedidos de clientes), ni se debe registrar en un tipo de lectura que pocos se han acostumbrado (de arriba hacia abajo).

¿Por qué es obligatorio verificar Count == 0 antes de Dequeue() o Pop()? ¿Qué ocurre en ejecución si se omite esta validación?

Porque no puedes revertir o extraer un elemento si no hay nada. En consecuencia, esos métodos no harían absolutamente nada.

En el método Deshacer, ¿por qué es necesario analizar el texto con .StartsWith() antes de revertir? ¿Qué error de estado evitaría esto?

Porque es impensable saber qué revertir, evitaría que revirtiera  pedidos que no se pueden revertir. 

¿Qué ventaja tiene entregar mediante Fork + Pull Request en lugar de un archivo comprimido? ¿Cómo facilita la evaluación, la trazabilidad y la retroalimentación?

Un archivo comprimido no tiene la complejidad ni el detalle de un Fork + Pull Request; se puede ver líneas de codigos cambiadas y/o borradas, y el docente sabe quien hizo fork para veracidad de la actividad del estudiante; la retroalimentación se facilita debido a que se pueden comentar en el mismo fork. Se abre un canal de comunicación entre docente y estudiante. Un archivo comprimido está aislado.