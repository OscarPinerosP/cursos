---
title: 7.3 Zonas Horarias
linktitle: 7.3 Zonas Horarias
type: book
date: '2024-01-20T00:00:00Z'
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
tags: 
weight: 4
---

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
