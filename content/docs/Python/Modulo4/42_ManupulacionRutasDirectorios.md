---
title: 4.2 Manipulación de Rutas de Archivos y Directorios
linktitle: 4.2 Manipulación de Rutas de Archivos y Directorios
type: book
date: '2024-01-20T00:00:00Z'
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
tags: 
weight: 3
---

En Python, la manipulación de rutas de archivos y directorios se realiza comúnmente utilizando los módulos `os.path` y `os`. Estos módulos proporcionan funciones para trabajar con rutas, verificar la existencia de archivos y directorios, y realizar diversas operaciones relacionadas con el sistema de archivos.

### Módulo `os.path`

El módulo `os.path` proporciona funciones para manipular rutas de manera independiente del sistema operativo. Algunas funciones útiles incluyen:

- `os.path.join()`: Combina varios componentes de ruta en una única ruta.
- `os.path.basename()`: Devuelve el componente de nombre de archivo de una ruta.
- `os.path.dirname()`: Devuelve el directorio de una ruta.
- `os.path.exists()`: Verifica si una ruta dada (archivo o directorio) existe.
- `os.path.isfile()`: Verifica si la ruta se refiere a un archivo regular.
- `os.path.isdir()`: Verifica si la ruta se refiere a un directorio.

```python
import os

# Ejemplo de uso del módulo os.path
ruta_completa = os.path.join("mi_directorio", "mi_archivo.txt")
nombre_archivo = os.path.basename(ruta_completa)
directorio = os.path.dirname(ruta_completa)

print(f"Ruta completa: {ruta_completa}")
print(f"Nombre del archivo: {nombre_archivo}")
print(f"Directorio: {directorio}")

# Verificar la existencia de un archivo
if os.path.exists(ruta_completa):
    print("El archivo existe.")
else:
    print("El archivo no existe.")
```

### Módulo `os`

El módulo `os` proporciona funciones que interactúan con el sistema operativo, incluyendo operaciones relacionadas con archivos y directorios. Algunas funciones útiles incluyen:

- `os.getcwd()`: Devuelve el directorio de trabajo actual.
- `os.chdir()`: Cambia el directorio de trabajo actual.
- `os.mkdir()`: Crea un nuevo directorio.
- `os.makedirs()`: Crea directorios recursivamente.
- `os.remove()`: Elimina un archivo.
- `os.rmdir()`: Elimina un directorio vacío.
- `os.removedirs()`: Elimina directorios recursivamente.

```python
import os

# Ejemplo de uso del módulo os
directorio_actual = os.getcwd()
print(f"Directorio actual: {directorio_actual}")

# Cambiar al directorio "mi_directorio"
os.chdir("mi_directorio")

# Crear un nuevo directorio
os.mkdir("nuevo_directorio")

# Verificar si el directorio existe
if os.path.exists("nuevo_directorio"):
    print("El directorio 'nuevo_directorio' existe.")

# Eliminar el directorio creado
os.rmdir("nuevo_directorio")
```

Ambos módulos, `os.path` y `os`, son poderosos y versátiles para manipular rutas de archivos y directorios, y realizar operaciones en el sistema de archivos. Estos módulos facilitan el desarrollo de aplicaciones que deben interactuar con archivos y directorios en un entorno multiplataforma.
