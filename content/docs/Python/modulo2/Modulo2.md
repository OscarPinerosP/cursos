---
title: Módulo 2 Estructuras de Datos en Python
linktitle: Módulo 2 Estructuras de Datos en Python
type: book
date: '2024-01-20T00:00:00Z'
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
tags: 
weight: 6
---


## 2.1 Listas, Tuplas y Diccionarios

### **Listas**

En Python, una lista es una colección ordenada y mutable de elementos. Los elementos en una lista pueden ser de cualquier tipo, y la lista puede contener diferentes tipos de datos. Las listas son una de las estructuras de datos más utilizadas en Python. Aquí hay información sobre cómo crear listas, acceder a sus elementos y algunos métodos básicos.

### Crear una lista

Las listas se crean utilizando corchetes `[]` y separando los elementos por comas.

```python
# Crear una lista de números
numeros = [1, 2, 3, 4, 5]

# Crear una lista de strings
frutas = ["manzana", "naranja", "uva"]

# Crear una lista mixta
mixta = [1, "dos", 3.0, True]
```

### Acceder a los elementos de una lista

Puedes acceder a los elementos de una lista utilizando índices. El índice comienza desde 0 para el primer elemento.

```python
frutas = ["manzana", "naranja", "uva"]

primera_fruta = frutas[0]  # Acceder a la primera fruta ("manzana")
segunda_fruta = frutas[1]  # Acceder a la segunda fruta ("naranja")
```

### Métodos básicos de las listas

1. **`append(elemento)`:** Agrega un elemento al final de la lista.

    ```python
    frutas = ["manzana", "naranja", "uva"]
    frutas.append("pera")
    print(frutas) # Imprimirá ["manzana", "naranja", "uva", "pera"]
    ```

- **`insert(posición, elemento)`:** Inserta un elemento en una posición específica de la lista.

    ```python
    frutas = ["manzana", "naranja", "uva"]
    frutas.insert(1, "pera")
    print(frutas) # Imprimirá ["manzana", "pera", "naranja", "uva"]
    ```

- **`remove(elemento)`:** Elimina la primera ocurrencia del elemento especificado.

    ```python
    frutas = ["manzana", "naranja", "uva"]
    frutas.remove("naranja")
    print(frutas) # Imprimirá ["manzana", "uva"]
    ```

- **`pop(posición)`:** Elimina el elemento en la posición especificada (o el último si no se proporciona una posición) y lo devuelve.

    ```python
    frutas = ["manzana", "naranja", "uva"]
    fruta_eliminada = frutas.pop(1)
    print(frutas) # Imprimirá ["manzana", "uva"]
    print(fruta_eliminada) # Imprimirá "naranja"
    ```

- **`len()`:** Devuelve la longitud (número de elementos) de la lista.

    ```python
    frutas = ["manzana", "naranja", "uva"]
    longitud = len(frutas)
    print(longitud) # Imprimirá 3
    ```

Estos son solo algunos de los métodos y operaciones que puedes realizar con listas en Python. Las listas en Python son muy versátiles y se utilizan comúnmente en programación para almacenar y manipular conjuntos de datos.

### **Tuplas**

En Python, una tupla es una colección ordenada e inmutable de elementos. La principal diferencia entre listas y tuplas radica en la mutabilidad: las listas son mutables (sus elementos pueden cambiarse), mientras que las tuplas son inmutables (una vez creadas, no pueden modificarse). Las tuplas se utilizan cuando se desea asegurar que los datos no cambien durante la ejecución del programa.

### Crear una tupla

Las tuplas se crean utilizando paréntesis `()` y separando los elementos por comas.

```python
# Crear una tupla de números
numeros = (1, 2, 3, 4, 5)

# Crear una tupla de strings
frutas = ("manzana", "naranja", "uva")

# Crear una tupla mixta
mixta = (1, "dos", 3.0, True)
```

### Acceder a los elementos de una tupla

Puedes acceder a los elementos de una tupla utilizando índices, de manera similar a las listas.

```python
frutas = ("manzana", "naranja", "uva")

primera_fruta = frutas[0]  # Acceder a la primera fruta ("manzana")
segunda_fruta = frutas[1]  # Acceder a la segunda fruta ("naranja")
```

### Métodos básicos de las tuplas

Dado que las tuplas son inmutables, tienen menos métodos disponibles en comparación con las listas. Algunos métodos básicos incluyen:

- **`count(elemento)`:** Devuelve el número de veces que aparece el elemento en la tupla.

```python
frutas = ("manzana", "naranja", "uva", "manzana")
cantidad_manzanas = frutas.count("manzana")
print(cantidad_manzanas) # Imprimirá 2
```

- **`index(elemento)`:** Devuelve el índice de la primera ocurrencia del elemento.

    ```python
    frutas = ("manzana", "naranja", "uva", "manzana")
    indice_naranja = frutas.index("naranja")
    print(indice_naranja) # Imprimirá 1
    ```

- **`len()`:** Devuelve la longitud (número de elementos) de la tupla.

    ```python
    frutas = ("manzana", "naranja", "uva")
    longitud = len(frutas)
    print(longitud) # Imprimirá 3
    ```

Las tuplas proporcionan una manera eficiente de almacenar datos inmutables y son especialmente útiles cuando se quiere garantizar que ciertos valores no cambien a lo largo del tiempo.

### **Diccionarios**

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

## 2.2 Conjuntos

En Python, un conjunto es una colección no ordenada de elementos únicos. Los conjuntos se utilizan para realizar operaciones de conjunto, como unión, intersección, diferencia y otras operaciones matemáticas en conjuntos. Aquí te explico cómo crear, acceder y realizar algunas operaciones con conjuntos:

### Crear un conjunto

Los conjuntos se crean utilizando llaves `{}` o la función `set()`.

```python
# Crear un conjunto con llaves
frutas = {"manzana", "naranja", "uva"}

# Crear un conjunto con la función set()
numeros = set([1, 2, 3, 4, 5])
```

### Acceder a los elementos de un conjunto

Los conjuntos no tienen índices, por lo que no se pueden acceder a elementos individuales de la misma manera que en listas o tuplas. Sin embargo, puedes verificar si un elemento está presente en un conjunto utilizando la palabra clave `in`.

```python
frutas = {"manzana", "naranja", "uva"}

if "manzana" in frutas:
    print("La manzana está en el conjunto")
```

### Operaciones con conjuntos

- **Unión (`union()` o `|`):** Combina dos conjuntos en un nuevo conjunto, incluyendo todos los elementos únicos.

    ```python
    conjunto1 = {1, 2, 3}
    conjunto2 = {3, 4, 5}
    union_resultado = conjunto1.union(conjunto2)
    # O usando el operador |
    union_resultado_operador = conjunto1 | conjunto2
    print(union_resultado) # Imprimirá {1, 2, 3, 4, 5}
    print(union_resultado_operador) # Imprimirá {1, 2, 3, 4, 5}
    ```

- **Intersección (`intersection()` o `&`):** Encuentra los elementos comunes entre dos conjuntos.

    ```python
    conjunto1 = {1, 2, 3}
    conjunto2 = {3, 4, 5}
    interseccion_resultado = conjunto1.intersection(conjunto2)
    # O usando el operador &
    interseccion_resultado_operador = conjunto1 & conjunto2
    print(interseccion_resultado) # Imprimirá {3}
    print(interseccion_resultado_operador) # Imprimirá {3}
    ```

- **Diferencia (`difference()` o `-`):** Encuentra los elementos en el primer conjunto que no están en el segundo.

    ```python
    conjunto1 = {1, 2, 3}
    conjunto2 = {3, 4, 5}
    diferencia_resultado = conjunto1.difference(conjunto2)
    # O usando el operador -
    diferencia_resultado_operador = conjunto1 - conjunto2
    print(diferencia_resultado) # Imprimirá {1, 2}
    print(diferencia_resultado_operador) # Imprimirá {1, 2}
    ```

- **Diferencia simétrica (`symmetric_difference()` o `^`):** Encuentra los elementos que están en uno de los conjuntos, pero no en ambos.

    ```python
    conjunto1 = {1, 2, 3}
    conjunto2 = {3, 4, 5}
    diferencia_simetrica_resultado = conjunto1.symmetric_difference(conjunto2)
    # O usando el operador ^
    diferencia_simetrica_resultado_operador = conjunto1 ^ conjunto2
    print(diferencia_simetrica_resultado) # Imprimirá {1, 2, 4, 5}
    print(diferencia_simetrica_resultado_operador) # Imprimirá {1, 2, 4, 5}
    ```

Estos son solo algunos ejemplos de las operaciones que puedes realizar con conjuntos en Python. Los conjuntos son útiles para realizar operaciones de conjunto y garantizar que los elementos sean únicos.

A continuación te proporciono ejemplos de cómo eliminar duplicados en una lista utilizando conjuntos y de cómo verificar la pertenencia de elementos con `in`:

### Eliminar duplicados en una lista utilizando conjuntos

```python
# Lista con duplicados
lista_con_duplicados = [1, 2, 2, 3, 4, 4, 5, 6, 6]

# Convertir la lista a un conjunto para eliminar duplicados
conjunto_sin_duplicados = set(lista_con_duplicados)

# Convertir de nuevo el conjunto a una lista (si es necesario)
lista_sin_duplicados = list(conjunto_sin_duplicados)

print(lista_sin_duplicados)
# Imprimirá [1, 2, 3, 4, 5, 6]
```

En este ejemplo, convertimos la lista a un conjunto (`set`) para eliminar los duplicados debido a la propiedad de los conjuntos de contener elementos únicos. Luego, si es necesario, convertimos el conjunto de nuevo a una lista.

### Verificación de pertenencia con `in`

```python
# Conjunto de frutas
frutas = {"manzana", "naranja", "uva", "kiwi"}

# Verificar si "kiwi" está en el conjunto
if "kiwi" in frutas:
    print("Sí, el kiwi está en el conjunto")
else:
    print("No, el kiwi no está en el conjunto")

# Verificar si "pera" está en el conjunto
if "pera" in frutas:
    print("Sí, la pera está en el conjunto")
else:
    print("No, la pera no está en el conjunto")
```

En este ejemplo, utilizamos la expresión `if "elemento" in conjunto` para verificar si un elemento específico está presente en el conjunto. En este caso, verificamos la pertenencia de "kiwi" y "pera" en el conjunto de frutas.

## 2.3 Cadenas o Strings, Acceso y Manipulación de Cadenas

En Python, una cadena o string es una secuencia de caracteres. Las cadenas son un tipo de dato inmutable, lo que significa que no se pueden cambiar una vez que se han creado. Puedes acceder y manipular cadenas de diversas formas. Aquí te proporciono información sobre la indexación, el slicing y algunos métodos básicos para manejar cadenas:

### Acceder a los elementos de una cadena (Indexación)

La indexación se utiliza para acceder a elementos individuales en una cadena. En Python, los índices comienzan desde 0 para el primer carácter. También puedes utilizar índices negativos para contar desde el final de la cadena.

```python
cadena = "Python"

primer_caracter = cadena[0]     # P
segundo_caracter = cadena[1]    # y
ultimo_caracter = cadena[-1]     # n
penultimo_caracter = cadena[-2]  # o
```

### Slicing

El slicing se utiliza para extraer porciones de una cadena utilizando la notación `[inicio:final]`.

```python
cadena = "Python"

subcadena1 = cadena[0:3]   # Pyt (incluye el índice de inicio pero no el de final)
subcadena2 = cadena[2:]    # thon (desde el índice 2 hasta el final)
subcadena3 = cadena[:4]    # Pyth (desde el principio hasta el índice 3)

# Slicing con pasos
subcadena4 = cadena[::2]   # Pto (toma cada segundo carácter)
```

### Métodos básicos para manejo de cadenas

- **`len()`:** Devuelve la longitud (número de caracteres) de la cadena.

    ```python
    cadena = "Python"
    longitud = len(cadena)
    print(longitud) # Imprimirá 6
    ```

- **`upper()`:** Convierte todos los caracteres de la cadena a mayúsculas.

    ```python
    cadena = "python"
    mayusculas = cadena.upper()
    print(mayusculas) # Imprimirá "PYTHON"
    ```

- **`lower()`:** Convierte todos los caracteres de la cadena a minúsculas.

    ```python
    cadena = "Python"
    minusculas = cadena.lower()
    print(minusculas) # Imprimirá "python"
    ```

- **`capitalize()`:** Convierte el primer carácter de la cadena a mayúscula y el resto a minúsculas.

    ```python
    cadena = "python"
    capitalizada = cadena.capitalize()
    print(capitalizada) # Imprimirá "Python"
    ```

- **`replace(subcadena_vieja, subcadena_nueva)`:** Reemplaza todas las ocurrencias de una subcadena con otra.

    ```python
    cadena = "python es divertido"
    nueva_cadena = cadena.replace("divertido", "genial")
    print(nueva_cadena) # Imprimirá "python es genial"
    ```

- **`count(subcadena)`:** Devuelve el número de ocurrencias de una subcadena en la cadena.

    ```python
    cadena = "python es divertido y python es útil"
    ocurrencias = cadena.count("python")
    print(ocurrencias) # Imprimirá 2
    ```

Dado que las cadenas en Python son inmutables, no puedes modificar directamente una cadena existente agregando un carácter. Sin embargo, puedes realizar operaciones que crean nuevas cadenas basadas en la cadena original. Hay algunas maneras de agregar caracteres a una cadena en Python:

### Concatenación

Puedes concatenar (unir) dos cadenas utilizando el operador `+` para agregar caracteres al final de la cadena:

```python
cadena_original = "Hola"
caracter_adicional = "!"

nueva_cadena = cadena_original + caracter_adicional
print(nueva_cadena)  # Imprimirá "Hola!"
```

### Formateo de cadenas

Puedes utilizar formateo de cadenas para crear una nueva cadena que contenga el carácter adicional:

```python
cadena_original = "Hola"
caracter_adicional = "!"

nueva_cadena = "{}{}".format(cadena_original, caracter_adicional)
print(nueva_cadena)  # Imprimirá "Hola!"
```

### Utilizando el operador de multiplicación

Puedes multiplicar una cadena por un número para repetirla y así agregar caracteres al final:

```python
cadena_original = "Hola"
caracter_adicional = "!"

nueva_cadena = cadena_original + (caracter_adicional * 3)
print(nueva_cadena)  # Imprimirá "Hola!!!"
```

Es importante tener en cuenta que en todos estos casos, se está creando una nueva cadena y no modificando la original. Si necesitas realizar muchas operaciones de este tipo y la eficiencia es crítica, podrías considerar el uso de una lista para la manipulación de caracteres y luego convertirla de nuevo a una cadena.

```python
lista_cadena = list("Hola")
caracter_adicional = "!"

lista_cadena.append(caracter_adicional)
nueva_cadena = "".join(lista_cadena)
print(nueva_cadena)  # Imprimirá "Hola!"
```

Recuerda que, en general, la concatenación de cadenas puede ser ineficiente para grandes cantidades de operaciones debido a la creación repetida de nuevas cadenas. En tales casos, se pueden considerar alternativas como el uso de una lista de caracteres y la función `join`, especialmente si estás realizando muchas manipulaciones en la cadena.

Estos son solo algunos ejemplos de métodos básicos para manejar cadenas en Python. Las cadenas son fundamentales en la programación y se utilizan en una variedad de situaciones para manipular y presentar información de texto.

## 2.4 Ejercicios Prácticos

- **Ejercicio 1:**
- Crear una lista de números y realizar operaciones de modificación.
- **Ejercicio 2:**
- Utilizar un diccionario para almacenar información y realizar actualizaciones.
- **Ejercicio 3:**
- Aplicar operaciones de conjunto para manipular datos.
