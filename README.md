# 📊 Proyecto Integrador: Preparación de Datos (Módulo 4)
### Diplomado en Fundamentos de Análisis de Datos — SENCE

---

## 📝 Descripción del Proyecto
Este proyecto desarrolla un pipeline completo de **Data Preparation** utilizando exclusivamente las librerías **NumPy** y **Pandas**. El objetivo es simular un entorno real de análisis de datos donde se deben integrar múltiples fuentes, limpiar inconsistencias y transformar la información para la toma de decisiones en un entorno de E-commerce.

El desarrollo se encuentra documentado paso a paso en un entorno de **Jupyter Notebook** (`.ipynb`), facilitando la reproducibilidad y la claridad técnica.

---

## 🎯 Objetivos Principales
*   **Generación de Datos:** Creación de datasets sintéticos con NumPy para pruebas de estrés.
*   **Integración Multifuente:** Consolidación de datos provenientes de archivos CSV, Excel y Web Scraping.
*   **Calidad de Datos:** Identificación y tratamiento de valores nulos (imputación) y outliers (método estadístico IQR).
*   **Data Wrangling:** Transformación de tipos, creación de métricas de negocio y discretización de variables.
*   **Reporting:** Generación de tablas dinámicas y reportes agrupados para análisis gerencial.

---

## 📂 Estructura del Repositorio

| Archivo | Descripción |
| :--- | :--- |
| `Proyecto_Modulo_4.ipynb` | **Archivo Principal.** Notebook con el código y explicaciones. |
| `clientes_ecommerce.csv` | Dataset original de entrada (CSV). |
| `clientes_ecommerce.xlsx` | Dataset original de entrada (Excel). |
| `dataset_final_ecommerce.xlsx` | **Resultado Final.** Datos limpios y transformados en Excel. |
| `dataset_final_ecommerce.csv` | **Resultado Final.** Datos limpios y transformados en CSV. |
| `datos_extra.npy` | Binario de NumPy con datos generados sintéticamente. |

---

## 🛠️ Tecnologías y Librerías
El proyecto fue desarrollado en **VS Code** utilizando:
*   **Python 3.13**
*   **NumPy:** Para manejo de arrays y generación de datos aleatorios.
*   **Pandas:** Para manipulación de DataFrames y análisis tabular.
*   **Openpyxl:** Motor necesario para la gestión de archivos Excel.

---

## 🚀 Metodología (Lecciones)

### 1. Generación y Exploración (Lecciones 1 y 2)
Se utilizaron funciones de NumPy para crear 10 registros adicionales, introduciendo intencionalmente **valores nulos** y **outliers** (montos superiores a 50,000) para validar los procesos de limpieza posteriores.

### 2. Integración de Datos (Lección 3)
Se consolidaron tres fuentes de datos en un único DataFrame. Se implementó un bloque `try-except` para la extracción web (`read_html`), manejando posibles errores de conexión o bloqueos de servidor (HTTP 403).

### 3. Limpieza y Tratamiento Estadístico (Lección 4)
*   **Nulos:** Imputación de `Monto_Total` mediante la **mediana** y `Edad` mediante la **media**.
*   **Outliers:** Aplicación del método de **Rango Intercuartílico (IQR)**. Se aplicó una técnica de *capping* para limitar los valores extremos al límite superior estadístico, evitando la pérdida de registros.

### 4. Transformación y Enriquecimiento (Lección 5)
Se aplicaron técnicas de *Data Wrangling*:
*   Eliminación de duplicados.
*   Creación de la métrica `Ticket_Promedio`.
*   Categorización de clientes mediante funciones `lambda`.
*   Discretización de edades en rangos (Joven, Adulto, Senior).

### 5. Análisis y Exportación (Lección 6)
Generación de un reporte de ventas por ciudad y una tabla pivote para analizar el comportamiento de gasto por rango etario. Finalmente, se exportaron los resultados en formatos estándar de industria.

---

## ⚙️ Instalación y Ejecución
Para replicar este proyecto localmente, asegúrese de tener instaladas las dependencias:

```bash
py -m pip install numpy pandas openpyxl lxml
