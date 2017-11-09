Resumen Microservicios Uber

Matt Ranney nos dice que en la actualidad el crecimiento en general consecuencia de la globalización está generan un proceso de scaling a una velocidad sin precedentes, donde se pueden observar grandes cambios en el transcurso de tan solo 1 año.
Utilizando el ejemplo de Uber, hace 1 año y medio había 200 ingenieros empleados por la compañía. Actualmente cuentan con 2000 lo que pone en evidencia el crecimiento exponencial. Este gran crecimiento ha llevado a Uber a aprender muchas lecciones “de vida” no necesariamente de una manera grata. Muchas veces se tuvo una falsa idea que había un control y se tuvo que aprender de la manera difícil. 
Probablemente existen a cierta escala una cantidad de compensaciones por utilizar microservicios. Cada vez que se planea cambiar algún funcionamiento existe una posibilidad de “romperlo”. ¿Tiene sentido nunca cambiar un software para que nunca se rompa? Los microservicios permiten a los equipos que se encuentran en constante crecimiento moverse y desarrollar ideas de manera independiente a los demás equipos. “Utilizar y correr en producción el código que uno mismo creo”. 
Normalmente llega un momento en que se piensa que se debería usar la “mejor” solución como estándar, pero ¿Qué significa mejor? ¿Mejor para quien o para qué? En muchas ocasiones, Uber intento utilizar lo mejor para todos pero esto significa utiliza un sistema distribuido el cual Matt nos explica que es mucho más difícil de administrar que un solo software. De pronto se tienen que manejar una gran cantidad de problemas, usuarios que no tienen las mismas opciones que en el software anterior, requerimientos específicos por región.
Los microservicios también tienen costos como el costo de estar siempre construyendo alrededor de los problemas y no solucionando los problemas anteriores. Ejemplos de módulos de microservicios de la aplicación Uber sobre el tema: 
•	Módulo de Despacho: escrito en Node.JS migrando a Go
•	Módulo Core: escrito en Python migrando a Go
•	Módulo Mapas: Python y Java
•	Módulo Data: Python y Java
•	Módulo de métricas: Go

Los microservicios permiten a los equipos escribir en el lenguaje que deseen y comunicarse entre sí sin problemas. Sin embargo, operar de esta manera trae consigo algunas desventajas: es complicado compartir código entre equipos, es complicado reubicar miembros de un equipo especifico en uno distinto, de alguna forma fragmenta la cultura empresarial ya que se aleja de manejar un estándar como empresa.
La cantidad de equipos que maneja Uber vuelve todo un reto gestionar el versionamiento de código, donde la creación de un repositorio completo sería tan grande que volvería imposible realizar revisiones correctas del código editado. Matt nos cuenta que actualmente Uber cuenta con alrededor de 8000 repositorios entre todos los equipos de la compañía. 
Otro punto consecuencia del uso de micro servicios se da a la hora de realizar los pases a producción. Manejar un número elevado de equipos significa que cada uno de estos equipos tienen un pace establecido de avance lo que podría conllevar a atrasos para los equipos que avanzan más rápido. Utilizar micro servicios genera la necesidad de llevar una buena gestión de coordinación entre los equipos.
Luego, Matt entra al campo de rendimiento o performance y nos dice “El rendimiento no es importante, hasta que lo es”. En pocas palabras nos quiere decir que, si dejamos de lado las métricas de evaluación para los equipos, llegara el momento en que empezaran a saltar problemas y nos volveremos reactivos antes que proactivos. Lógicamente es complicado crear un dashboard que logre mostrar de manera estandarizada el rendimiento de todos los equipos. Sin embargo, este es un punto que debe tomarse en cuenta siempre y no dejar de lado.
Al utilizar micro servicios es muy importante adjuntar una descripción que sirva como contexto a los requests. Esto, con la finalidad de poder realizar un trace correcto al detectarse un problema en un request. 
Existen dos buenas practicas que se deben forzar a aplicarse ya que por experiencia propia de Matt en algún momento dado fueron obviadas y esto causó serios problemas a la empresa:
•	Logging
•	Failure y load Testing

Finalmente, Matt nos advierte sobre las aplicaciones Legacy. En años recientes la velocidad con la que estas aplicaciones cambian ha aumentado bastante. Hay que destacar que es muy importante que las empresas realicen estos cambios por temas de seguridad informática o de cumplimiento con normas o nuevas funciones operacionales que la empresa requiere y no son posibles con la tecnología antigua. Forzar un cambio solo por el hecho de cambiar no es bueno ni recomendable.

