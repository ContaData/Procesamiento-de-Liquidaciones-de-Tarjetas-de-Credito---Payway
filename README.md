# Procesamiento-de-Liquidaciones-de-Tarjetas-de-Credito---Payway
Proyecto Python para extraer, normalizar y clasificar datos clave de liquidaciones de tarjetas de crédito. Procesa información como tipo de tarjeta, banco, fechas, CUIT, e importes contables (comisiones, IVA, retenciones y saldos) desde documentos PDF, incluyendo contenido escaneado o en imágenes.


## 📄 Descripción General

Este proyecto en Python automatiza la **extracción detallada y el procesamiento contable** de liquidaciones de tarjetas de crédito, principalmente desde documentos PDF. Su funcionalidad clave reside en su capacidad para interpretar y capturar una amplia gama de datos esenciales, tanto de texto estándar como de contenido incrustado en imágenes (gracias a la integración de OCR).

El script está diseñado para:

* **Identificar y extraer** información fundamental como el tipo de tarjeta, el banco emisor, el número de liquidación, fechas, CUIT del comercio y datos de la empresa receptora.
* **Segmentar y cuantificar** importes críticos para la registración contable, incluyendo comisiones, IVA, retenciones, percepciones, multas, importes presentados, saldo final y descuentos totales.
* **Manejar PDFs complejos**, incluyendo la extracción de texto de imágenes mediante OCR (`PaddleOCR`) y la definición de áreas de recorte para una precisión mejorada.
* **Normalizar y estructurar** los datos extraídos en un formato tabular (`pandas DataFrame`), listo para ser utilizado en sistemas de gestión, conciliación contable o análisis financiero.

En esencia, esta herramienta simplifica y agiliza la tarea manual de procesar liquidaciones, reduciendo errores y optimizando el tiempo en la gestión financiera.

🛠️ Tecnologías Utilizadas
Este proyecto fue desarrollado con las siguientes herramientas y librerías:

Lenguaje de Programación: Python 3.12.7

Librerías Python:

pandas (versión 2.2.3): Esencial para la manipulación y análisis de los datos extraídos, permitiendo estructurarlos en DataFrames.

PyMuPDF (versión 1.25.2): Utilizada para la lectura, navegación y extracción de texto de los documentos PDF de liquidación.

re (módulo estándar de Python): Empleado para el uso de expresiones regulares en la búsqueda de patrones y limpieza de texto.

os (módulo estándar de Python): Para interactuar con el sistema operativo, gestionar rutas de archivos y directorios.

Pillow (PIL, versión 11.0.0): Para el procesamiento de imágenes, crucial en la preparación de las mismas para el reconocimiento OCR.

io (módulo estándar de Python): Permite trabajar con flujos de datos en memoria, como los bytes de las imágenes extraídas de los PDFs.

paddleocr (versión 2.7.0.3): El motor de OCR principal, encargado de reconocer y extraer texto de las imágenes y secciones escaneadas dentro de los PDFs.

numpy (versión 1.26.4): Fundamento para operaciones numéricas eficientes, especialmente en el manejo de arrays de datos de imágenes para el OCR.

