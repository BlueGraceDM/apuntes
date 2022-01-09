## Teoría: Invocar una función

A pesar de que invocar funciones en Python no se trata de lanzar un hechizo o similar, a veces funciona de maravilla. Comencemos con el concepto. Básicamente, una **función** es un fragmento estructurado de código que podemos querer usar en más de un lugar y más de una vez. Por otra parte, las funciones nos permiten leer mucho mejor tanto nuestro código como el de otra persona. ¿Aún no se han convertido en tus favoritos?

Aquí hay una simple llamada a la función:

```
multiply(1, 7)
```

Aquí está el nombre de la función, y los números entre paréntesis son sus **argumentos.** ¿Qué es un argumento? Bueno, es solo un valor, que se usará dentro del cuerpo de la función. ¡Profundicemos en ello!`multiply``(1, 7)`

##### Invocar print()

Para **llamar**o **invocar** **una función** en su programa, simplemente escriba su nombre y agregue paréntesis después de él. ¡Eso es todo lo que se necesita! Dato curioso: si alguna vez has escrito una expresión como esta, ya sabes un poco sobre funciones. En este pequeño ejemplo, sin embargo, vemos el mensaje entre paréntesis después del nombre de la función. ¿Qué significa? Esta cadena es solo un argumento. Y la mayoría de las veces, las funciones tienen argumentos. En cuanto a la función, también podemos usarla sin ningún argumento o incluso con múltiples argumentos:`print("Hello, world!")`"Hello, world!"`print``print`

```python
print("Hello, world!")
print()
print("Bye,", "then!")
```

Y aquí está el resultado:

```python
Hello, world!

Bye, then!
```

Entonces, la primera llamada imprime una cadena, la segunda llamada de sin argumentos imprime, de hecho, una línea vacía, y la última llamada genera nuestros dos mensajes como una expresión. ¿Te sorprenden estos resultados? Luego puede aprender cómo funciona la función con más detalle de su [documentación.](https://docs.python.org/3/library/functions.html#print) La documentación de Python contiene todo tipo de información sobre la función de su interés, por ejemplo, qué argumentos espera.`print``print`

##### Funciones integradas

Las funciones pueden hacer la vida más fácil, siempre que uno sea consciente de su existencia. Muchos algoritmos ya están escritos, por lo que no hay necesidad de reinvención, excepto tal vez con fines educativos. El intérprete de Python tiene una serie de funciones y tipos **integrados,** por lo que siempre están disponibles. Actualmente, el número de [funciones integradas asciende a 69](https://docs.python.org/3/library/functions.html) (en la última versión **Python 3.8).** Algunos de ellos se utilizan para convertir el **tipo de objeto,**por ejemplo, devuelve una cadena, devuelve un entero, devuelve un número de coma flotante. Otros se ocupan **de los números:**puedes ellos y ellos, encontrar el mínimo o el máximo. Otros nos dan información sobre el objeto: su longitud o longitud. ¡Considerémoslos en acción!`str()``int()``float()``round()``sum()``min()``max()``type()``len()`

En el siguiente ejemplo, cuenta el número de caracteres de la cadena (lo mismo ocurre con cualquier **secuencia).**`len()`

```python
number = "111"

# finding the length of an object
print(len(number))  # 3
```

Luego declaramos las variables y escribimos su suma en . Por cierto, la función también se ocupa de las secuencias.`integer``float_number``my_sum``sum()`

```python
# converting types
integer = int(number)
float_number = float(number)
print(str(float_number))  # "111.0"

# adding and rounding numbers
my_sum = sum((integer, float_number))
```

El resultado es un número de coma flotante, que se vuelve claro después de imprimir.`my_sum`

```python
print(my_sum)  # 222.0
print(round(my_sum))  # 222
```

Además, puede ver cómo encontrar los valores mínimos y máximos: el número más pequeño es igual y el número más grande pertenece a los flotadores. 111222.0

```python
# finding the minimum and the maximum
print(min(integer, float_number))  # 111
print(type(max(integer, float_number, my_sum)))  # <class 'float'>
```

Hay mucho más que explorar, pero vamos a resumirlo.

##### Resumen

La belleza de las funciones es que podemos usarlas sin una visión clara de su estructura interna y cómo logran realizar lo que necesitamos. Pero si desea hacer un buen uso de una función, asegúrese de verificar su documentación o intente invocar la función especial con el nombre de la función en cuestión envuelto entre paréntesis. Puede ser necesario si, por ejemplo, la función no devuelve ningún valor, escribe datos procesados en un archivo o imprime la salida en la pantalla.`help()`

Hagamos un breve resumen:

- las funciones están destinadas a ser reutilizables, lo que significa que somos libres de aplicarlo varias veces con diferentes argumentos,
- para llamar a una función, escriba su nombre seguido de paréntesis y coloque los argumentos dentro,
- normalmente, una función tiene documentación, que a veces puede ser de gran ayuda.

## Theory: Markdown: extended elements **![img](https://hyperskill.azureedge.net/static/img/non-track.85927cc6.svg)**

 8 minutes0 / 0 problems solved

Skip this topicStart practicing

**319** users solved this topic. Latest completion was **about 17 hours ago**.

You're probably familiar with the basic Markdown syntax, but page layout would not be complete without such elements as links, images, code, and tables. Knowing how to add them will help you improve the structure of your text, share links to external resources, better convey the essence and content of the text with a suitable image, and show some code snippets to comment on. This topic is aimed at teaching you how to do all the above. So, let's get to it.

##### Links

Suppose you start making your document using Markdown, but it turns out that you need to provide links to external resources. Of course, you don't want to have them just out in the open. You want to send users to an external resource when they click on some piece of text. For this Markdown allows you to format text as links. This is very useful when you need to refer to some external information. You can create links according to the following template:

```markdown
[Link text](URL)
```

Inside square brackets you need to specify the text of the link and the URL address between parentheses. Do not separate the different types of brackets with space or other characters, otherwise you will not be able to create a link. Take a look at the example below:

| **Markdown**                 | **Result**                    |
| ---------------------------- | ----------------------------- |
| [Github](https://github.com) | [Github](https://github.com/) |

##### Images

When you want to add variety to your text, enhance its readability, or explain important details, adding images is often a good solution. Adding images of diagrams, charts, and graphs will help you better present your ideas. Photos from your trips will diversify your travel blog and generate additional interest from the readers. Illustrations will help you better present your product.

Markdown has an option to add images to the document. You can do it the following way:

```markdown
![Alternative text](URL)
```

First, write the exclamation point, then add an alternative text for an image in square brackets, and, finally, add the URL of the image in parentheses.

**The alternative text** is a text description of the image that will be displayed if the user's browser for some reason cannot load it. Below you can see what adding an image to Markdown looks like:

| **Markdown**                        | **Result**                                                   |
| ----------------------------------- | ------------------------------------------------------------ |
| ![Github logo](img/github_logo.png) | ![img](https://ucarecdn.com/d5d6a253-4099-40ab-b5aa-0ea07ca31827/) |

##### Code

Sometimes you might need to visually separate the code from the rest of the text. This could be in correspondence with a colleague, chatting on a forum, or it can even happen during the writing of the project description. Situations are different, but one thing remains the same: there is a need to somehow indicate that a certain part of the text is code. Markdown provides you with the tools for this.

When you need to show that part of the text in a sentence is code, enclose it in backticks (```). Such code snippets will stand out from the rest of the text with a background color and a monospaced font.

| **Markdown**                                            | **Result**                                              |
| ------------------------------------------------------- | ------------------------------------------------------- |
| The `<html>` tag indicates that it is an HTML document. | The `<html>` tag indicates that it is an HTML document. |

You can also create blocks of code in Markdown. This is useful when you need to insert several lines of code at once. For example, to quote program source code or demonstrate your code snippet.

To create code blocks, you will need to start each line of the code with an indentation of *four spaces* or *one tab*.

| **Markdown**                               | **Result**                                  |
| ------------------------------------------ | ------------------------------------------- |
| <html> <head></head> <body></body> </html> | `<html> <head></head> <body></body></html>` |

The text will look like a formatted code block until you write a line without the four-space indentation.

##### Tables

If your document contains a lot of the same type of data, you can try to structure it and present it in a form that's convenient for your readers. For example, you can organize data into rows and columns. Markdown has tables for this. Tables can be useful if you need to present data for analysis in your document.

In Markdown, you can create a table using pipes (`|`) to separate columns and hyphens (`-`) to specify the column's header. The finished table will look something like this:

| **Markdown**                                                 | **Result**                                                   |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| `| Name       | Age || ---------------- | --- || Laura Heath   | 34 || Gilbert Simmons | 22 || William Perkins | 40 |` | **Name****Age**Laura Heath34Gilbert Simmons22William Perkins40 |

##### Conclusion

Markdown is a markup language. It was developed to make it easier to write and read markup code, which in turn makes it easier to understand. In this topic you've learned how to create tables in Markdown, how to add links and images, and how to format text as code. Also, you've read about the situations in which these elements are commonly used. Let's practice what you've learned so far.



##### Description

Before we start implementing the project, we need to think about the functionality. Remember [the Markdown Guide](https://www.markdownguide.org/basic-syntax/) from the previous stage? Let's go through it one more time and recall the basic features:

- plain — a normal text without any formatting
- **bold**/*italic —* self-explanatory
- inline-code — for example, `python editor.py`
- link — for example, [google.com](https://google.com/)
- header — look at the header of this stage.
- unordered-list — this very list is an example of an unordered list
- ordered-list — a list with enumerated elements
- new-line — switches to the next line

In this stage, you need to implement these features in your editor. Let's also add special commands to our tool:

- `!help` — prints available syntax commands.
- `!done` — saves the markdown and exits the app.

Let's do it!

##### Objectives

Implement the help function that will print available syntax commands, which we have indicated above, as well as the special commands. When called, it should print the following:

```no-highlight
Available formatters: plain bold italic header link inline-code ordered-list unordered-list new-line
Special commands: !help !done
```

Implement the exit function that exits the editor without saving.

Ask a user for input:

```
Choose a formatter:
```

`!help` prints the help page, `!done` exits the editor.

If the input contains one of the correct formatters (plain, bold, italic, etc.), ask for the input once again.

If the input contains no formatters or unknown command is sent, print the following message and ask for input again: `Unknown formatting type or command`

##### Examples

The greater-than symbol followed by a space (`> `) represents the user input. Note that it's not part of the input.

**Example 1:**

```no-highlight
	Choose a formatter: > non-existing-formatter
Unknown formatting type or command
Choose a formatter: > !help
Available formatters: plain bold italic header link inline-code ordered-list unordered-list new-line
Special commands: !help !done
Choose a formatter: > header
Choose a formatter: > ordered-list
Choose a formatter: > !done

```

## [Lógica booleana](https://hyperskill.org/learn/step/6025) Exclusivo o 

 Duro 

**21453** usuarios resolvieron este problema. La última finalización fue **hace aproximadamente 5 horas**.



¡Uau! Este problema es un poco complicado. Si estás listo para ponerte tu gorra de pensamiento, ¡prepárate y buena suerte! De lo contrario, puede omitirlo por ahora y regresar en cualquier momento más tarde.



**Exclusive OR**, o simplemente **XOR**, es una operación lógica binaria. Devuelve sólo si ambos argumentos son diferentes (uno es , el otro es ).`True``True``False`

Aquí hay una tabla con salidas XOR para diferentes valores de las variables **a** y **b:**

| `**a**`   | `**b**`   | `**XOR**`     | **Descripción**                                            |
| --------- | --------- | ------------- | ---------------------------------------------------------- |
| Verdadero | Verdadero | **Falso**     | El resultado es porque los operandos son los mismos`False` |
| Verdadero | Falso     | **Verdadero** | El resultado es porque los operandos son diferentes`True`  |
| Falso     | Verdadero | **Verdadero** | El resultado es porque los operandos son diferentes`True`  |
| Falso     | Falso     | **Falso**     | El resultado es porque los operandos son los mismos`False` |

En las opciones a continuación, verá varias expresiones. Dependiendo de los valores de las variables booleanas **a** y **b,**los resultados de las expresiones son diferentes. Seleccionamos aquellos de ellos, cuyo resultado es el mismo que si aplicáramos **XOR** **a** a y **b.** Significa que debe calcular qué valores toma cada expresión en cuatro casos (como en la tabla anterior) y asegurarse de que sean los mismos que la expresión que ***\*tomaría una XOR\** b** en el mismo caso.



```python
```

