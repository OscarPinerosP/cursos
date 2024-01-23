---
title: 6.2 Sintaxis Básica de Expresiones Regulares
linktitle: 6.2 Sintaxis Básica de Expresiones Regulares
type: book
date: '2024-01-20T00:00:00Z'
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
tags: 
weight: 3
---

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
