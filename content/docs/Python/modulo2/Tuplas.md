---
title: Tuplas
linktitle: Tuplas
type: book
date: '2024-01-20T00:00:00Z'
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
tags: 
weight: 3
---

## 2.2 Tuplas

En Python, una tupla es una colección ordenada e inmutable de elementos. La principal diferencia entre listas y tuplas radica en la mutabilidad: las listas son mutables (sus elementos pueden cambiarse), mientras que las tuplas son inmutables (una vez creadas, no pueden modificarse). Las tuplas se utilizan cuando se desea asegurar que los datos no cambien durante la ejecución del programa.

### Crear una tupla

Las tuplas se crean utilizando paréntesis `()` y separando los elementos por comas.

```python
# Crear una tupla de números
numeros = (1, 2, 3, 4, 5)

# Crear una tupla de strings
frutas = ("manzana", "naranja", "uva")

# Crear una tupla mixta
mixta = (1, "dos", 3.0, True)
```

### Acceder a los elementos de una tupla

Puedes acceder a los elementos de una tupla utilizando índices, de manera similar a las listas.

```python
frutas = ("manzana", "naranja", "uva")

primera_fruta = frutas[0]  # Acceder a la primera fruta ("manzana")
segunda_fruta = frutas[1]  # Acceder a la segunda fruta ("naranja")
```

### Métodos básicos de las tuplas

Dado que las tuplas son inmutables, tienen menos métodos disponibles en comparación con las listas. Algunos métodos básicos incluyen:

- **`count(elemento)`:** Devuelve el número de veces que aparece el elemento en la tupla.

```python
frutas = ("manzana", "naranja", "uva", "manzana")
cantidad_manzanas = frutas.count("manzana")
print(cantidad_manzanas) # Imprimirá 2
```

- **`index(elemento)`:** Devuelve el índice de la primera ocurrencia del elemento.

    ```python
    frutas = ("manzana", "naranja", "uva", "manzana")
    indice_naranja = frutas.index("naranja")
    print(indice_naranja) # Imprimirá 1
    ```

- **`len()`:** Devuelve la longitud (número de elementos) de la tupla.

    ```python
    frutas = ("manzana", "naranja", "uva")
    longitud = len(frutas)
    print(longitud) # Imprimirá 3
    ```

Las tuplas proporcionan una manera eficiente de almacenar datos inmutables y son especialmente útiles cuando se quiere garantizar que ciertos valores no cambien a lo largo del tiempo.
