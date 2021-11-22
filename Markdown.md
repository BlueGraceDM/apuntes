## Teoría: Markdown 

##### Introducción

**Markdown** es un lenguaje de marcado ligero que le permite dar formato a texto sin formato. Con él puede agregar títulos en artículos, hacer palabras en negrita o cursiva, insertar listas y mucho más. Al mismo tiempo, el texto original será comprensible y fácilmente legible para las personas. Usar Markdown es una buena idea para diseñar texto corto y simple, como publicaciones en mensajeros y foros, archivos README. En este tema, aprenderá la sintaxis básica de Markdown y dónde usarla.

##### Encabezados

Para dividir el texto en secciones y organizar mejor la jerarquía dentro del documento, utilizamos encabezados. Ayudan a los lectores a navegar por el texto más rápidamente.

Para hacer un encabezado en Markdown, simplemente escriba hash () delante del texto. Un símbolo significa un encabezado de primer nivel, dos símbolos significan un encabezado de segundo nivel, y así sucesivamente. Echemos un vistazo a algunos ejemplos claros de cómo crear encabezados.`#`

| **Descuento**     | **Resultado**                                                |
| ----------------- | ------------------------------------------------------------ |
| ### Sistema Solar | ![img](https://ucarecdn.com/a245c87d-5fc8-4bf6-bb1b-3822c4062cd5/) |
| ## Planetas       | ![img](https://ucarecdn.com/7d91e9a8-03c1-4092-8115-935c12f8175f/) |
| # Júpiter         | ![img](https://ucarecdn.com/36063a75-88bb-4597-adf8-e70449ed0e06/) |

Hay un total de *seis niveles* de rúbricas. Esto es más que suficiente para fines prácticos, la mayoría de los documentos usan dos o tres niveles. Recuerde usar el encabezado de primer nivel solo una vez. Siga la jerarquía: se recomienda que los encabezados de segundo nivel se usen solo después de los encabezados de primer nivel.

##### Estilo de fuente

Con Markdown puedes cambiar el estilo de fuente. Por ejemplo, para resaltar el texto en negrita, agregue dos asteriscos () antes y después de este texto. El tipo de negrita se usa cuando desea enfatizar ciertas palabras o frases. Por ejemplo, puede resaltar términos o nombres importantes de algo con él.`**`

| **Descuento**                                  | **Resultado**                                  |
| ---------------------------------------------- | ---------------------------------------------- |
| **Júpiter** es el quinto planeta desde el Sol. | **Júpiter** es el quinto planeta desde el Sol. |

También puede llamar la atención de los lectores sobre las palabras mediante el uso de cursiva. Para ello, agregue un solo asterisco () antes y después del texto.`*`

| **Descuento**                                                | **Resultado**                                                |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| * Galileo Galilei * descubrió las cuatro lunas más grandes de Júpiter. | *Galileo Galilei* descubrió las cuatro lunas más grandes de Júpiter. |

Puede combinar estas características para dar formato al texto.

##### Listas

La sintaxis de Markdown también le permite crear listas ordenadas / desordenadas y anidarlas entre sí. Las listas ordenadas están numeradas y las listas no ordenadas están marcadas.

Para las listas **ordenadas,** todo lo que necesita hacer es agregar posiciones con números seguidos de puntos delante del texto. Para crear **una lista desordenada,**debe agregar el símbolo delante del texto que se convertirá en un elemento de su lista desordenada. Para anidar una lista en otra, agregue espacios como en el ejemplo siguiente.`-`

| **Descuento**                                                | **Resultado**                                                |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| `- Moons of Jupiter - Io - Europa - and so on- Spacecrafts in flyby missions 1. Pioneer 10 2. Pioneer 11 3. and others` | ![img](https://ucarecdn.com/7efdc7aa-e388-479a-991a-aa87b988526b/-/crop/244x216/0,3/-/preview/) |

##### Presupuestos

Si necesita citar a alguien, Markdown también puede ayudarlo con eso. Para convertir un texto en una cita, coloque un corchete angular () delante de él.`>`

| **Descuento**                                         | **Resultado**                                                |
| ----------------------------------------------------- | ------------------------------------------------------------ |
| > Júpiter es el planeta más grande del Sistema Solar. | ![img](https://ucarecdn.com/b397692c-f5b6-4c68-973f-be62283e5612/-/crop/389x63/568,745/-/preview/) |

Esta característica hace que Markdown sea conveniente en sitios web que permiten a las personas comunicarse entre sí.

##### Conclusión

Markdown ofrece muchas opciones para formatear información textual, acabamos de presentarle algunas de ellas. Puede encontrar más información sobre la sintaxis de Markdown visitando el sitio [de markdownguide.org.](https://www.markdownguide.org/basic-syntax)

Markdown se usa a menudo para escribir blogs, documentación y descripciones de proyectos en *Github* y *Gitlab.* La usabilidad y simplicidad del diseño del texto fueron apreciadas por el sitio *Stack Overflow,* donde los programadores pueden hacer preguntas e intercambiar experiencias. La sintaxis de Markdown se utiliza en productos que ayudan a organizar el trabajo en equipo en proyectos, como *Trello* o *Jira.* Ahora, pasemos a las tareas.

# John Lennon

or ***John Winston Ono Lennon*** was one of *The Beatles*.
Here are the songs he wrote I like the most:

- Imagine
- Norwegian Wood
- Come Together
- In My Life
- ~~Hey Jude~~ (that was *McCartney*)

## Teoría: Programa con números

Los programas en los que no hay nada que calcular son bastante raros. Por lo tanto, aprender a programar con números nunca es una mala idea. Una habilidad aún más valiosa que estamos a punto de aprender es el procesamiento de datos de usuarios. Con su ayuda, puede crear aplicaciones interactivas y, con mucho, más flexibles. ¡Así que comencemos!

##### Lectura de números de la entrada del usuario

Dado que se ha familiarizado con la función en Python, no es nuevo para usted que los datos pasados a esta función se traten como una **cadena.** Pero, ¿cómo debemos lidiar con los valores numéricos? Como regla general, se convierten explícitamente a los tipos numéricos correspondientes:`input()`

```python
integer = int(input())
floating_point = float(input())
```

Preste atención a las mejores prácticas actuales: es crucial no nombrar sus variables como tipos integrados (por ejemplo, **float** o **int).** Además, debemos tener en cuenta los errores del usuario: si un usuario escribe una entrada inexacta, por ejemplo, una cadena '' en lugar de un número, se producirá una. Por el momento, no nos centraremos en ello; pero no se preocupe, hay más información sobre errores disponible en un tema dedicado. Ahora, considere un ejemplo más detallado y pragmático de manejo de entradas numéricas.two2`ValueError`

##### Millas aéreas gratuitas

Imagine que tiene una tarjeta de crédito con un programa de bonificación de millas aéreas gratuitas (o tal vez ya tenga una). Como usuario, se espera que ingrese la cantidad de dinero que gasta en promedio de esta tarjeta por mes. Supongamos que el programa de bonificación le brinda 2 millas aéreas gratuitas por cada dólar que gaste. Aquí hay un programa simple para averiguar cuándo puede viajar a algún lugar de forma gratuita:

```python
# the average amount of money per month
money = int(input("How much money do you spend per month: "))

# the number of miles per unit of money
n_miles = 2

# earned miles
miles_per_month = money * n_miles

# the distance between London and Paris
distance = 215

# how many months do you need to get
# a free trip from London to Paris and back
print(distance * 2 / miles_per_month)
```

Este programa calculará cuántos meses se tarda en recorrer la distancia seleccionada y de regreso.



Aunque se recomienda escribir mensajes para los usuarios en la función, evítelos en nuestros desafíos de programación educativa, de lo contrario su código puede no pasar nuestras pruebas.`input()`



##### Formas avanzadas de asignación

Cada vez que se utiliza un signo igual, en realidad se asigna algún valor a un nombre. Por esa razón, se conoce típicamente como un **operador de asignación.** Mientras tanto, hay otros operadores de asignación que puede usar en Python. También se les denomina **operadores de asignación compuesta,**ya que realizan una operación aritmética y asignación en un solo paso. Echa un vistazo al fragmento de código a continuación:`=``=`

```python
# simple assignment
number = 10
number = number + 1  # 11
```

Este código es equivalente al siguiente:

```python
# compound assignment
number = 10
number += 1  # 11
```

Se puede ver claramente en el ejemplo que la segunda pieza de código es más concisa (ya que no repite el nombre de la variable).

Naturalmente, existen formas de asignación similares para el resto de operaciones aritméticas: , , , , , . Dada la oportunidad, utilítelos para ahorrar tiempo y esfuerzo.`-=``*=``/=``//=``%=``**=`

Una posible aplicación de la asignación de compuestos viene a continuación.

##### Variable de contador

En programación, los bucles se utilizan junto con variables especiales **llamadas contadores.** Un **contador** cuenta cuántas veces se ejecuta un código en particular. También se deduce que los contadores deben ser enteros. Ahora vamos al grano: puede usar los operadores y aumentar o disminuir el contador respectivamente.`+=``-=`

Considere este ejemplo en el que un usuario determina el valor en el que se incrementa el contador:

```python
counter = 1
step = int(input())  # let it be 3
counter += step
print(counter)  # it should be 4
```

En caso de que solo necesite enteros no negativos del usuario (¡después de todo, estamos aumentando el contador!), Puede evitar entradas incorrectas utilizando la función. Es una función integrada de Python que devuelve el valor absoluto de un número (es decir, el valor independientemente de su signo). Reajustemos un poco nuestro último programa:`abs()`

```python
counter = 1
step = abs(int(input()))  # user types -3
counter += step
print(counter)  # it's still 4
```

Como ves, gracias a la función conseguimos un número positivo.`abs()`



Por ahora, está bien que no sepa mucho sobre los detalles mencionados de **errores,** **bucles** y **funciones integradas** en Python. Nos vamos a poner al día y nos aseguraremos de que conozca estos temas de manera integral. ¡Sigue aprendiendo!



##### Conclusión

Por lo tanto, hemos arrojado algo de luz sobre nuevos detalles sobre la aritmética entera y el procesamiento de entradas numéricas en Python. Siéntase libre de usarlos en sus proyectos futuros.

```python
425
5
n = int(input())
print(str(n)[-1])
```

