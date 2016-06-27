Documentacion Tecnica
***********************

Tecnologias utilizadas
=======================

Application Server
-------------------

* RocksDB
* Google Test
* Google Mock
* Mongoose
* JsonCPP
* Docker
* Doxygen
* Travis CI
* gCov
* Google Cloud Messaging

Shared Server
--------------

* Angular
* Node js
* Heroku
* HTML
* bootstrap
* PostgreSQL


Cliente
---------

* Android
* Doxygen
* Geolocalizacion



Documentacion del codigo fuente
================================

Al documentar las clases del servidor de aplicacion y del cliente se utilizaron
estandares para generar documentacion a partir de comentarios en el codigo utilizando
doxygen:

`Documentacion del Cliente <../../../Doxygen/Cliente/index.html>`_

`Documentacion del Application server <../../../Doxygen/Appserver/index.html>`_




Estructuras de bases de datos de Application Server
=====================================================


Credenciales de usuarios:
--------------------------

claveDeUsuario{id} | Password | IdSharedServer

Candidatos:
------------

U1U2 | claveUsuario1 | claveUsuario2 | estadoDeVoto1 | estadoDeVoto2

  U1U2: "usuario1 usuario2" (el orden de los usuarios depende de sus caracteres ASCII).

  estadoDeVoto'n': Es un numero.
                  0: usuario n voto en contra
                  1: usuario n voto a favor
                  2: usuario n fue notificado sobre el otro usuario pero no emitio voto
                  3: usuario n no fue notificado.

  claveUsuario'n': "usuarion"


Conversaciones
-------------------


U1U2 | mensajes

  U1U2: "usuario1 usuario2" (el orden de los usuarios depende de sus caracteres ASCII).

  mensajes: Es un jsonArray que contiene los mensajes enviados entre los dos usuarios
            de la clave.

            mensaje: Es un jsonObject con las claves emisor y mensaje.




Cliente
========

Especificaciones técnicas:

Descripción de actividades de la aplicación:

1.	MainActivity: ScreenSplash actividad, básicamente es una pantalla de bienvenida/carga, donde se inicia la conexión con el server. De ser posible se van pasando actividades sin que el usuario tenga que volver a ingresar el login, o tenga que ingresar el ip:port, si esos datos ya están persistidos y de esta manera llega de forma rápida a MatchingActivity.
2.	SelectLoginOrRegistryActivity: Se elige la modalidad para ingresar a la aplicación.
3.	LoginActivity: en esta modalidad de ingreso a la aplicación, el usuario ya debe estar registrado, de otra forma obtendrá un mensaje al loguearse y no podrá loguearse de esta forma.
4.	RegistryActivity: en esta modalidad para ingresar a la aplicación, el usuario es un usuario nuevo, si es un usuario ya registrado obtendrá un error al registrarse. Se piden datos básicos como nombre, edad (menor que 150), alias, contraseña (mayor a 5 caracteres), email, contraseña. Ninguno de estos datos pueden estar vacíos o violar las restricciones propuestas, sino el usuario obtiene un mensaje para rectificar los datos.
5.	InterestsActivity: Se agregan intereses que se obtienen del Appserver.
6.	MatchingActivity: actividad de matcheo de personas.
7.	InformationActivity: Información básica junto con una image.
8.	ChatListActivity: Listado de todos los chats disponibles para el usuario.
9.	ChatActivity: chat del usuario con otro usuario, desde aquí se contempló que al error de enviar un mensaje, se pueda volver a enviar el mensaje nuevamente clickeando en la burbuja.
10.	ProfileActivity: perfil del usuario.
11.	EditProfileActivity: Perfil del usuario editable.
12.	AreYouSureActivity: actividad donde se advierte al usuario de que Borrar su perfil no tiene vuelta atrás.

Descripción de las vistas usadas en las actividades:

1.	 MainActivity: Se usaron dos WebViews para reproducir dos animaciones .gif y un TextView para personalizar un mensaje para el usuario.
2.	SelectLoginOrRegistryActivity: Simples Buttons con sus Onclick especificados para ir a Actividades diferentes.
3.	LoginActivity: EditTextView para la edición del Usuario y Contraseña, un CheckBox para habilitar o deshabilitar ocultar la contraseña.
4.	RegistryActivity: EditTextView para la edición del Nombre, Alias, Edad (numérico), Email, y Contraseña. Mismo CheckBox que la actividad anterior, y dos RadioButton para representar el género del usuario (Solo uno de los dos puede quedar seleccionado).
5.	MatchingActivity: Se usó varios ImagenViews para representar tanto la imagen de perfil del usuario como los botones de voto e información del usuario a votar.
6.	InformationActivity: Se usó TextViews para representar el Nombre, Alias, Edad, Sexo e Intereses. Un ExpandableListView para representar los intereses del usuario a votar.
7.	ChatListActivity: ListView para modelizar los usuarios matcheados.
8.	ChatActivity: ListView para modelizar los mensajes que se intercambian los usuarios y un RelativeLayout donde yace un EditText y un Button para editar el próximo mensaje a enviar.
9.	ProfileActivity:  Se tienen TextViews para representar el Nombre, Alias, Edad, Sexo e Intereses en formato HTML. Un ExpandableListView para representar los intereses del usuario a votar.
10.	EditProfileActivity: TextView para modelizar un header Nombre, Alias e Intereses. EditText para editar el Nombre y Alias. Y un ExpandableListView con EditViews como childs para editar los intereses, a su vez se va setear texto en los EditText, para que aparezcan los intereses anteriores del usuario.
11.	AreYouSureActivity: simple activdad con dos Buttons, uno Borra el usuario y va a SelectLoginOrRegistryActivity y el otro vuelve a MatchingActivity.

	Vistas usadas por las ListViews y ExpandableListViews:

1.	Interesest_item: EditText, ImageView (símbolo de +), y un TextVIew como marquesina (usado por  los ExpandableVIews de InterestActivity y EditProfileActivity)
2.	List_group: básico TextView con un fondo negro, para modelizar un header.
3.	List_item: item de ChatListActivity, lo usa su ListView. Consta de una ImageView para visualizar la imagen de perfil del usuario matcheado y dos TextViews uno para el nombre del usuario matcheado y otro para el último mensaje entre ambos.
4.	Profile_interestItem: único TextView para modelizar a los childs del ExpandableListView tanto de ProfileActivity cómo de InformartionActivity.
