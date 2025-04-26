# Proyecto Antofagasta - Limpieza y Análisis de Datos Solares ☀️

Este proyecto tiene como objetivo limpiar, reconstruir y analizar datos solares de Antofagasta, partiendo de un archivo de datos sucios (`antofagasta_dirty.csv`).

## Proceso General

### 1. Limpieza de Datos Solares
Se parte desde un archivo CSV original (`antofagasta_dirty.csv`) que contenía:

- Valores anómalos (irradiancias superiores a 1200 W/m², temperaturas fuera de rango, etc.).
- Datos faltantes y dispersos en varios años.

**Acciones realizadas:**
- Filtrado de valores fuera de rangos físicos plausibles:
  - GHI: 0–1200 W/m²
  - DNI: 0–1200 W/m²
  - DHI: 0–800 W/m²
  - Temperatura: -20°C a 60°C
  - Velocidad del viento: 0–30 m/s
- Reconstrucción de un año completo usando datos de varios años anteriores (priorizando 2014 como base).
- Generación del nuevo archivo limpio: `antofagasta_clean_final.csv`.

### 2. Análisis Exploratorio de Datos (EDA)
Posteriormente, sobre el archivo limpio:

- Se realizó un análisis exploratorio básico (EDA).
- Se generaron gráficos de:
  - Irradiancia Global Horizontal (GHI) en el tiempo.
  - Temperatura ambiente anual.
  - Velocidad del viento anual.
- También se realizaron histogramas de distribución para visualizar tendencias.

---

## Archivos del proyecto

| Archivo | Descripción |
|:--------|:------------|
| `antofagasta_dirty.csv` | Datos solares originales (crudos). |
| `limpiar_csv.py` | Script que limpia y reconstruye los datos solares, generando `antofagasta_clean_final.csv`. |
| `antofagasta_clean_final.csv` | Datos solares limpios y reconstruidos para un año completo. |
| `eda_antofagasta_limpio.py` | Script de análisis exploratorio (EDA) sobre los datos limpios. |
| `requirements.txt` | Librerías necesarias para ejecutar los scripts. |
| `README.md` | Este documento de descripción del proyecto. |

---

## Requisitos

- Python 3.10 o superior
- Librerías:
  - pandas
  - matplotlib
  - numpy

Instalación rápida:

```bash
pip install -r requirements.txt
