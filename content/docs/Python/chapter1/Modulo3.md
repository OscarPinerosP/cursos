---
title: Módulo 3 Manejo de Errores y Excepciones
linktitle: Módulo 3 Manejo de Errores y Excepciones
type: book
date: '2024-01-20T00:00:00Z'
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
tags: 
weight: 4
---


## 3.1 Try, Except y Finally

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

## 3.2 Creación de Excepciones Personalizadas

En Python, puedes crear excepciones personalizadas creando una nueva clase que herede de la clase base `Exception` o de una clase específica de excepción. Al crear tus propias excepciones, puedes proporcionar información adicional y manejar situaciones específicas de error de una manera más estructurada. Aquí tienes un ejemplo básico de cómo puedes crear una excepción personalizada:

```python
class MiExcepcionPersonalizada(Exception):
    def __init__(self, mensaje="Se produjo un error personalizado."):
        self.mensaje = mensaje
        super().__init__(self.mensaje)

# Ejemplo de uso de la excepción personalizada
def funcion_que_puede_generar_error(valor):
    if valor < 0:
        raise MiExcepcionPersonalizada("El valor no puede ser negativo.")

# Uso de la función
try:
    valor_ingresado = int(input("Ingrese un número positivo: "))
    funcion_que_puede_generar_error(valor_ingresado)
except MiExcepcionPersonalizada as error:
    print(f"Error personalizado: {error}")
except ValueError:
    print("Error: Ingrese un número válido.")
```

En este ejemplo, se define una nueva clase de excepción llamada `MiExcepcionPersonalizada`, que hereda de la clase base `Exception`. Esta clase tiene un método `__init__` para inicializar la excepción con un mensaje predeterminado, pero también puedes personalizarlo al crear una instancia de la excepción.

Luego, se utiliza esta excepción personalizada en una función (`funcion_que_puede_generar_error`). Si el valor ingresado es negativo, la función lanza la excepción personalizada.

En el bloque `try`, se llama a la función y se captura la excepción personalizada `MiExcepcionPersonalizada`. Si se produce esta excepción, se imprime el mensaje personalizado asociado.

Crear excepciones personalizadas es útil cuando deseas distinguir entre diferentes tipos de errores en tu código y proporcionar información específica sobre el error que ocurrió. Esto puede facilitar la depuración y el mantenimiento del código.

- **Definición de Excepciones Personalizadas:**
- Creación de clases para excepciones personalizadas.
- Herencia de la clase base `Exception`.

## 3.3 Ejercicios Prácticos

- **Ejercicio 1:**
- Utilizar un bloque try-except para manejar la división por cero.
- **Ejercicio 2:**
- Crear una excepción personalizada y manejarla en un programa.
- **Ejercicio 3:**
- Gestionar excepciones al leer o escribir en un archivo.
