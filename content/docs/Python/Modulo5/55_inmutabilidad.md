---
title: 5.5 Inmutabilidad
linktitle: 5.5 Inmutabilidad
type: book
date: '2024-01-20T00:00:00Z'
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
tags: 
weight: 6
---

Aunque Python no es un lenguaje puramente funcional, puedes escribir código que favorezca la inmutabilidad, evitando la modificación directa de datos y prefiriendo la creación de nuevos objetos.

```python
# Ejemplo de inmutabilidad
lista_original = [1, 2, 3]
lista_modificada = lista_original + [4] # Crear una nueva lista en lugar de modificar la original
print(lista_original) # Imprimirá [1, 2, 3]
print(lista_modificada) # Imprimirá [1, 2, 3, 4]
```

La programación funcional en Python permite escribir código más claro, modular y fácil de entender en muchos casos. Sin embargo, la elección de utilizar enfoques funcionales o imperativos depende del problema específico y de las preferencias del programador. En Python, es común combinar ambos estilos de programación según sea necesario.
