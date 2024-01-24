---
title: 1.4 Funciones y Modularidad
linktitle: 1.4 Funciones y Modularidad
type: book
date: '2024-01-20T00:00:00Z'
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
tags: 
weight: 5
---

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
