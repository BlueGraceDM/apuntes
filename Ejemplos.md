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

