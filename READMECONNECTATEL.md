ConnectaTel – Análisis de Comportamiento de Usuarios en Telecomunicaciones
📌 Descripción del Proyecto

Este proyecto analiza el comportamiento de uso de clientes de ConnectaTel, una empresa de telecomunicaciones que opera en Latinoamérica.
El objetivo del análisis es comprender cómo los usuarios utilizan los servicios de llamadas y mensajes, identificar patrones de consumo, detectar valores atípicos y segmentar clientes para generar insights accionables para el negocio.

El análisis se basa en datos históricos registrados hasta 2024.

🎯 Objetivos del Análisis

Evaluar la calidad de los datos y realizar limpieza básica.

Analizar el comportamiento de uso de llamadas y mensajes.

Detectar valores atípicos (outliers) en el uso de servicios.

Segmentar clientes según:

Nivel de uso

Grupo de edad

Identificar patrones que permitan mejorar la oferta comercial de planes.

🗂 Dataset Utilizados

El análisis utiliza tres datasets principales:

1️⃣ plans.csv

Información de los planes ofrecidos por la empresa.

Incluye:

Precio mensual

Minutos incluidos

Datos incluidos (GB)

Costos adicionales por uso extra

2️⃣ users_latam.csv

Información demográfica y contractual de los usuarios.

Incluye:

ID del usuario

Nombre

Edad

Ciudad

Fecha de registro

Plan contratado

Fecha de cancelación (churn)

3️⃣ usage.csv

Registro de uso del servicio por evento.

Incluye:

Tipo de evento (call o text)

Duración de llamadas

Longitud de mensajes

Fecha de uso

🧹 Limpieza y Preparación de Datos

Durante el proceso de limpieza se identificaron los siguientes problemas:

Valores sentinel (-999) en la columna age.

Valores "?" en la columna city.

Fechas registradas como texto que requirieron conversión a formato datetime.

Valores nulos estructurales en:

duration (cuando el evento es text)

length (cuando el evento es call)

Acciones realizadas:

Reemplazo de sentinels por la mediana de edad.

Conversión de "?" a valores nulos (NA).

Conversión de fechas a formato datetime.

Validación de fechas fuera de rango.

📊 Análisis Exploratorio

Se realizaron análisis estadísticos y visualizaciones para entender:

Distribución de edades de los usuarios

Cantidad de mensajes enviados

Cantidad de llamadas realizadas

Total de minutos hablados

También se utilizaron boxplots para detectar outliers en las variables de uso.

👥 Segmentación de Clientes

Los usuarios fueron segmentados en dos dimensiones principales:

Segmentación por Nivel de Uso

Basada en número de llamadas y mensajes:

Grupo	Condición
Bajo uso	< 5 llamadas y < 5 mensajes
Uso medio	< 10 llamadas y < 10 mensajes
Alto uso	resto de usuarios
Segmentación por Edad
Grupo	Edad
Joven	< 30
Adulto	30 – 59
Adulto Mayor	≥ 60
🔎 Hallazgos Principales

La mayoría de los usuarios presenta niveles de uso bajo o medio.

Existe un grupo reducido de usuarios intensivos (heavy users) que generan mayor consumo de llamadas y minutos.

La base de clientes está compuesta principalmente por adultos entre 30 y 59 años.

Los valores extremos detectados corresponden principalmente a usuarios con alto consumo real, no a errores en los datos.

💡 Recomendaciones para el Negocio

A partir del análisis se sugieren las siguientes acciones:

Diseñar planes premium dirigidos a usuarios de alto consumo.

Ofrecer planes básicos de menor costo para usuarios de bajo uso.

Analizar el comportamiento de heavy users, ya que representan una oportunidad de mayor ingreso.

Continuar monitoreando patrones de uso para optimizar la oferta de servicios.
