---
title: Módulo 7 Manejo de Fechas y Tiempo
linktitle: Módulo 7 Manejo de Fechas y Tiempo
type: book
date: '2024-01-20T00:00:00Z'
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
tags: 
weight: 11
---


En Python, el manejo de fechas y horas se realiza principalmente mediante el módulo `datetime`. Aquí hay una introducción al manejo de fechas y horas, las directivas de formato y algunos ejemplos:

## 7.1 **Módulo datetime**

El módulo `datetime` proporciona clases para trabajar con fechas y horas. Algunas de las clases más utilizadas son `datetime`, `date`, `time` y `timedelta`.

## 7.**2 Directivas de Formato**

Las directivas de formato se utilizan para representar y dar formato a las fechas y horas. Algunas de las directivas comunes son:

- `%Y`: Año con siglo como número decimal de cuatro dígitos.
- `%m`: Mes como número decimal de dos dígitos.
- `%d`: Día del mes como número decimal de dos dígitos.
- `%H`: Hora (00-23).
- `%M`: Minuto (00-59).
- `%S`: Segundo (00-59).

### **Ejemplos:**

- **Obtener la Fecha y Hora Actuales:**

```python
from datetime import datetime

fecha_hora_actual = datetime.now()
print("Fecha y hora actuales:", fecha_hora_actual)
```

- **Formatear una Fecha:**

```python
from datetime import datetime

fecha = datetime(2023, 1, 19)
formato_personalizado = fecha.strftime("%Y-%m-%d")
print("Fecha formateada:", formato_personalizado)
```

- **Parsear una Cadena a Fecha:**

```python
from datetime import datetime

cadena_fecha = "2023-01-19"
fecha_parseada = datetime.strptime(cadena_fecha, "%Y-%m-%d")
print("Fecha parseada:", fecha_parseada)
```

- **Operaciones con Fechas:**

```python
from datetime import datetime, timedelta

fecha_actual = datetime.now()
diferencia_dias = timedelta(days=7)
nueva_fecha = fecha_actual + diferencia_dias
print("Fecha actual:", fecha_actual)
print("Fecha después de 7 días:", nueva_fecha)
```

- **Diferencia entre Fechas:**

```python
from datetime import datetime, timedelta

fecha1 = datetime(2023, 1, 19)
fecha2 = datetime(2023, 1, 25)
diferencia = fecha2 - fecha1
print("Diferencia entre fechas:", diferencia)
```

Estos son solo ejemplos básicos, y hay muchas más funcionalidades disponibles en el módulo `datetime`, como el manejo de zonas horarias, el cálculo de diferencias entre fechas, la extracción de componentes de fecha y hora, etc.

Para obtener información detallada sobre las directivas de formato y métodos del módulo `datetime`, puedes consultar la documentación oficial: datetime — Tipos básicos de fecha y hora.

## 7.3 Zonas Horarias

En Python, el manejo de zonas horarias se realiza comúnmente utilizando el módulo `pytz`. Este módulo proporciona funcionalidades para trabajar con zonas horarias y realizar conversiones entre ellas. Aquí te dejo un ejemplo de cómo manejar zonas horarias y realizar conversiones:

### Instalación de `pytz`

```bash
pip install pytz
```

### Ejemplo de Manejo de Zonas Horarias y Conversión

```python
from datetime import datetime
import pytz

# Obtener la fecha y hora actual con la zona horaria UTC
fecha_hora_utc = datetime.now(pytz.utc)
print("Fecha y hora en UTC:", fecha_hora_utc)

# Obtener la zona horaria de Nueva York
zona_horaria_ny = pytz.timezone('America/New_York')

# Convertir la fecha y hora UTC a la zona horaria de Nueva York
fecha_hora_ny = fecha_hora_utc.astimezone(zona_horaria_ny)
print("Fecha y hora en Nueva York:", fecha_hora_ny)

# Obtener la zona horaria de Tokio
zona_horaria_tokio = pytz.timezone('Asia/Tokyo')

# Convertir la fecha y hora UTC a la zona horaria de Tokio
fecha_hora_tokio = fecha_hora_utc.astimezone(zona_horaria_tokio)
print("Fecha y hora en Tokio:", fecha_hora_tokio)
```

Este ejemplo muestra cómo obtener la fecha y hora actual en UTC, luego cómo convertir esa fecha y hora a las zonas horarias de Nueva York y Tokio utilizando el módulo `pytz`.

**Nota:** Asegúrate de tener la última versión de `pytz` para obtener las últimas zonas horarias y ajustes de cambio de horario de verano.

El módulo `pytz` proporciona una lista completa de zonas horarias, además, el módulo `pytz` permite manejar eficientemente reglas de cambio de horario de verano y ajustes para diferentes zonas horarias, con el siguiente código puedes accesar a el listado de todas las zonas horarias.

### Listado de todas las zonas horarias

```python
import pytz
pytz.all_timezones
```

### Script para mostrar el listado de todas las zonas horarias con respecto a UTC

```python
import pytz

# Zona horaria de referencia (UTC)
zona_horaria_referencia = pytz.timezone('UTC')

# Obtener la lista de todas las zonas horarias
todas_las_zonas_horarias = pytz.all_timezones

# Imprimir todas las zonas horarias con sus diferencias de horas respecto a UTC
for zona_horaria in todas_las_zonas_horarias:
    # Obtener la zona horaria actual
    zona_horaria_actual = pytz.timezone(zona_horaria)
    
    # Obtener la diferencia de horas respecto a UTC
    diferencia_horas = zona_horaria_referencia.utcoffset(datetime.utcnow()) - zona_horaria_actual.utcoffset(datetime.utcnow())
    
    # Formatear la diferencia de horas
    signo = '+' if diferencia_horas.total_seconds() >= 0 else '-'
    diferencia_formateada = f"{signo}{abs(diferencia_horas)}"

    # Imprimir la información
    print(f"{zona_horaria}: (GMT{diferencia_formateada})")
```

## 7.4 Ejercicios Prácticos

- **Ejercicio 1:**
- Crear un programa que muestre la fecha y hora actuales.
- **Ejercicio 2:**
- Realizar cálculos de fechas, como calcular la fecha dentro de 7 días.
- **Ejercicio 3:**
- Convertir fechas entre diferentes zonas horarias.
