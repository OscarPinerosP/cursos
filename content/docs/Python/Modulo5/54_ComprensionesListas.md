---
title: 5.4 Comprensiones de listas
linktitle: 5.4 Comprensiones de listas
type: book
date: '2024-01-20T00:00:00Z'
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
tags: 
weight: 5
---

Python permite construir listas utilizando comprensiones de listas, que es una forma concisa y expresiva de aplicar transformaciones a los elementos de una lista.

```python
# Comprensión de lista para obtener cuadrados de los números pares
numeros = [1, 2, 3, 4, 5]
cuadrados_pares = [x ** 2 for x in numeros if x % 2 == 0]
print(cuadrados_pares) # Imprimirá [4, 16]
```
