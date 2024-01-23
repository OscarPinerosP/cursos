---
title: 4.1 Creación, Lectura y Escritura de Archivos de Texto
linktitle: 4.1 Creación, Lectura y Escritura de Archivos de Texto
type: book
date: '2024-01-20T00:00:00Z'
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
tags: 
weight: 2
---

Para crear un archivo de texto en Python, puedes usar la función `open()` con el modo de apertura `"w"` (escritura). Aquí hay un ejemplo sencillo:

```python
# Abrir un archivo en modo de escritura ("w")
with open("nuevo_archivo.txt", "w") as archivo:
    # Escribir contenido en el archivo
    archivo.write("Hola, este es un nuevo archivo de texto.\n")
    archivo.write("Puedes agregar más líneas si lo deseas.\n")

# El archivo se cierra automáticamente al salir del bloque "with"
```

Este código crea un nuevo archivo llamado "nuevo_archivo.txt" y escribe dos líneas de texto en él. La instrucción `with open(...) as archivo` asegura que el archivo se cierre correctamente después de que se realicen las operaciones de escritura.

Puedes cambiar el nombre del archivo o especificar una ruta de archivo diferente según tus necesidades. Si el archivo ya existe, el modo `"w"` lo sobrescribirá, eliminando su contenido anterior. Si deseas agregar contenido sin borrar el contenido existente, puedes usar el modo `"a"` (anexar) en lugar de `"w"`.

```python
with open("archivo_existente.txt", "a") as archivo:
    archivo.write("Esta línea se añadirá al final del archivo.\n")
```

Este código abrirá el archivo existente en modo de anexar y agregará la nueva línea al final del archivo sin eliminar su contenido previo.

En Python, puedes manejar archivos de texto utilizando las funciones incorporadas `open()` para abrir un archivo y `close()` para cerrarlo. Además, hay varios modos de apertura que especifican cómo se debe interactuar con el archivo (lectura, escritura, etc.).

### Abrir y cerrar archivos

```python
# Abrir un archivo en modo de lectura
archivo_lectura = open("archivo.txt", "r")

# Realizar operaciones de lectura o escritura

# Cerrar el archivo
archivo_lectura.close()
```

### Modos de apertura

- `"r"`: Lectura. Abre el archivo para leer. El puntero del archivo se coloca al principio del archivo.
- `"w"`: Escritura. Abre el archivo para escribir. Si el archivo ya existe, trunca su contenido. Si no existe, crea un nuevo archivo.
- `"a"`: Anexar. Abre el archivo para escribir. Si el archivo ya existe, coloca el puntero al final del archivo. Si no existe, crea un nuevo archivo.
- `"b"`: Binario. Abre el archivo en modo binario.
- `"x"`: Crear. Crea un nuevo archivo. Si el archivo ya existe, lanza un error.

### Métodos para lectura

```python
# Leer todo el contenido del archivo
contenido = archivo_lectura.read()

# Leer una línea del archivo
linea = archivo_lectura.readline()

# Leer todas las líneas del archivo en una lista
lineas = archivo_lectura.readlines()
```

### Métodos para escritura

```python
# Escribir una cadena en el archivo
archivo_escritura.write("Hola, mundo!")

# Escribir una lista de cadenas en el archivo
archivo_escritura.writelines(["Línea 1\n", "Línea 2\n"])
```

### Ejemplo completo

```python
# Abrir un archivo en modo de escritura
with open("mi_archivo.txt", "w") as archivo:
    # Escribir algunas líneas en el archivo
    archivo.write("Primera línea\n")
    archivo.write("Segunda línea\n")
    archivo.write("Tercera línea\n")

# Abrir el archivo en modo de lectura
with open("mi_archivo.txt", "r") as archivo:
    # Leer todas las líneas del archivo
    lineas = archivo.readlines()

# Imprimir las líneas leídas
for linea in lineas:
    print(linea.strip())  # strip() elimina los caracteres de nueva línea al final
```

En este ejemplo, se abre un archivo en modo de escritura, se escriben algunas líneas y luego se vuelve a abrir en modo de lectura para leer las líneas. La cláusula `with` se utiliza para garantizar que el archivo se cierre correctamente después de su uso.

Recuerda cerrar siempre los archivos después de trabajar con ellos para liberar recursos del sistema. La gestión de archivos utilizando la declaración `with` asegura que el archivo se cierre automáticamente, incluso si ocurre una excepción.

El modo de apertura `"r+"` en Python se utiliza para abrir un archivo en modo de lectura y escritura simultánea. Este modo permite tanto leer como escribir en el archivo. Sin embargo, es importante tener en cuenta que el puntero del archivo se coloca al principio del archivo, y cualquier escritura que realices sobrescribirá el contenido existente desde el principio del archivo.

### Ejemplo de uso de "r+"

```python
# Abrir un archivo en modo de lectura y escritura
with open("mi_archivo.txt", "r+") as archivo:
    # Leer el contenido actual del archivo
    contenido = archivo.read()
    print("Contenido actual del archivo:")
    print(contenido)

    # Mover el puntero al principio del archivo
    archivo.seek(0)

    # Escribir una nueva línea al principio
    archivo.write("Nueva línea al principio\n")

    # Leer el contenido modificado
    archivo.seek(0)
    nuevo_contenido = archivo.read()

    print("\nContenido después de la modificación:")
    print(nuevo_contenido)
```

En este ejemplo, el archivo `"mi_archivo.txt"` se abre en modo `"r+"`. Se lee el contenido actual del archivo, se imprime en la consola y luego se agrega una nueva línea al principio del archivo. Después de la modificación, se vuelve a leer el contenido y se imprime nuevamente.

Es importante destacar que cuando se utiliza `"r+"`, debes tener cuidado con la posición del puntero del archivo, ya que cualquier escritura comenzará desde la posición actual del puntero y sobrescribirá datos existentes. Además, ten en cuenta que si la escritura es más corta que los datos existentes, los datos adicionales pueden quedar en el archivo después de la escritura, lo que puede causar resultados inesperados.
