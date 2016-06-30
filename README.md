# Taller de programacion 2 - Tinder Documentacion

Para generar la documentacion es necesario tener sphinx instalado en nuestros sistemas.

Entramos a la carpeta SphinxDocumentation y ejecutamos el siguiente comando:

      > sphinx-build -b html \source \build

En caso de ser exitosa la operacion nos generara los correspondientes archivos html en SphinxDocumentation/build.

Se deben colocar las documentaciones html correspondientes del appserver y del cliente en una carpeta llamada Doxygen/Cliente/ y Doxygen/Appserver/

y una carpeta Appserver-Coverage/ que contiene los archivos generados al obtener el coverage (en formato html).
