Pregunta 1 � Martin Fowler y su exposici�n sobre Microservicios

Martin Fowler comienza su presentaci�n present�ndose, a qu� se dedic� los �ltimos a�os y como desarroll� microsevicios sin que se a�n sean llamados como tales.

A continuaci�n, habla sobre la agenda que seguir� su charla y comienza hablando sobre la arquitectura de microservicios. Aqu� hace referencia al libro de 	Christopher Alexander �The Timeless Way of Building�, el cual es un libro sobre arquitectura de construcci�n de edificaciones, en el que se basaron los patrones de dise�o de software.

Al entrar al detalle de la arquitectura, Fowler divide este tema en dos: estandarizaci�n y metas.

El expositor narra que desde el comienzo de los tiempos del desarrollo de software se ha trabajado con arquitecturas monol�ticas. Sin embargo, en los �ltimos tiempos se est� haciendo una transici�n de las arquitecturas monol�ticas a las arquitecturas por microservicios. Esto se debe a que esta arquitectura permite separar las funciones de negocio en contextos delimitados, espec�ficamente un contexto delimitado para un servicio.

Los microservicios son de cierta forma �amigables� para realizar migraciones graduales ya que, como se explic� anteriormente, se separan contextos delimitados diferentes y eso hace que toda la arquitectura no sea dependiente entre s�.

El expositor afirma que los microservicios brinda a sus usuarios escalabilidad. Estos permiten descomponer las funciones por las cosas que hacen cada una y luego estas pueden escalar, independientemente de las dem�s.

Luego, Martin habla sobre los principios que cumplen los microservicios. Estos son: Encapsulaci�n, automatizaci�n, dominio c�ntrico, descentralizado, independiente, a prueba de fallos y observable.

Tambi�n habla de hacer el c�digo de cierta forma �mantenible� y de priorizar eso.

El siguiente tema importante a tratar en la exposici�n es el de patrones. Se presentan los siguientes patrones:

- CQRS (Command Query Responsibility Segregation): Indica que no se deben realizar las acciones de lectura y escritura en las mismas operaciones en el mismo momento.
- Event Sourcing: Se basa en la secuencia de eventos
- API Gateway / Proxy: Es una manera de extraer algunas de las complicaciones de seguridad que se puedan presentar.	
- Orchestrated API: Es una manera de micro manejo de hacer las cosas.

Luego se realiza la siguiente pregunta. �Qu� define el �xito de los microservicios? Fowler dice que lo siguiente explica qu� define su �xito:
-	Es hol�stico, mientras m�s se enfoque de esta manera, m�s sentido tendr�.
-	Hace lo que est� destinado a hacer y nada m�s.
-	Cumple con las necesidades de los usuarios, si no lo usan es porque hay alg�n problema.
-	Es seguro.
-	Es escalable.
-	Es robusto, �sea puede aceptar cambios y errores.
-	F�cil de dar soporte

Seguidamente se hablan de los pros y contras de los microservicios, los que ser�n detallados a continuaci�n.
Pros:
-	La performance es un beneficio a largo plazo. Se puede escalar f�cilmente.
-	Cumplir con las expectativas de los usuarios de alto nivel en base a la arquitectura.
-	Ubiquidad del lenguaje alrededor de un problema, f�cil de probar y barato de escalar.
-	Si se tiene un cuello de botella se puede separar ese parte de la aplicaci�n, escalarlo si modificar otras partes.
Contras:
-	Es m�s complejo en los sistemas distribuidos, por las pruebas unitarias dadas la dependencia, por lo que se necesita una buena interfaz de trabajo.
-	Las transacciones distribuidas. Soluci�n: event outsourcing.
-	Administraci�n del sistema (tooling).
-	Gran cantidad de uso de memoria.
-	Dependencia en la organizaci�n, su cultura y la madurez de la compa��a.

Finalmente se hablan sobre los detalles de las tecnolog�as que se usan al desarrollar microservicios. Estas son las siguientes:

CQRS: Separar la acci�n de lectura de la de escritura. Sirve como punto de partida para descomponer tu c�digo.
Event Sourcing: Es secuencial, si se cambia algo en el medio del c�digo se sabr� si afecta lo dem�s o no.
?	Evento c�ntrico en el enfoque de dominio de modelos
?	Guarda eventos, no objetos de estado
?	El almacenamiento de eventos es el intermediario de la base de datos y los mensajes
?	Consigue los eventos para las entidades
?	Guarda los eventos que se asociaran a las entidades y sus dependencias
DDD / Bounded context (Domain Driven Design): El dise�o es complicado, se debe conocer el negocio, el problema y el alcance para as� aislar los l�mites de cada problema y que pueda ser espec�fico.
API Gateway: Esto soluciona los siguientes problemas:
?	Una granularidad muy fina.
?	Las distintas necesidades de informaci�n de los distintos clientes.
?	La cantidad y ubicaci�n de los distintos servicios que cambian din�micamente.
?	El particionamiento de servicios el cual deber�a estar oculto para los clientes.
Lenguaje para los problemas de espacio: Permite aplicar un lenguaje en el cual sea �til para un problema en espec�fico lo cual minimiza el c�digo a utilizar.
