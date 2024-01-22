---
title: Cadenas o Strings, Acceso y Manipulación de Cadenas
linktitle: Cadenas o Strings, Acceso y Manipulación de Cadenas
type: book
date: '2024-01-20T00:00:00Z'
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
tags: 
weight: 6
---

## 2.5 Cadenas o Strings, Acceso y Manipulación de Cadenas

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
