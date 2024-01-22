---
title: Módulo 5 Programación Funcional en Python
linktitle: Módulo 5 Programación Funcional en Python
type: book
date: '2024-01-20T00:00:00Z'
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
tags: 
weight: 6
---


La programación funcional es un paradigma de programación que trata los cálculos como evaluaciones de funciones matemáticas y evita cambiar estados y datos mutables. Se basa en el concepto matemático de funciones y se centra en la inmutabilidad de los datos, la ausencia de efectos secundarios y la aplicación de funciones de primera clase.

En Python, aunque el lenguaje no es puramente funcional, soporta muchos conceptos y técnicas de programación funcional. Aquí hay algunas características clave de la programación funcional en Python:

## **5.1 Funciones de primera clase**

En Python, las funciones son objetos de primera clase, lo que significa que puedes pasar funciones como argumentos a otras funciones, devolver funciones como resultados y asignar funciones a variables.

```python
def cuadrado(x): return x ** 2
def aplicar_funcion(func, valor): return func(valor)
resultado = aplicar_funcion(cuadrado, 5)
print(resultado) # Imprimirá 25
```

## **5.2 Funciones lambda**

Puedes definir funciones anónimas y pequeñas utilizando expresiones lambda.

```python
cuadrado = lambda x: x ** 2
resultado = cuadrado(5)
print(resultado) # Imprimirá 25
```

## **5.3 Map, Filter y Reduce**

Python proporciona funciones integradas como `map()`, `filter()`, y `functools.reduce()` que son comunes en la programación funcional.

```python
# Ejemplo de map()
lista = [1, 2, 3, 4, 5]
cuadrados = list(map(lambda x: x ** 2, lista))
print(cuadrados) # Imprimirá [1, 4, 9, 16, 25]
# Ejemplo de filter()
pares = list(filter(lambda x: x % 2 == 0, lista))
print(pares) # Imprimirá [2, 4]
# Ejemplo de reduce()
from functools import reduce
suma = reduce(lambda x, y: x + y, lista)
print(suma) # Imprimirá 15
```

## **5.4 Comprensiones de listas**

Python permite construir listas utilizando comprensiones de listas, que es una forma concisa y expresiva de aplicar transformaciones a los elementos de una lista.

```python
# Comprensión de lista para obtener cuadrados de los números pares
numeros = [1, 2, 3, 4, 5]
cuadrados_pares = [x ** 2 for x in numeros if x % 2 == 0]
print(cuadrados_pares) # Imprimirá [4, 16]
```

## **5.5 Inmutabilidad**

Aunque Python no es un lenguaje puramente funcional, puedes escribir código que favorezca la inmutabilidad, evitando la modificación directa de datos y prefiriendo la creación de nuevos objetos.

```python
# Ejemplo de inmutabilidad
lista_original = [1, 2, 3]
lista_modificada = lista_original + [4] # Crear una nueva lista en lugar de modificar la original
print(lista_original) # Imprimirá [1, 2, 3]
print(lista_modificada) # Imprimirá [1, 2, 3, 4]
```

La programación funcional en Python permite escribir código más claro, modular y fácil de entender en muchos casos. Sin embargo, la elección de utilizar enfoques funcionales o imperativos depende del problema específico y de las preferencias del programador. En Python, es común combinar ambos estilos de programación según sea necesario.

## 5.4 Ejercicios Prácticos

- **Ejercicio 1:**
- Crear una función lambda y utilizarla en una función de orden superior.
- **Ejercicio 2:**
- Aplicar comprensiones de listas para filtrar y transformar datos.
- **Ejercicio 3:**
- Utilizar funciones de orden superior incorporadas en Python.
