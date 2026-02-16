Proyecto Integrador — Módulo 4: Preparación de Datos (NumPy + Pandas)
Descripción
Este proyecto corresponde al Módulo 4 del curso y tiene como objetivo aplicar técnicas de preparación y transformación de datos usando exclusivamente NumPy y Pandas, integrando información desde distintas fuentes y generando un dataset final listo para análisis.

El desarrollo se realizó en un Notebook (Proyecto_Modulo_4.ipynb) con secciones por lección, combinando explicación (Markdown) y ejecución de código.

Objetivo
Generar datos sintéticos con NumPy.
Explorar, transformar y limpiar datos con Pandas.
Integrar datos desde CSV, Excel y una fuente web (cuando está disponible).
Detectar y tratar valores nulos y outliers (método IQR).
Realizar data wrangling: deduplicación, conversión de tipos, creación de variables y discretización.
Crear reportes con groupby y pivot_table.
Exportar un dataset final en CSV y Excel.
Archivos del repositorio
Archivos principales
Proyecto_Modulo_4.ipynb: Notebook con el desarrollo completo por lecciones (Markdown + código + outputs).
clientes_ecommerce.csv: dataset de entrada (consigna).
clientes_ecommerce.xlsx: dataset de entrada (consigna).
Archivos generados (salidas)
dataset_final_ecommerce.csv: dataset final consolidado y transformado.
dataset_final_ecommerce.xlsx: dataset final consolidado y transformado.
Archivos intermedios (evidencia del proceso)
datos_extra.npy: datos generados con NumPy.
clientes_extra.csv: clientes sintéticos en formato tabular.
clientes_consolidado.csv: unión de fuentes (antes de limpieza).
clientes_limpio.csv: dataset tras imputación de nulos y tratamiento de outliers.
clientes_optimizado.csv: dataset tras wrangling (nuevas columnas y categorizaciones).
Resumen del flujo de trabajo (por lecciones)
Lección 1 — NumPy
Generación de datos sintéticos (clientes extra).
Inserción intencional de un nulo y un outlier para practicar limpieza posterior.
Lección 2 — Pandas (exploración)
Conversión de los datos a DataFrame.
Exploración inicial (head, describe) y exportación de un CSV preliminar.
Lección 3 — Integración de fuentes
Lectura de archivos locales con read_csv y read_excel.
Intento de extracción desde web con read_html (puede fallar por restricciones HTTP/403).
Consolidación de fuentes en un solo dataset.
Lección 4 — Limpieza (nulos y outliers)
Detección de nulos por columna.
Imputación:
Monto_Total: se completa con mediana (robusta ante outliers).
Edad: se completa con media.
Detección de outliers con IQR y tratamiento mediante capping.
Lección 5 — Data Wrangling
Eliminación de duplicados tras consolidación.
Conversión de tipos (ID, Edad).
Columnas nuevas:
Ticket_Promedio
Categoria_Cliente
Rango_Etario (discretización con pd.cut)
Lección 6 — Reportes
groupby por ciudad (métricas agregadas).
pivot_table cruzando Rango_Etario y Categoria_Cliente.
Exportación final a CSV y Excel.
Requisitos / Dependencias
Python 3.x
numpy
pandas
openpyxl (necesario para leer/escribir .xlsx con Pandas)
Instalación (Windows / VS Code terminal):

bash
Copy
py -m pip install numpy pandas openpyxl
Cómo ejecutar
Abrir Proyecto_Modulo_4.ipynb en VS Code (con soporte de Jupyter).
Seleccionar el intérprete / kernel correcto.
Ejecutar todas las celdas con Run All.
Notas
La extracción web con pd.read_html() puede devolver HTTP 403 dependiendo de la disponibilidad o bloqueo del sitio. El notebook maneja este caso y continúa con las fuentes locales.
