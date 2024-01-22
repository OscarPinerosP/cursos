---
title: Listas
linktitle: Listas
type: book
date: '2024-01-20T00:00:00Z'
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
tags: 
weight: 6
---


## 2.1 Listas

En Python, una lista es una colección ordenada y mutable de elementos. Los elementos en una lista pueden ser de cualquier tipo, y la lista puede contener diferentes tipos de datos. Las listas son una de las estructuras de datos más utilizadas en Python. Aquí hay información sobre cómo crear listas, acceder a sus elementos y algunos métodos básicos.

### Crear una lista

Las listas se crean utilizando corchetes `[]` y separando los elementos por comas.

```python
# Crear una lista de números
numeros = [1, 2, 3, 4, 5]

# Crear una lista de strings
frutas = ["manzana", "naranja", "uva"]

# Crear una lista mixta
mixta = [1, "dos", 3.0, True]
```

### Acceder a los elementos de una lista

Puedes acceder a los elementos de una lista utilizando índices. El índice comienza desde 0 para el primer elemento.

```python
frutas = ["manzana", "naranja", "uva"]

primera_fruta = frutas[0]  # Acceder a la primera fruta ("manzana")
segunda_fruta = frutas[1]  # Acceder a la segunda fruta ("naranja")
```

### Métodos básicos de las listas

1. **`append(elemento)`:** Agrega un elemento al final de la lista.

    ```python
    frutas = ["manzana", "naranja", "uva"]
    frutas.append("pera")
    print(frutas) # Imprimirá ["manzana", "naranja", "uva", "pera"]
    ```

- **`insert(posición, elemento)`:** Inserta un elemento en una posición específica de la lista.

    ```python
    frutas = ["manzana", "naranja", "uva"]
    frutas.insert(1, "pera")
    print(frutas) # Imprimirá ["manzana", "pera", "naranja", "uva"]
    ```

- **`remove(elemento)`:** Elimina la primera ocurrencia del elemento especificado.

    ```python
    frutas = ["manzana", "naranja", "uva"]
    frutas.remove("naranja")
    print(frutas) # Imprimirá ["manzana", "uva"]
    ```

- **`pop(posición)`:** Elimina el elemento en la posición especificada (o el último si no se proporciona una posición) y lo devuelve.

    ```python
    frutas = ["manzana", "naranja", "uva"]
    fruta_eliminada = frutas.pop(1)
    print(frutas) # Imprimirá ["manzana", "uva"]
    print(fruta_eliminada) # Imprimirá "naranja"
    ```

- **`len()`:** Devuelve la longitud (número de elementos) de la lista.

    ```python
    frutas = ["manzana", "naranja", "uva"]
    longitud = len(frutas)
    print(longitud) # Imprimirá 3
    ```

Estos son solo algunos de los métodos y operaciones que puedes realizar con listas en Python. Las listas en Python son muy versátiles y se utilizan comúnmente en programación para almacenar y manipular conjuntos de datos.
