---
title: 5.3 Map, Filter y Reduce
linktitle: 5.3 Map, Filter y Reduce
type: book
date: '2024-01-20T00:00:00Z'
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
tags: 
weight: 4
---

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
