# Contar las repeticiones en un texto

```python
p = input().lower().split() # split divide una cadena a una lista 
new_dic =  {element: p.count(element) for element in p} 
for key, value in new_dic.items():
	print(key, value)
```

# Asignar valores por cadena en un diccionario

```python
some_iterable = input().split()

# use dictionary comprehension to create a new dictionary
new_dict = {i.upper(): i.lower() for i in some_iterable}
print(new_dict)
```

# Buscar valores específicos en un diccionario

```python
potential_dates = [{"name": "Julia", "gender": "female", "age": 29,
                    "hobbies": ["jogging", "music"], "city": "Hamburg"},
                   {"name": "Sasha", "gender": "male", "age": 18,
                    "hobbies": ["rock music", "art"], "city": "Berlin"}, 
                   {"name": "Maria", "gender": "female", "age": 35,
                    "hobbies": ["art"], "city": "Berlin"},
                   {"name": "Daniel", "gender": "non-conforming", "age": 50,
                    "hobbies": ["boxing", "reading", "art"], "city": "Berlin"}, 
                   {"name": "John", "gender": "male", "age": 41,
                    "hobbies": ["reading", "alpinism", "museums"], "city": "Munich"}]

def select_dates(potential_dates):
    suitable_dates = [entry['name'] for entry in potential_dates if
                      entry['age'] > 30 and 'art' in entry['hobbies'] and entry['city'] == 'Berlin']
    return ', '.join(suitable_dates)
```

# Conseguir el mínimo y máximo de un diccionario

```python
d = {"a": 43, "b": 1233, "c": 8}
# d.items()
print("min:", min(d, key=d.get))
print("max:", max(d, key=d.get))
```

# Operaciones con valores de una cadena

```python
# Save the input in this variable
ticket = input()

# Add up the digits for each half
half1 = int(ticket[0])+int(ticket[1])+int(ticket[2])
half2 = int(ticket[-1])+int(ticket[-2])+int(ticket[-3])
print(half1, half2)
# Thanks to you, this code will work
if half1 == half2:
   print("Lucky")
else:
   print("Ordinary")
```

# Saber si es la misma lista o una nueva

````python
# use the function blackbox(lst) that is already defined
lst = ['random', 'stuff', 'in', 'it']
x = blackbox(lst)

if id(lst) == id(x):
    print('modifies')
elif id(lst) != id(x):
    print('new')

````

# Añadir nuevo elemento con función a una lista

```python
def add_player(player, team=[]):
   ...
   team.append(player)
   return team

ice_hockey_team = add_player("Chris", ["Robert", "Alice"]) # Crea 
print(ice_hockey_team)    # ['Robert', 'Alice', 'Chris']
```

# Pequeño problema de porcentaje

```python
def get_bonus(salary, percentage=35):
   if percentage is None:
      percentage = 35

   salary_total = int((salary * percentage)/100)
   return salary_total

### Es lo mismo que :
def get_bonus(salary, percentage=35):
	return int((salary * percentage)/100)
	
    # If the arguments are string is not necesary declare t
```

# Añadir datos a una lista especifica

```python
def add_viewer(name, fan_list=None):
   if fan_list is None:
      no_fan = list()
      no_fan.append(name)
      return no_fan
   else:
      fan_list.append(name)
   return fan_list

print(add_viewer('Dorian'))
```

# Utiliza una clase

```python
class Persona:
   def __init__(self, nombre, edad):
      self.nombre = nombre
      self.edad = edad

   def greet(self, otra_persona):
      return f'Hola {otra_persona.nombre}. Bienvenida, soy {self.nombre}'
   
vicente = Persona('Vicente', 31)
fernanda = Persona('Fernanda', 32)

print(vicente.greet(fernanda))
```

# Función para suma y multiples argumentos

```python
def add(a, b, *args):
    total = a + b
    for n in args:
        total += n
    return total
```

```python
def will_survive(*names):
    for name in names:
        print("Will", name, "survive?")


will_survive("Daenerys Targaryen", "Arya Stark", "Brienne of Tarth")
```

La salida para esta llamada de función será la siguiente:

```python
Will Daenerys Targaryen survive?
Will Arya Stark survive?
Will Brienne of Tarth survive?
```

#  Logica de los argumentos con calculos integrados

```python
def sq_sum(num, *args):
    total = (num ** 2)
    for calc in args:
        total += (calc ** 2)
        
    return total
```

# Promedios entre numeros

``` python
def average_mark(num1, *args):
	count = (len(args) + 1)
	for calc in args:
		num1 += calc
	num1 /= count
	num1 = round(num1, 1)
	return num1


print(average_mark(3, 4, 5, 3))

### OR
def average_mark(*students):
    return round(sum(students) / len(students), 1)
```

# Buscar un final en especifico y cambiarlo e imprimir (.endswith('?'))

```python
Find all words that end in "s" and print them together separated by an underscore.
After such words there will be no punctuation marks, you do not need to worry about that.

for char in phrase:
    if char.endswith('s'):
        new_list.append(char)
x = '_'.join(new_list)
print(x)

```

# Insertar dos variables en un input

```python
x, y = input().split()
print(f'{x} of {y}')
```

# Usar Capitalize

```python
#capitalize( )
s1 = 'my name is khan'
print(s1.capitalize())
-- My name is khan

#capwords( ) from string
import string
s1 = 'my name is khan'
print(string.capwords(s1))
-- My Name Is Khan
print(string.capwords(s1, 'a'))
-- My naMe is khaN

# Otro ejemplo con replace

y = input().split()
x = ''.join(y).title().replace('_', '')

print(x)
```

# Prueba FizzBuzz

```python
for n in range(1,101):
    if n % 3 == 0 and n % 5 == 0:
        print('FizzBuzz')
    elif n % 3 == 0:
        print('Fizz')
    elif n % 5 == 0:
        print('Buzz')
    else:
        print(n)
```

# Uso de la funcion Filter

```python
class Empleado:
    def __init__(self, nombre, cargo, salario):
        self.nombre = nombre
        self.cargo = cargo
        self.salario = salario

    def __str__(self):
        return '{} que trabaja como {} tiene un salario de {} $'.format(self.nombre, self.cargo, self.salario)

listaEmpleados = [
    Empleado('Juan', 'Director', 750000),
    Empleado('Ana', 'Presidenta', 850000),
    Empleado('Antonio', 'Administrativo', 25000),
    Empleado('Sara', 'Secretaria', 27000),
    Empleado('Mario', 'Botones', 21000),
]
salarios_altos = filter(lambda empleado: empleado.salario > 50000, listaEmpleados)
for empleado_salario in salarios_altos:
    print(empleado_salario)
```

```shell
Juan que trabaja como Director tiene un salario de 750000 $
Ana que trabaja como Presidenta tiene un salario de 850000 $
```

# Uso de funcion Map

```python
class Empleado:
    def __init__(self, nombre, cargo, salario):
        self.nombre = nombre
        self.cargo = cargo
        self.salario = salario

    def __str__(self):
        return '{} que trabaja como {} tiene un salario de {} $'.format(self.nombre, self.cargo, self.salario)

listaEmpleados = [
    Empleado('Juan', 'Director', 6700),
    Empleado('Ana', 'Presidenta', 7500),
    Empleado('Antonio', 'Administrativo', 2100),
    Empleado('Sara', 'Secretaria', 2150),
    Empleado('Mario', 'Botones', 1800),
]
def calculo_comision(empleado):
    
    if(empleado.salario <= 3000):
        empleado.salario = empleado.salario * 1.03
    return empleado

listaEmpleadosComision = map(calculo_comision, listaEmpleados)
for empleado in listaEmpleadosComision:
    print(empleado)
```

```shell
Juan que trabaja como Director tiene un salario de 6700 $
Ana que trabaja como Presidenta tiene un salario de 7500 $
Antonio que trabaja como Administrativo tiene un salario de 2163.0 $
Sara que trabaja como Secretaria tiene un salario de 2214.5 $
Mario que trabaja como Botones tiene un salario de 1854.0 $

```

```python
# Ot
# place `import` statement at top of the program
from math import copysign

# don't modify this code or the variables may not be available
x, y = map(float, input().split(' '))

print(copysign(x, y))
```

```python
# place `import` statement at top of the program
from random import randint, seed

# don't modify this code or variable `n` may not be available
n = int(input())

# put your code here
seed(n)
k = randint(-100, 100)
print(k) 
```

# Crear contrasena

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

# Usar SQL

## Crear tablas

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

## INSERTAR DATOS

```sqlite
-- recuerda saber cuantos campos existen
INSERT INTO CARRERAS VALUES (1, 'ING SISTEMAS', 5);
-- varios datos al mismo tiempo
INSERT INTO CARRERAS VALUES (2, 'DERECHO', 3), (3, 'CONTABILIDAD', 5);
-- cuando es autoincrement se usa lo siguiente
    INSERT INTO TABLA VALUES (NULL, 'DATOS')
```

## VISUALIZAR DATOS

```sql
-- * significa TODO
SELECT * FROM TABLA 
-- elegir solo algunas campos
SELECT CAMPO1, CAMPO2 FROM TABLA
-- usando select en la busqueda
SELECT * FROM CARRERAS WHERE DURACION = 5 
-- =! (negacion) | < (menor que) | > (mayor que)
```

## INNER JOIN

```sqlite
-- senalamos con un punto cual es el dato que vamos a sustituir de 
-- otra tabla, ON le indica el reemplazo
SELECT CODIGO_A,NOMBRE_A,NOMBRE FROM ALUMNOS 
INNER JOIN CARRERAS ON ALUMNOS.CODIGO_A = CARRERAS.CODIGO_C
```

## MODIFICAR DATOS

```sqlite
UPDATE CLIENTES
SET NOMBRE_C = 'PEDRO'
WHERE CODIGO_C = 2 

---
UPDATE CLIENTES
SET NOMBRE_C = 'ROBERTO' WHERE NOMBRE_C = 'JUAN'
```



## BORRAR DATOS

```sqlite
-- borrar todos los datos de una tabla
DELETE FROM TABLA
-- solo un registro
DELETE FROM TABLA WHERE CODIGO = 2 AND CONDICIONAL = 'NOMBRE'
-- eliminar tabla 
DROP TABLA
```

## NOTNULL

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

> Precaución. No solo abre el archivo , de no existir lo crea



# Usar SQL con Python

## CREAR UNA TABLA

```python
import sqlite3 
conexion = sqlite3.connect("ejemplo.db")
cursor = conexion.cursor()

cursor.execute("CREATE TABLE persona (codigo_p INTEGER, nombre VARCHAR (100), edad INTEGER, PRIMARY KEY (codigo_p))")
conexion.commit()
conexion.close()
```

## INSERTAR REGISTROS

```python
import sqlite3 
conexion = sqlite3.connect("ejemplo.db")
cursor = conexion.cursor()
cursor.execute("INSERT INTO productos VALUES (NULL, 'PC',1500)")
conexion.commit()
conexion.close()
```

## INGRESAR VARIOS DATOS

```python
import sqlite3
conexion = sqlite3.connect('ejemplo.db')
cursor = conexion.cursor()
personas = [(2, "Roel", 24),
            (3, "Juan", 45),
            (4, "Pedro", 25)]
cursor.executemany("INSERT INTO persona VALUES (?, ?, ?)", personas)

conexion.commit()
conexion.close()
```

## MOSTRAR DATOS  (Recuperar datos)

```python
import sqlite3
conexion = sqlite3.connect('ejemplo.db')
cursor = conexion.cursor()

cursor.execute('SELECT * FROM persona') # Solicitud
personas = cursor.fetchone() # Muestra el primer dato, para todos  .FETCHALL()

for p in personas # Si no usamos FOR se imprimirá como lista
	    print(f'ID: {p[0]} NOMBRE: {p[1]} EDAD: {p[2]}') # Con formato

conexion.commit()
conexion.close()
```

## MODIFICAR DATOS

```python
import sqlite3
conexion = sqlite3.connect('ejemplo.db')
cursor = conexion.cursor()

cursor.execute("UPDATE persona SET nombre = 'Alex Ch' WHERE codigo_p =1")

conexion.commit()
conexion.close()
```

## BORRAR DATOS

```python
import sqlite3

conexion = sqlite3.connect('ejemplo.db')
cursor = conexion.cursor()

cursor.execute("DELETE FROM persona WHERE codigo_p =2")

conexion.commit()
conexion.close()
```

# Cambiar letras de una lista a otra

```python
name = input()

def normalize(new_name):

    # put your code here
    old_values = ["é", "ë", "á", "å", "œ", "æ"]
    new_values = ["e", "e", "a", "a", "oe", "ae"]
    for count, value in enumerate(old_values):
        new_name = new_name.replace(value, new_values[count])

    return new_name

print(normalize(name))


####
name = input()

def normalize(old_name):
    working_dict = {
        'é': 'e',
        'ë': 'e',
        'á': 'a',
        'å': 'a',
        'œ': 'oe',
        'æ': 'ae',
    }

    new_name = old_name
    for old_char, new_char in working_dict.items():
        new_name = new_name.replace(old_char, new_char)

    return new_name

print(normalize(name))
###
name = input()

def normalize():
    new_name = name.replace("é", "e").replace("ë", "e")
    new_name = new_name.replace("á", "a").replace("å", "a")
    new_name = new_name.replace("œ", "oe").replace("æ", "ae")
    # put your code here
    print(new_name)

normalize()
```

# Agregar una letra e invocar un elemento de un diccionario

```python
    #### OTHER
    
money = int(input())
animal = ["sheep", "cow", "pig", "goat", "chicken"]
animals = ["sheep", "cows", "pigs", "goats", "chickens"]
price = [6769, 3848, 1296, 678, 23]
i = 0
while True:
    if money < price[4]:
        print("None")
        break
    if money >= price[i]:
        amount = money // price[i]
        if amount == 1:
            print(amount, animal[i])
        else:
            print(amount, animals[i])
        break
    i += 1
```

```python
# Usar el valor de un diccionario
car = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}

x = car.get("model")

print(x)

```

# Usar la comparativa para usar un dato

```python
def main():
	numbers = {'00': 'RaRo', '01': 'RaTa', '02': 'ReNo', '03': 'ReMo', '04': 'RoCa', '05': 'RieL', '06': 'RiSa',
	           '07': 'RiFa', '08': 'RaCHa', '09': 'RoBot',
	           '0': 'aRo', '1': 'Tea', '2': 'Noe', '3': 'huMo', '4': 'oCa', '5': 'oLa', '6': 'oSo', '7': 'uFo',
	           '8': 'haCHa', '9': 'aVe', '10': 'ToRo',
	           '11': 'TeTa', '12': 'TiNa', '13': 'aToMo', '14': 'TaCo', '15': 'TeLa', '16': 'ToS', '17': 'TuFo',
	           '18': 'TeCHo', '19': 'TuBo', '20': 'NoRia',
	           '21': 'NaTa', '22': 'NeNe', '23': 'NeMo', '24': 'NuCa', '25': 'NiLo', '26': 'aNiS', '27': 'NiFe',
	           '28': 'NiCHo', '29': 'NuBe', '30': 'MaR',
	           '31': 'MoTo', '32': 'MoNo', '33': 'MoMia', '34': 'haMaCa', '35': 'MuLa', '36': 'MeSa', '37': 'MaFia',
	           '38': 'MeCHa', '39': 'aMeBa', '40': 'CoRo',
	           '41': 'CoheTe', '42': 'CoNo', '43': 'CaMa', '44': 'CoCo', '45': 'CoLa', '46': 'CaSa', '47': 'CaFe',
	           '48': 'CoCHe', '49': 'CuBo', '50': 'LoRo',
	           '51': 'LaTa', '52': 'LuNa', '53': 'LiMa', '54': 'LoCo', '55': 'LuLu', '56': 'LoSa', '57': 'aLFa',
	           '58': 'LuCHa', '59': 'LoBo', '60': 'SoR',
	           '61': 'SeTa', '62': 'SeNa', '63': 'SiMa', '64': 'SaCo', '65': 'SoL', '66': 'SeSo', '67': 'SoFa',
	           '68': 'SaCHo', '69': 'SeBo', '70': 'FaRo',
	           '71': 'FoTo', '72': 'FaeNa', '73': 'FaMa', '74': 'FoCa', '75': 'FaLo', '76': 'FoSa', '77': 'FiFi',
	           '78': 'fiCHa', '79': 'eFeBo', '80': 'haCHeRo',
	           '81': 'CHiTa', '82': 'CHiNo', '83': 'CHeMo', '84': 'CHiCa', '85': 'CHaL', '86': 'CHaS', '87': 'CHaFa',
	           '88': 'CHuCHo', '89': 'CHiVo', '90': 'BaR',
	           '91': 'BoTa', '92': 'ViNo', '93': 'BuuM', '94': 'VaCa', '95': 'VeLa', '96': 'VaSo', '97': 'BoFo',
	           '98': 'BaCHe', '99': 'BeBe'}


	lista = []

	cbo = input()

	if cbo in numbers:
		lista.append(numbers.get(cbo))
	print(lista)
	main()
if __name__ == '__main__':
	main()
```

# Clase area de triangulo

```python

class RightTriangle:
    def __init__(self, hyp, leg_1, leg_2):
        self.hyp = hyp
        self.leg_1 = leg_1
        self.leg_2 = leg_2
        self.area = 0.5 * leg_1 * leg_2


input_c, input_a, input_b = [int(x) for x in input().split()]
right = RightTriangle(input_c, input_a, input_b)

if right.hyp ** 2 == right.leg_1 ** 2 + right.leg_2 ** 2:
    print(right.area)
else:
    print("Not right")
```

# Tomar la letra segun la posicion

```python
customer_name = "John Milton"

letra2 = customer_name[0]
print(letra2)
```

