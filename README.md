# Análisis de Comportamiento de Clientes - ConnectaTel (2022-2024)

Este proyecto realiza un análisis exploratorio de datos (EDA) y una limpieza profunda sobre la base de clientes de la empresa de telecomunicaciones **ConnectaTel**, con el fin de identificar patrones de consumo, segmentación demográfica y áreas de oportunidad comercial.

## 🎯 Objetivo del Proyecto
El objetivo principal es transformar datos brutos en información estratégica para la toma de decisiones, enfocándose en:
*   Identificar el perfil demográfico dominante (edad y ubicación).
*   Analizar el comportamiento de consumo según el plan contratado (Básico vs. Premium).
*   Detectar y corregir anomalías técnicas en los registros de la base de datos para asegurar reportes precisos.

## 📊 Datasets Utilizados
El análisis integra datos transaccionales y demográficos que incluyen las siguientes variables clave:
*   **Demográficos:** `age` (edad), `city` (ciudad), `gender` (género).
*   **Servicios:** `plan` (tipo de suscripción), `monthly_bill` (facturación).
*   **Consumo:** `calls_made` (cantidad de llamadas), `duration` (minutos), `messages_sent` (SMS), `data_used` (GB).
*   **Temporales:** `registration_date` (fecha de alta).

## 🛠️ Etapas del Análisis
El flujo de trabajo se dividió en cuatro fases críticas:

1.  **Limpieza de Datos (Data Wrangling):**
    *   Tratamiento de valores centinela (ej. edad `-999` sustituida por la mediana).
    *   Corrección de inconsistencias temporales (fechas registradas en el futuro como 2026).
    *   Estandarización de valores categóricos faltantes (`"?"` en ciudades).
2.  **Análisis Exploratorio (EDA):**
    *   Cálculo de estadísticas descriptivas (promedios de consumo de 23.31 min y 5.5 mensajes).
    *   Visualización de distribuciones de edad y planes.
3.  **Segmentación:**
    *   Comparativa de uso entre usuarios de planes Básico (64.88%) y Premium (35.12%).
4.  **Conclusiones Estratégicas:**
    *   Identificación de oportunidades de *upselling* y recomendaciones de retención.

## 🚀 Cómo ejecutar el Notebook

### Opción 1: Google Colab (Recomendado)
Para ejecutar este proyecto sin instalar nada localmente:
1. Sube el archivo `.ipynb` y los datasets a tu unidad de **Google Drive**.
2. Haz clic derecho sobre el notebook y selecciona **Abrir con > Google Colaboratory**.
3. Asegúrate de que las rutas de carga de los archivos CSV en el código coincidan con la ubicación en tu Drive o súbelos directamente a la sesión temporal de Colab usando el icono de carpeta en la barra lateral izquierda.

### Opción 2: Local (Jupyter / VS Code)
1. Clona este repositorio o descarga los archivos.
2. Asegúrate de tener instalado Python 3.8+ y las librerías necesarias:
   ```bash
   pip install pandas numpy matplotlib seaborn
