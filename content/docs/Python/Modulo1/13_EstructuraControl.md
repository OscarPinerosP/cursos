---
title: 1.3 Estructuras de Control
linktitle: 1.3 Estructuras de Control
type: book
date: '2024-01-20T00:00:00Z'
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
tags: 
weight: 4
---

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
