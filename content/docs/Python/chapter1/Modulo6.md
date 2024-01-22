---
title: Módulo 6 Expresiones Regulares (Regex)
linktitle: Módulo 6 Expresiones Regulares (Regex)
type: book
date: '2024-01-20T00:00:00Z'
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
tags: 
weight: 10
---


## **6.1 Expresiones Regulares (Regex)**

Las expresiones regulares, también conocidas como regex o regexp, son secuencias de caracteres que forman un patrón de búsqueda. Estos patrones se utilizan para buscar, extraer y manipular texto de manera eficiente. Las expresiones regulares son una herramienta poderosa para trabajar con cadenas de texto, permitiendo búsquedas flexibles y complejas.

Las expresiones regulares utilizan caracteres especiales y metacaracteres para definir patrones. Un patrón puede incluir letras, números, caracteres especiales y secuencias que representen ciertas estructuras o condiciones. Al aplicar un patrón a una cadena de texto, se pueden realizar operaciones como búsqueda, coincidencia, sustitución y más.

## **6.2 Patrones para Buscar y Manipular Texto**

- **Búsqueda:** Puedes buscar patrones específicos en un texto. Por ejemplo, encontrar todas las direcciones de correo electrónico en un documento o buscar números de teléfono.
- **Coincidencia:** Las expresiones regulares pueden verificar si una cadena coincide con un patrón dado. Esto es útil para validar entradas de usuario, como direcciones de correo electrónico o números de teléfono.
- **Sustitución:** Puedes reemplazar partes de una cadena que coincidan con un patrón por otra cadena. Esto es útil para realizar cambios en el formato de texto.
- **Extracción:** Puedes extraer información específica de una cadena utilizando grupos de captura. Por ejemplo, extraer números de teléfono de un texto.

### Ejemplo 1 Búsqueda con Expresiones Regulares en Python

Supongamos que queremos encontrar todas las direcciones de correo electrónico en un texto:

```python
import re

texto = "Contacta con support@example.com o info@company.com para obtener ayuda."
patron_email = r'\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Z|a-z]{2,}\b'

resultados = re.findall(patron_email, texto)
print(resultados)
```

En este ejemplo, `re.findall()` se utiliza para buscar todas las coincidencias del patrón de dirección de correo electrónico en el texto.

### Ejemplo 2 Coincidencia con Expresiones Regulares en Python

Supongamos que queremos verificar si una cadena es un número de teléfono válido:

```python
import re

numero_telefono = "123-456-7890"
patron_telefono = r'^\d{3}-\d{3}-\d{4}$'

if re.match(patron_telefono, numero_telefono):
    print("Número de teléfono válido.")
else:
    print("Número de teléfono no válido.")
```

En este ejemplo, `re.match()` se utiliza para verificar si la cadena coincide con el patrón de número de teléfono desde el principio hasta el final.

### Ejemplo 3 Sustitución con Expresiones Regulares en Python

Supongamos que queremos ocultar todas las contraseñas en un texto con asteriscos:

```python
import re

texto = "La contraseña es: secreto123 y la otra contraseña es: clave456."
patron_contraseña = r'\b(secreto123|clave456)\b'

texto_oculto = re.sub(patron_contraseña, '********', texto)
print(texto_oculto)
```

En este ejemplo, `re.sub()` se utiliza para reemplazar todas las ocurrencias de las contraseñas especificadas con asteriscos.

### Ejemplo 4 Extracción con Expresiones Regulares en Python

Supongamos que queremos extraer fechas en formato "dd/mm/aaaa" de un texto:

```python
import re

texto = "Hoy es 01/02/2023 y mañana será 15/03/2023."
patron_fecha = r'\b(\d{2}/\d{2}/\d{4})\b'

fechas_encontradas = re.findall(patron_fecha, texto)
print(fechas_encontradas)
```

En este ejemplo, `re.findall()` se utiliza para encontrar todas las fechas en el formato especificado en el texto.

Estos son solo ejemplos básicos, y las expresiones regulares pueden volverse más complejas según las necesidades específicas. Es recomendable utilizar herramientas en línea, como regex101.com, para probar y entender expresiones regulares mientras te familiarizas con su sintaxis y funcionalidades.

## **6.3 Sintaxis Básica de Expresiones Regulares**

La sintaxis básica de las expresiones regulares incluye caracteres literales, metacaracteres, grupos y cuantificadores. Aquí hay una breve descripción de cada uno:

1. **Caracteres Literales:**
    - Los caracteres literales coinciden exactamente con ellos mismos.
    - Ejemplo: El patrón `"python"` coincide con la cadena "python" en un texto.
2. **Metacaracteres:**
    - Son caracteres especiales con significados especiales en expresiones regulares.
    - Algunos metacaracteres comunes: `^`, `$`, `.`, ``, `+`, `?`, `\`, `|`, `[ ]`, `{ }`, `( )`.
    - Ejemplo: El patrón `"\d"` coincide con cualquier dígito.
3. **Grupos:**
    - Los paréntesis `( )` se utilizan para agrupar expresiones y aplicar operadores a ellas.
    - Los grupos pueden ser capturadores o no capturadores.
    - Ejemplo de grupo capturador: `"(abc)+"` coincide con "abc", "abcabc", etc.
    - Ejemplo de grupo no capturador: `"(?:abc)+"` tiene el mismo efecto, pero no captura el grupo.
4. **Cuantificadores:**
    - Se utilizan para especificar cuántas veces debe aparecer un elemento.
    - Algunos cuantificadores comunes: `` (cero o más), `+` (uno o más), `?` (cero o uno), `{n}` (exactamente n), `{n,}` (n o más), `{n,m}` (entre n y m).
    - Ejemplo: El patrón `"\d{2,4}"` coincide con dos, tres o cuatro dígitos.

**Ejemplos:**

1. **Caracteres Literales:**

    ```python
    import re
    texto = "Python es un lenguaje de programación."
    patron = r"Python"
    coincidencias = re.findall(patron, texto)
    print(coincidencias) # Imprimirá ['Python']
    ```

- **Metacaracteres:**

    ```python
    import re
    texto = "123-456-7890"
    patron = r"^\d{3}-\d{3}-\d{4}$"
    coincidencia = re.match(patron, texto)
    if coincidencia: print("Número de teléfono válido.")
    else: print("Número de teléfono no válido.")
    ```

- **Grupos:**

    ```python
    import re
    texto = "abcabcabc"
    patron_con_grupo = r"(abc)+"
    coincidencias = re.findall(patron_con_grupo, texto)
    print(coincidencias) # Imprimirá ['abc', 'abc', 'abc']
    patron_sin_grupo = r"abc+"
    coincidencia_sin_grupo = re.findall(patron_sin_grupo, texto)
    print(coincidencia_sin_grupo) # Imprimirá ['abcabcabc']
    ```

- **Cuantificadores:**

    ```python
    import re
    texto = "12345"
    patron_con_cuantificador = r"\d{2,4}"
    coincidencia_con_cuantificador = re.findall(patron_con_cuantificador, texto)
    print(coincidencia_con_cuantificador) # Imprimirá ['1234']
    patron_sin_cuantificador = r"\d\d\d\d"
    coincidencia_sin_cuantificador = re.findall(patron_sin_cuantificador, texto)
    print(coincidencia_sin_cuantificador) # Imprimirá ['1234']
    ```

Estos son solo ejemplos básicos. Las expresiones regulares pueden volverse más complejas a medida que se combinan diferentes elementos para crear patrones más específicos y flexibles.

Aquí tienes una explicación de algunos de los metacaracteres comunes en expresiones regulares junto con ejemplos de su uso:

1. **`^` - Ancla de inicio:**
    - Coincide con el inicio de una cadena.
    - Ejemplo: `^abc` coincide con "abc" al principio de la cadena.
2. **`$` - Ancla de fin:**
    - Coincide con el final de una cadena.
    - Ejemplo: `abc$` coincide con "abc" al final de la cadena.
3. **`.` - Corresponde a cualquier carácter excepto nueva línea:**
    - Coincide con cualquier carácter excepto una nueva línea (`\n`).
    - Ejemplo: `a.c` coincide con "abc", "adc", etc.
4. `*` **- Cero o más repeticiones:**
    - Coincide con cero o más repeticiones del elemento anterior.
    - Ejemplo: `ab*c` coincide con "ac", "abc", "abbc", etc.
5. **`+` - Una o más repeticiones:**
    - Coincide con una o más repeticiones del elemento anterior.
    - Ejemplo: `ab+c` coincide con "abc", "abbc", pero no con "ac".
6. **`?` - Cero o una repetición:**
    - Coincide con cero o una repetición del elemento anterior.
    - Ejemplo: `ab?c` coincide con "ac" y "abc", pero no con "abbc".
7. **`\` - Carácter de escape:**
    - Utilizado para escapar un metacaracter y tratarlo como un carácter literal.
    - Ejemplo: `a\.b` coincide con "a.b".
8. **`|` - Alternancia:**
    - Coincide con uno de los elementos separados por `|`.
    - Ejemplo: `a|b` coincide con "a" o "b".
9. **`[ ]` - Conjunto de caracteres:**
    - Coincide con cualquier carácter dentro del conjunto.
    - Ejemplo: `[aeiou]` coincide con cualquier vocal.
10. **`{ }` - Cuantificador específico:**
    - Especifica un número exacto o un rango de repeticiones.
    - Ejemplos:
        - `a{3}` coincide con "aaa".
        - `a{2,4}` coincide con "aa", "aaa" o "aaaa".

Estos son solo algunos de los metacaracteres más comunes en expresiones regulares. La combinación de estos elementos permite construir patrones flexibles y poderosos para buscar y manipular texto de manera efectiva.

## **6.4 Aplicaciones Comunes de las Expresiones Regulares**

1. **Validación de Formularios:** Verificar que los datos ingresados por el usuario cumplen con un formato específico, como direcciones de correo electrónico, números de teléfono o códigos postales.
2. **Procesamiento de Texto:** Buscar y reemplazar patrones específicos en archivos de texto o cadenas de texto grandes. Esto es útil en tareas de edición y manipulación de documentos.
3. **Análisis de Log:** Analizar registros (logs) de archivos para extraer información específica, como fechas, direcciones IP o mensajes de error.
4. **Extracción de Datos:** Extraer información estructurada de documentos o páginas web utilizando patrones específicos.
5. **Desarrollo Web:** Validar y procesar cadenas de consulta en URLs, manipular datos JSON o XML, y realizar otras tareas relacionadas con el manejo de datos en aplicaciones web.
6. **Limpieza de Datos:** Limpiar y formatear datos para su análisis, eliminando caracteres no deseados o normalizando el formato.

Es importante señalar que las expresiones regulares pueden llegar a ser complejas, y el aprendizaje gradual de sus conceptos y construcciones es útil. En Python, el módulo `re` proporciona funcionalidades para trabajar con expresiones regulares.

Los siguientes son ejemplos de expresiones regulares en Python para diferentes casos:

## 6.5 Ejercicios Prácticos

- **Ejercicio 1:**
- Crear una expresión regular para validar direcciones de correo electrónico.
- **Ejercicio 2:**
- Utilizar expresiones regulares para extraer información de un texto.
- **Ejercicio 3:**
- Realizar sustituciones en un texto utilizando expresiones regulares.
