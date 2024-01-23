---
title: 5.1 Funciones de primera clase
linktitle: 5.1 Funciones de primera clase
type: book
date: '2024-01-20T00:00:00Z'
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
tags: 
weight: 2
---

En Python, las funciones son objetos de primera clase, lo que significa que puedes pasar funciones como argumentos a otras funciones, devolver funciones como resultados y asignar funciones a variables.

```python
def cuadrado(x): return x ** 2
def aplicar_funcion(func, valor): return func(valor)
resultado = aplicar_funcion(cuadrado, 5)
print(resultado) # Imprimirá 25
```
