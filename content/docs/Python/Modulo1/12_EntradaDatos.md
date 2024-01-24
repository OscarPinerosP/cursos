---
title: 1.2 Entrada de Datos
linktitle: 1.2 Entrada de Datos
type: book
date: '2024-01-20T00:00:00Z'
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
tags: 
weight: 3
---

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
