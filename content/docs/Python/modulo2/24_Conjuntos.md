---
title: 2.4 Conjuntos
linktitle: 2.4 Conjuntos
type: book
date: '2024-01-20T00:00:00Z'
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
tags: 
weight: 5
---

En Python, un conjunto es una colección no ordenada de elementos únicos. Los conjuntos se utilizan para realizar operaciones de conjunto, como unión, intersección, diferencia y otras operaciones matemáticas en conjuntos. Aquí te explico cómo crear, acceder y realizar algunas operaciones con conjuntos:

### Crear un conjunto

Los conjuntos se crean utilizando llaves `{}` o la función `set()`.

```python
# Crear un conjunto con llaves
frutas = {"manzana", "naranja", "uva"}

# Crear un conjunto con la función set()
numeros = set([1, 2, 3, 4, 5])
```

### Acceder a los elementos de un conjunto

Los conjuntos no tienen índices, por lo que no se pueden acceder a elementos individuales de la misma manera que en listas o tuplas. Sin embargo, puedes verificar si un elemento está presente en un conjunto utilizando la palabra clave `in`.

```python
frutas = {"manzana", "naranja", "uva"}

if "manzana" in frutas:
    print("La manzana está en el conjunto")
```

### Operaciones con conjuntos

- **Unión (`union()` o `|`):** Combina dos conjuntos en un nuevo conjunto, incluyendo todos los elementos únicos.

    ```python
    conjunto1 = {1, 2, 3}
    conjunto2 = {3, 4, 5}
    union_resultado = conjunto1.union(conjunto2)
    # O usando el operador |
    union_resultado_operador = conjunto1 | conjunto2
    print(union_resultado) # Imprimirá {1, 2, 3, 4, 5}
    print(union_resultado_operador) # Imprimirá {1, 2, 3, 4, 5}
    ```

- **Intersección (`intersection()` o `&`):** Encuentra los elementos comunes entre dos conjuntos.

    ```python
    conjunto1 = {1, 2, 3}
    conjunto2 = {3, 4, 5}
    interseccion_resultado = conjunto1.intersection(conjunto2)
    # O usando el operador &
    interseccion_resultado_operador = conjunto1 & conjunto2
    print(interseccion_resultado) # Imprimirá {3}
    print(interseccion_resultado_operador) # Imprimirá {3}
    ```

- **Diferencia (`difference()` o `-`):** Encuentra los elementos en el primer conjunto que no están en el segundo.

    ```python
    conjunto1 = {1, 2, 3}
    conjunto2 = {3, 4, 5}
    diferencia_resultado = conjunto1.difference(conjunto2)
    # O usando el operador -
    diferencia_resultado_operador = conjunto1 - conjunto2
    print(diferencia_resultado) # Imprimirá {1, 2}
    print(diferencia_resultado_operador) # Imprimirá {1, 2}
    ```

- **Diferencia simétrica (`symmetric_difference()` o `^`):** Encuentra los elementos que están en uno de los conjuntos, pero no en ambos.

    ```python
    conjunto1 = {1, 2, 3}
    conjunto2 = {3, 4, 5}
    diferencia_simetrica_resultado = conjunto1.symmetric_difference(conjunto2)
    # O usando el operador ^
    diferencia_simetrica_resultado_operador = conjunto1 ^ conjunto2
    print(diferencia_simetrica_resultado) # Imprimirá {1, 2, 4, 5}
    print(diferencia_simetrica_resultado_operador) # Imprimirá {1, 2, 4, 5}
    ```

Estos son solo algunos ejemplos de las operaciones que puedes realizar con conjuntos en Python. Los conjuntos son útiles para realizar operaciones de conjunto y garantizar que los elementos sean únicos.

A continuación te proporciono ejemplos de cómo eliminar duplicados en una lista utilizando conjuntos y de cómo verificar la pertenencia de elementos con `in`:

### Eliminar duplicados en una lista utilizando conjuntos

```python
# Lista con duplicados
lista_con_duplicados = [1, 2, 2, 3, 4, 4, 5, 6, 6]

# Convertir la lista a un conjunto para eliminar duplicados
conjunto_sin_duplicados = set(lista_con_duplicados)

# Convertir de nuevo el conjunto a una lista (si es necesario)
lista_sin_duplicados = list(conjunto_sin_duplicados)

print(lista_sin_duplicados)
# Imprimirá [1, 2, 3, 4, 5, 6]
```

En este ejemplo, convertimos la lista a un conjunto (`set`) para eliminar los duplicados debido a la propiedad de los conjuntos de contener elementos únicos. Luego, si es necesario, convertimos el conjunto de nuevo a una lista.

### Verificación de pertenencia con `in`

```python
# Conjunto de frutas
frutas = {"manzana", "naranja", "uva", "kiwi"}

# Verificar si "kiwi" está en el conjunto
if "kiwi" in frutas:
    print("Sí, el kiwi está en el conjunto")
else:
    print("No, el kiwi no está en el conjunto")

# Verificar si "pera" está en el conjunto
if "pera" in frutas:
    print("Sí, la pera está en el conjunto")
else:
    print("No, la pera no está en el conjunto")
```

En este ejemplo, utilizamos la expresión `if "elemento" in conjunto` para verificar si un elemento específico está presente en el conjunto. En este caso, verificamos la pertenencia de "kiwi" y "pera" en el conjunto de frutas.
