<H1 align="center"> MVC_TOURS </H1>

*En el presente repositorio, se encuentra el código correspondiente al proyecto MVC_Tour, donde de igual manera, se encuentra el archivo MD, **MVC_Tour**, el cual contiene, la documentación pertienente del proyecto.*

<hr>

<H1> Prerequisitos </H1>
<H2> Creación de Cuenta MongoDB Atlas </H2>

Para comenzar, se tendrá que acceder a la página oficial de **MongoDB Atlas**, en la que se tendrá que registrar una nueva cuenta. <a href="https://cloud.mongodb.com/"> Dar clic para dirigirse a página oficial Mongo DB Atlas </a>

Donde una vez creada la cuenta, se accederá a ella y se realizaran, los pasos guía, que se nos despliegan, al entrar por primera vez a nuestra cuenta. Donde una vez realizado los primeros pasos, nos ubicará en la página de nuestro primer proyecto.

![Página_Proyecto](https://raw.githubusercontent.com/JorgeBarcenas/MVC/master/Git/Ambientacion/Usuario.PNG)

Donde nos dirigeremos a la pestaña **Security**, donde en la parte superior derecho, abra un botón verde, qel cual dirá **Add new user**, donde se dará clic en el y se creará un usuario con privilegios de **Administrador**. En este caso se crea usuario administrador, con su respectiva contraseña, donde dicho administrador, cuenta con los permisos de poder editar cualquier colección de cualquier base de datos que almacene Cloud.

![Contraseña](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Ambientacion/Usuariocreado.png)

<hr>

<H2> Creación de BD </H2>

Dentro de la página principal de nuestro proyecto en Atlas, se dará clic, sobre el botón **Collections**,el cual nos dirigirá a una nueva ventana, en la que se dará clic sobre el botón **Add Database**, donde nos desplegará una ventana, en la que tendremos que colocar el nombre de nuestra base de datos.

![add_DB](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Ambientacion/BD.png)

<hr>

<H2> Importar Colecciones </H2>

Una vez creada la base de datos dentro de nuestro proyecto Atlas, este no contiene ninguna colección, por lo que no cuenta con ningún tipo de información, por lo que se procede con la importación de nuestras colecciones almacenadas dentro de nuestro equipo.

![Info_Atlas](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Ambientacion/Infoatlas.png)

Dentro de la página de Atlas, se pueden conocer los comandos a ejecutar para la importación de colecciones, donde se utiliza el comano **mongo import**, seguido de las especificaciones, las cuales son:

En la primera parte del código, se agregan, las direcciones y el nombre de los servidores, que pertenecen en nuestro Cloud, (Podría funcionar con solo un servidor, sin embargo, es preferible anexar los otros dos, en caso de que el servidor principal colapse o caiga).

**Cluster0-shard-0/cluster0-shard-00-00-e5wzw.mongodb.net:27017, cluster0-shard-00-01-e5wzw.mongodb.net:27017, cluster0-shard-00-02-e5wzw.mongodb.net:27017**

Posteriormente se especifica, el nombre de la base de datos **learning_mongo** donde se anexará la colección, así como el correspondiente nombre, que tendrá nuestra colección **tour**, y la ubicación dentro de nuestro equipo, en el que se encuentra el archivo correspondiente a importar.
**--db learning_mongo --collection tour --type json --file C:\Users\hp\Desktop\Mongo\tours.json --jsonArray**

Por último, se agregan las credenciales del administrador, con las cuales se tendrá acceso a Cloud

**--authenticationDatabase admin --ssl --username root --password toor**

Dicho código se ejecutará en una ventana CMD, en la ubicación en la que se encuentra la configuración de nuestro MongoDB, este comando se ejecutara para cada uno de los archivos que contienen nuestras colecciones, que se importaran a la base de datos dentro de lanube.

![cmd1](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Ambientacion/CMD1.png)

![cmd2](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Ambientacion/CMD2.png)

![cmd3](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Ambientacion/CMD3.png)

Por lo que una vez, ejecutado el comando, dentro de nuestro Cloud, deberá de aparecer las colecciones que se importaron.

![Evidencia](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Ambientacion/Evidencia.png)

<hr>

<H2> Instalación de Drivers </H2>

Una vez teniendo las bases de datos en la nube, se procede a la instalación de las librerías, que nos permitirán, realizar las peticiones, dentro de nuestros archivos JS.
Para ello, se abrirá Visual Studio Code, y se abrirá una línea de comandos, y se establecerá en la ubicación en la que se tengan almacenada la carpeta con los archivos JS, para poder ejecutar el comando 
**npm install -nombre de librería-**

![Install1](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Ambientacion/Install1.png)

![Install2](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Ambientacion/Install2.png)

![Install3](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Ambientacion/Install3.png)

Donde una vez instalado, los drivers, se comienza con la edición de los programas JS, para que la consulta resulte exitosa, para ello se tiene que configurar el archivo Key.JS, el cual nos permitirá, realizar una conexión con la Nube, para el acceso a la base de datos.

<hr>

<h1 align="center"> MVC TOUR PROYECT </H1>

<H2> Comando Node </H2>
Una vez configurado la conexión a la API, dentro de la aplicación Visual Studio Code, se abre una terminal, donde se ejecutará el comando, Node junto con el nombre del archivo que ejecutará, el cual compilará el archivo **APP.JS**.

![Comando Node](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Comando%20Node/comando%20node.png)

Una vez ejecutado dicho comando, nos despliega un mensaje la terminal, que nos indica que sea ah realizado la conexion al servidor exitosamente, por lo que se puede proseguir con la ejecución de las pruebas.
Una vez ejecutado el comando, el sistema realizara conexión con el servidor.

![Conexion](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Consulta%20Tour/ConexionBD.png)

<hr>

<H2> Consulta Tour </H2>

<ul>
 <li type="circle"> Configuración de URL en Postman </li>
 <li type="circle"> Archivo App.js </li>
 <li type="circle"> Archivo Admin.js </li>
 <li type="circle"> Archivo Tour.js </li>
 <li type="circle"> Resultado </li>
</ul> 

<h3> <b> Configuración URL en Postman </b> </h3>

Donde una vez conectado el servidor, se procede a abrir a aplicación Postman, en el cual dentro de la barra en la que se coloque, la URL. Donde se seleccionará la opción **GET**, seguida de la siguiente URL
**localhost:3000/api/tours/**
La cual consiste en **localhost** nombre de nuestro servidor, seguido de **3000** el cual es el puerto por el que se transmite información dentro de la aplicación Postman, **api/tours** el cual es el nombre con el que se manda a llamar las instrucciones de la consulta.

![URL_Postman](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Consulta%20Tour/URLPostman.png)

<h3> <b> Archivo App.js </b> </h3>

El cual consta del servidor local, el puerto por el que se realiza la petición, y el nombre de la solicitud, que se encuentra definido dentro del archivo **APP.JS:**

![Archivo APP](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Consulta%20Tour/App.png)

<h3> <b> Archivo Admin.js </b> </h3>

El cual nos redirige a el archivo **amdmin.js**, donde se encuentra, la especificación de la consulta que se realizara con la especificación enviada en la URL

![Archivo ADMIN](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Consulta%20Tour/Admin.png)

<h3> <b> Archivo Tour.js </b> </h3>

El cual toma la ayuda del archivo Tour.js, en el que con el uso del driver Mongoose, se crea un modelo para definir las propiedades de nuestro documento, almacenada en nuestra nube, esto para poder facilitar a búsqueda y obtención de información.

![Archivo_Tour](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Consulta%20Tour/Tour.png)

Donde cabe mencionar, que se especifico la colección a la que se entrara para la obtención de datos, mediante el código:

![Linea_Tour](https://raw.githubusercontent.com/JorgeBarcenas/MVC/master/Git/Consulta%20Tour/Tourlinea.PNG)

 Ya que, al tener más de 1 colección en nuestra misma base de datos, a la hora de realizar la conexión a la base de datos, esta entra en conflicto, ya que, dentro del archivo Tour.js no se especifica la colección a la cual pertenece el modelo, creado para la obtención de información.
 
 <h3> <b> Resultado </b> </h3>

Donde una vez realizado el proceso, se dirige a la nube, junto a la base de datos y coleccione especificada, para posteriormente, obtener la información, la cual consta de la selección total, de la colección, **“db.tour.find()”**, por lo que la recogerla, la envía devuelta a el usuario para su despliegue.

![Evidencia_1](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Consulta%20Tour/Evidencia%20Consulta%201.png)


![Evidencia_2](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Consulta%20Tour/Evidencia%20Consulta%202.png)

<hr>

<H2> Consulta inqId </H2>

<ul>
 <li type="circle"> Configuración de URL en Postman </li>
 <li type="circle"> Archivo App.js </li>
 <li type="circle"> Archivo Admin.js </li>
 <li type="circle"> Archivo Tour.js </li>
 <li type="circle"> Resultado </li>
</ul> 

<h3> <b> Configuración de URL en Postman </b> </h3>

Se realizará una consulta a la colección Tour, dentro de nuestra base de datos en la nube, en la que constará de una búsqueda específica, por ID, en la que una vez posicionado en la aplicación Postman, se introducirá, en la barra de búsqueda URL, lo siguiente: **localhost:3000/api/tours/”ID_definido”**.

En el que se ingresará algún ID, existente dentro de nuestra colección Tour, donde en este caso se hará uso del siguiente ID: **5cbf9d125476ba2a647aa252**.
La cual consiste en **localhost** nombre de nuestro servidor, seguido de **3000** el cual es el puerto por el que se transmite información dentro de la aplicación Postman, **api/tours** el cual es el nombre con el que se manda a llamar las instrucciones de la consulta y **5cbf9d125476ba2a647aa252** el cual es la condición con la que se realizara las instrucciones.

![URLPostman](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Consulta%20InqID/URL.png)

<h3> <b> Archivo App.js </b> </h3>

El cual realizará el mismo proceso que la consulta a la colección Tour, previamente detallado, el cual inicia en el archivo **app.js**, donde busca, el formato al que pertenece. 

![Archivo_App](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Consulta%20InqID/App.png)

<h3> <b> Archivo Admin.js </b> </h3>

El cual nos dirige al archivo **admin.js** donde busca, las especificaciones de la consulta que se realizaran, así como la leyenda que se desplegará en caso de tener éxito en la búsqueda de la información.

![Archivo_Admin](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Consulta%20InqID/Admin.png)

<h3> <b> Archivo Tour.js </b> </h3>

Donde posteriormente nos dirige, al archivo Tour.js, donde ya este especificado el modelo a usar, así como el nombre de la colección a la que se accederá.

![Archivo_Tour](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Consulta%20InqID/Tour.png)

<h3> <b> Resultado </b> </h3>

Donde posterior, se dirigirá a la base de datos dentro de nuestra nube, en la que se realizará la búsqueda de la información de la consulta, la cual corresponde a una consulta, de un registro (ID) especifico: **db.tour.find({ID: 5cbf9d125476ba2a647aa252})**. Donde una vez realizado el proceso, se obtendrá la información y se le desplegará al usuario en la aplicación Postman.

![Evidencia](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Consulta%20InqID/Evidencia.png)

<hr>

<H2> Consult InqByName </H2>

<ul>
 <li type="circle"> Configuración de URL en Postman </li>
 <li type="circle"> Archivo App.js </li>
 <li type="circle"> Archivo Admin.js </li>
 <li type="circle"> Archivo Tour.js </li>
 <li type="circle"> Resultado </li>
</ul> 

<h3> <b> Configuración de URL en Postman </b> </h3>

Se realizará una consulta dentro de la colección Tour, dentro de nuestra base de datos en Atlas, en la que constará de una búsqueda específica, por nombre del tour, en la que una vez posicionado en la aplicación Postman, se introducirá, en la barra de búsqueda URL, lo siguiente:
**localhost:3000/api/tours/” Nombre de tour definido”**
En el que se ingresará un Nombre de tour, existente dentro de nuestra colección Tour, para este ejemplo, se hará uso del siguiente nombre de tour: **In the Steps of John Muir**
La cual consiste en **localhost** nombre de nuestro servidor, seguido de **3000** el cual es el puerto por el que se transmite información dentro de la aplicación Postman, **api/tours** el cual es el nombre con el que se manda a llamar las instrucciones de la consulta y **In the Steps of John Muir** el cual es la condición con la que se realizara las instrucciones.

![URL](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Consulta%20InqByName/URL.PNG)

<h3> <b> Archivo App.js </b> </h3>

De igual manera realizará el mismo proceso que las consultas previamente expuestas, donde una vez realizado la petición en Postman, inicia en el archivo **app.js**, donde busca, el formato al que pertenece. 

![APP](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Consulta%20InqByName/App.PNG)

<h3> <b> Archivo Admin.js </b> </h3>

El cual redirige la información al archivo **admin.js** donde busca, las especificaciones de la consulta que se realizaran, así como la leyenda que se desplegará en caso de tener éxito en la búsqueda de la información.

![ADMIN](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Consulta%20InqByName/Admin.png)

<h3> <b> Archivo Tour.js </b> </h3>

El cual solicita el archivo **Tour.js**, para basarse en el modelo, descrito en e archivo, para la búsqueda de las solicitudes, así como la colección a la que tendrá que acceder dentro de la base de datos.

![Tour](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Consulta%20InqByName/Tour.png)

<h3> <b> Resultado </b> </h3>

Donde una vez realizado, el procedimiento se realizará la petición a nuestra base de datos en Atlas, para la obtención de información de la colección Tour, en la cual, se realizará, una consulta:
**db.tour.find({tourName:In the Steps of John Muir})**
En el cual, al finalizar, se desplegará toda la información que cumpla con la condición, solicitada por el usuario dentro de la aplicación Postman.

![Evidencia](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Consulta%20InqByName/Evidencia.PNG)

<hr>

<H2> Insert Tour </H2>

<ul>
 <li type="circle"> Configuración de URL en Postman </li>
 <li type="circle"> Archivo Admin.js </li>
 <li type="circle"> Archivo Tour.js </li>
 <li type="circle"> Resultado </li>
</ul> 

<h3> <b> Configuración de URL en Postman </b> </h3>

Esta ocasión se realizará un insert dentro de la colección Tour dentro de nuestra base de datos learning_mongo, almacenada en nuestra nube Atlas, en la cual en el apartado izquierdo donde se coloca la URL, se tendrá que cambiar la condición de **GET a POST**.
De igual manera, se tendrá que dirigir a la pestaña “Body”, posteriormente seleccionar la opción “Raw”, en la cual nos desplegará una terminal, donde se tendrá que introducir, toda a información que se requiera registrar en la colección.
**localhost/3000/api/tours/names/"Insertar informacion"**
La cual consiste en **localhost** nombre de nuestro servidor, seguido de **3000** el cual es el puerto por el que se transmite información dentro de la aplicación Postman, **api/tours/names** el cual es el nombre con el que se manda a llamar las instrucciones de la consulta y **Insertar inforamción** el cual es la condición con la que se realizara las instrucciones.

Donde para la inserción de información se dirigirá a la pestaña **Body**, junto con la opción **Raw**, se escribirá, la información de los siguientes documentos:

<ul>
 <li> tourName <b> String </b> </li>
 <li> tourDifficuly <b> String </b> </li>
 <li> tourDescription <b> String </b> </li>
 <li> tourLenght <b> Number </b> </li> 
 <li> tourPrice <b> Number </b> </li>
 <li> tourTags <b> String </b> </li>
 <li> tourPackage <b> String </b> </li>
 <li> tourOrganizer <b> String </b> </li>
 <li> organizarName <b> String </b> </li>
 <li> organizerPhone <b> String </b> </li>
 </ul>

![URL](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Insert%20Tour/URL.PNG)

Donde una vez escrito y enviado la información, se nos desplegará una confirmación en la terminal, cuando se allá generado la información dentro de la colección.

![Terminal](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Insert%20Tour/Terminal.png)

<h3> <b> Archivo Admin.js </b> </h3>

La cual, dicha leyenda esta especificada, dentro del archivo Admin.js

![Admin](https://raw.githubusercontent.com/JorgeBarcenas/MVC/master/Git/Insert%20Tour/Fuente.png)

<h3> <b> Resultado </b> </h3>

En el cual podemos verificar, la información cuando se realiza una respectiva consulta dentro de la colección Tour. Verificando de esta manera, el almacenamiento de la información previamente enviada.

![Evidencia](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Insert%20Tour/Evidencia.png)

<hr>

<H2> Eliminar Tour </H2>

<ul>
 <li type="circle"> Configuración de URL en Postman </li>
 <li type="circle"> Archivo App.js </li>
 <li type="circle"> Archivo Admin.js </li>
 <li type="circle"> Resultado </li>
</ul> 

<h3> <b> Configuración de URL en Postman </b> </h3>

Se realizará la eliminación completa de un objeto, para este servicio, se requiere posicionarse dentro la aplicación Postman, en la que se requiere seleccionar el servicio DELETE, de la parte izquierda donde se coloca la URL.
Y escribir sobre la parte de URL, la siguiente línea:

**localhost:3000/api/tours/5cc54d84d4755a33b0084179**
La cual consiste en **localhost** nombre de nuestro servidor, seguido de **3000** el cual es el puerto por el que se transmite información dentro de la aplicación Postman, **api/tours** el cual es el nombre con el que se manda a llamar las instrucciones de la consulta y **5cc54d84d4755a33b0084179** el cual es la condición con la que se realizara las instrucciones.

![URL](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Delete%20Tour/URL.png)

<h3> <b> Archivo App.js </b> </h3>

Una vez introducido la información correspondiente, el programa, inicia en el archivo Admi.js, en el que obtiene el nombre de la operación que realizamos.

![App](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Delete%20Tour/App.png)

<h3> <b> Archivo Admin.js </b> </h3>

Para posterior, dirigirse al archivo Admin.js, en el que se encuentra definida la operación a realizar dentro de la base de datos.

![Admin](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Delete%20Tour/Admin.png)

Donde procede a acceder a la base de datos, para ejecutar las instrucciones, donde le envía una respuesta a el usuario mediante una leyenda, confirmándole al usuario que la instrucción enviada resulto exitosa.

![Terminal](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Delete%20Tour/Terminal.png)

<h3> <b> Resultado </b> </h3>

Donde si se realiza una consulta del elemento eliminado, no se desplegará ninguna información del elemento previamente eliminado.

![Evidencia](https://raw.githubusercontent.com/JorgeBarcenas/Data-Mining-and-Data-Warehousing/master/Git/Delete%20Tour/Evidencia.png)

<hr>

<H2> Funcionamiento de sistema </H2>

<ul>
 <li type="circle"> Tipos de Parametros </li>
 <li type="circle"> Flujo MVC </li>
</ul> 

<H3> <b> Tipos de Parametros </b> </h3>

El servicio de Web REST consta de 4 parametros:

<ul>
 <li> <b> HeadParams: </b> Son los parámetros incluidos en el encabezado de la solicitud, generalmente relacionados con la autorización. </li>
 <li> <b> PathParams: </b> Son los parámetros dentro de la ruta del punto final, antes de la cadena de consulta. Estos se llegan a  poner dentro de llaves dentro de las colecciones. </li>
 <li> <b> QueryParams: </b> Son parámetros en la cadena de consulta del punto final, normalmente van despues del caracter especial (?), denrto de la ruta. </li>
 <li> <b> BodyParams: </b> Son parámetros incluidos dentro del cuerpo de la solicitud que se enviará. Usualmente enviado como JSON. </li>
 </ul>
 
 <hr>
 
 <H3> <b> Flujo MVC </b> </H3>
 
<ul>
 <li type="square"> <b> Postman URL: </b> Inicialmente se coloca dentro de la aplicación Postman, el tipo de servicio web REST, que deseamos realizar, <b> GET, POST, PUT, DELETE </b>, posteriormente, se introduce la URL, y se envia la información. </li>
 <li type="square"> <b> Archivo App.js: </b> La URL enviada por el usuario desde Postman, llega a el archivo App.js, en la que busca la misma línea ingresada por el usuario <b> (localhost/3000/api/tour) </b>, dentro del archivo, donde una vez identificada, se dirije a el archivo Admin.js en la carpeta controlador. </li>
 <li type="square"> <b> Archivo Admin.js: </b> En este archivo, se buscan los procedimientos que realizara, la URL introducida por el usuario, para posteriormente, su ejecución dentro de la base de datos. </li>
 <li type="square"> <b> Archivo Tour.js: </b> Dentro de este archivo, se encuentra un modelo, de la base de datos a la que se accedera, con la finalidad de optimizar la busqueda dentro de la colección en la base de datos de nuestra nube. </li>
 <li type="square"> <b> Archivo Key.js: </b> Este archivo contiene las credenciales y la configuración para la conexión con la base de datos en la nube. </li>
 <li type="square"> <b> Base de datos: </b> Una vez enviado la información a la base de datos dentro de nuestra nube, se procedera a realizarse la consulta correspondiente al nombre de la URL proporcionada por el usuario. Donde una vez encontrado,  la información, le envá un mensaje a el usuario, confirmando su busqueda, así como el envío de la respectiva información a e usuario </li>
 <li type="square"> <b> Despliegue de información: </b> Una vez obtenida la información se desppliega la información a el usuario conforma a la informacón encontrada, en base a la consulta. </li>
 </ul>
 
 ![MVCtour](https://raw.githubusercontent.com/JorgeBarcenas/MVC/master/Git/MVC/Tour.PNG)
 
<hr>
