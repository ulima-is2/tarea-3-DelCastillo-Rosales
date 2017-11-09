Resumen Microservicios Uber

Matt Ranney nos dice que en la actualidad el crecimiento en general consecuencia de la globalizaci�n est� generan un proceso de scaling a una velocidad sin precedentes, donde se pueden observar grandes cambios en el transcurso de tan solo 1 a�o.
Utilizando el ejemplo de Uber, hace 1 a�o y medio hab�a 200 ingenieros empleados por la compa��a. Actualmente cuentan con 2000 lo que pone en evidencia el crecimiento exponencial. Este gran crecimiento ha llevado a Uber a aprender muchas lecciones �de vida� no necesariamente de una manera grata. Muchas veces se tuvo una falsa idea que hab�a un control y se tuvo que aprender de la manera dif�cil. 
Probablemente existen a cierta escala una cantidad de compensaciones por utilizar microservicios. Cada vez que se planea cambiar alg�n funcionamiento existe una posibilidad de �romperlo�. �Tiene sentido nunca cambiar un software para que nunca se rompa? Los microservicios permiten a los equipos que se encuentran en constante crecimiento moverse y desarrollar ideas de manera independiente a los dem�s equipos. �Utilizar y correr en producci�n el c�digo que uno mismo creo�. 
Normalmente llega un momento en que se piensa que se deber�a usar la �mejor� soluci�n como est�ndar, pero �Qu� significa mejor? �Mejor para quien o para qu�? En muchas ocasiones, Uber intento utilizar lo mejor para todos pero esto significa utiliza un sistema distribuido el cual Matt nos explica que es mucho m�s dif�cil de administrar que un solo software. De pronto se tienen que manejar una gran cantidad de problemas, usuarios que no tienen las mismas opciones que en el software anterior, requerimientos espec�ficos por regi�n.
Los microservicios tambi�n tienen costos como el costo de estar siempre construyendo alrededor de los problemas y no solucionando los problemas anteriores. Ejemplos de m�dulos de microservicios de la aplicaci�n Uber sobre el tema: 
�	M�dulo de Despacho: escrito en Node.JS migrando a Go
�	M�dulo Core: escrito en Python migrando a Go
�	M�dulo Mapas: Python y Java
�	M�dulo Data: Python y Java
�	M�dulo de m�tricas: Go

Los microservicios permiten a los equipos escribir en el lenguaje que deseen y comunicarse entre s� sin problemas. Sin embargo, operar de esta manera trae consigo algunas desventajas: es complicado compartir c�digo entre equipos, es complicado reubicar miembros de un equipo especifico en uno distinto, de alguna forma fragmenta la cultura empresarial ya que se aleja de manejar un est�ndar como empresa.
La cantidad de equipos que maneja Uber vuelve todo un reto gestionar el versionamiento de c�digo, donde la creaci�n de un repositorio completo ser�a tan grande que volver�a imposible realizar revisiones correctas del c�digo editado. Matt nos cuenta que actualmente Uber cuenta con alrededor de 8000 repositorios entre todos los equipos de la compa��a. 
Otro punto consecuencia del uso de micro servicios se da a la hora de realizar los pases a producci�n. Manejar un n�mero elevado de equipos significa que cada uno de estos equipos tienen un pace establecido de avance lo que podr�a conllevar a atrasos para los equipos que avanzan m�s r�pido. Utilizar micro servicios genera la necesidad de llevar una buena gesti�n de coordinaci�n entre los equipos.
Luego, Matt entra al campo de rendimiento o performance y nos dice �El rendimiento no es importante, hasta que lo es�. En pocas palabras nos quiere decir que, si dejamos de lado las m�tricas de evaluaci�n para los equipos, llegara el momento en que empezaran a saltar problemas y nos volveremos reactivos antes que proactivos. L�gicamente es complicado crear un dashboard que logre mostrar de manera estandarizada el rendimiento de todos los equipos. Sin embargo, este es un punto que debe tomarse en cuenta siempre y no dejar de lado.
Al utilizar micro servicios es muy importante adjuntar una descripci�n que sirva como contexto a los requests. Esto, con la finalidad de poder realizar un trace correcto al detectarse un problema en un request. 
Existen dos buenas practicas que se deben forzar a aplicarse ya que por experiencia propia de Matt en alg�n momento dado fueron obviadas y esto caus� serios problemas a la empresa:
�	Logging
�	Failure y load Testing

Finalmente, Matt nos advierte sobre las aplicaciones Legacy. En a�os recientes la velocidad con la que estas aplicaciones cambian ha aumentado bastante. Hay que destacar que es muy importante que las empresas realicen estos cambios por temas de seguridad inform�tica o de cumplimiento con normas o nuevas funciones operacionales que la empresa requiere y no son posibles con la tecnolog�a antigua. Forzar un cambio solo por el hecho de cambiar no es bueno ni recomendable.

