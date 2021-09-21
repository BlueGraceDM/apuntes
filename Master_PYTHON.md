

___

---

# NOTAS MASTER EN PYTHON

---
___

## FUNCION PRINCIPAL

> Desde aqui empieza la funcion principal

 ``` python
 # Arriba de la funcion principal se ponen las demas fuciones y vque vamos a usar para construirla
 # Funcion principal
 def main():
     pass
 # Punto de entrada de la aplicacion
 if __name__=='__main__':
     main()
 ```



## LISTAS

---
### Metodos

|**Método**|**Acción**|**Formula**|
|:---|:---:|---:|
|append|agrega un item hasta el final de la lista|list.append(*x*)
|extend|extiende (fusiona con otra lista) la lista agregándole todos los items del iterable|list.extend(*iterable*)
|insert|inserta un item en la posición dada. el primer argumento es el indice del item delante del cuales insertara, por lo tanto a.insert(0,x) inserta al principio de la lista a.insert(len(a), x) equivale a a.append(x)|list.insert(*i,x*)|
|remove|quita el primer item de la lista cuyo valor sea *x*, si no existe lanza un ValueError, se puede usar el nombre del item o la posición [i]|liste.remove(*x*)
|pop / popleft|quita el item dada en la lista y lo retorna, si no se especifica *i* utiliza el ultimo dato|list.pop([*i*])
|clear|elimina todos los datos de la lista, esquivale a *del a[:]|list.clear()|
|index|retorna el indice basado en cero del primer elemento cuyo valor sea igual a *x*, si no existe tira ValueError|list.index(*x[,start[,end]]*)|
|count|retorna el numero de veces que *x* aparece en la lista|list.count(*x*)
|sort|personaliza el orden de los elementos|list.sort(*\*,key=None, reverse=False*)
|reverse|revierte los elementos de la lista|list.reverse()
|copy|retorna una copia superficial de la lista equivalente a *a[:]*|list.copy()
---


### Modificar un dato

```python
lista[0]=1
# recordar que debe de ser del mismo tipo de dato 
```
### Contar lista

```python
len(lista)
```
### Fusionar lista

```python
nueva_variable = lista1 + lista2
```
---
### DEL
del  a[n] / a[:] 
elimina los elementos que necesitamos solo debemos saber lo que queremos



## INPUT

dar formato al input
```python
print(f'Nombre: {nombre}\n','Edad: {edad}')
```
cambiar tipo de dato
```python
a = int(a)
```



---

## DICCIONARIOS

### Acceder a un elemento dentro de un diccionario 

> diccionario =[*X*]



### Agregar un elemento la clave no se puede repetir

> diccionario['*clave*'] = *x*



### Buscar un valor usamos **GET**, solo se puede usar claves

>diccionario.*get*(*clave* **,** texto alternativo si no existe)



### Conocer solo las claves

>diccionario.*keys()*



### Conocer los valores

>diccionario.*values()*



### Conocer claves y valores

> diccionarios.*intems()*



### Eliminar un elemento

> diccionario.pop(*clave*, mensaje si no existe)



### Eliminar todos los elementos

> diccionario.*clear()*



### Iterar claves

> *for* diccionario *in* diccionario:
>
> print(diccionario)



### iterar valores

> *for* diccionario in diccionario.values():
>
> print(diccionario)



### iterar items

> *for* clave, valor *in* diccionario.items():
>
> print(clave, valor)

### DEL
del  a[n] / a[:] 
elimina los elementos que necesitamos solo debemos saber lo que queremos



---

## CONJUNTOS

Un conjunto no puede almacenar un valor que se repita, en caso de tenerlo no aparecerá
>**a=set( )** / **a={'a', 'b',...}**---Ej a=set('abradacabra) === {'d','c','r','b','a'}

Si utilizamos operadores como: 

|simbolo|ejemplo|resultado|
|---|---|---|
| - | a-b=| aparecen letras que están en "a" pero no en "b"|
|Pipe|a(pipe)b=| suma los caracteres que no aparecen|
| & |a&b=| letras que tienen en común|
| ^ |a ^ b=| letras que no se encuentran en ambas

|CODIGO|ACTIVIDAD|
|---|---|
|a.add('x')|agrega un nuevo elemento al conjunto|
|a.discard('x')|elimina el elemento que selecciones|
|a.clear()|eliminar todos los elementos del conjunto|

---
## NOTAS NO DEFINIDAS

Si queremos saber si algún dato se encuentran en una variable, lista o tuple

```python
print('dato' in variable)
```

> break en un loop para el proceso 
> continue se salta el numero 
> while es igual que usar if

### Limitar decimales en float
>"{0:.**n**f}".format(*X*)

n= numero de decimales x= variable
### AND EN EXPRESION IF
Solo recordar que en caso de realizar esta condicion doble repetir la variable despues de and or
>if x >= n and x <= n2:   || 
>if n>= x <= n2:


---
## FUNCIONES
Partes de código que pueden volverse a usar
**def** es su definition
> def nombre_función():
>   aquí ponemos que es lo que necesitamos en la función

Para utilizarla solo tenemos que poner
>nombre_function()

### CREAR UNA VARIABLE GLOBAL

Al crear una variable dentro de una función solo podremos utilizarla dentro de la misma
, si es que requerimos usarla en otras zonas de programa 
podemos añadir la imostramos nstrucción **Global**

```python
def función()
    global variable 
    variable = i
```

### RETURN

Con Return devuelve el valor, para capturarla necesitamos
meterla en una variable o usar print, y define la misma función 
por lo que ahí termina la función.
**Es posible crear una variable a partir de una función 
para imprimirla sin tener que usar paren tesis o acorta el nombre, pero si 
quieres retornar varias variables se creará una *TUPLA***

---
#PARÁMETROS Y ARGUMENTOS
Parameters son cuando enviamos valores a la función estos pueden estar posteriormente
Mientras que argumentos son elementos que enviamos ala función

```python
def función(parametro):
    return f'texto,{parametro} continua texto
   
variable = función('argumento')
print (variable)
°°°°°°°°°°°°°°°°°°°°°°°°°°°°°°°°°°°°°°°°°°°°°°°°°°°°
#  ejemplificando:

def saludar(nombre):
    return f'Hola, {nombre} desde la función saludar'

saludo = saludar('Roel')
print(saludo)
```
### ARGUMENTOS POR POSICIÓN
Es cuando ambos argumentos están colocados en orden.
```python
#ej.
def sumar(a, b)
    return a + b
suma = sumar(10,20)
print(suma)---30
```
### ARGUMENTOS POR NOMBRE
```python
def restar(a, b)
    return a - b
resta = restar(b = 20, a = 40)
print(resta)-----20
```
###PARAMETROS POR DEFECTO

```python
def restar(a=None b=None):
    if a = None or b = None:
        print('Error: Debes enviar dos numero')
        return
        
resta = restar(a=30,b=10)----20
```
### FUNCION CON ARGUMENTOS DETERMINADOS
Con *args (convencionalmente) definimos 
argumentos por **posicion**
```python
def sumar(*args):
    suma=0
    for n in  args
        suma += n
       return suma
        
suma_total = sumar(1,2,3,4,5)
print('La suma total es: , suma_total)
```
 ###ARGUMENTOS INDETERMINADOS POR NOMBRE

```python
def sumar(*args, **kwargs):
    suma = 0
    for n in args:
        suma += n
    return suma, kwargs
    
suma_total, datos =sumar(10,20,3,4,5,6,100,nombre = 'Alex', edad = 25)
print('La suma total es: ', suma_total)
print(datos)
```
Si notamos *args es una tupla, mientras que kwargs 
es un diccionario

---
###FUNCIONES RECURSIVAS Y LAMBDAS
se le llamar lambda a las funciones anonimas
> sumar=lambda a, b: a=b || def sumar(a,b):
>
> ```python
>                    return a+b
> ```

### COMPARACIONES ENTRE LAMBDA Y UNA FUNCION
```python
def sumar(a,b):
	return a + b 
```

``` python
Lambda a,b:a+b
```




---

### CREAR NUMEROS AL AZAR
Importamos random y luego asignamos

>x = random.randint(limite_1, limite_2)



``` python
def sumar(a,b):
    return a+b
sumar=lambda a,b:a+b

# Para trabajar con la funcion lambda 
print(sumar(10,20))
```

> Ejemplo para duplicar un numero

```python
doblar = lambda n: n*2
# saber si es par o impar
par = lambda n: n % 2 == 0
impar = lambda n: n%2 !=0

print(sumar(10,20))
print(doblar(10))
print(par(4))
```

> Función anónima para invertir una cadena 

```python
revertir = lambda cadena: cadena[::-1]
print(revertir('hola'))
```



### FUNCIONES INTEGRADAS

Son funciones ya integradas como:

| Función                             | Significado                                                  |
| ----------------------------------- | ------------------------------------------------------------ |
| len( )                              | cuenta la cadena                                             |
| round(n,x) \| n=numero, x=decimales | redondea el numero                                           |
| eval('n+n2')                        | avalúa una cadena de caracteres pero si se puede resolver de manera aritmética la realiza, como si fuese un int |
| abs(n)                              | devuelve el valor absoluto de los números                    |
| bin(X)                              | convierte en binario                                         |
| hex(X)                              | convierte en hexadecimal                                     |
| help( )                             | ayuda                                                        |

### METODOS DE CADENAS DE CARACTERES

Y = cadena de caracteres o variable | Y.M

| METODO             | CARACTERISTICA                                               |
| ------------------ | ------------------------------------------------------------ |
| .upper( )          | convierte en mayusculas                                      |
| .lower( )          | convierte en minusculas                                      |
| .capitalize( )     | convierte en modo titulo                                     |
| .title( )          | cada primera letra de una palabra sera mayuscula             |
| .count('x')        | cuenta cuantos caracteres hay en una cadena de texto         |
| .remplace('x','r') | remplaza un caracter por otro                                |
| .strip(X)          | borra todos los espacios o caracteres inecesarios            |
| .split(X)          | convierte cadena en lista por espacios o lo que le indiquemos |
| .islower\|.is...   | verifica si una cadena tiene alguna caracteristica en especifico |

#### Practicas Generador de contraseña 
```python
import random
random.choise(variable)
# Se usa para elegir un valor al azar de una lista determinada
```
```python
import random


def generar_contrasena():
    mayusculas = ['A', 'B', 'C', 'D', 'F', 'G', 'H', 'I']
    minusculas = ['a', 'b', 'c', 'd', 'e', 'g', 'h', 'i']
    numeros = ['1', '2', '3', '4', '5', '6', '7', '8', '9', '0']
    simbolos = ['!', '@', '#', '$', '%', '-']

    caracteres = mayusculas + minusculas + numeros + simbolos
    contrasena = []

    # aqui senalamos cuantas veces va a realizar el ciclo para generar la contrasena
    for i in range(15):
        caracter_random = random.choice(caracteres)
        contrasena.append(caracter_random) #senalamos donde lo vamos a compilar con append

    contrasena = ''.join(contrasena) # se usa para cambiar de lista a cadena
    return contrasena # nos regrese el valor de cadena

def main():
    contrasena = generar_contrasena() # creamos una variable para contener la funcion
    print('Tu nueva contraseña es: ', contrasena)

if __name__=='__main__':
    main()
```
#### Convertidor de moneda
```python
def convertir(valor_dolar, pais):
    cantidad_moneda = float(input(f'ingrese cantidad de {pais}: '))
    dolares = cantidad_moneda / valor_dolar
    dolares = round(dolares, 2)  # aplicar redondeo
    print(f'Tienes ${dolares} Dolares')

convertir(3.61, 'soles')
```

### CICLOS ANIDADOS
```python
def anidados():
    for y in range(1, 11):
        for x in range(1, 11):
            print(y * x, end='\t') # END es un parametro para que sea herizontal el for
        print(' ') #  para hacer salto de linea
```


### MODULARIDAD

Se utiliza para generar bloques de codigo para crear programas para:
- reutilizar 
- evitar colapsos
- mantenible
- legibilidad
- solucion rapida de problemas

Esto permite:
- Dividir el programa en diferentes modulos o archivos
- Separar los modulos de archivos en paquetes

## MODULOS

### CREAR E IMPORTAR MODULOS

Para crear modulos y luego reutilizar sus funciones solo debemos crear 
las funciones que deseemos utilizar y para importar seguir la siguiente
sintaxis
```python
import nombre_Archivo

#Para usarlo
nombre_Archivo.nombre_Funcion(valores)

# Recordar que podemos crear una variable para asignar el nombre del archivo
```
### OTRAS FORMAS DE IMPORTAR MODULOS
#### IMPORTACION DE CLASE ESPECIFICA
```python
from modulo import funcion_deseada
# Por lo que solo tendremos que poner la funcion y el argumento
funcion(argumento)
```
Para importar varias funciones especificas solo debemos de añadir
comas entre ellas. O, para importar todas las funciones
solo es mecesario usar " * " (asterisco)  

De ser necesario podemos usar un *Alias* 

```python
modulo import funcion as f
f(argumento)
```
## EJECUTANDO MODULOS COMO SCRIPS
### MODULO ESTANDARD ***"SYS"***
Es necesario utilizar un modulo integrado
a python para interactuar con el sistema
```python
import sys
```
**SYS** Recupera lo que se esta enviando como argumento
al momento de recuperar el script utilizando el **ARGV**
que los depositará en una lista

````python
import sys

print(sys.argv)
````
Para enviar argumentos en caso de enviar cadena de texto 
usar comillas, una vez ejecutado enviará el nombre de script y los valores del mismo

Otro ejemplo es definir la impresion del script definiendo los argumentos
````python
import sys
texto =  sys.argv[1]

# Conciderando que el numero 0 esta ocupado por el nombre de las script
if len(sys.argv) == 3:
    cantidad = int(sys.argv[2])
    c == 0
    while c < cantidad:
        print(texto)
        c += 1
else:
    print('Falta de argumentos')
````
#### FORMATEAR LA INFORMACION
Es posible darle formato a la informacion capturada de las siguientes 
formas:
```python
# Manera simple
from sys import argv
if len(argv) == 4:
    nombre = argv[1]
    edad = int(argv[2])
    altura = float(argv[3])
    print(f'Nombre: {nombre} \nEdad:{edad} \nAltura: {altura}')

else:
    print('Error, Ingrese los argumentos correctamente')
```
```python
# Mediante el uso de format
from sys import argv
if len(argv) == 4:
    nombre = argv[1]
    edad = int(argv[2])
    altura = float(argv[3])
    print('Nombre: {} \nEdad:{} \nAltura: {}'.format(nombre, edad, altura))

else:
    print('Error, Ingrese los argumentos correctamente')
```
En este ultimo ejemplo las posiciones se ponen al final y la **f** se omite
```python
# Tambien podemos dar referencia a los corchetes
from sys import argv
if len(argv) == 4:
    nombre = argv[1]
    edad = int(argv[2])
    altura = float(argv[3])
    print('Nombre: {n} \nEdad:{e} \nAltura: {a}'.format(a = altura, n = nombre, e = edad))

else:
    print('Error, Ingrese los argumentos correctamente')
```
#### ULTIMA FORMA DE DAR FORMATO ANTIGUA (version 2)
```python
from sys import argv
if len(argv) == 4:
    nombre = argv[1]
    edad = int(argv[2])
    altura = float(argv[3])
    print('Nombre: %s \nEdad: %i \nAltura: %f'%(nombre, edad, altura))

else:
    print('Error, Ingrese los argumentos correctamente')
```
|Conversión|Significado|Notas|
|---|---|---|
|'d'|Entero decimal con signo.
|'i'|Entero decimal con signo.
|'o'|Valor octal con signo.|(1)
|'u'|Obsoleto – es idéntico a 'd'.|(6)
|'x'|Hexadecimal con signo (En minúsculas)|(2)
|'X'|Hexadecimal con signo (En mayúsculas)|(2)
|'e'|Formato en coma flotante exponencial (En minúsculas).|(3)
|'E'|Formato en coma flotante exponencial (En mayúsculas).|(3)
|'f'|Formato en coma flotante decimal.|(3)
|'F'|Formato en coma flotante decimal.|(3)
|'g'|Formato en coma flotante. Usa formato exponencial con minúsculas si el exponente es menor que -4 o no es menor que la precisión, en caso contrario usa el formato decimal.|(4)
|'G'|Formato en coma flotante. Usa formato exponencial con mayúsculas si el exponente es menor que -4 o no es menor que la precisión, en caso contrario usa el formato decimal.|(4)
|'c'|Un único carácter (Acepta números enteros o cadenas de caracteres de longitud 1)
|'r'|Cadena de texto (Representará cualquier objeto usando la función repr()).|(5)
|'s'|Cadena de texto (Representará cualquier objeto usando la función str()).|(5)
|'a'|Cadena de texto (Representará cualquier objeto usando la función ascii()).|(5)
|'%'|No se representa ningún argumento, obteniéndose en el resultado la cadena '%'.|

Notas:

La forma alternativa hace que se inserte antes del primer dígito un prefijo indicativo del formato octal ('0o')
La forma alternativa hace que se inserte antes del primer dígito uno de los dos prefijos indicativos del formato hexadecimal '0x' or '0X' (Que se use uno u otro depende de que indicador de formato se haya usado, 'x' or 'X').
La forma alternativa hace que se incluya siempre el símbolo del punto o coma decimal, incluso si no hubiera dígitos después.
La precisión determina el número de dígitos que vienen después del punto decimal, y por defecto es 6.
La forma alternativa hace que se incluya siempre el símbolo del punto o coma decimal, y los ceros a su derecha no se eliminan, como seria el caso en la forma normal.
La precisión determina el número de dígitos significativos que vienen antes y después del punto decimal, y por defecto es 6.
Si la precisión es N, la salida se trunca a N caracteres.

Como en Python las cadenas de caracteres tiene una longitud explícita, la conversión de %s no requiere que la cadena termine con '\0'.
Distinto en la versión 3.1: Las conversiones %f para números con valores absolutos mayores que 1e50 ya no son reemplazadas por conversiones %g.


### FUNCION ***"DIR"***
Esta funcion da informacion sobre un modulo
```python
print(dir(mudulo))
> 'funcion1', 'funcion2' 
```
si no ingresamos argumentos lo que nos va a arrojar son los modulos que
estamos utilizando en el programa

### MODULO MATH
```python
import math as m
m.floor(numero_decimal) # redondea hacia abajo

m.ceil(numero_decimal) # redondeo hacia arriba

n = [0.99999, 1, 2, 3]
m.fsum(n)
> 6.99999  # Te hace la sumatoria

m.trunc(45.785)
> 45 # Despues del decimal ignora el resto

m.pow(argumento1, argumento2)
> Potencia de los argumentos

m.sqrt(numero)
> Raiz cuadrada

m.pi
> valor de pi

m.e
>valor de Euler
```
### MODULO ***"DATATIME***
```python
from datetime import datetime as d

d.now() # Indica el tiempo actual
dt = d.now()

dt.year
> imprime el año 

dt.month
> imprime el mes

dt.day
> imprime el dia

dt.hour
> imprime la hora

# aplica con .hour, .seconds, .microseconds
```

## PAQUETES 
Son simples directorios o carpetas. Lo que vuelve importante a esto es 
su archivo ***__init__.py*** .Lo cuales nos van a ayudar a ordenar o 
estructurar nuestros modulos
### IMPORTAR LOS PAQUETES Y SUS MODULOS
```python
from sound.effects import echo
```
### IMPORTAR LOS PAQUETES DENTRO DE UN PAQUETE
```python
from  . import echo
from  .. import formats
from  ..filters import equalizer
```
Un ejemplo 
```python
def sumar(*args):
    suma = 0
    for n in args
        suma += n
    return suma

restar = lambda a, b:a - b

potencia = lambda a, b: a**b
```
> ls main.py    my_paquete/

```python
import my_paquete as a


def main():
    suma = a.sumar(4,4,5,8,7,9)
    resta = a.restar(10-5)
    potencia = a.potencia(3,3)
    print('La suma es: ', suma)
    print('La resta es: ', resta)
    print('La potencia es: ', potencia)

if __name__ == '__main__':
    main()

> resuelve las operaciones aritmeticas
```

## PROGRAMACION ORIENTADA A OBJETOS 
Se compone de cuatro elementos:
- Clases -> Molde  (Modelo de un objeto)
- Propiedades -> Atributos
- Metodos -> Comportamiento
- Objetos -> Objetos

### Pilares de POO
- Encapsulamiento
- Abstraccion
- Herencia
- Polimorfismo

> Un objeto son aquellos que tienen propiedades (atributos) y comportamientos
> funciones

### CLASE 
Es el modelo desde que se contruyen objetos. Es el molde para los objetos. 
De una clase podemos crear muchos objetos

#### ABSTRACCION
Es necesario analizar los objetos para crear clases. cada objeto tiene caracteristicas
generales para construir la aplicacion

#### PARTES DE UNA CLASE
- ***Identidad:*** Nombre de la clase (Solo se puede tener una clase)
- ***Atributo:*** Son los atributos de los objetos para los objetos
- ***Comportamiento:*** Son los metodos de la clase

|Clase|Objeto 1|Objeto 2|
|---|---|---|
|Usuarios|Usuario 1|Usuario 2|
|Numbre|Alex|Roel|
|Iniciar Sesion|Iniciar Sesion|Iniciar Sesion|

```python
# Este es el archivo de metodos y clases

class Persona: # El nombre de la clase va en mayuscula la primera letra
    nombre = None # Tambien se puede dejar ''
    edad = None
    
''' Los atributos son variables, la funcion dentro de una clase se llama metodo
    Y son comportamientos de los objetos'''
    
    def mostrar_datos(self): # Self muestra que esta funcion pertenece a la clase
        print('Nombre: ', self.nombre)
        print('Edad: ', self.edad)
```
 Al crear una varible y asignar una clase se convierte en un objeto. A esto se le llama instancia

```python
# Este es el modulo principal
from POO.herencia.persona import Persona

persona1 = Persona()
persona1.nombre = 'Alex'
persona1.edad = 25

persona2 = Persona()
persona2.nombre = 'Roel'
persona2.edad = 26

persona2.mostrar_datos()
print('=' * 25)
persona1.mostrar_datos()
```
```shell
>
Nombre:  Roel 
Edad:  26
=========================
Nombre:  Alex
Edad:  25
```

### CONSTRUCTORES
Aquel que construye al objeto para simplificar al momento de crear un objeto, simplificando el trabajo
```python
class Persona:

    # Muestra que se esta creando el constructor
    def __init__(self, nombre, edad): # El segundo parametro senala los atributos
        self.nombre = nombre
        self.edad = edad
        
    def mostrar_datos(self):
        print('Nombre: ', self.nombre)
        print('Edad: ', self.edad)
```

```python
from POO.herencia.persona import Persona

persona1 = Persona('Alex', 25)
persona1.mostrar_datos()
```
Para actualizar datos
```python
persona1.nombre('Roel') # Actualiza desde el objeto el nombre del mismo
```
Si deseo imprimir ***print(persona1)*** me mostrara la referencia en la memoria y no el objeto
. Para ello se puede usar lo siguiente
```python
def __str__(self):
    return f'Nombre: ' {self.nombre} \n'Edad: '{self.edad}
```
Por lo que podemos resumir todo lo anterior:
```python
# Modulo - Archivo
class Pokemon:
    def __init__(self, name ,atributo):
        self.name = name
        self.atributo = atributo

    def __str__(self):
        return f'Nombre: {self.name}\n Atributo: {self.atributo}'

```
```python
# Main - Archivo
from pokemon import Pokemon

pokemon1 = Pokemon('Pikachu','Electro')

print(pokemon1)
```
```shell
> Nombre: Pikachu
 Atributo: Electro
```

### ENCAPSULACION

Debemos definir como metodos y atributos de una clase los atributos que no sean
accesibles desde fuera, para que los atributos no sean accesibles y no se puedan modificar
desde fuera
```python
class Persona:
    # Son atributos privados al agregar '__atributo'

    __nombre = None
    __edad = None
```

```python
from POO.herencia.persona import Persona

persona1 = Persona()

print(persona1.__nombre)
```
```shell
> AttributeError: 'Persona' object has no attribute '__nombre'
```
Esta forma se puede utilizar tambien al crear metodos / funciones
```python
# Se usa para retornar en el modulo
def get_nombre(self):
    return self.__nombre

# Para modificar
def set__nombre(self,nombre): # Nombre = al dato que se va a modificar
    self.__nombre = nombre
def set__edad(self,edad):
    self.__edad = edad
```

```python
from POO.herencia.persona import Persona

persona1 = Persona('Alex', 25)
persona1.set_nombre('Roel')

print(persona1.get_nombre)
print(persona1)
```

### HERENCIA

````python
class Persona:  # Clase padre o super clase
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad

    def detalle_persona(self):
        print(f'Nombre: {self.nombre}\n Edad: {self.edad}')

    def __str__(self): # Se crea para poder imprimir
        return f'Nombre: {self.nombre}\n Edad: {self.edad}'


class Cliente(Persona):  # Subclase que va a heredar
    pass

````

``````python
from POO.herencia.persona import Cliente  # Crear cliente

cliente1 = Cliente('Alejandra', 29)
cliente2 = Cliente('Bricia', 25)

cliente1.detalle_persona()  # En el modulo ya indica que se imprima

print(cliente2)  # Para esto se creó el def __str__(self):
``````

### FUNCION SUPER
```python
class Persona:  # Clase padre o super clase
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad

    def detalle_persona(self):
        print(f'Nombre: {self.nombre}\n Edad: {self.edad}')

    def __str__(self):
        return f'Nombre: {self.nombre}\n Edad: {self.edad}'


class Cliente(Persona):  # Subclase que va a heredar
    pass

# Clase empleado que hereda de persona
class Empleado(Persona): # Va a tener atributo sueldo
    def __init__(self, nombre, edad, sueldo): # Se ponen todos los atributos
        super().__init__(nombre, edad) # Se hereda el constructor de la clase persona
        self.sueldo = sueldo # Se genera la parte que falta
    # Anadir detalle persona
    
    def detalle_empleado(self):
        super().detalle_persona()
        print('Sueldo:', self.sueldo)# Agrego le que falta

    # Para mostrar el estado
    def __str__(self):
        return super().__str__() + f'\nSueldo: {self.sueldo}'# Se hereda el str de persona
```

```python
from POO.herencia.persona import Cliente, Empleado

empleado1 = Empleado('Sabrina', 25, 1500)
empleado2 = Empleado('Abby', 18, 2000)

empleado1.detalle_persona()  # Acceder a detalle
empleado1.detalle_empleado()

print(empleado2)
```
```shell
> Nombre: Sabrina
 Edad: 25
Nombre: Sabrina
 Edad: 25
Sueldo: 1500
Nombre: Abby
 Edad: 18
Sueldo: 2000
```

### HERENCIA SIN SUPER
En esta version solo se va a utilizar el nombre de la clase para
heredar su constructor, metodos y estado del metodo
````python
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad

    def detalle_persona(self):
        print(f'Nombre: {self.nombre}\n Edad: {self.edad}')

    def __str__(self):
        return f'Nombre: {self.nombre}\n Edad: {self.edad}'


class Cliente(Persona):
    pass



class Empleado(Persona):
    def __init__(self, nombre, edad, sueldo):
        Persona.__init__(self, nombre, edad)
        self.sueldo = sueldo

    def detalle_empleado(self):
        Persona.detalle_persona(self)
        print('Sueldo:', self.sueldo)

    def __str__(self):
        return Persona.__str__(self) + f'\nSueldo: {self.sueldo}'

````

```python
from POO.herencia.persona import Cliente, Empleado

empleado1 = Empleado('Sabrina', 25, 1500)
empleado2 = Empleado('Abby', 18, 2000)

empleado1.detalle_persona()
empleado1.detalle_empleado()

print(empleado2)
```
```shell
> Nombre: Sabrina
 Edad: 25
Nombre: Sabrina
 Edad: 25
Sueldo: 1500
Nombre: Abby
 Edad: 18
Sueldo: 2000
```
### POLIMORFISMO
Podemos modificar o reescribir los metodos de las clases padres
```python
class Persona(object):
    def __init__(self, nombre):
        self.nombre = nombre

    def moverse(self):
        print('Ando caminando')

# Vamos a reescribir el metodo y tendra una funcion distinta
class Atleta(Persona): # Donde obtiene su transformador

    def moverse(self):
        print('Ando corriendo')

class Ciclista(Persona):

    def moverse(self):
        print('Ando moviendome en mi bicicleta')
```
```python
'''
Se crea la varioble para no repetir el nombre, se usa la clase y
define el valor
variable y se agrupa el modo (acccion definida)
'''
from persona import Persona, Atleta, Ciclista

persona = Persona('Alex')
persona.moverse()

atleta = Atleta('Fernanda')
atleta.moverse()

ciclista = Ciclista('Veronica')
ciclista.moverse()
```
```shell
> Ando caminando
  Ando corriendo
  Ando moviendome en mi bicicleta
```
HERENCIA MULTIPLE
Se puede aplicar este concepto a diferencia de otros lenguajes
```python
class A(object):
    def __init__(selfself):
        print("soy clase A")
    def a(self):
        print('Soy metodo A')

class B(object):
    def __init__(self):
        print("soy clase B")
    def b(self):
        print('soy metodo b')
        
# Le da mas importancia a la la clase a la izquierda
class C(B, A): 
    def c(self):
        print('Soy metodo de C')
        

''' 
c1 = C()
> Soy clase B, esto es por que la clase C mo tiene un constructor
por lo que hereda de la B que si lo tiene. Podemos acceder a los metodos
de las clases heredadas
> c1.a()
Soy el metodo de A
> c1.c()
'''
```



#### RESULTADO RETO

```python

	def area(self):
		pass

	def perimetro(self):
		pass


class Rectangulo(Figura): # Solo se define de donde se hereda
	def __init__(self, base, altura):
# Se redefine el nombre para obtener el nombre del objeto rectangulo
		self.nombre = __class__.__name__  # Saca el nombre de la clase
		self.base = base
		self.altura = altura
	
	def area(self):
		return self.base * self.altura

	def perimetro(self):
		return 2 * self.base + 2 * self.altura
	
	def __str__(self):
		return f'{self.nombre}[base:{self.base} altura:{self.altura}]'



class Circulo(object):
	def __init__(self,radio):
		self.nombre = __class__.__name__
		self.radio = radio
	def area(self):
		return math.pi * self.radio * self.radio

	def perimetro_(self):
		return 2 * math.pi * self.radio

	def __str__(self):
		return f'{self.nombre}[radio:{self.radio}]'

	

def probar_figura(figura): # Por que vamos a recibir el objeto figura
	print(figura) #Imprimimos el objeto a recibir
	print('Area: ', figura.area())
	print('Perimetro: ', figura.perimetro())
```

```python
from figuras import Rectangulo, Circulo, probar_figura

def main():
	while True:
		menu = '''
		AREA Y PERIMETRO DE FIGURAS GEOMETRICAS
		
		1 - RECTANGULO
		2 - CIRCULO
		3 - SALIR
		Ingrese una Opción:
		'''

		opcion = int(input(menu))

		if opcion == 1:
			base = float(input('Ingrese la Base: '))
			altura = float(input('Ingrese la Altura'))
			r= Rectangulo(base, altura)
			probar_figura(r)
		elif opcion == 2:
			radio = float(input('ingrese el Radio: '))
			c = Circulo(radio)
			probar_figura(c)
		elif opcion == 3:
			print('Cerrando sistema')
			break
		else:
			print('Opcion incorrecta')
	

if __name__== '__main__':
	main()
```

---

## MANEJO DE ERRORES Y ARCHIVOS

Los errores pueden ser:

- Tiempo de interpretacion 
- Tiempo de Ejecución

> Los errores mas comunes son:
>
> - Error de sintaxis
> - Asignaciones incorrectas
> - No seguir las reglas

### EXCEPCION

Es un error que sucede durante la ejecucion del programa y muestra donde surgio y de no corregir se cerrará el programa. Gracias a esto es posible resolver estos errores robusteciendo a nuestro programa

```python
c = 0
suma = 0
while c < 3:
    try:  #Donde se genera el problema se usa Try
    	n = int(input('Ingrese un numero: {c=1}: '))
    	suma += n
    	c += 1
    except:
        print('Ingrese solo numeros')
    else: # Solo si es necesaria la comprobación
        print('Todo funciona correctamente')
    finally:
        print('Fin de la ejecución')
print('La suma total es: ', suma)	
```

 ```shell
 > Error , ingrese solo numeros enteros
 ```

#### GESTION DE EXCEPCIONES MULTIPLES

```python
divi =0
try:
a=int(input('Ingrese el Dividendo'))
b=int(input('Ingrese el Divisor'))

divi = a/b
except ValueError:
    print('Ingrese solo numeros enteros')
except ZeroDivisionError:
    print('No se puede dividir entre Cero')
except Exception as error:
    print('Ha ocurrido un error no previsto: ', type(error).__name__)
print('la division es: ', divi)
```



```shell
Ha ocurrido un error no previsto: division by zero
```



#### LANZAR ERROR

```python
def dividir(0,0):
    if b == 0:
        raise ZeroDivisionError('Error:  No se puede dividir entre Cero')
    else:
        return a/b
    dividir(4/0)
```



```shell
Error: No se puede dividir entre Cero
```

#### CREAR EXCEPCIONES

```python
Class OperadorException(Exception):
    def __init__(self, mensaje):
        super().__init__(mensaje)

def dividir(0,0):
    if b == 0:
        raise OperadorException('Error:  No se puede dividir entre Cero')
    else:
        return a/b
    dividir(4/0)
```

```shell
__main__.OperadorException: Error: No se puede dividir entre Cero
```

## MANEJO DE DATOS

Para almacenar datos necesitamos una base de datos para no perder los registros

> Es necesario usar el modulo **io** que es entrada y salida de datos, la w da el mando de escribir y sobre escribir

```python
from io import open # Abre un archivo

def escribir_archivo():
    # w = escribir 
    archivo = open('texto.txt','w') # Si no existe el archivo lo crea
    archivo.close()
    
# Tambien es posible borrar todo el archivo si solo abrimos y cerramos el archivo
```

### LEER ARCHIVOS

```python
from io import open
from os import path # Permite la verificacion del archivo

def leer_archivo():
    if path.isfile('texto.txt'): # Revisa si existe
        archivo = open('texto.txt', 'r') # Modo lectura
        textos = archivo.read() # Solo lee la primera linea
        archivo.close()
        
        print(textos)
    else: # Si no existe lo mostrara
        print('No existe el archivo')
        
leer_archivo()

```

### CADA LINEA  SEA  PARTE DE UNA LISTA

```python
def leer_archivo():
    if path.isfile('texto.txt'): # Revisa si existe
        archivo = open('texto.txt', 'r') # Modo lectura
        textos = archivos.readlines() # Lee todas las lineas
        # devuelve una lista, usa \n
        archivo.close()
        
        print(textos)
    else: # Si no existe lo mostrara
        print('No existe el archivo')
    leer_archivo()
```

### FLUJO DE ACTUALIZAR( AGREGAR ELEMENTOS )

```python
def agregar_datos():
    if path.isfile('texto.txt'): # Revisa si existe
         archivo = open('texto.txt', 'a') # Modo actualizar datos
# Necesitamos dar un salto de linea
		archivo.write('\nHola es nueva linea')
         archivo.close()

    else: # Si no existe lo mostrara
        print('No existe el archivo')

agregar_datos()
```



### ACTUALIZAR UNA LINEA DEL ARCHIVO

```python
def modificar_dato():
    if path.isfile('texto.txt'):
        archivo = open('texto.txt', 'r+') # Modo luctura escritura
    # Necesitamos recuperar los datos en una lista en una variable
        texto = archivo.readlines()
        print(texto)
        texto[1] = 'nuevo valor\n'
		print(texto)
        archivo.close()

    else:
        print('No existe el archivo')
```



### PUNTERO

Si queremos  crear un puntero para especificar donde editar dentro de un párrafo usaremos lo siguiente:

```python
def modificar_dato():
    if path.isfile('texto.txt'):
        archivo = open('texto.txt', 'r+') # Modo luctura escritura
    # Necesitamos recuperar los datos en una lista en una variable
        texto = archivo.readlines()
        print(texto)
        texto[1] = 'nuevo valor\n'
		print(texto)
        archivo.seek(0) # La posicion donde lo necesitamos (caracter)
        archivo.writelines(texto)
        archivo.close()
        print(texto) # verificar el contenido

    else:
        print('No existe el archivo')
modificar_dato()
```

# INTRODUCCION DE BASE DE DATOS

## ABREVIACION PARA ESQUEMA

| SIMBOLO | SIGNIFICADO                                |
| ------- | ------------------------------------------ |
| ▭       | Objeto que figura en nuestra base de datos |
| 🔹       | Relación entre entidades                   |
| ▔▔      | Unión de entidades                         |
| ◯       | Atributos                                  |
| ●       | Clave primaria                             |
| ◐       | Atributo foráneo o clave secundaria        |



#### SQLITE

- Permite hasta 2 terabytes de base de datos
- Por ser ligeros es utilizado en dispositivos moviles
- Podemos usarlo en Python, Perl, Ruby, Java y C++ entre otros
- Es multiplataforma 
- Las listas se conocen como entidades



## CREAR BASE DE DATOS Y SU ENTIDAD

### CREAR Y SELECCIONAR DB

```sqlite
-- crea la base de datos

CREATE DATABASE EJEMPLO

-- coloca la BD EJEMPLO en memoria para poder hacer modificaciones

USE TURISMO
```

### CREAR TABLAS

```sqlite
-- Crea una tabla con incremento
	
CREATE TABLE "carreras" (
	"codigo_c"	INTEGER,
	"nombre"	TEXT,
	"duracion"	INTEGER,
	PRIMARY KEY("codigo_c" AUTOINCREMENT)
);

-- Crea una foreign key
CREATE TABLE ALUMNOS(
    'CODIGO_A' INTEGER,
    'NOMBRE_A' VARCHAR(100),
    'EDAD_A' INTEGER,
    'TELEFONO_A' INTEGER,
    'CARRERA_FK'INTEGER,
    PRIMARY KEY (CODIGO_A),
    FOREIGN KEY (CARRERA_FK) REFERENCES CARRERAS (CODIGO_C)
);
```

### INSERTAR DATOS

```sqlite
-- recuerda saber cuantos campos existen
INSERT INTO CARRERAS VALUES (1, 'ING SISTEMAS', 5);
-- varios datos al mismo tiempo
INSERT INTO CARRERAS VALUES (2, 'DERECHO', 3), (3, 'CONTABILIDAD', 5);
-- cuando es autoincrement se usa lo siguiente
    INSERT INTO TABLA VALUES (NULL, 'DATOS')
```

### VISUALIZAR DATOS

```sql
-- * significa TODO
SELECT * FROM TABLA 
-- elegir solo algunas campos
SELECT CAMPO1, CAMPO2 FROM TABLA
-- usando select en la busqueda
SELECT * FROM CARRERAS WHERE DURACION = 5 
-- =! (negacion) | < (menor que) | > (mayor que)
```

### INNER JOIN

```sqlite
-- senalamos con un punto cual es el dato que vamos a sustituir de 
-- otra tabla, ON le indica el reemplazo
SELECT CODIGO_A,NOMBRE_A,NOMBRE FROM ALUMNOS 
INNER JOIN CARRERAS ON ALUMNOS.CODIGO_A = CARRERAS.CODIGO_C
```

### MODIFICAR DATOS

```sqlite
UPDATE CLIENTES
SET NOMBRE_C = 'PEDRO'
WHERE CODIGO_C = 2 

---
UPDATE CLIENTES
SET NOMBRE_C = 'ROBERTO' WHERE NOMBRE_C = 'JUAN'
```



### BORRAR DATOS

```sqlite
-- borrar todos los datos de una tabla
DELETE FROM TABLA
-- solo un registro
DELETE FROM TABLA WHERE CODIGO = 2 AND CONDICIONAL = 'NOMBRE'
-- eliminar tabla 
DROP TABLA
```

### NOTNULL

```sqlite
CREATE TABLE "carreras" (
	"codigo_c"	INTEGER,
	"nombre"	TEXT NOT NULL,
	"duracion"	INTEGER,
	PRIMARY KEY("codigo_c" AUTOINCREMENT)
```



 ## CONECTAR PYTHON A SQL

```python
import sqlite3

# conectar a la base de datos
coneccion = sqlite3.connect('tienda.db')
# cerrar la base de datos
coneccion.close()
```

> Precaucion. No solo abre el archivo , de no existir lo crea

---

# INTRODUCCION NUMPY

## ARRAY

Estructura de datos,coleccion de elementos (valores o variables identificado por almenos un indice ***contenedor***)

> En ***Numpy***:
>
> - Cada dimension se denomina ***axis*** 
> - El numero de dimensiones ***rank*** 
> - Lista de dimensiones con su  correspondiente longitud ***shape***
> - Numero total de elementos (multiplicación de la longitud de las dimensiones) ***size***




---
## NOTAS MISCELÁNEAS
### PRINT END
```python
print(end=' ')
```
Se utiliza para que al final de cada una de las impresiones
exista un espacio

