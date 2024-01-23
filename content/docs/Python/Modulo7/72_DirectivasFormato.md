---
title: 7.2 Directivas de Formato
linktitle: 7.2 Directivas de Formato
type: book
date: '2024-01-20T00:00:00Z'
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
tags: 
weight: 3
---

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
