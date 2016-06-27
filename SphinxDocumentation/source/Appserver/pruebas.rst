Pruebas - Application Server
******************************

  El Application server cuenta con pruebas tanto unitarias como de API que ayudan
  a verificar su correcto funcionamiento. En las siguientes secciones daremos a
  conocer los conceptos basicos que se deben saber acerca de ellas.

Coverage
========

  Para asegurarnos de que cada clase sea probada en la mayoria de sus metodos,
  se genera un informe de code coverage para saber que las clases se probaron en
  una medida suficiente.

  `Click aqui para ver el informe de coverage actual <../../../Appserver-Coverage/index.html>`_

Pruebas de API
==============

  El proyecto cuenta con pruebas especificas para probar la API rest existente
  entre el Cliente y el Application Server.

¿Como correrlas?
------------------

  Para correr las pruebas debemos posicionarnos en el directorio raiz del
  proyecto del Application Server, luego:

  > cd Appserver

  > cd Test

  > ./correr_pruebas_API.sh


Pruebas Unitarias
==================

  El proyecto ademas cuenta con pruebas especificas para probar la funcionalidad
  de cada clase en particular.

¿Como correrlas?
-----------------

  Una vez posicionados en el directorio raiz del proyecto del Application server
  ejecutar los siguientes comandos:

  > cd Appserver

  > cd Test

  > ./correrUnitTests.sh



.. warning:: ¡Es necesario que el proyecto haya sido compilado para poder correr las pruebas!
