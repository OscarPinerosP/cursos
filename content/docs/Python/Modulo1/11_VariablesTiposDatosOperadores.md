---
title: 1.1 Variables, Tipos de Datos y Operadores
linktitle: 1.1 Variables, Tipos de Datos y Operadores
type: book
date: '2024-01-20T00:00:00Z'
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
tags: 
weight: 4
---

### **Variables**

En programación Python, las variables son nombres simbólicos que se utilizan para almacenar y manipular datos en la memoria de un computador. Estos nombres están asociados a ubicaciones específicas en la memoria que contienen valores, como números, cadenas de texto, listas, objetos, entre otros. Las variables permiten a los programadores referirse a estos valores mediante un nombre significativo en lugar de tener que recordar la ubicación exacta en la memoria.

Para declarar una variable en Python, simplemente se asigna un valor a un nombre utilizando el operador de asignación (`=`). Aquí hay un ejemplo simple:

```python
# Declaración de una variable llamada 'edad' con el valor 25
edad = 25

# Declaración de una variable llamada 'nombre' con el valor "Juan"
nombre = "Juan"

# Declaración de una variable llamada 'lista_numeros' con una lista de números
lista_numeros = [1, 2, 3, 4, 5]

```

En el código anterior, `edad`, `nombre` y `lista_numeros` son nombres de variables, y cada uno tiene asignado un valor específico.

Es importante destacar que en Python no es necesario declarar explícitamente el tipo de variable, ya que el intérprete de Python infiere automáticamente el tipo de datos basándose en el valor asignado. Por ejemplo, en el código anterior, Python entenderá que `edad` es un entero (`int`), `nombre` es una cadena de texto (`str`), y `lista_numeros` es una lista (`list`).

### **Tipos de Datos Básicos**

Python ofrece varios tipos de datos básicos para trabajar con diferentes tipos de información. Aquí hay algunos de los tipos de datos más comunes en Python, junto con ejemplos:

- **Enteros (int):**
Representan números enteros sin decimales.

```python
edad = 25
numero_negativo = -10
```

- **Flotantes (float):**
Representan números con decimales.

```python
altura = 1.75
precio = 19.99
```

- **Cadenas de texto (str):**
Representan secuencias de caracteres.

    ```python
    nombre = "Juan"
    mensaje = 'Hola, ¿cómo estás?'
    ```

- **Booleanos (bool):**
Representan valores de verdad: Verdadero (`True`) o Falso (`False`).

    ```python
    es_mayor_de_edad = True
    esta_lloviendo = False
    ```

- **Listas:**
Almacenan secuencias ordenadas de elementos.

```python
numeros = [1, 2, 3, 4, 5]
colores = ['rojo', 'verde', 'azul']
```

- **Tuplas:**
Son similares a las listas, pero son inmutables (no pueden ser modificadas después de la creación).

```python
coordenadas = (10, 20)
dias_semana = ('lunes', 'martes', 'miércoles')
```

- **Diccionarios:**
Almacenan pares clave-valor para representar información estructurada.

```python
estudiante = {'nombre': 'Ana', 'edad': 21, 'curso': 'Python'}
```

- **Conjuntos:**
Colecciones no ordenadas de elementos únicos.

    ```python
    numeros_primos = {2, 3, 5, 7, 11}
    ```

Estos son solo algunos ejemplos de los tipos de datos básicos en Python. La flexibilidad en el manejo de tipos de datos es una de las características clave de Python.

### **La función type()**

La función `type()` en Python se utiliza para obtener el tipo de un objeto o valor. Puedes pasar un valor como argumento a la función `type()` y te devolverá el tipo de ese valor. Aquí tienes un ejemplo:

```python
edad = 25
tipo_edad = type(edad)

print(tipo_edad)  # Esto imprimirá <class 'int'>
```

En este ejemplo, `type(edad)` devuelve el tipo de la variable `edad`, que es un entero (`int`). La función `type()` es útil cuando necesitas verificar el tipo de un objeto en tiempo de ejecución o cuando deseas realizar ciertas operaciones según el tipo de dato de una variable.

Puedes utilizar `type()` con otros tipos de datos y objetos, como cadenas, listas, diccionarios, funciones, etc. Por ejemplo:

```python
nombre = "Juan"
tipo_nombre = type(nombre)

print(tipo_nombre)  # Esto imprimirá <class 'str'>

lista_numeros = [1, 2, 3, 4, 5]
tipo_lista = type(lista_numeros)

print(tipo_lista)  # Esto imprimirá <class 'list'>
```

Esta función es especialmente útil en situaciones donde necesitas realizar comprobaciones de tipo dinámicamente en tu código.

### **Operadores Básicos**

Python incluye una variedad de operadores básicos que permiten realizar diferentes operaciones en variables y valores. Aquí algunos de los operadores básicos en Python, junto con ejemplos:

- **Operadores Aritméticos:**
- `+` : Suma
- `-` : Resta
- `*` : Multiplicación
- `/` : División
- `%` : Módulo (devuelve el resto de la división)
- `*` : Exponenciación

```python
a = 10
b = 3
suma = a + b # 13
resta = a - b # 7
multiplicacion = a * b # 30
division = a / b # 3.3333 (en Python 3)
modulo = a % b # 1
exponente = a ** b # 1000
```

- **Operadores de Comparación:**
- `==` : Igual a
- `!=` : No igual a
- `<` : Menor que
- `>` : Mayor que
- `<=` : Menor o igual que
- `>=` : Mayor o igual que

```python
x = 5
y = 10
igual = x == y # False
no_igual = x != y # True
menor_que = x < y # True
mayor_que = x > y # False
menor_o_igual = x <= y # True
mayor_o_igual = x >= y # False
```

- **Operadores Lógicos:**
- `and` : Operador lógico AND
- `or` : Operador lógico OR
- `not` : Operador lógico NOT

    ```python
    a = True
    b = False
    resultado_and = a and b # False
    resultado_or = a or b # True
    resultado_not = not a # False
    ```

- **Operadores de Asignación:**
- `=` : Asignación simple
- `+=`, `=`, `=`, `/=` : Asignación con operación aritmética

    ```python
    x = 5
    x += 3 # Equivalente a x = x + 3 (x ahora es 8)
    ```

Estos son solo algunos ejemplos de los operadores básicos en Python. Puedes combinar estos operadores para realizar operaciones más complejas y expresiones en tu código.
