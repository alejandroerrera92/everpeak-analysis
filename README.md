Análisis de Datos y Segmentación de Clientes para EverPeak Holdings 📊

Este repositorio contiene un análisis exhaustivo de los datos transaccionales de EverPeak Holdings, realizado como parte del proceso de adquisición por parte de SilverBasket Retail Group. El objetivo principal es evaluar la calidad de los datos, identificar patrones de comportamiento de los clientes y desarrollar una segmentación estratégica.

📋 Contenido
everpeak_retail_analysis.ipynb: El notebook principal con todo el código, explicaciones y visualizaciones del análisis.
🎯 Objetivos del Análisis
Evaluar la Calidad y Consistencia de los Datos: Revisar la estructura, volumen y presencia de valores faltantes en el dataset.
Limpieza y Preparación de Datos: Implementar un pipeline robusto para estandarizar formatos, manejar valores nulos y corregir inconsistencias.
Análisis Estadístico y Manejo de Atípicos: Realizar un estudio detallado de variables clave (order_value, customer_age) para entender su distribución y tratar valores atípicos.
Segmentación de Clientes: Desarrollar una segmentación de clientes basada en el valor de las transacciones y la edad, para identificar grupos estratégicos de alto valor y potencial de crecimiento.
🚀 Dataset Utilizado
El análisis se basa en el dataset everpeak_retail.csv, que contiene 5,008 observaciones y 11 columnas representando transacciones individuales. Las variables clave incluyen:

order_id, customer_id
order_date
product_category, price, quantity, order_value
payment_method, city, state, customer_age
🧹 Limpieza y Preparación de Datos
Se implementó un pipeline modular para la limpieza de datos, que incluyó:

Columnas de Texto: Estandarización a minúsculas, eliminación de espacios, y reemplazo de valores ? o nulos por 'Unknown'.
Columnas Numéricas: Conversión a tipo numérico, tratamiento de sentinelas (-999) y imputación de valores faltantes con la media.
Fechas: Conversión de order_date a formato datetime.
Duplicados: Eliminación de registros duplicados.
Este proceso aseguró un dataset limpio y consistente, listo para el análisis.

📈 Análisis Estadístico y Manejo de Atípicos
Se realizó un análisis detallado de order_value y customer_age:

order_value
Distribución: Asimétrica a la derecha, con la mayoría de las transacciones en valores bajos y medios.
Atípicos: Identificados mediante el método IQR. Se eliminaron 165 outliers para evitar distorsiones en la segmentación.
Resumen: Tras la limpieza, la variable muestra un mean de 8,507.72 y una median de 10,136.00, con un rango intercuartílico amplio.
customer_age
Distribución: Relativamente simétrica, con una edad promedio de 49.52 años y una mediana de 49.12 años.
Rango: Edades entre 18 y 80 años, coherente con un perfil de cliente diverso.
Conclusión: La variable es estable y adecuada para segmentación por edad sin necesidad de tratar atípicos.
👥 Segmentación de Clientes
Se desarrolló una estrategia de segmentación combinando order_value y customer_age, resultando en los siguientes grupos:

Segmento	Clientes
Senior VIP	2005
Low Value	1699
Jr. Medium Value	654
Junior VIP	485
Senior VIP: El grupo más numeroso y estratégico, compuesto por clientes de alto gasto y mayor edad, indicando lealtad y estabilidad.
Low Value: Segundo grupo en tamaño, con potencial para estrategias de activación y crecimiento.
Jr. Medium Value y Junior VIP: Grupos más pequeños pero clave para el crecimiento futuro, combinando menor edad con gasto medio o alto.
Esta segmentación proporciona una visión clara y accionable de la base de clientes de EverPeak.

🛠️ Tecnologías Utilizadas
Python
Pandas
Matplotlib
Seaborn
🏃‍♀️ ¿Cómo ejecutar el Notebook?
Abrir en Google Colab: Puedes abrir el notebook directamente en Google Colab haciendo clic en el enlace del archivo .ipynb en este repositorio y seleccionando "Abrir en Colab".
Ejecutar Celdas: Ejecuta cada celda del notebook secuencialmente. Asegúrate de que todas las celdas se ejecuten sin errores para reproducir el análisis.
📝 Conclusiones y Próximos Pasos
El análisis de EverPeak Holdings revela una base de datos robusta con necesidades de limpieza manejables. La segmentación de clientes proporciona insights valiosos sobre la distribución demográfica y de valor, identificando grupos clave para la estrategia de SilverBasket Retail Group.

Se recomienda utilizar estos segmentos para desarrollar campañas de marketing dirigidas, estrategias de retención y evaluar el potencial de crecimiento a futuro tras la adquisición.
