# 📊 Dashboard de Análisis de Préstamos (Excel)

## 🧩 Descripción del proyecto

Este proyecto consiste en la transformación, análisis y visualización de un dataset de préstamos mediante Excel, siguiendo un enfoque progresivo desde nivel esencial hasta un dashboard interactivo.

Los datos han sido limpiados, estructurados y analizados para extraer insights relevantes sobre financiación, comportamiento de los préstamos y distribución geográfica.

---

## 🗂️ Preparación de los datos

### 🔹 Estandarización de columnas

Los encabezados fueron traducidos al español para mejorar la comprensión:

* Identificador
* Monto financiado
* Monto del préstamo
* Actividad
* Sector
* País
* Fecha de publicación, entre otros

---

### 🔹 Limpieza de datos

* Los valores vacíos fueron reemplazados por **"Sin dato"** para evitar errores en el análisis.
* Se verificó la consistencia de formatos (fechas y números).

---

### 🔹 Conversión a tabla

Se transformó el dataset en una **tabla estructurada de Excel (Ctrl + T)** para:

* Facilitar filtros
* Mejorar rendimiento
* Permitir referencias dinámicas

---

## 📈 Análisis exploratorio

### 🔹 Formato condicional

Se aplicaron técnicas visuales para identificar patrones rápidamente:

* **Monto financiado**

  * Barras de datos para visualizar volumen de financiación

* **Número de prestamistas**

  * Escala de color:

    * 🔴 Rojo → pocos prestamistas
    * 🟡 Amarillo → valor medio
    * 🟢 Verde → alto número de prestamistas

Esto permite detectar fácilmente:

* Préstamos con mayor impacto
* Nivel de participación en cada operación

---

## ⚖️ Creación de variables

### 🔹 Clasificación del tamaño del préstamo

Se creó una nueva columna: **"Tamaño del Préstamo"**

```excel
=SI([@[Monto del préstamo]]<3000;"Pequeño";SI([@[Monto del préstamo]]<=7000;"Medio";"Grande"))
```

Esto permite segmentar los préstamos en:

* Pequeños
* Medianos
* Grandes

Facilitando el análisis comparativo.

---

## 📊 Tablas dinámicas

Se desarrollaron **5 tablas dinámicas** para resumir la información:

### 🔹 KPIs principales

1. Total prestado
2. Promedio del préstamo
3. Total de prestamistas

---

### 🔹 Análisis por dimensión

4. Total prestado por país
5. Total prestado por sector

Estas tablas permiten analizar:

* Distribución geográfica
* Sectores con mayor financiación

---

## 🎛️ Interactividad

Se añadieron **segmentadores (slicers)** para:

* País
* Sector

Esto permite filtrar todo el dashboard de forma dinámica y explorar los datos de manera interactiva.

---

## 📉 Visualización de datos

Se crearon **4 gráficos**:

### 🔹 Por país

* Gráfico de barras
* Gráfico circular

### 🔹 Por sector

* Gráfico de barras
* Gráfico circular

Estos gráficos representan:

* Distribución del total prestado
* Comparación entre categorías

---
