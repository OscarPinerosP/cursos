---
title: Diccionarios
linktitle: Diccionarios
type: book
date: '2024-01-20T00:00:00Z'
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
tags: 
weight: 6
---


## 2.3 Diccionarios

En Python, un diccionario es una colección no ordenada de pares clave-valor. Cada elemento en un diccionario consiste en una clave y su correspondiente valor. Los diccionarios son útiles para representar relaciones entre datos y permiten acceder eficientemente a los valores utilizando las claves.

### Crear un diccionario

Los diccionarios se crean utilizando llaves `{}` y especificando pares clave-valor separados por comas.

```python
# Crear un diccionario de información del estudiante
estudiante = {
    "nombre": "Juan",
    "edad": 20,
    "curso": "Python",
    "calificaciones": [90, 85, 88]
}

# Crear un diccionario vacío
diccionario_vacio = {}
```

### Acceder a los elementos de un diccionario

Puedes acceder a los valores utilizando las claves.

```python
nombre_estudiante = estudiante["nombre"]  # Acceder al valor de la clave "nombre"
calificaciones = estudiante["calificaciones"]  # Acceder al valor de la clave "calificaciones"
```

### Métodos básicos de los diccionarios

Algunos de los métodos básicos de los diccionarios incluyen:

- **`keys()`:** Devuelve una vista de todas las claves en el diccionario.

    ```python
    claves = estudiante.keys()
    print(claves) # Imprimirá dict_keys(['nombre', 'edad', 'curso', 'calificaciones'])
    ```

- **`values()`:** Devuelve una vista de todos los valores en el diccionario.

    ```python
    valores = estudiante.values()
    print(valores) # Imprimirá dict_values(['Juan', 20, 'Python', [90, 85, 88]])
    ```

- **`items()`:** Devuelve una vista de todos los pares clave-valor en el diccionario.

    ```python
    items = estudiante.items()
    print(items) # Imprimirá dict_items([('nombre', 'Juan'), ('edad', 20), ('curso', 'Python'), ('calificaciones', [90, 85, 88])])
    ```

- **`get(clave, valor_por_defecto)`:** Devuelve el valor asociado con la clave dada. Si la clave no existe, devuelve el valor por defecto especificado.

    ```python
    edad_estudiante = estudiante.get("edad", 0)
    print(edad_estudiante) # Imprimirá 20
    ciudad_estudiante = estudiante.get("ciudad", "Desconocida")
    print(ciudad_estudiante) # Imprimirá "Desconocida"
    ```

- **`update(diccionario)`:** Actualiza el diccionario con elementos de otro diccionario o de una secuencia de pares clave-valor.

    ```python
    nuevo_diccionario = {"ciudad": "Ciudad del Este", "nota_final": 92}
    estudiante.update(nuevo_diccionario)
    print(estudiante)
    # Imprimirá {'nombre': 'Juan', 'edad': 20, 'curso': 'Python', 'calificaciones': [90, 85, 88], 'ciudad': 'Ciudad del Este', 'nota_final': 92}
    ```

Aquí algunos otros ejemplos de manejo de diccionarios, para acceder a los elementos de un diccionario, utiliza la clave correspondiente.

```python
# Crear un diccionario
mi_diccionario = {"nombre": "Juan", "edad": 25, "ciudad": "Ciudad del Este"}

# Acceder a un valor mediante su clave
nombre = mi_diccionario["nombre"]
edad = mi_diccionario["edad"]
ciudad = mi_diccionario["ciudad"]

print(nombre, edad, ciudad)
# Imprimirá "Juan 25 Ciudad del Este"
```

### Elementos de un diccionario

Los elementos de un diccionario son los pares clave-valor. En el ejemplo anterior, `"nombre"`, `"edad"` y `"ciudad"` son las claves, y `"Juan"`, `25` y `"Ciudad del Este"` son los valores asociados.

### Adicionar o modificar un elemento en un diccionario

Puedes agregar o modificar un elemento en un diccionario asignando un nuevo valor a una clave existente o a una clave nueva.

```python
# Agregar un nuevo elemento
mi_diccionario["profesion"] = "Programador"

# Modificar un elemento existente
mi_diccionario["edad"] = 26

print(mi_diccionario)
# Imprimirá {'nombre': 'Juan', 'edad': 26, 'ciudad': 'Ciudad del Este', 'profesion': 'Programador'}
```

### Eliminar un elemento de un diccionario

Puedes eliminar un elemento de un diccionario utilizando la palabra clave `del` seguida de la clave.

```python
# Eliminar un elemento
del mi_diccionario["ciudad"]

print(mi_diccionario)
# Imprimirá {'nombre': 'Juan', 'edad': 26, 'profesion': 'Programador'}
```

### Métodos para operaciones en diccionarios

Además de las operaciones básicas mencionadas, hay varios métodos que puedes utilizar para realizar operaciones en diccionarios, como `pop()`, `popitem()`, `keys()`, `values()`, `items()`, entre otros. Aquí hay un ejemplo de algunos de estos métodos:

```python
# Crear un diccionario
mi_diccionario = {"nombre": "Juan", "edad": 25, "ciudad": "Ciudad del Este"}

# Eliminar un elemento con pop()
edad_eliminada = mi_diccionario.pop("edad")

# Obtener y eliminar el último elemento con popitem()
ultimo_elemento = mi_diccionario.popitem()

# Obtener las claves con keys()
claves = mi_diccionario.keys()

# Obtener los valores con values()
valores = mi_diccionario.values()

# Obtener los pares clave-valor con items()
pares_clave_valor = mi_diccionario.items()

print(edad_eliminada)
# Imprimirá 25

print(ultimo_elemento)
# Imprimirá ('ciudad', 'Ciudad del Este')

print(claves)
# Imprimirá dict_keys(['nombre', 'edad'])

print(valores)
# Imprimirá dict_values(['Juan', 25])

print(pares_clave_valor)
# Imprimirá dict_items([('nombre', 'Juan'), ('edad', 25)])
```

Estos son solo algunos de los métodos básicos disponibles para los diccionarios en Python. Los diccionarios son estructuras de datos versátiles y ampliamente utilizadas en Python.
