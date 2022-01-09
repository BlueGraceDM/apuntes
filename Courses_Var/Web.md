# HTML

Es un lenguaje formado de etiquetas dependiendo de su función

El formato preliminar de un ***HTML*** es:

```html
<!DOCTYPE html> <!--codificacion de archivo-->
<html lang="en"> <!--etiqueta principal / idioma-->
<head>
    <meta charset="UTF-8"> <!--codificación-->
    <title>Title</title> <!--titulo-->
</head>
<body>
			<!--cuerpo-->
</body>
</html>
```

### ETIQUETAS GENERALES

```html
<h1>Encabezados principal</h1>
<h2>Encabezado secundario</h2>
<p>Parrafo<br>Salto de linea</p>
<hr> crea una linea diagonal
<pre>Texto preformateado, se resperan los saltos y espacios como ''' en py</pre>
```

### FORMATO DE TEXTO

```html
<p>My<b>textos en negrita</b></p>
<strong>Textos importantes en negrita</strong>
<i>Texto en cursiva</i>
<em>Texto importante en cursiva</em>
<u>Texto subrayado</u>
<small>texto pequeño</small>
<code>Insertar codigo de programación</code>
	
```

### ETIQUETAS DE CITAS

```html
    <h1>Citas</h1>
    <hr>

    <p>Mi parrafo de mi página</p>
    <blockquote site="http://oregon.com/html">
        Cita de fuente externa
    </blockquote>

    <hr>
    <p>Otro parrafo de mi página</p>
        <q>Una cita breve</q>
	<hr>
    <p>Tercer parrafo de cita</p>
    <abbr title="Hyper Text Markup Language">HTML</abbr>
    <hr>
    <p>Cuarto parrafo de cita</p>
    <address>
        Cita para contacto
        podemos poner todos los datos
    </address>
    <hr>
    <p><cite>Curso de fotografía</cite> Centro aprendiendo. Hecho 2021</p>

```

## LISTAS

### LISTAS DESORDENADAS

```html
  <h1> LISTAS </h1>

  <h2>LISTAS DESORDENADAS</h2>
  <ul> <!--Muestra que son listas desordenadas-->
      <li> Elemento 01 </li><!--Elemento de lista-->
      <li> Elemento 02 </li>
      <ul> <!--Muestra que son listas desordenadas-->
        <li> Elemento 01 </li><!--Elemento de lista-->
        <li> Elemento 02 </li>
        <!--lista dentro de otra-->
      </ul>
  </ul>
```



```html
    <h2>LISTAS ORDENADAS</h2>
    <ol> <!--Listas enumeradas-->
        <li>Elemento 01</li>
        <ol>
        <li> Subelemento 01 </li>
        </ol>
    </ol>
```

### TABLAS

```html
<h1>TABLAS</h1>
    <table border="2"> <!--borde-->
        <tr>
            <th>Nombre</th> <!--Encabezado-->
            <th>Correo</th>
            <th>Telefono</th>
        </tr><!--filas-->
        <tr>
            <td>Aiza</td><!--información-->
            <td>correo@correo.com</td>
            <td>55261537</td>
        </tr>
        <tr>
            <td>Fernanda</td>
            <td>correo2@correo.com</td>
            <td>55897823</td>
        </tr>
    </table>
```

### ENLACES

```html
    <h1>ENLACES</h1>
    <!-- _self abre en la misma pestaña
         _blank abre en otra pestaña-->
    <a href="www.pagina.com" target="_self">Ir a Pagina </a>
    <h1>ENLACES</h1>
    <p> Inicio de parrafo
    <a href="www.pagina2.com" target="_blank">Ir a Pagina 2</a>
    fin del parrafo
    </p>
    <a href="nombre_archivo.html"></a>
```

### IMAGENES

```html
<body>
    <h1>ESTRELLA</h1>
    <hr>
    <img src="ruta/deimagen.jpg" alt="texto_alternativo" width="100" height="100">
</body>
```

### VIDEO

```html
    <h1>Video</h1>
    <video width="320" height="280" controls>
        <source src="ruta/video.mp4" type="video/mp4">
    </video>
    <br>
    <video width="320" height="280" autoplay>
        <source src="ruta/video.mp4" type="video/mp4">
    </video>
```

### AUDIO

```html
<h1>AUDIO</h1>
    <audio controls>
        <source src="ruta/audio.mp3" type="audio/mp3">
    </audio>
```

### YOUTUBE VIDEO

```html
<h1>YOUTUBE</h1>
    <iframe src="ruta/video" width="320" height="240" frameborder="0"></iframe>

```



## FORMULARIOS

### TIPOS DE CAMPOS DE TEXTO (INPUT)

```html
    <h1>CAMPOS DE TEXTO</h1>

    <form action="">
        <label for="numero:">Numero</label><!--Campo números-->
<!--para asociar se debe poner después de for un nombre como atributo
igual debe estar en input-->
        <input type="number" id="numero", name="numero">
<!--Si queremos ingresar texto no va a permitir-->
        <br>
        <label for="nombre">Nombre</label><!--Campo Texto-->
        <input type="text" id="nombre" name="nombre">
        <br>
        <label for="email">Email:</label><!--Campo Email-->
        <input type="email" id="email" name="email">
        <br>
        <label for="pass">Password:</label><!--Campo para password-->
        <input type="password" id="pass" name="pass"><!--Oculta con *-->
        <br>
        <label for="button"></label>
        <input type="submit" value="Enviar">
<!--También hay para checkbox, color, date, datetime, datetime-local,-->
<!--file-->
    </form>
```



### ATRIBUTOS DE INPUT

|   VALOR   | ATRIBUTO                       |
| :-------: | :----------------------------- |
|   type    | Tipo de input                  |
|   name    | Nombre del input               |
|    id     | Para unir con label            |
|   value   | Valor por defecto              |
| readonly  | Solo lectura                   |
| disabled  | Deshabilitado                  |
|   size    | Tamaño de input                |
| maxLength | Cantidad de caracteres         |
| required  | Campo requerido                |
| autofocus | El puntero enfoca en ese input |



## NOTAS MISCELÁNEAS

### TODO

```html
<!--todo usamos esta etiqueta para dejar notas en el modulo TODO-->
```

