# Teoría: Introducción a los sistemas operativos

¿Cómo puede ser que haya miles de modelos de computadora diferentes pero todos puedan ejecutar los mismos programas? ¿Ha pensado alguna vez en cómo interactúan los programas con el hardware? Estas y otras características son posibles gracias a los sistemas operativos.

##### Sistema operativo

**Un sistema operativo (SO)** es un conjunto de software que gestiona la comunicación entre todas las demás aplicaciones y hardware. Convierte una computadora en algo más que un montón de piezas metálicas, es decir, un sistema complejo que puede realizar diferentes tareas de manera efectiva.

Hoy en día, existen muchos sistemas operativos entre los que puede elegir. Para las computadoras personales, las más populares son las distribuciones de Microsoft Windows, macOS y Linux. Los dos principales sistemas operativos móviles son Android e iOS. Si alguna vez ha oído hablar de hervidores y refrigeradores inteligentes, incluso ellos tienen su propio sistema operativo.

Por supuesto, los sistemas operativos para tal gama de dispositivos difieren mucho entre sí. Lo que tienen en común son los medios que proporcionan a los programas y a quienes los utilizan.



Por un lado, es solo una ilusión que su navegador favorito sea el mismo en Windows que en macOS. Por otro lado, puede ejecutar la misma aplicación en diferentes computadoras con el mismo sistema operativo.



##### Funciones del SO

Un sistema operativo controla la comunicación entre todo el software y hardware de la computadora. Un sistema operativo puede dar a los programas acceso restringido a unidades de procesador, memoria, discos duros, red, periféricos y otros recursos.

Puede ejecutar un navegador, un reproductor multimedia y otras diez aplicaciones, y su sistema operativo es el que les brinda todos los recursos que necesitan para funcionar correctamente. Al mismo tiempo, este sistema operativo actúa como un árbitro justo que prohíbe que cualquier aplicación ocupe más recursos de los que realmente necesita.

Como mediador entre las aplicaciones y el hardware, el sistema operativo nos permite comunicarnos con el dispositivo sin entrar en detalles sobre sus especificaciones o mecánicas.

![img](https://ucarecdn.com/192e16f1-427b-4b2d-815b-7f9c9d10e6f8/)

Cualquier sistema operativo tiene varias funciones esenciales. Aquí hay una lista de algunos de ellos:

- protección de datos y acceso seguro;
- Administración de recursos;
- interacción entre hardware y periféricos;
- gestión de archivos;
- ejecutando otros programas.

Es posible distinguir más funciones de los sistemas operativos modernos, pero las enumeradas anteriormente son suficientes para empezar.

##### Componentes de los sistemas operativos

Una parte obligatoria de todos los sistemas operativos, su núcleo, es **el kernel** . Por lo general, es uno de los primeros programas que se carga cuando enciende su computadora. Proporciona todos los medios necesarios para ejecutar los programas que desee.

Normalmente, cuando inicia su sistema operativo, ve **la** **interfaz gráfica de usuario (GUI).** Es el tipo de interfaz que permite a los usuarios interactuar con el dispositivo mediante iconos gráficos e indicadores de audio. Otra forma de interactuar con el sistema operativo es utilizar comandos en un terminal basado en texto conocido como **interfaz de línea de comandos (CLI).**

![img](https://ucarecdn.com/701288a7-1d33-4712-84e6-87e171591e02/)

Hay dos tipos de granos, conocidos como monolíticos y micronúcleos. Un **kernel monolítico** es un programa grande que realiza la mayoría de las funciones del sistema operativo. Al mismo tiempo, un **microkernel** realiza solo un pequeño subconjunto de las funciones del sistema operativo, pero podemos extenderlo con módulos adicionales conocidos como **controladores** .

Hay otras partes importantes del sistema operativo además del kernel y la interfaz gráfica de usuario. Los revisaremos en el próximo tema. Por ahora, use la siguiente imagen para repasar todo lo que hemos cubierto hasta ahora:

![img](https://ucarecdn.com/28005216-bd94-4fe9-b422-b4f49e59f67d/)

##### Conclusión

El sistema operativo distribuye eficientemente los recursos de la computadora de la manera que describimos anteriormente. Es importante comprender que sin el sistema operativo, no sería posible utilizar la computadora.

Ahora conoces las principales funciones de los sistemas operativos y sus elementos esenciales. ¡Probemos lo que has aprendido hasta ahora!



# Teoría: tipos de archivos

Como ya sabrá, es conveniente almacenar datos en archivos. En este tema, averiguaremos qué más podemos hacer con los archivos, cómo distinguirlos y cuáles son sus tipos principales.



A continuación, proporcionamos una lista de tipos de archivos en el sistema Unix. En otros sistemas operativos, los tipos pueden diferir ligeramente, pero los básicos, de los que hablaremos con más detalle, se pueden encontrar en casi todas partes.



##### Tipos de archivos Unix

En general, un archivo es un contenedor de cierta información. Podemos poner casi cualquier cosa en este contenedor: una foto, un texto, un enlace a otro archivo, o simplemente otro contenedor con otros archivos anidados, etc. Todos estos datos son diferentes y por lo tanto los archivos en los que se almacenan son de varios tipos.

Los tipos de archivos de Unix son:

1. **archivos regulares** donde normalmente guarda sus datos personales, como textos, imágenes, etc.
2. **directorios** *,* o carpetas que hacen que sea más fácil de organizar otros archivos en el sistema,
3. **canalizaciones con nombre** *,* que permiten que diferentes procesos intercambien datos,
4. **enlaces simbólicos** *,* que contienen enlaces a otros archivos,
5. **archivos de dispositivo** *,* que contienen datos requeridos por el sistema operativo para interactuar con dispositivos físicos,
6. **sockets** *,* que proporcionan intercambio de datos entre procesos.

Estudiaremos con más detalle los tipos de archivos más utilizados. Estos son los que se pueden encontrar en todos los sistemas operativos: archivos regulares, directorios y enlaces simbólicos .

##### Archivos regulares

![img](https://ucarecdn.com/b7d183d0-fb2e-4fbc-9d56-fb4486026f99/)

Los archivos regulares son comunes porque los usuarios generalmente almacenan sus datos en ellos: documentos, videos, fotos, música, etc. En general, cualquier dato en dichos archivos se puede presentar de dos formas:

- datos textuales con algo de codificación, entonces el archivo se llamará **archivo de texto**
- cualquier otra secuencia de bytes sin restricciones de codificación, entonces dicho archivo se llama **archivo binario**

Para que sea más fácil averiguar qué archivo es texto y cuál es binario, estudiemos un par de ejemplos. Los archivos de texto suelen contener textos en formato plano, datos tabulares, archivos de configuración y formatos de datos como CSV o JSON. Los archivos binarios a menudo contienen datos como video, audio, bases de datos, archivos.

Los archivos binarios y de texto tienen características diferentes y, por lo tanto, requieren diferentes herramientas para trabajar con ellos. Vale la pena conocer estas diferencias porque definitivamente le ahorrará tiempo al leer o escribir sus datos en estos archivos.

La principal diferencia entre los archivos de texto y binarios es que estos últimos no tienen restricciones inherentes. Significa que pueden contener cualquier secuencia de bytes y deben abrirse en un programa apropiado que conozca el formato de archivo específico, como Media Player, Photoshop, Office, etc. Por otro lado, los archivos de texto se pueden editar en cualquier editor de texto. programa. Además, deben corresponder a varias restricciones, como contenido legible por humanos, formato de datos orientado a líneas, lectura universal de secuencias de nueva línea, etc.

##### Directorio

![img](https://ucarecdn.com/c8c7b523-27b9-4d40-871e-00abe40184df/)

Los directorios, que a veces también se denominan **carpetas** , son contenedores para los archivos. Por ejemplo, puede colocar sus archivos de música en un directorio titulado " *Música* ". La mayoría de los sistemas de archivos también permiten que un directorio contenga otros directorios. Se llama directorio **padre que** contiene directorios o **subdirectorios** **secundarios** . De esta manera, los datos de organización se almacenan en un medio en estructuras jerárquicas en forma de árbol, donde los directorios que no tienen padres se denominan **raíz.**directorios y sirven como base de esta estructura. Esta jerarquía proporciona vínculos claros entre archivos y hace que sea mucho más conveniente buscar datos en un disco. Solo necesitamos saber la ruta completa a un archivo, eso es todo. Para obtener esta ruta completa, necesitamos un nombre de archivo completo, es decir, agregamos la carpeta principal al archivo, y para la carpeta principal, también agregamos su principal y así sucesivamente hasta llegar a la raíz.

Los nombres de directorio en un nombre de archivo completo suelen estar separados por una barra `/`diagonal o una barra invertida `\`. Entonces, si hay un directorio raíz llamado " *directorio_raíz* " que contiene un subdirectorio llamado " *sub_directorio* ", y en este subdirectorio hay un archivo llamado " *mi_archivo* ", el sistema de archivos le asignará un nombre de archivo completo como " *directorio_raíz / subdirectorio / mi_archivo* " .

Además, las estructuras jerárquicas en forma de árbol nos permiten seleccionar grupos de archivos y administrarlos. Además, utilizando una estructura organizada jerárquicamente, podemos transferirlo a otra computadora.

##### Enlaces simbólicos

Por último, hay otro tipo de archivo especial que vale la pena considerar. Estos archivos se denominan **enlaces simbólicos** en el sistema Unix. Si usa Windows, es posible que los conozca como *atajos* . Un enlace simbólico contiene una referencia a otro archivo o directorio en forma de ruta absoluta o relativa. Supongamos que desea acceder a algunos archivos desde varios directorios. Si copia este archivo y coloca sus copias en cada directorio, cada vez que modifique una de las copias tendrá que ir y modificar todas las demás, y esto se siente como una pérdida de tiempo. Si coloca enlaces simbólicos que hacen referencia a este archivo en cada directorio, en realidad abrirían el archivo original al que hacen referencia.

##### Conclusión

En resumen, en este tema hemos aprendido que:

- los datos personales se almacenan en archivos regulares,
- los datos de los archivos normales pueden estar en formato binario o de texto,
- Además de los archivos normales, también hay directorios, enlaces simbólicos, sockets, canalizaciones con nombre y archivos de dispositivo,
- los directorios son contenedores para otros archivos,
- puede almacenar enlaces a archivos en archivos especiales llamados enlaces simbólicos.

Ahora, pasemos a los ejercicios para ver qué tan bien comprende los diferentes tipos de archivos.



# Teoría: descripción general de la línea de comandos

Mientras trabaja en la computadora, debe comunicarse con el **sistema operativo** (SO) para hacer las cosas por usted. Por ejemplo, si desea abrir un archivo, debe informarlo al sistema operativo (Windows, Linux o macOS). Hay dos formas de interactuar con el sistema operativo: una es más verbal mientras que la otra es más visual, pero ambas definitivamente merecen un reconocimiento. Estos dos métodos son la interfaz de línea de comandos y la interfaz gráfica de usuario.

##### ¿Qué es la línea de comandos?

La **interfaz de línea de comandos** o **CLI** es una forma de interactuar con un sistema operativo a través de comandos de texto. Por otro lado, la **interfaz gráfica de usuario** o **GUI** proporciona una interfaz con muchos iconos y menús. Aquí, le da comandos al sistema operativo haciendo clic en estos íconos o elementos del menú.

En el pasado, las interfaces de línea de comandos eran el único medio de interactuar con una computadora. Pero, ¿por qué usarlo ahora, cuando tiene una interfaz gráfica sencilla y familiar? Bueno, en general, las interfaces de línea de comandos son mucho más flexibles y tienen más opciones. Por ejemplo, puede combinar comandos para crear uno nuevo, mientras que no puede hacerlo a través de una interfaz gráfica. Algunos programas pueden incluso tener solo una interfaz de línea de comandos, por lo que requieren que el usuario conozca los conceptos básicos de la línea de comandos.

Además, los programas ejecutables por la interfaz de línea de comandos se pueden escribir en un lenguaje de comandos. Se denominan **scripts de shell** en UNIX y sistemas similares a UNIX, como GNU / Linux y macOS, y **archivos** por **lotes** en Windows.

Todos los sistemas operativos tienen interfaces de línea de comandos. Las aplicaciones también pueden tenerlo. Además, los lenguajes de programación modernos proporcionan un modo de línea de comandos interactivo, en el que se ejecuta el código línea por línea.

##### Acceder al intérprete de línea de comandos

Por lo general, no tiene que ir a la ubicación del **intérprete de línea de comandos** o **terminal** para abrirlo. Puede abrirlo simplemente buscando *cmd* en Windows y *terminal* en distribuciones de Linux.

Si te sientes más como un explorador y quieres encontrar la ubicación por tu cuenta, prueba las siguientes rutas:

- Para Windows 10 u 8 en *Inicio-> Sistema de Windows-> Símbolo del sistema* .
- Para Windows 7, Vista o XP en *Inicio-> Todos los programas-> Accesorios-> Símbolo del sistema* .
- Para Mac OS en *Aplicaciones-> Utilidades-> Otro-> Terminal* . Algunos usuarios de Mac prefieren iTerm2, un reemplazo de Terminal, porque es un poco más fácil de usar. Puede encontrar los detalles en el [sitio web oficial de iTerm](https://www.iterm2.com/downloads.html) e instalarlo en su computadora.
- Para Linux: depende de su sistema, pero por lo general, CLI se encuentra en *Aplicaciones-> Accesorios-> Terminal* o en *Aplicaciones-> Sistema-> Terminal* . Si no lo encuentra aquí, simplemente busque en Google cómo acceder a la línea de comandos en su sistema.

Cuando lo abra, verá una ventana negra (o blanca). Si todo está bien, verá el **símbolo del sistema** donde estará escribiendo su comando, un indicador de que su computadora está lista para aceptar comandos. Para Windows, el símbolo del sistema termina con `*>*`, mientras que para Linux y Mac OS, es `$`. Para ejecutar un comando, escríbalo y luego presione Enter.

##### Comandos de aprendizaje

Es hora de aprender algunos comandos importantes. Abramos el intérprete de la línea de comandos y escribamos algunos comandos. Cuando lo abra, verá algo similar al texto a continuación.

```
C:\Users\name>
```

Significa que está en este directorio y puede trabajar en la CLI. Ahora intentemos usarlo.

Imagínese que acaba de despertarse en el suelo de una habitación que no conoce. De hecho, todo te es desconocido, no recuerdas nada, ni siquiera tu nombre. Solo hay una computadora con la terminal abierta y esta guía, por lo que decide que podría ser útil encontrar algo. Entonces, ahora escribirás tu comando junto a esta ruta.

Primero, escriba `whoami`y presione *Entrar* . Desafortunadamente, no le proporcionará una respuesta profunda y satisfactoria sobre quién es realmente, pero verá algo como esto:

```
desktop-qd7c3ju\shanika
```

Bien, ahora sabes tu nombre, uno imaginario, al menos. Como ya pudo adivinar, el `whoami`comando simplemente le devuelve el nombre de usuario que usó en su máquina. Es por eso que ve la salida anterior.

A continuación, escriba `dir`si usa Windows o `ls`si usa Linux / macOS y presione *Entrar* . Ambos comandos devuelven la lista de archivos y carpetas en su directorio actual. Este es uno de los comandos más utilizados por los desarrolladores, especialmente cuando trabajan en servidores.

Si tiene Windows, verá algo similar a la imagen de abajo.

![img](https://ucarecdn.com/7d86c81a-7896-42ed-8c88-1fe7e6e5aa01/)

No hay ningún archivo que sea útil para su situación. ¡Pobre de mí!

¿No hay una orden para escapar? Sí, hay uno. Simplemente escriba `exit`y estará fuera ... del intérprete de línea de comandos porque este comando le permite salir de él. Buenas noticias, ¡acabas de aprender algunos comandos útiles y completar la misión, Shanika! Ahora puedes ser libre.

En el [sitio web de SS64](https://ss64.com/) , puede encontrar una lista completa de comandos para [Windows](https://ss64.com/nt/) , así como para [Linux](https://ss64.com/bash/) y [macOS.](https://ss64.com/osx/)

##### Conclusión

Lo importante que debe saber es que las excelentes GUI no han dejado obsoleta la CLI. Sigue siendo una de las formas más rápidas de hacer su trabajo. Especialmente, si va a ser desarrollador, es muy importante tener un buen conocimiento de los comandos que están disponibles para usted.

En este tema, presentamos la interfaz de línea de comandos: qué es, dónde se puede encontrar y cómo se puede utilizar. Probamos varios comandos, así: `whoami`, `dir`o `ls`, y `exit`. Más adelante aprenderemos los comandos CLI en detalle, ¡pero ahora practiquemos por un tiempo!



## Teoría: parámetros y opciones

Esperamos que ya sepa cómo abrir el intérprete de línea de comandos y ejecutar algunos comandos básicos. Ahora demos un paso más y aprendamos cómo expandir la funcionalidad de los comandos y cómo obtener más información sobre ellos.

##### Comandos con parámetros

A veces, usar un solo comando no es suficiente. Echemos un vistazo al comando `mkdir`, que se usa para crear una nueva carpeta en el directorio actual. Si intenta usarlo como está, obtendrá un error. ¡El terminal necesita saber cómo nombrar una nueva carpeta! Ahí es donde los parámetros son útiles. Un **parámetro** es información adicional que le da al comando. En pocas palabras, los parámetros son variables que pueden tomar los comandos.

Ahora, escriba el comando `mkdir`con un parámetro `papers`. Usamos este comando para crear una carpeta llamada *papeles* :

```bash
C:\users\student> mkdir papers
```

Aunque el directorio actual sigue siendo el mismo, si sigue esta ruta, verá que la nueva carpeta de *papeles* se creó en el directorio de *estudiantes* .



Todos los ejemplos de este tema son para el sistema operativo Windows, pero los comandos enumerados también son relevantes para Linux y macOS. Tenga en cuenta que el separador de ruta en Windows es una barra invertida, pero en Linux / macOS es una barra inclinada.



¡Ahora cambiemos nuestra ubicación y vayamos a la carpeta que acaba de crear! Utilice el `cd`comando con la ruta a la carpeta de *trabajos* como parámetro.

```bash
C:\users\student> cd C:\users\student\papers
C:\users\student\papers>
```

Otro parámetro útil del `cd`comando es `..`. Le permite ir al **directorio principal** *,* el directorio un nivel por encima del actual.

```bash
C:\users\student\papers> cd ..
C:\users\student>
```

También puede volver a la **carpeta raíz** , un directorio de nivel superior en el sistema de archivos. Para volver al directorio raíz, puede usar el `/`parámetro:

```bash
C:\users\student> cd /
C:\
```

Gracias a los comandos y parámetros, ¡parece que hemos vuelto a las raíces! En realidad, sin parámetros, la mayoría de los comandos serían inútiles.

##### Opciones

Si busca en Google algo sobre comandos y una terminal, encontrará el término "opciones". ¡No le tengas miedo! Exploremos brevemente lo que significa.

**Las opciones** , como sugiere el nombre, suelen ser opcionales y se utilizan para cambiar de alguna manera el comportamiento común del comando. Si usa Windows y ya está harto y cansado de explorar la unidad actual, puede cambiarla agregando la `/d`opción a `cd`. No olvide establecer la ruta que desea seguir como parámetro, por ejemplo `F:\Codepen snippets`:

```bash
C:\users\student\Desktop> cd /d F:\Codepen snippets
F:\Codepen snippets>
```

Ahora ves que con opciones y parámetros puedes transformar un simple comando en algo complicado.

En resumen: ¿qué son esencialmente opciones y parámetros? Ambos son solo dos tipos particulares de argumentos. Mientras que una **opción** cambia el comportamiento de un comando, se usa un **parámetro** para asignar información a un comando o una de sus opciones. Una de las diferencias clave entre ellos es que la cantidad de valores posibles en las opciones es limitada y está bloqueada en el código, mientras que con los parámetros los usuarios tienen más libertad ya que no tienen tales limitaciones.

##### Manual de ayuda

Nadie puede recordar todos los comandos, opciones y parámetros existentes. No se preocupe por eso. El `help`comando está ahí para ti. Escríbalo en Windows y obtendrá una lista de comandos disponibles.



Para Linux y macOS, una forma de obtener información sobre los comandos depende del shell que utilice. La forma más sencilla para Linux es una `--help`bandera. También está el `man`comando, abreviatura de *manual* . Se puede utilizar similar al comando de ayuda en Windows: `man mkdir`.



Eso no es todo. El `help`comando puede tomar cualquier comando como parámetro y devolver todas las opciones disponibles. Intentemos. Usaremos el comando más simple que hemos aprendido hasta ahora, el `cd`comando.

```bash
C:\users\student> help cd

Displays the name of or changes the current directory.
 
CD [/D] [drive:][path]
CD [..]

   ..  Specifies that you want to change to the parent directory.

Type CD drive: to display the current directory in the specified drive.
Type CD without parameters to display the current drive and directory.

Use the /D switch to change the current drive in addition to changing the current directory for a drive.

<...>
```

Como puede ver, estos son todos los detalles que necesita saber sobre el `cd`comando. Llamamos a esta descripción el **manual de ayuda** .

Analicemos lo que incluye el manual de ayuda. Primero, establece lo que se supone que debe hacer el comando. Para el `cd`comando, dice, *"Muestra el nombre o cambia el directorio actual".* Luego devuelve todas las combinaciones de ese comando junto con todos los parámetros posibles que puede usar. También puede notar que en Windows los comandos no distinguen entre mayúsculas y minúsculas, a diferencia de Linux y macOS. Veamos el ejemplo del manual:

```bash
CD [/D] [drive:][path]
```

Entonces, el comando anterior tiene tres partes. `CD`es el nombre del comando. `[/D]`es una opción y `[drive:][path]`es un parámetro. Quizás se pregunte qué `[]`significan estos corchetes. Bueno, son solo una *notación* que significa que los parámetros son opcionales para los comandos. No debe agregar estos corchetes cuando use comandos.

Puede leer [este artículo](https://www.lifewire.com/how-to-read-command-syntax-2618082) para Windows o el manual del [comando cat](https://www.hscripts.com/tutorials/linux-commands/cat.html) en Linux / macOS para obtener más información sobre la sintaxis de la línea de comandos y ver los ejemplos.

##### Conclusión

Resumamos lo que hemos aprendido hasta ahora:

- Puede utilizar opciones y parámetros para ampliar la funcionalidad de los comandos.
- Puede pasar diferentes valores con los parámetros.
- Puede obtener una lista completa de comandos usando los comandos `help`y `man`.
- Puede abrir un manual de ayuda para un comando escribiendo `help [command_name]`o `man [command_name]`. Este manual explica cómo usar un comando correctamente y qué opciones y parámetros tiene, si los hubiera.

Aunque puede sentir que el uso de estos comandos ralentizaría el trabajo del desarrollador y que son menos eficientes, le recomendamos que los pruebe. Tienes que acostumbrarte a estos comandos lo antes posible. Una vez que se acostumbre a trabajar con ellos, encontrará que usarlos es mucho más fácil que recurrir a la GUI en muchas ocasiones.

 

# Teoría: Pip

Un hecho asombroso sobre Python es que tiene una comunidad enorme y diversa de contribuyentes. Básicamente, eso significa que hay muchas soluciones para una amplia gama de problemas en el acceso abierto. Este hecho es útil, especialmente cuando está trabajando en sus propios proyectos. Es muy probable que pueda encontrar un paquete adecuado para tareas específicas y usarlo de manera efectiva para satisfacer sus necesidades. Ahora vamos a aprender sobre las herramientas estándar para la gestión de paquetes en Python.

##### Que es pip

En este momento, probablemente se haya familiarizado con la biblioteca estándar de Python. Contiene muchos módulos integrados útiles y debe preinstalarse con su distribución de Python. De hecho, una cosa más que está preinstalada (comenzando con **Python 3.4** ) es el administrador de paquetes estándar llamado **pip** (el acrónimo comúnmente se expande como"Pip instala paquetes").

**Pip** está diseñado tanto para ampliar la funcionalidad de la biblioteca estándar mediante la instalación de paquetes adicionales en su computadora como para ayudarlo a compartir sus propios proyectos y contribuir así al desarrollo de Python.

Ahora **asegurémonos de** tener instalado **pip** . Todo lo que necesita hacer es abrir un símbolo del sistema / terminal y ejecutar esta línea:

```no-highlight
pip --version
```

La salida debe informar su versión actual de pip. Por ejemplo, la última versión es:

```no-highlight
pip 20.0.2
```

En caso de que no esté instalado (o desee actualizarlo), siga estas [instrucciones de instalación](https://pip.pypa.io/en/stable/installing/) específicas para su sistema operativo.



Si su terminal no puede encontrar el `pip`comando, intente utilizarlo `pip3`en su lugar.



##### Capacidades de pip

Dado que **pip** es el instalador recomendado para Python, el comando más obvio y crucial para empezar es `install`. Eche un vistazo a la siguiente línea:

```no-highlight
pip install some_package
```

La instalación es realmente simple. Sin embargo, si está interesado en una determinada versión del paquete, debe especificarla después del nombre del paquete de esta manera:

```no-highlight
pip install some_package==1.1.2
```

O, al menos, defina una versión mínima adecuada:

```no-highlight
pip install "some_package>=1.1.2"
```

Tenga en cuenta que la última expresión debe estar encerrada entre comillas dobles para que el operador de comparación se interprete sin ningún problema.

Otra cosa útil es el `show`comando. Muestra información sobre los paquetes instalados, por ejemplo, su versión, autor, licencia, ubicación o requisitos. A continuación, se muestra un ejemplo general:

```no-highlight
pip show some_package
```

Además, el `list`comando podría ser útil. Enumera todos los paquetes que ha instalado en su computadora en orden alfabético:

```no-highlight
pip list
```

Si imprime el `list`comando con la opción `--outdated`, o simplemente `-o`, obtendrá la lista de paquetes desactualizados junto con las versiones actuales y más recientes disponibles.

```no-highlight
pip list --outdated
```

o con una variante un poco más corta:

```no-highlight
pip list -o
```

Después de ejecutar una de las líneas mencionadas, verá un resultado similar:

```no-highlight
first_package (Current: 2.1.1 Latest: 3.0.1)
second_package (Current: 4.2.1 Latest: 4.2.2)
```

Después de haber descubierto paquetes obsoletos, es posible que desee actualizarlos a la versión más reciente disponible:

```no-highlight
pip install --upgrade some_package
```

Para eliminar un paquete de su computadora, ejecute el `uninstall`comando:

```no-highlight
pip uninstall some_package
```

Al desarrollar su proyecto, puede resultar ventajoso mantener una lista de los paquetes que se instalarán, es decir, las dependencias, en un archivo especial (consulte [Formato de archivo de requisitos](https://pip.pypa.io/en/stable/reference/requirements-file-format/) ). Es conveniente porque puede instalar los paquetes directamente desde él:

```no-highlight
pip install -r requirements.txt
```

Por supuesto, no se supone que usted mismo escriba este archivo enumerando todos los paquetes necesarios. Bastará con ejecutar el siguiente código para obtenerlo:

```no-highlight
pip freeze > requirements.txt
```

Examinemos la línea de arriba en detalle. `freeze`es un comando que se utiliza para obtener todos los paquetes instalados en el formato de requisitos. Entonces, todos los paquetes que había instalado antes de la ejecución del comando y que presumiblemente había usado en algunos proyectos se enumerarían en el archivo llamado"requirements.txt". Además, se especificarían sus versiones exactas (consulte [Especificadores de requisitos](https://pip.pypa.io/en/stable/reference/pip_install/#requirement-specifiers) ).

Considere un resultado de ejemplo del `freeze`comando:

```no-highlight
beautifulsoup4==4.7.1
nltk==3.4.1
numpy==1.16.3
scikit-learn==0.21.1
scipy==1.3.0
```

Lo importante es que en `freeze`realidad enumera **todas** las bibliotecas instaladas, lo que rara vez es necesario y podría considerarse una mala práctica. Por esta razón, le recomendamos que adopte un enfoque más consciente y revise el archivo de *requisitos* obtenido usted mismo.

##### Resumen

En general, hemos aprendido los conceptos básicos para la instalación de paquetes a través de **pip** :

- cómo instalar paquetes (ya sea una versión específica o no específica),
- cómo crear un archivo de *requisitos* y utilizarlo para la instalación,
- cómo obtener información sobre los paquetes instalados,
- y, finalmente, cómo desinstalar paquetes.

Para obtener más detalles, intente consultar la [documentación](https://pip.pypa.io/en/stable/#) o ejecutar el comando `help`.

¡Ahora vamos a practicar para que puedas usar toda esta información en el futuro!



# Teoría: Entorno virtual

##### Introducción

Si pasa mucho tiempo programando, lo más probable es que trabaje con diferentes versiones de Python con bastante frecuencia. Es por eso que necesita instalar paquetes y módulos adicionales fuera de la biblioteca estándar. La mayoría de los paquetes se actualizan con regularidad y existen muchas versiones, antiguas y nuevas. Puede presentar un problema si necesita mantener un proyecto desactualizado, ya que no puede tener dos versiones de un paquete al mismo tiempo. A menos que uses un truco. Para administrar diferentes versiones de paquetes y módulos, existe una solución llamada **[entorno virtual](https://docs.python.org/3/tutorial/venv.html)** .

En términos generales, un **entorno virtual** es un directorio que contiene **una versión particular de Python** y con **paquetes** . Puede crear un entorno virtual independiente para cada proyecto que requiera algo que entre en conflicto con lo que usa habitualmente. Muy conveniente, ¿no?

##### Creando entorno virtual

En este tema, nos referiremos a una herramienta de la biblioteca estándar de Python. Es [venv](https://docs.python.org/3/library/venv.html#module-venv) . Puede interactuar con él a través de la línea de comandos. Para crear un entorno virtual, puede escribir:

```no-highlight
python -m venv new_project
```

o:

```no-highlight
python3 -m venv new_project
```

La **variable de Python** define la versión de Python que le gustaría usar. La `-m`bandera representa el **nombre** del **módulo** .

Hemos creado el `new_project`directorio que contiene un montón de otros directorios junto con el intérprete de Python, la biblioteca estándar y varios archivos de soporte. Cambiemos nuestro directorio actual por conveniencia:

```no-highlight
cd new_project
```

Para empezar a trabajar con nuestro entorno virtual, necesitamos activarlo.

En Windows, puede ejecutar:

```no-highlight
Scripts\activate.bat
```

En Unix o macOS, ejecute:

```no-highlight
source bin/activate
```

Después de esto, verá el entorno virtual en su shell:

![img](https://ucarecdn.com/129e2161-f3fa-4817-8361-1b9f9f867cd3/)

##### Trabajando con paquetes

Puede hacer muchas cosas `pip`en su entorno virtual:

- se puede instalar, actualizar y eliminar paquetes con `pip install`, `pip install --upgrade`y `pip uninstall`, respectivamente:

    ![img](https://ucarecdn.com/c2797a90-08d5-4b8a-ab81-927d83dbbc06/)

- `pip install package_name==package_version` especifica una versión particular de un paquete:

    ![img](https://ucarecdn.com/3c04f152-2957-421d-9697-55ea78b5b4e2/)

- `pip show package_name` muestra la información detallada sobre un paquete, incluida la versión, el resumen, el autor, la ubicación, etc.

    ![img](https://ucarecdn.com/4af23037-2ce2-49ee-a130-96eef3ed4141/)

- `pip list` muestra los paquetes instalados:

    ![img](https://ucarecdn.com/8ec524aa-e0af-4f75-958c-c5b3b8974d27/)

- para crear un `requirements.txt`archivo, use `pip freeze`:

    ![img](https://ucarecdn.com/b345ab1f-ea6b-438a-9ab8-093eaef23d9e/)

Cuando haya terminado con el entorno virtual, desactívelo:

![img](https://ucarecdn.com/14614d9c-2ad2-422f-ae68-4d4e8a9daf22/)

Una vez que haya creado un entorno, se almacenará en su máquina. Puede activar y desactivar en cualquier momento. Si no necesita el entorno, elimine el directorio. Por ejemplo, para Unix o macOS, ejecute:

```no-highlight
rm -r new_project
```

para Windows:

```no-highlight
rmdir new_project
```

Insinuación



##### Otras bibliotecas

Como ya sabe, `venv`es parte de la biblioteca estándar de Python, pero existen bastantes paquetes externos para el mismo propósito. Cada uno tiene sus propias peculiaridades y herramientas adicionales. Intentaremos cubrirlos brevemente:

- [virtualenv](https://pypi.org/project/virtualenv/) es probablemente la biblioteca externa más popular para trabajar con entornos virtuales. Desde hace poco, el subconjunto se ha integrado en el `venv`módulo. `Virtualenv`aborda varios problemas `venv`, como un rendimiento más lento, capacidad de actualización, incapacidad para crear entornos separados para versiones arbitrales de Python y varios otros.
- [pyenv](https://github.com/pyenv/pyenv) es otra biblioteca externa para administrar entornos virtuales. Facilita el trabajo con muchas versiones diferentes de Python y es ideal para probar entre versiones.

##### Resumen

En este tema, hemos aprendido qué es un entorno virtual y cómo trabajar con él usando el `venv`módulo de la biblioteca estándar de Python. Ahora sabe cómo crear, activar, administrar y desactivar paquetes en el entorno. También hemos mencionado otras opciones que pueden ayudarlo a administrar entornos virtuales.



# Teoría: Introducción a Django

**Django** es uno de los frameworks de Python más utilizados en programación web. Cuando navega por tableros en Pinterest, revisa código en Bitbucket o hace comentarios con la ayuda de Disqus, está utilizando productos Django. Puede obtener más información sobre los servicios más conocidos que utilizan Django en este [artículo sobre sitios web en Django](https://www.shuup.com/django/25-of-the-most-popular-python-and-django-websites/) .

El nombre del marco está inspirado en el nombre artístico de un famoso guitarrista de jazz, Django Reinhardt, por lo que los desarrolladores que crearon muchos complementos útiles para el marco llaman a su grupo Jazzband. Al principio, no necesitará todas las herramientas, pero siempre que necesite más, puede encontrarlas en [su cuenta de Github](https://github.com/jazzband) .

El marco de Django proporciona una API para crear plantillas de páginas HTML, hacer conexiones a bases de datos y usar servicios de backend HTTP. Django tiene muchos atajos y utilidades útiles para el desarrollo web en un solo lugar. Para comenzar a trabajar con el marco, elija la versión que usará. Para Django en su versión *ABC* , *AB* significa lanzamiento de características y *C* para lanzamiento de parche. Al elegir una versión adecuada, preste atención a su número de versión de función. Cuando haya terminado de elegir, descargue la última versión del parche para esta versión. Para aprovechar al máximo Django, comience con la última versión.

##### LTS

**LTS** (soporte a largo plazo) es un estándar bien conocido en el desarrollo de software. Significa que los desarrolladores admitirán esta versión del marco durante un período de tiempo prolongado (para Django, generalmente es de 3 años o más). Puede actualizar de forma segura su versión a una versión de parche más reciente sin temor a romper la compatibilidad con el código fuente. Durante este período, todos los errores y pérdidas de seguridad se solucionarán lo antes posible. Por el contrario, las versiones que no son LTS son compatibles solo hasta que salga una versión de función más nueva (tenga en cuenta que los desarrolladores de Django admiten las dos últimas versiones de funciones a la vez).

Por ejemplo, la versión 2.2 de LTS será compatible hasta abril de 2022, aunque ya se encuentran disponibles versiones más nuevas. Por otro lado, el equipo de desarrollo ya no admite una versión 3.0 posterior que no sea LTS.

En nuestros temas, usaremos la versión estable de Django, [versión 3.1](https://docs.djangoproject.com/en/3.1/) de agosto de 2020. La información que proporcionamos se ajustará a todas las versiones superiores a 3.0.

##### Instalación

Seguramente no puede esperar para finalmente instalar Django y ponerse a trabajar. Hay dos formas de instalar el paquete: puede instalarlo globalmente, que es más simple, o obtenerlo en un entorno virtual de Python. Se recomienda crear un entorno virtual para cada nuevo proyecto para que los módulos instalados no entren en conflicto entre sí.

Para instalar Django, necesita un administrador de paquetes de Python **pip** . Django no es diferente de cualquier otro paquete de Python, así que si desea instalarlo en su sistema, asumiendo que ha creado y activado suvenv, ejecute lo siguiente:

```bash
pip install Django==3.1.1
```

##### Compruebe la instalación

Una vez que haya instalado Django, obtendrá el `django-admin`comando en su shell (si ha instalado Django en un entorno virtual, no olvide activarlo). `django-admin`es un ayudante que puede crear un diseño de plantilla para un nuevo proyecto o agregar una aplicación a un proyecto existente. Puede hacerlo todo manualmente, pero es mucho más fácil de usar `django-admin`para este propósito.

Ahora solo necesita verificar la versión del paquete instalado:

```bash
django-admin version
# 3.1.1
```

¡Significa que su instalación fue exitosa y puede comenzar a usar Django! Tienes los elementos básicos para crear tu primer proyecto, ¡así que buena suerte!

# Teoría: Django MVC

Los productos de software complejos tienen su propia arquitectura. Aunque cada ejemplo es único, por lo general todos contienen patrones de diseño comunes. Los patrones son estructuras repetibles y bastante independientes del lenguaje, por lo que familiarizarse con solo uno de ellos significa comprender un montón de aplicaciones que lo comparten. Es básicamente un lenguaje general para expresar ideas, y Model-View-Controller ( **MVC** ) es un patrón particularmente útil para aprender, ya que muchos frameworks populares como Django (Python), Spring (Java) y Ruby On Rails (Ruby) son usándolo.

##### Paradigmas MVC y MTV

La idea principal de MVC es dividir las responsabilidades entre tres componentes.

- **La** parte del **Modelo** sabe todo sobre los datos, cómo acceder a ellos, cómo verificarlos y cómo se relacionan los datos entre sí.
- **La Vista** determina qué datos recibir y cómo mostrarlos al usuario.
- **El controlador** es una capa que reacciona a las acciones del usuario administrando el flujo de datos entre el *modelo* y la *vista* .

Django sigue este paradigma pero tiene diferentes nombres para los componentes correspondientes: Modelo, Plantillas y Vistas ( **MTV** ):

- **El Modelo** ➡ **Modelo:** el Modelo permanece igual que en MVC.
- **La Vista** ➡ **Plantillas:** recibir y mostrar datos al usuario corresponde a *Vista* desde MVC pero se llama *Plantillas* .
- **El Controlador** ➡ **Vistas:** las funciones de manejo lógico que corresponden al *Controlador* de MVC se denominan *Vistas* .

Si desea leer más sobre por qué Django no usa los nombres estándar de MVC, no dude en leer la [sección de preguntas frecuentes al respecto](https://docs.djangoproject.com/en/dev/faq/general/#django-appears-to-be-a-mvc-framework-but-you-call-the-controller-the-view-and-the-view-the-template-how-come-you-don-t-use-the-standard-names) .

Para comprender mejor de qué se encarga cada componente, echemos un vistazo a cómo se realiza una solicitud a un sitio web.

##### Solicitar bajo el capó (the hood)

Cuando un usuario navega por Internet, por su parte, solo cambia enlaces y páginas, pero ¿qué está pasando bajo el capó? Vamos a ver:

1. Un usuario ve un enlace o un botón **:** pertenece al componente **Plantillas** , y dentro, es solo un HTML y CSS que conforman una página web.
2. El usuario hace clic en el botón o enlace y se crea una solicitud.
3. Las **Vistas** reciben la solicitud.
4. Pasa la solicitud a un controlador apropiado.
5. El controlador llama a los métodos **Model** para recuperar objetos del almacenamiento de datos.
6. Finalmente, elige la plantilla Ver para generar una respuesta.
7. Un usuario ve una respuesta.

Cada parte tiene sus propios métodos y clases base en el paquete Django. Debes separar el trabajo con cada componente como lo hacen los desarrolladores de Django: de esta manera otros desarrolladores entenderán tu código y tú entenderás el de ellos. Lo cubriremos con más detalle en los siguientes temas.

##### Conclusión

Ha aprendido el patrón Modelo-Vista-Controlador que se usa en muchos marcos web populares. Está construido sobre los tres componentes:

1. Model está a cargo de los datos;
2. Ver se ocupa de recibir datos y mostrarlos al usuario;
3. El controlador gestiona las interacciones entre las acciones del usuario y los componentes Modelo y Vista.

Django se basa en el mismo paradigma pero tiene diferentes nombres para los componentes: Vista se llama Plantillas y Controlador se llama Vistas, por lo que el patrón se llama Modelo-Plantillas-Vistas. ¡Esperamos que no te confunda demasiado! En nuestros temas, usaremos la terminología MTV.

> Modelo: sabe todo sobre los datos, cómo acceder a ellos, cómo verificarlos y cómo se relacionan los datos entre sí
>
> Vista: Determina qué datos recibir y cómo mostrarlos al usuario
>
> Controlador: Reacciona a las acciones del usuario gestionando el flujo de datos entre los otros dos componentes



# Teoría: estructura del proyecto Django

El proyecto Django es la raíz de todo el código que está escribiendo para el servicio y debe tener al menos una aplicación. Para aislar unidades de código con lógica empresarial diferente, puede crear más aplicaciones. Por ejemplo, un proyecto de *tienda en* línea puede tener el *blog, los autores, el foro* y *las* aplicaciones de *soporte* .



Dividir el código en aplicaciones ayuda a controlar la complejidad a medida que la base de código se hace más grande con el tiempo.



##### Comenzando un nuevo proyecto

La `django-admin`utilidad ayuda a organizar el diseño de su proyecto. Puede crear todos los archivos necesarios manualmente, pero el uso `django-admin`será una buena guía para la estructura común de un proyecto. Tenga en cuenta que las diferentes versiones de Django tienen diferentes diseños predeterminados, y cualquiera que sea la versión que use, intente ceñirse a la estructura provista: hará que su código sea más fácil de mantener.

Continuemos el ejemplo con la tienda online. Para crear el proyecto y la primera aplicación, ejecute el siguiente código en la línea de comando:

```bash
django-admin startproject store
cd store
django-admin startapp blog
```

Una vez ejecutados estos comandos, obtendrá un árbol de archivos completo para el proyecto. La carpeta "tienda" será la raíz de tu sitio y la carpeta interna "blog" será la primera aplicación que creamos. ¿Recuerda el paradigma de MTV? Sus componentes se pueden vincular con los siguientes archivos y carpetas:

```bash
store/
├── blog
    ├── ...
    ├── models.py    # Model
    └── views.py     # Views
├── store
    ├── ...
    └── urls.py      # Views
└── templates        # Templates
```

Ahora echemos un vistazo a cada uno de los componentes con más detalle.

##### Modelo

```bash
store/
└── blog
    └── models.py
```

Como recordará, el componente Modelo está a cargo de los datos de su proyecto. Incluye todas las operaciones de la base de datos con los objetos de negocio del proyecto. Un **objeto comercial** es simplemente una entidad con atributos personalizados; refleja un dato estructurado de su aplicación que desea almacenar de forma permanente o temporal. Por ejemplo, en una aplicación de tienda, puede ser un cliente, un producto y una compra; en un blog, los objetos comerciales pueden ser autores, publicaciones y comentarios.

Para mantener su código claro, debe implementar todas las operaciones con los objetos comerciales en el módulo " *models.py* ". Cuanto más grande se vuelve la base de código, más difícil es mantener todo en un archivo, pero es un buen punto de partida.

Así es como puede verse *models.py* en un proyecto muy simple:

```python
from django.db import models

class Post(models.Model):
    title = models.CharField(max_length=200)
    content = models.TextField()
```

Django tiene una `Model`clase incorporada para crear modelos de base de datos. En el fragmento de arriba, creamos nuestro modelo para publicaciones que tiene dos campos: un título y un contenido.

Django proporciona algunos de los modelos más utilizados desde el primer momento. Cuando comienzas con tus propios proyectos, puedes usar `User`y `Group`modelos de `django.contrib.auth.models`. El `User`es una persona registrada en su servicio web y el `Group`es un conjunto de usuarios. Crearemos algunos de esos y discutiremos cómo trabajar con ellos en detalle más adelante cuando adjuntemos una base de datos al proyecto.

##### Plantillas

```bash
store/
├── blog
    └── templates
        └── blog
            └── index.html
└── templates
    └── base.html
```

Nadie sabrá lo que hace el servicio a menos que tenga alguna forma de interpretación visual. Las plantillas son una representación de su servicio web; es lo que ve el usuario.

Este componente se almacena en plantillas, archivos que admiten los lenguajes de plantilla Django / Jinja2. También pueden incluir contenido con HTML, CSS y JavaScript. El lenguaje de plantilla utiliza la capacidad de usar construcciones similares a las que usa en Python: tiene una sintaxis diferente pero las mismas palabras funcionales. Así es como puede verse el archivo de plantilla más simple:

```html
<!DOCTYPE html>
<title>Example</title>

<h1>First template</h1>

<p>This is a simple html-page without any additional functionality.</p>
```

Sí, es solo un archivo HTML simple. Aprenderá a usar lenguajes de plantilla y agregar contenido en CSS o JavaScript en los temas posteriores.

El directorio de "plantillas" se puede crear para todo el proyecto o para cada aplicación por separado. Por ahora, comencemos con la colocación de plantillas de alto nivel.

##### Puntos de vista

```bash
store/
├── blog
     └── views.py
└── store
      └── urls.py
```

Las plantillas y los modelos son buenos instrumentos, pero algo debería administrar cómo funcionan juntos, y aquí pasamos a la parte de Vistas. Hay dos tipos de archivos: " *views.py* " y " *urls.py* ".

En " *urls.py* ", define el enrutamiento para su servicio. **El enrutamiento** es un proceso de hacer coincidir los enlaces de solicitud con los controladores de vista adecuados. Un **controlador de vista** es una función o una clase que responde a las solicitudes.

Los enlaces de enrutamiento principales deben registrarse manualmente en el archivo " *<nombre_proyecto> / <nombre_proyecto> /urls.py".* Primero, informe al proyecto a qué dirección pertenece nuestra aplicación. Pegue el siguiente código en el `urls.py`archivo del proyecto :

```python
from django.contrib import admin
from django.urls import include, path

urlpatterns = [
    path('', include('NAME_OF_APP.urls')),   # defining our app routings
    path('admin/', admin.site.urls),         # defining admin panel
]
```

Ahora dejemos en claro a la aplicación qué enlaces deben procesarse dentro de ella y dónde se encuentran, en relación con los enlaces principales. Cree un nuevo archivo *"urls.py"* en la carpeta de su aplicación, debe estar en " *<nombre_proyecto> / <a nombre_aplicación> /urls.py"* y pegue el siguiente código:

```python
from django.urls import path
from . import views      # importing all handlers from views.py

urlpatterns = [
    path('', views.example_view, name='NAME_OF_YOUR_VIEW'),
]
```

Los controladores de vista se definen en el archivo " *views.py* " correspondiente . Las funciones de visualización desempeñan un papel de mediador entre las capas Modelo y Plantillas. Creemos el `example_view`del ejemplo anterior:

```python
from django.http import HttpResponse


def example_view(request):
    return HttpResponse("Hello, world")
```

El `HttpResponse`objeto es un objeto especial que almacena todos los datos necesarios para ser devueltos al cliente. Descubrirá más sobre esto en los siguientes temas, por ahora basta con decir que la vista de ejemplo devuelve la línea "Hola mundo".

##### Conclusión

Aprendió a crear un nuevo proyecto con la ayuda `django-admin`y repitió los conceptos básicos del patrón MTV. También debe saber qué archivos de un proyecto están asociados con qué componente e incluso echar un vistazo a su contenido. ¡Esperamos que te ayude a comprender mejor la estructura de los proyectos de Django



```django
django-admin startproject blog---proyecto	
python manage.py startapp books---aplicacion
```



# Teoría: iniciar un proyecto



Ahora que conoce la estructura del proyecto, ¡es hora de crear uno usted mismo! En este tema, finalmente tendrás la oportunidad de hacerlo. El proyecto estará dedicado a Alan Smithee, un prolífico director de cine. Crearemos el proyecto " *smithee* " en sí, la aplicación " *películas* ", una plantilla y un controlador de vista.

##### Estructura del proyecto

Comience ejecutando el siguiente código desde su shell en cualquier directorio que desee:

```bash
django-admin startproject smithee
cd smithee
python3 manage.py startapp movies
cd movies
```

En las aplicaciones Django, las plantillas se almacenan en el directorio "<app_name> / templates / <app_name>". Entonces, para nuestra aplicación actual, crearemos el directorio de "plantillas" dentro de nuestra aplicación "películas", y luego nuevamente el subdirectorio "películas":

```bash
mkdir templates  # note that we're in the "smithee/movies" dir
cd templates
mkdir movies     # and now we're in the "smithee/movies/templates/movies" dir
```

##### Plantillas y vistas

Ahora, agregue el siguiente código al archivo *templates / movies / index.html* :

```django
<!DOCTYPE html>
<title>Movies</title>

<h1>Films by {{ director }}</h1>

<ul>
{% for movie in movies %}
  <li>{{ movie.year }} - {{ movie.title }}</li>
{% endfor %}
</ul>
```

No profundice en el código ahora mismo: discutiremos el lenguaje de plantilla de Django en un tema separado. Pero por ahora, es suficiente que tenga en cuenta que imprimimos las variables entre llaves dobles, y también hacemos un bucle for para revisar la lista de películas. ¿De dónde obtenemos todas estas variables? Pasemos al archivo *movies / views.py* .

Pegue este código en el archivo:

```python
from django.conf import settings
from django.shortcuts import render

my_movies = [
    {
        'title': 'Catchfire',
        'year': 1990,
    },
    {
        'title': 'Mighty Ducks the Movie: The First Face-Off',
        'year': 1997,
    },
    {
        'title': 'Le Zombi de Cap-Rouge',
        'year': 1997,
    },
]


def all_films(request):
    return render(request, 'index.html', {'movies': my_movies, 'director': settings.DIRECTOR})
```

Como puede ver, definimos la lista `my_movies`y luego escribimos una función que renderiza una página. El `render`método básicamente muestra la plantilla al usuario. Nuevamente, lo cubriremos más adelante, pero en este momento, tenga en cuenta que se necesita una solicitud, nuestro archivo de plantilla *index.html* y un diccionario con las variables necesarias para la plantilla. Las claves en este diccionario son lo que llamamos los datos correspondientes en la plantilla, y los valores son los datos reales: la lista de dictados que se iterarán en la plantilla y la cadena con el nombre del director. Tenga en cuenta también que para el director, usamos la variable `settings.DIRECTOR`del módulo *settings.py* . Un poco más adelante veremos cómo definirlo.

##### urls.py

Para que las páginas sean visibles en direcciones específicas, debemos definirlas en los módulos *urls.py.* En Django, generalmente tenemos un módulo *urls.py a* nivel de *proyecto* (ubicado en el directorio raíz del proyecto) y luego un *urls.py* para cada aplicación por separado.

En el nivel de proyecto *urls.py,* definiremos la URL que será una ruta base a la aplicación de películas. Hagámoslo una raíz. Edite *smithee / urls.py de la* siguiente manera:

```python
from django.urls import include, path

urlpatterns = [
    # will look for all paths in movies.urls
    path('', include('movies.urls')),
]
```

Veamos qué hace este código. El método `include('movies.urls')`recopila todas las URL definidas en el *módulo movies.urls* (es decir, el archivo ' *movies / urls.py* '). Y el `path()` método agrega el prefijo especificado (en nuestro caso "", una cadena vacía) a todas las URL recopiladas. Esto es muy útil cuando tenemos toneladas de URL en cada aplicación y no queremos añadir a todos ellos de forma explícita en el nivel de proyecto *urls.py* . El prefijo puede ser el que desee. Por ejemplo, si tiene más de una aplicación con URL similares, puede agregar diferentes prefijos (por ejemplo, 'app1', 'app2', etc.), entonces las URL para app1 se enrutarán como *'/ app1 / some / url / ruta '* .

Además, edite el *archivo smithee / movies / urls.py a* nivel de la aplicación :

```bash
from django.urls import path
from . import views

urlpatterns = [
    path('', views.all_films),
] 
```

Aquí, el `path()`método conecta la ruta "" (raíz) a la vista *all_films* de las vistas.

Juntando todo eso, ahora se puede *acceder a la* plantilla *index.html* en la URL raíz de su aplicación.

##### Conclusión

A partir de ahora, puede crear un proyecto de Django. Ha aprendido qué archivos deben prepararse, dónde están ubicados y con qué parte del proyecto se ocupan. Esperamos que este sencillo ejemplo le proporcione la comprensión necesaria para construir proyectos más complejos en el futuro.



