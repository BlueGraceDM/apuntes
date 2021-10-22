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

