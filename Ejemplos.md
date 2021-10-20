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

