---
title: 3.2 Creación de Excepciones Personalizadas
linktitle: 3.2 Creación de Excepciones Personalizadas
type: book
date: '2024-01-20T00:00:00Z'
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
tags: 
weight: 3
---

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
