#QuizBot

Chatbot que permite recoger datos de encuestas definidas mediante un compilador a trav�s de Telegram y consultar gr�ficas simples e informes sobre los datos recogidos.

##Pasos para ejecutar QuizBot

A continuaci�n se detallan los pasos a seguir para poder ejecutar correctamente QuizBot.

###Instalaci�n

Abrimos un terminal en la carpeta */QuizBot* y ejecutamos el siguiente comando

	$> pip install -r requirements.txt

Una vez instaladas las dependencias, podemos empezar a ejecutar el proyecto.

###Definici�n de la encuesta

Primeramente, debemos de crear la encuesta. Esta se crea en el fichero *Mi_Encuesta* dentro de la carpeta *QuizBot/cl*.  Inicialmente, hay una encuesta de ejemplo ya creada.

Se debe de seguir el formato de encuesta planteado en este apartado de la pr�ctica:

	https://gebakx.github.io/QuizBot/#compilador

Una vez creada, abrimos un terminal en la carpeta *QuizBot/cl* y ejecutamos el siguiente comando

	$> python  test.py  Mi_Encuesta.txt

Esto nos crear�:

1. Un archivo .png de la forma **nombreEncuesta_grafo.png** con la representaci�n en forma de grafo de nuestro AST en este mismo directorio *QuizBot/cl* 

2. Un fichero de datos binario de la forma **nombreEncuesta_graph** con la informaci�n de la encuesta extra�da del grafo del AST en el directorio *QuizBot/bot*

###Ejecuci�n de QuizBot en Telegram

A continuaci�n, debemos irnos al directorio donde se encuentra el c�digo del bot, *QuizBot/bot*. Aqu�, abrimos un terminal y ejecutamos el siguiente comando

	$> python bot.py

y lo dejamos corriendo. Ahora, podremos interactuar con nuestro bot a trav�s de Telegram y hacer la encuesta que hay de ejemplo en esta pr�ctica.


###Modificaci�n de la encuesta

Si se quiere modificar la encuesta, se han de seguir los siguientes pasos.

####1 - Eliminar el fichero binario XXX_graph  de */QuizBot/bot*
####2 - Eliminar el fichero user_data (en caso de que exista) de */QuizBot/bot*
####3 - Modificar el fichero Mi_Encuesta.txt de */QuizBot/cl*
Se modifica la encuesta en este fichero. 
Los identificadores de **pregunta**, **respuesta**, **item**, **alternativa** y **encuesta**, pueden ser cualquier cadena de caracteres alfanum�ricos [a-zA-Z0-9] �nica entre todos los identificadores. No obstante, **los identificadores que listan las posibles respuestas a una pregunta solo pueden ser caracteres num�ricos**.

####4  - Volver a generar el fichero binario con la nueva encuesta
Esto se hace en el directorio *QuizBot/cl* ejecutando el comando

	$> python test.py Mi_Encuesta.txt

#Autor

Aar�n Acosta Fernandez
aaron.acosta@est.fib.upc.edu

Facultat d'Inform�tica de Barcelona (UPC)
Grau en Enginyeria Inform�tica
Assignatura de Llenguatges de Programaci�