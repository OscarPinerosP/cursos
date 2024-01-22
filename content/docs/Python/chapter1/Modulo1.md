---
title: Módulo 1 Conceptos Básicos de Programación en Python
linktitle: Módulo 1 Conceptos Básicos de Programación en Python
type: book
date: '2019-05-05T00:00:00+01:00'
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
tags: 
weight: 4
---


## 1.1 Variables, Tipos de Datos y Operadores

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

## 1.2 Entrada de Datos

En Python, la entrada de datos se realiza comúnmente mediante la función `input()`.

El método `input()` función permite al usuario ingresar datos desde el teclado, y la entrada se devuelve como una cadena. Aquí tienes algunos ejemplos de cómo utilizar `input()` para obtener entrada de datos:

### Ejemplo simple

```python
# Pedir al usuario que ingrese su nombre
nombre = input("Ingrese su nombre: ")

# Imprimir un saludo con el nombre ingresado
print("Hola, " + nombre + "!")
```

### Convertir la entrada a otros tipos de datos

Dado que `input()` devuelve una cadena, si necesitas que la entrada sea de otro tipo (por ejemplo, entero o flotante), debes convertirla utilizando las funciones `int()` o `float()`.

```python
# Pedir al usuario que ingrese un número entero
numero_entero = int(input("Ingrese un número entero: "))

# Pedir al usuario que ingrese un número decimal
numero_decimal = float(input("Ingrese un número decimal: "))

# Realizar alguna operación con los números ingresados
suma = numero_entero + numero_decimal
print("La suma es:", suma)
```

### Manipular la entrada

Puedes realizar manipulaciones adicionales en la entrada antes de usarla, como dividirla en partes o aplicar condiciones.

```python
# Pedir al usuario que ingrese una lista de nombres separados por comas
nombres_str = input("Ingrese una lista de nombres separados por comas: ")

# Dividir la entrada en una lista de nombres
lista_nombres = nombres_str.split(',')

# Imprimir los nombres ingresados
print("Nombres ingresados:", lista_nombres)
```

Recuerda que la entrada de `input()` siempre se trata como una cadena, así que debes convertirla según sea necesario.

Es importante señalar que la función `input()` detiene la ejecución del programa hasta que el usuario ingrese datos y presione "Enter". Además, ten en cuenta que la entrada del usuario es tratada como texto, por lo que si esperas un número, deberás convertir la entrada a un tipo numérico.

## 1.3 Estructuras de Control

Las estructuras condicionales en Python permiten ejecutar diferentes bloques de código según una condición especificada. Las estructuras condicionales más comunes son `if`, `else`, y `elif` (abreviatura de "else if"). Aquí hay algunos ejemplos:

### Estructura `if` simple

```python
edad = 18

if edad >= 18:
    print("Eres mayor de edad")
```

En este ejemplo, el bloque de código dentro del `if` se ejecutará solo si la condición `edad >= 18` es verdadera.

### Estructura `if` con `else`

```python
edad = 16

if edad >= 18:
    print("Eres mayor de edad")
else:
    print("Eres menor de edad")
```

En este caso, si la condición del `if` es falsa, se ejecutará el bloque de código dentro del `else`.

### Estructura `if` con `elif`

```python
puntaje = 75

if puntaje >= 90:
    print("Excelente")
elif puntaje >= 70:
    print("Bien hecho")
else:
    print("Necesitas mejorar")
```

Aquí, se evalúan múltiples condiciones en orden. Si la primera condición (`puntaje >= 90`) es verdadera, se ejecuta el bloque de código dentro del primer `if`. Si no, se verifica la siguiente condición (`puntaje >= 70`) en el `elif`. Si ninguna de las condiciones anteriores es verdadera, se ejecuta el bloque dentro del `else`.

### Estructuras condicionales anidadas

```python
temperatura = 25

if temperatura > 30:
    print("Hace mucho calor")
else:
    if temperatura > 20:
        print("Está agradable")
    else:
        print("Hace frío")
```

En este ejemplo, se tienen estructuras condicionales anidadas. Si la primera condición del `if` es falsa, se evalúa la condición del `else`, y se puede tener otra estructura condicional dentro de este bloque.

Estas son algunas de las formas básicas de usar estructuras condicionales en Python. Puedes combinarlas y anidarlas según las necesidades de tu programa.

### Bucles

Los bucles en Python son estructuras que permiten ejecutar un bloque de código repetidamente, ya sea un número específico de veces o hasta que se cumpla una condición. Los dos tipos principales de bucles en Python son el bucle `for` y el bucle `while`.

### Bucle `for`

El bucle `for` se utiliza para iterar sobre una secuencia (como una lista, tupla, cadena de texto, etc.) o cualquier objeto iterable.

### Ejemplo 1: Iterando sobre una lista

```python
frutas = ["manzana", "banana", "cereza"]

for fruta in frutas:
    print(fruta)
```

Este bucle `for` itera sobre la lista `frutas` e imprime cada elemento de la lista.

### Ejemplo 2: Utilizando la función `range()`

```python
for i in range(5):
    print(i)
```

Este bucle `for` utiliza la función `range(5)` para generar una secuencia de números del 0 al 4, e imprime cada número.

### Bucle `while`

El bucle `while` se utiliza para repetir un bloque de código mientras una condición sea verdadera.

### Ejemplo 1: Bucle `while` simple

```python
contador = 0

while contador < 5:
    print(contador)
    contador += 1
```

Este bucle `while` imprime los números del 0 al 4. La condición `contador < 5` se verifica en cada iteración.

### Ejemplo 2: Bucle `while` con `break`

```python
numero = 0

while True:
    print(numero)
    numero += 1

    if numero >= 5:
        break
```

Este bucle `while` se ejecuta indefinidamente hasta que se encuentra la instrucción `break` cuando `numero` alcanza el valor 5.

Ambos bucles, `for` y `while`, son herramientas poderosas que permiten automatizar tareas repetitivas en un programa. La elección entre ellos depende de la situación y de la lógica específica que deseas implementar.

### Ejemplo 3: Un bucle `while` que utiliza `break` y `continue`

```python
numero = 0

while numero < 10:
    numero += 1

    # Saltar los números impares
    if numero % 2 != 0:
        continue

    print(numero)

    # Salir del bucle si el número alcanza 6
    if numero == 6:
        break
```

En este ejemplo:

- `continue` se utiliza para saltar los números impares. Si el número actual es impar, el bucle se salta a la siguiente iteración sin ejecutar el resto del código dentro del bucle.
- `break` se utiliza para salir del bucle cuando el número alcanza el valor 6.

La salida de este código será:

```python
2
4
6
```

Aquí, el bucle `while` imprime los números pares del 2 al 6 y luego sale del bucle cuando el número alcanza el valor 6 debido a la instrucción `break`.

## 1.4 Funciones y Modularidad

En Python, una función es un bloque de código reutilizable que realiza una tarea específica. Las funciones permiten dividir un programa en bloques más pequeños y modularizar el código, facilitando su mantenimiento y reutilización. La estructura básica de una función en Python es la siguiente:

```python
def nombre_de_la_funcion(parametro1, parametro2, ...):
    # Cuerpo de la función
    # Realiza operaciones utilizando los parámetros

    # Opcional: Puede tener un valor de retorno
    return resultado

```

Donde:

- `def` es la palabra clave utilizada para definir una función.
- `nombre_de_la_funcion` es el nombre que le asignas a la función.
- `(parametro1, parametro2, ...)`: Los parámetros son valores que la función espera recibir cuando se llama. Estos son opcionales.
- `:` indica el inicio del cuerpo de la función, y todo el código indentado debajo de la declaración de la función forma parte de la función.
- `return resultado`: La declaración `return` se utiliza para devolver un valor opcional desde la función.

Ejemplo de una función simple sin parámetros y sin valor de retorno:

```python
def saludar():
    print("¡Hola, mundo!")

# Llamada a la función
saludar()
```

Ejemplo de una función con parámetros y valor de retorno:

```python
def sumar(a, b):
    resultado = a + b
    return resultado

# Llamada a la función
resultado_suma = sumar(3, 5)
print(resultado_suma)  # Imprimirá 8
```

En este ejemplo, `sumar` es una función que toma dos parámetros (`a` y `b`), realiza la suma y devuelve el resultado.

Los términos "parámetros" y "argumentos" se utilizan a menudo de manera intercambiable, pero hay una distinción técnica:

- **Parámetros:** Son los nombres de las variables utilizadas en la definición de la función.
- **Argumentos:** Son los valores reales que se pasan a la función cuando esta se llama.

En el ejemplo anterior, `a` y `b` son parámetros de la función `sumar`, mientras que cuando llamamos a `sumar(3, 5)`, `3` y `5` son los argumentos que se pasan a la función.

### **Módulos y Reutilización de Código**

En Python, un módulo es un archivo que contiene definiciones y declaraciones de Python. Estas definiciones y declaraciones pueden incluir funciones, variables y clases. La idea principal detrás de los módulos es organizar el código en archivos separados para facilitar la reutilización y el mantenimiento.

La reutilización de código es un concepto fundamental en programación que se refiere a la práctica de escribir código de manera que pueda ser utilizado en diferentes partes de un programa o incluso en diferentes programas. Al dividir el código en funciones, clases o módulos, puedes reutilizar esos componentes en lugar de tener que volver a escribir el mismo código una y otra vez.

La importación de módulos y funciones en Python se realiza mediante la palabra clave `import`. Aquí hay algunos ejemplos:

### Importar un módulo completo

```python
# Importar todo el módulo math
import math

# Utilizar una función del módulo math
raiz_cuadrada = math.sqrt(25)
print(raiz_cuadrada)  # Imprimirá 5.0
```

En este ejemplo, estamos importando el módulo `math` y utilizando la función `sqrt()` del módulo para calcular la raíz cuadrada de 25.

### Importar una función específica de un módulo

```python
# Importar solo la función sqrt del módulo math
from math import sqrt

# Utilizar la función directamente sin usar el nombre del módulo
raiz_cuadrada = sqrt(36)
print(raiz_cuadrada)  # Imprimirá 6.0
```

En este caso, solo importamos la función `sqrt` del módulo `math` y la utilizamos directamente sin tener que usar el nombre del módulo.

### Renombrar un módulo o función durante la importación

```python
# Importar el módulo math y renombrarlo como mt
import math as mt

# Utilizar la función sqrt utilizando el nuevo nombre del módulo
raiz_cuadrada = mt.sqrt(16)
print(raiz_cuadrada)  # Imprimirá 4.0
```

En este ejemplo, hemos importado el módulo `math` pero lo hemos renombrado como `mt` para abreviar.

La importación de módulos y funciones en Python permite una gestión eficiente del código, facilitando la organización y reutilización de funcionalidades en diferentes partes de un programa o en proyectos distintos.

## 1.5 Ejercicios Prácticos

- **Ejercicio 1:**
- Crear una función que calcule el área de un rectángulo.
- **Ejercicio 2:**
- Utilizar estructuras condicionales para determinar si un número es par o impar.
- **Ejercicio 3:**
- Implementar un bucle que genere la serie de Fibonacci hasta un número dado.
