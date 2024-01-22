---
title: 3.1 Try, Except y Finally
linktitle: 3.1 Try, Except y Finally
type: book
date: '2024-01-20T00:00:00Z'
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
tags: 
weight: 2
---

En Python, el manejo de excepciones se realiza mediante los bloques `try` y `except`. Estos bloques permiten gestionar situaciones excepcionales o errores que pueden ocurrir durante la ejecución de un programa. La idea principal es intentar ejecutar un bloque de código dentro de `try` y, si ocurre una excepción, manejarla de manera controlada en el bloque `except`.

### Estructura básica del manejo de excepciones

```python
try:
    # Bloque de código que puede generar una excepción
    resultado = 10 / 0  # Genera una excepción de división por cero
except Exception as error:
    # Bloque de código que se ejecuta si se produce una excepción
    print(f"Se produjo un error: {error}")
```

En este ejemplo, el código dentro del bloque `try` intenta realizar una operación de división por cero, lo cual generará una excepción. El bloque `except` se encargará de manejar la excepción, imprimir un mensaje y continuar con la ejecución del programa.

### Tipos de excepciones

Puedes capturar excepciones específicas dependiendo del tipo de error que estés esperando. Por ejemplo, si estás trabajando con archivos, puedes capturar excepciones relacionadas con la manipulación de archivos.

```python
try:
    # Bloque de código que puede generar una excepción
    with open("archivo_inexistente.txt", "r") as archivo:
        contenido = archivo.read()
except FileNotFoundError:
    # Bloque de código específico para manejar el error de archivo no encontrado
    print("El archivo no se encontró.")
except Exception as error:
    # Bloque de código para manejar otras excepciones
    print(f"Se produjo un error: {error}")
```

### Bloque `else` y `finally`

Además de `try` y `except`, puedes utilizar los bloques `else` y `finally`. El bloque `else` se ejecuta si no se produce ninguna excepción en el bloque `try`, y el bloque `finally` se ejecuta siempre, independientemente de si se produjo una excepción o no.

```python
try:
    # Bloque de código que puede generar una excepción
    resultado = 10 / 2
except ZeroDivisionError:
    # Bloque de código para manejar el error de división por cero
    print("¡Error! División por cero.")
else:
    # Bloque de código que se ejecuta si no se produce una excepción
    print("El resultado es:", resultado)
finally:
    # Bloque de código que se ejecuta siempre
    print("Fin del bloque try-except.")
```

Estos bloques adicionales proporcionan flexibilidad en el manejo de excepciones y permiten realizar acciones específicas según el flujo de ejecución del programa. Es importante señalar que es una buena práctica capturar únicamente las excepciones que se esperan y no capturar todas las excepciones indiscriminadamente, a menos que sea estrictamente necesario. Esto ayuda a identificar y solucionar problemas de manera más eficiente.
