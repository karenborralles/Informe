# Informe Patrones en Concurrencia
Programación Concurrente
Investigación Patrones en la Concurrencia (fase 2)

Integrantes:
Ana Karen Álvarez Borralles - 223196
Yazmin Reyes Ruiz - 221262
Luis Eddie Toledo Espinosa - 223191

Ingeniería en Software “7A”

Profesor:
Alí Santiago López Zunún

01/12/2024

UP CHIAPAS

Introducción
La programación concurrente es un paradigma esencial en el desarrollo de
aplicaciones que requieren realizar múltiples tareas simultáneamente. Los patrones
de diseño en programación concurrente son soluciones estructuradas y probadas
que abordan problemas recurrentes, mejorando la eficiencia, rendimiento y
seguridad de las aplicaciones. Esta investigación explorará los principales patrones
utilizados en la programación concurrente y cómo se aplican en el desarrollo de
sistemas concurrentes.

Investigación: Patrones de Diseño en Programación Concurrente

Patrones en la Programación Concurrente

1. Patrón Productor-Consumidor
Este patrón implica dos tipos de procesos: el productor, que genera datos y
los coloca en un buffer (generalmente una cola), y el consumidor, que toma
estos datos para procesarlos. Es muy utilizado en aplicaciones de
procesamiento por lotes y sistemas de mensajería.
Ventaja: Desacopla la producción y el consumo de datos, facilitando una
gestión eficiente de los recursos.
Ejemplo: Un servidor web donde los clientes envían peticiones y el servidor
las procesa.

2. Patrón Lectores-Escritores
Este patrón gestiona el acceso concurrente a un recurso compartido,
permitiendo que múltiples lectores accedan simultáneamente, pero solo un
escritor puede hacerlo a la vez.
Ventaja: Optimiza el rendimiento en sistemas donde las lecturas son más
frecuentes que las escrituras.
Ejemplo: Un sistema de base de datos donde varios usuarios pueden leer
datos, pero solo uno puede modificarlo.

3. Patrón de Barrera de Sincronización
Utilizado para sincronizar varios hilos o procesos que deben llegar a un punto
específico antes de continuar, asegurando que todos los procesos terminen
una tarea antes de iniciar la siguiente.
Ejemplo: En aplicaciones de procesamiento por lotes, todos los hilos deben
completar una fase antes de pasar a la siguiente.

4. Patrón Objeto Activo
Este patrón desacopla la invocación de un método de su ejecución. Permite
que las solicitudes sean procesadas de manera asíncrona y gestionadas en
un hilo de ejecución independiente.
Ejemplo: En aplicaciones gráficas, donde las interacciones del usuario se
gestionan en hilos separados para evitar bloquear la interfaz.

5. Patrón Monitor Object
Encapsula la sincronización de un recurso compartido y proporciona un
conjunto de operaciones sincronizadas, asegurando que varios hilos accedan
al recurso de manera segura.
Ejemplo: En una base de datos, donde múltiples hilos pueden realizar
consultas sin interferir entre sí.

6. Patrón Suspensión con Guardia
Utilizado para gestionar la suspensión de hilos que intentan acceder a un
recurso cuando este no está disponible, forzando la espera hasta que el
recurso sea accesible.
Ejemplo: En servidores de red, cuando un hilo de cliente espera a que un
recurso esté libre.

7. Patrón de Balanceo (Balancing)
Gestiona la distribución de trabajo entre hilos o procesos para evitar que
algunos queden inactivos mientras otros están sobrecargados. Ideal en
sistemas con múltiples recursos de procesamiento.
Ejemplo: Un sistema que reparte tareas entre diferentes servidores para
equilibrar la carga de trabajo.

8. Patrón Scheduler (Planificador)
Organiza la ejecución de hilos o procesos según las políticas de planificación
de un sistema operativo, optimizando los recursos y gestionando prioridades.
Ejemplo: En un sistema operativo, que gestiona la ejecución de procesos de
acuerdo con sus prioridades.

9. Patrón Thread Storage (Almacenamiento de Hilos)
Proporciona un espacio de almacenamiento independiente por hilo, evitando
que los hilos compartan información y previniendo interferencias entre ellos.
Ejemplo: En servidores web, donde cada sesión de usuario tiene su propio
almacenamiento de datos.

10.Patrón Thread Pool (Grupo de Hilos)
Utiliza un conjunto predefinido de hilos que son reutilizados para ejecutar
tareas, evitando el costo de crear y destruir hilos.
Ejemplo: En aplicaciones de procesamiento por lotes, donde varios
hilos manejan tareas de procesamiento de datos.

11. Patrón Reactor
Permite manejar múltiples eventos o solicitudes en un solo hilo, distribuyendo
los eventos a los manejadores apropiados sin bloquear el hilo principal.
Ejemplo: Un servidor que maneja múltiples conexiones de clientes de
manera no bloqueante usando un solo hilo.

12.Patrón Objeto Inmutable
Los objetos inmutables no pueden ser modificados después de su creación,
evitando problemas de sincronización en sistemas concurrentes.
Ejemplo: Clases como string en Java, que son inmutables,
garantizando que no haya problemas al ser compartidas entre varios hilos.

13.Patrón Proactor
Similar al patrón Reactor, pero en lugar de utilizar un solo hilo, delega la
ejecución de tareas a un manejador de eventos que se ejecuta de manera
asíncrona.
Ejemplo: Un servidor que maneja operaciones de I/O asincrónicas.

Características de los Patrones Concurrentes

Los patrones en programación concurrente permiten gestionar los problemas
derivados de ejecutar tareas simultáneamente. 

Algunas características clave son:

● Desacoplamiento: Los procesos concurrentes trabajan independientemente,
lo que mejora la modularidad y escalabilidad.

● Sincronización: Asegura que los procesos no interfieran entre sí,
manteniendo la coherencia de los datos.

● Optimización de Recursos: Permite el uso simultáneo de recursos,
aumentando la eficiencia.


Aplicación de Patrones Concurrentes

Un ejemplo práctico de la aplicación de patrones concurrentes es en el desarrollo de
aplicaciones de procesamiento paralelo, como sistemas de procesamiento de video
o aplicaciones de cálculo distribuido. Estos sistemas emplean patrones como
productor-consumidor y barreras de sincronización para manejar grandes
volúmenes de datos simultáneamente, mejorando el rendimiento y la eficiencia.


Bibliografía
● Shaw, M. (1999). Concurrent Software Development. McGraw-Hill.

● Hennessy, J. L., & Patterson, D. A. (2019). Computer Architecture: A
Quantitative Approach (6ª ed.). Elsevier.

● Sutter, H., & Larus, J. (2005). Software and the Concurrency Revolution. ACM
Press.

● Ponce, H. (2012). Patrones de diseño en programación concurrente.

Ediciones UAM.
● Hidalgo, J. L. (2013). Introducción a la programación concurrente y paralela
con Java. Editorial Alfaomega.
