---
title: 6.1 Patrones para Buscar y Manipular Texto
linktitle: 6.1 Patrones para Buscar y Manipular Texto
type: book
date: '2024-01-20T00:00:00Z'
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
tags: 
weight: 2
---

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
