# Teoría: Lista

En sus programas, a menudo necesita agrupar varios elementos para procesarlos como un solo objeto. Para ello, necesitará utilizar diferentes colecciones. Una de las colecciones más útiles de Python es una **lista** . Es una de las cosas más importantes de Python.

## Crear e imprimir listas

Mire una lista simple que almacena varios nombres de razas de perros:

```python
dog_breeds = ['corgi', 'labrador', 'poodle', 'jack russell']
print(dog_breeds)  # ['corgi', 'labrador', 'poodle', 'jack russell']
```

En la primera línea, usamos corchetes para crear una lista que contiene cuatro elementos y luego la asignamos a la `dog_breeds`variable. En la segunda línea, la lista se imprime a través del nombre de la variable. Todos los elementos se imprimen en el mismo orden en que se almacenaron en la lista porque las listas están **ordenadas** .

Aquí hay otra lista que contiene cinco números enteros:

```python
numbers = [1, 2, 3, 4, 5]
print(numbers)  # [1, 2, 3, 4, 5]
```

Otra forma de crear una lista es invocar la `list`función. Se utiliza para crear una lista a partir de un objeto **iterable** : es decir, un tipo de objeto en el que puede obtener sus elementos uno por uno. El concepto de iterabilidad se explicará en detalle más adelante, pero veamos los ejemplos a continuación:

```python
list_out_of_string = list('danger!')
print(list_out_of_string)  # ['d', 'a', 'n', 'g', 'e', 'r', '!']

list_out_of_integer = list(235)  # TypeError: 'int' object is not iterable
```

Entonces, la `list`función crea una lista que contiene cada elemento del objeto iterable dado. Por ahora, recuerde que una **cadena** es un ejemplo de un objeto **iterable** y un **número entero** es un ejemplo de un objeto **no iterable** . Una **lista en** sí misma también es un objeto **iterable** .

Notemos también la diferencia entre la `list`función y la creación de una lista usando corchetes:

```python
multi_element_list = list('danger!')
print(multi_element_list)  # ['d', 'a', 'n', 'g', 'e', 'r', '!']

single_element_list = ['danger!']
print(single_element_list)  # ['danger!']
```

Los corchetes y la `list`función también se pueden utilizar para crear **listas vacías** que no tienen ningún elemento.

```python
empty_list_1 = list()
empty_list_2 = []
```

En los siguientes temas, consideraremos cómo llenar listas vacías.

## Características de las listas

Las listas pueden almacenar **valores duplicados** tantas veces como sea necesario.

```python
on_off_list = ['on', 'off', 'on', 'off', 'on']
print(on_off_list)  # ['on', 'off', 'on', 'off', 'on']
```

Otro aspecto importante de las listas es que pueden contener **diferentes tipos** de elementos. Por lo tanto, no hay restricciones ni tipos de lista fijos, y puede agregar a su lista cualquier dato que desee, como en el siguiente ejemplo:

```python
different_objects = ['a', 1, 'b', 2]
```

## Longitud de una lista

A veces es necesario saber cuántos elementos hay en una lista. Hay una función incorporada llamada `len`que se puede aplicar a cualquier objeto **iterable** y devuelve simplemente la **longitud** de ese objeto.

Entonces, cuando se aplica a una lista, devuelve el número de elementos en esa lista.

```python
numbers = [1, 2, 3, 4, 5]
print(len(numbers))  # 5

empty_list = list()
print(len(empty_list))  # 0

single_element_list = ['danger!']
print(len(single_element_list))  # 1

multi_elements_list = list('danger!')
print(len(multi_elements_list))  # 7
```

En el ejemplo anterior, puede ver cómo `len()`funciona la función. Nuevamente, preste atención a la diferencia entre `list()`y `[]`según se aplica a las cadenas: es posible que no resulte en lo que esperaba.

## Resumen

Como resumen, observamos que las listas son:

- **ordenado** , es decir, cada elemento tiene una posición fija en una lista;
- **iterable** , es decir, puede obtener sus elementos uno por uno;
- capaz de almacenar **valores duplicados** ;
- capaz de almacenar **diferentes tipos de elementos** .

# Teoría: índices

Hay varios tipos de colecciones para almacenar datos en Python. Las colecciones de elementos ordenados posicionalmente se suelen denominar **secuencias** , y tanto las listas como las cadenas les pertenecen. Cada elemento de una lista, así como cada carácter de una cadena, tiene un **índice** que corresponde a su posición. Los índices se utilizan para acceder a elementos dentro de una secuencia. La indexación se *basa en cero* , por lo que si ve a una persona que cuenta desde cero, debe haber conocido a un programador.

## Índices de elementos

Para acceder a un elemento de una lista por su índice, debe utilizar **corchetes.** Agrega los corchetes después de la lista y, entre ellos, escribe el índice de un elemento que desea obtener.

No se olvide **,** los índices comienzan en 0, por lo que el índice del primer elemento es 0. El índice del último elemento es igual `len(list) - 1`.

Echemos un vistazo al siguiente ejemplo:

```python
colors = ['red', 'green', 'blue']

first_elem = colors[0]   # 'red'
second_elem = colors[1]  # 'green'
third_elem = colors[2]   # 'blue'
```

Las cadenas funcionan de la misma manera:

```python
pet = "cat"

first_char = pet[0]   # 'c'
second_char = pet[1]  # 'a'
third_char = pet[2]   # 't'
```

## Peligros potenciales

Al usar índices, es importante mantenerse dentro del rango de su secuencia: obtendrá un error (llamado `IndexError`) si intenta acceder a un elemento con un índice no existente.

```python
colors = ['red', 'green', 'blue']
pet = "cat"

print(colors[3])  # IndexError: list index out of range
print(pet[3])     # IndexError: string index out of range
```

Hay un obstáculo más en tu camino. Imagina que quieres cambiar uno de los elementos de una lista. Se puede hacer fácilmente:

```python
colors = ['red', 'green', 'blue']

colors[1] = 'white'
print(colors)  # ['red', 'white', 'blue']
```

Sin embargo, cuando se trata de cadenas, dicha reasignación es imposible. Las cadenas, a diferencia de las listas, son inmutables, por lo que no puede modificar su contenido con índices:

```python
pet = "cat"

pet[0] = "b"
# TypeError: 'str' object does not support item assignment
```

No se preocupe, después de un poco de práctica, no encontrará estos errores.

## Índices negativos

La forma más fácil de acceder a los elementos al final de una lista o una cadena es usar **índices negativos** : el menos antes del número cambia tu perspectiva de alguna manera y miras la secuencia desde el final. Entonces, el último elemento de una lista, en este caso, tiene el índice igual a **-1** , y el primer elemento de la lista tiene el índice `-len(list)`(la longitud de la lista).

Por ejemplo:

```python
colors = ['red', 'green', 'blue']

last_elem = colors[-1]    # 'blue'
second_elem = colors[-2]  # 'green'
first_elem = colors[-3]   # 'red'

pet = "cat"

last_char = pet[-1]    # 't'
second_char = pet[-2]  # 'a'
first_char = pet[-3]   # 'c'
```

Como puede ver, funciona igual para listas y cadenas.



Si escribe un índice negativo no existente, también obtendrá `IndexError`. Tenga cuidado con los índices para evitar errores uno por uno en su código.



La siguiente imagen muestra el concepto general de índices en una lista:

![img](https://ucarecdn.com/5485f397-8a2f-4279-b534-a496fe509469/)

## Resumen

En este tema, hemos aprendido qué son los índices positivos y negativos en Python, cómo encontrar elementos en una lista por sus índices y qué errores pueden ocurrir al usarlos. Dado que ha aprendido el concepto de índices, esperamos que a partir de ahora no encuentre dificultades al utilizarlos.

# Teoría: invocar una función

Aunque invocar funciones en Python no se trata de lanzar un hechizo o algo parecido, a veces funciona de maravilla. Empecemos por el concepto. Básicamente, una **función** es un fragmento estructurado de código que podemos querer usar en más de un lugar y más de una vez. Por otro lado, las funciones nos permiten leer mucho mejor tanto nuestro código como el de otra persona. ¿Aún no se han convertido en tus favoritos?

Aquí hay una llamada de función simple:

```
multiply(1, 7)
```

Aquí `multiply`está el nombre de la función y los números entre paréntesis `(1, 7)`son sus **argumentos** . ¿Qué es un argumento? Bueno, es solo un valor, que se usará dentro del cuerpo de la función. ¡Vamos a profundizar más en ello!

## Invocando print ()

Para **llamar** , o **invocar** , **una función** en su programa, simplemente escriba su nombre y agregue paréntesis después. ¡Eso es todo lo que se necesita! Dato curioso: si alguna vez ha escrito una expresión como esta `print("Hello, world!")`, ya sabe un poco sobre funciones. En este pequeño ejemplo, sin embargo, vemos el mensaje"¡Hola Mundo!"entre paréntesis después del nombre de la `print`función. ¿Qué significa? Esta cadena es solo un argumento. Y la mayoría de las veces, las funciones tienen argumentos. En cuanto a la `print`función, también podemos usarla sin ningún argumento o incluso con múltiples argumentos:

```python
print("Hello, world!")
print()
print("Bye,", "then!")
```

Y aquí está la salida:

```python
Hello, world!

Bye, then!
```

Entonces, la primera llamada imprime una cadena, la segunda llamada `print`sin argumentos imprime, de hecho, una línea vacía y la última llamada genera nuestros dos mensajes como una expresión. ¿Le sorprenden estos resultados? Luego, puede aprender cómo `print`funciona la función con más detalle en su [documentación](https://docs.python.org/3/library/functions.html#print) . La documentación de Python contiene todo tipo de información sobre la función de su interés, por ejemplo, qué argumentos espera.

## Funciones integradas

Las funciones pueden hacer la vida más fácil, siempre que uno sea consciente de su existencia. Muchos algoritmos ya están escritos, por lo que no es necesario reinventarlos, excepto quizás con fines educativos. El intérprete de Python tiene una serie de funciones y tipos **integrados** , por lo que siempre están disponibles. Actualmente, el número de [funciones integradas asciende a 69](https://docs.python.org/3/library/functions.html) (en la última versión **Python 3.8** ). Algunos de ellos se utilizan para convertir el **tipo de objeto** , por ejemplo, `str()`devuelve una cadena, `int()`devuelve un entero, `float()`devuelve un número de punto flotante. Otros se ocupan de los **números** : puedes `round()`ellos y `sum()`ellos, encuentra el mínimo `min()`o el máximo`max()`. Otros más nos dan información sobre el objeto: su `type()`longitud `len()`. ¡Considérelos en acción!

En el siguiente ejemplo, `len()`cuenta el número de caracteres de la cadena (lo mismo ocurre con cualquier **secuencia** ).

```python
number = "111"

# finding the length of an object
print(len(number))  # 3
```

Luego declaramos las variables `integer`y `float_number`y escribir su suma en `my_sum`. Por cierto, la `sum()`función también se ocupa de secuencias.

```python
# converting types
integer = int(number)
float_number = float(number)
print(str(float_number))  # "111.0"

# adding and rounding numbers
my_sum = sum((integer, float_number))
```

El resultado es un número de punto flotante, que se aclara después de la impresión `my_sum`.

```python
print(my_sum)  # 222.0
print(round(my_sum))  # 222
```

Además, puede ver cómo encontrar los valores mínimo y máximo: el número más pequeño es igual a 111 y el mayor numero 222.0 pertenece a los flotadores.

```python
# finding the minimum and the maximum
print(min(integer, float_number))  # 111
print(type(max(integer, float_number, my_sum)))  # <class 'float'>
```

Hay mucho más por explorar, pero resumámoslo.

## Resumen

La belleza de las funciones es que podemos usarlas sin tener una idea clara de su estructura interna y cómo se las arreglan para realizar lo que necesitamos. Pero si desea darle un buen uso a una función, asegúrese de verificar su documentación o intente invocar la función especial `help()`con el nombre de la función en cuestión entre paréntesis. Puede ser necesario si, por ejemplo, la función no devuelve ningún valor, escribe los datos procesados en un archivo o imprime la salida en la pantalla.

Hagamos un breve resumen:

- Las funciones están destinadas a ser reutilizables, lo que significa que podemos aplicarlas varias veces con diferentes argumentos,
- para llamar a una función escriba su nombre seguido de paréntesis y coloque los argumentos dentro,
- normalmente, una función tiene documentación, lo que a veces puede ser de gran ayuda.