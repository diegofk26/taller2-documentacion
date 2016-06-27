Informacion general
********************

Hipotesis y supuestos
========================





Lecciones aprendidas
======================

1. Mejorar la organizacion y division de tareas, asignando a cada persona a una
tecnologia sobre la cual pueda trabajar comodamente, ya que nos paso que una de
las personas asignadas al application server tenia problemas con su sistema
operativo y con los problemas que traia la virtualizacion del sistema utilizado
por los demas opto por trabajar dentro de un container con emacs, sin saber
utilizarlo.

2. No confiarse ni creer en que un modulo totalmente desconocido sera facil de
desarrollar, esto es con el shared server le llevo mucho mas tiempo del que nos
dieron a entender que llevaria por el hecho de que no se conocian los temas de
bases de datos, Mensajes HTTP, Angular, HTML, etc.

3. La importancia de documentar desde un principio con el formato final, para este
caso con sphinx, ya que los demas informes los realizamos en google docs lo cual
a la hora de querer pasarlo a sphinx lleva su tiempo.

4. Poner un esfuerzo extra en un principio para poder llegar mas tranquilos a la
entrega final.

5. Elegir el entorno de testing mas conveniente de entrada. Nos paso que para
tener pruebas lo antes posibles tomamos cppunit y lo utilizamos, pero luego
nos parecio mejor idea utilizar google test, y la migracion de las pruebas
existentes llevo su tiempo.

6. Poner en funcionamiento y entender rocksDB y Mongoose tomo mucho mas tiempo del
estipulado.

7. Automatizar algunas pruebas nos consumio demasiado tiempo, y en algunos casos
se escribian de manera incorrecta por algun detalle que no teniamos en cuenta y
daban resultados erroneos aun estando bien implementadas las clases.
Un ejemplo de esto fue en las clases que dependen de una base de datos, para la
mayoria de las pruebas seutiliza la misma base de datos por lo que debiamos invocar
un script de bash que limpie el entorno de testing tras la corrida de una prueba.


8. Querer optimizar de entrada sin ser necesario. Se perdio bastante tiempo al
tratar de implementar una solucion eficiente pero demasiado compleja, la cual
luego de desarrollar una parte fue descartada y se opto por una mas sencilla.



Known issues
===============

Application Server
--------------------

1. Mala estructura jerarquica de carpetas.
2. Algunas clases como EstadisticasCandidatos tienen muchas responsabilidades.
3. FactoryServicios podria estar mejor modularizada.
4. Se responde a todos los HTTP Requests mal formulados con el mismo mensaje.
5. Se podria haber implementado un iterador para recorrer ListadoDeUsuarios.

Cliente
---------

1. Aleatoriamente se generan en el expandable list view hijos o childs de mas.
2. Si se cierra el appserver mientras estoy conectado y entro a editListViewActivity
   no se actualizan las vistas.

Shared Server
--------------

1. En el cliente web: no funciona la modificacion de fotos.



Shared
