# Ε Proyecto Epsilon | Análisis de Rentabilidad de Planes de Telecomunicaciones

## Descripción

Megaline es una empresa de telecomunicaciones que ofrece a sus clientes dos planes de prepago: **Surf** y **Ultimate**. El objetivo de este proyecto fue analizar el comportamiento de consumo de los usuarios y determinar cuál de los dos planes genera mayores ingresos para la compañía.

Para ello, se trabajó con información de llamadas, mensajes de texto, consumo de internet y características de los planes contratados. A partir de estos datos se calcularon los ingresos mensuales generados por cada cliente y se aplicaron pruebas estadísticas para evaluar si las diferencias observadas entre los planes eran significativas.

## Objetivos

- Evaluar la calidad de los datos disponibles.
- Analizar los patrones de consumo de los clientes.
- Calcular el uso mensual de llamadas, mensajes y datos móviles.
- Estimar los ingresos generados por cada usuario.
- Comparar el desempeño financiero de los planes Surf y Ultimate.
- Analizar el comportamiento de consumo por tipo de servicio.
- Aplicar pruebas estadísticas para validar diferencias entre grupos.
- Generar recomendaciones para apoyar decisiones comerciales basadas en datos.

## Herramientas utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Jupyter Notebook
- Estadística descriptiva
- Pruebas de hipótesis

## Fuente de datos

El proyecto utiliza información operativa de clientes de Megaline durante 2018.

Archivos utilizados:

- `megaline_users.csv`
- `megaline_calls.csv`
- `megaline_messages.csv`
- `megaline_internet.csv`
- `megaline_plans.csv`

## Metodología

### 1. Preparación de datos

- Exploración inicial de todas las tablas.
- Revisión de tipos de datos.
- Identificación de valores ausentes.
- Búsqueda de duplicados explícitos e implícitos.
- Corrección y estandarización de variables relevantes.

### 2. Construcción de métricas mensuales

Se calcularon para cada usuario:

- Número de llamadas por mes.
- Minutos consumidos por mes.
- Mensajes enviados por mes.
- Volumen mensual de datos móviles.

Posteriormente, todas las métricas fueron integradas en una única tabla consolidada.

### 3. Cálculo de ingresos

Para cada usuario se calcularon:

- Excedentes de minutos.
- Excedentes de mensajes.
- Excedentes de datos móviles.
- Costos adicionales según las condiciones de cada tarifa.

Finalmente se estimó el ingreso total mensual generado por cada cliente.

### 4. Análisis exploratorio

Se analizaron:

- Minutos consumidos por plan.
- Mensajes enviados por plan.
- Consumo de internet por plan.
- Ingresos generados por plan.

Para ello se utilizaron:

- Gráficos de barras.
- Histogramas.
- Diagramas de caja.
- Estadísticas descriptivas.

### 5. Pruebas estadísticas

Se aplicaron pruebas de hipótesis para:

- Comparar los ingresos promedio entre Surf y Ultimate.
- Comparar los ingresos de usuarios de NY-NJ frente al resto de regiones.

## Principales hallazgos

### Consumo de llamadas

- El consumo promedio de minutos fue muy similar entre ambos planes.
- La mayoría de los usuarios utilizó menos minutos que los incluidos en sus tarifas.
- No se observaron diferencias relevantes en el patrón de llamadas entre Surf y Ultimate.

### Consumo de mensajes

- Los usuarios de Ultimate enviaron más mensajes en promedio.
- Aun así, el volumen de mensajes permaneció muy por debajo de los límites incluidos en ambos planes.

### Consumo de internet

- Ultimate presentó un consumo promedio de datos ligeramente superior.
- Muchos usuarios de Surf se acercaron o superaron el límite de datos incluido en el plan.
- El consumo de internet resultó ser uno de los principales factores asociados a cargos adicionales.

### Ingresos por plan

Ingreso promedio mensual:

- Surf: **57,29 USD**
- Ultimate: **72,12 USD**

Los usuarios de Ultimate generaron mayores ingresos promedio que los usuarios de Surf.

Además:

- Ultimate mostró ingresos más estables.
- Surf presentó una alta variabilidad debido a los cargos por excedentes de consumo.

## Resultados de las pruebas estadísticas

### Comparación de ingresos entre Surf y Ultimate

Hipótesis:

- H₀: ambos planes generan el mismo ingreso promedio.
- H₁: los ingresos promedio son diferentes.

Resultado:

- p-value = 4.88 × 10⁻²⁵

Conclusión:

Se rechazó la hipótesis nula, lo que indica que existe una diferencia estadísticamente significativa entre los ingresos generados por ambos planes.

### Comparación de ingresos entre NY-NJ y otras regiones

Hipótesis:

- H₀: los ingresos promedio son iguales.
- H₁: los ingresos promedio son diferentes.

Resultado:

- p-value = 0.0186

Conclusión:

Se rechazó la hipótesis nula, indicando diferencias significativas entre los ingresos generados por los clientes de NY-NJ y los clientes del resto de regiones.

## Visualizaciones desarrolladas

- Consumo promedio de minutos por mes y por plan.
- Distribución del consumo de minutos.
- Diagramas de caja para llamadas.
- Consumo promedio de mensajes por plan.
- Consumo promedio de datos por plan.
- Distribución del uso de internet.
- Diagramas de caja del consumo de datos.
- Distribución de ingresos por plan.

## Archivos principales

- `epsilon_telecom_plan_profitability_analysis.ipynb`
- `megaline_users.csv`
- `megaline_calls.csv`
- `megaline_messages.csv`
- `megaline_internet.csv`
- `megaline_plans.csv`

## Conclusión

El análisis permitió identificar diferencias claras entre los planes Surf y Ultimate tanto en el comportamiento de consumo como en los ingresos generados para la compañía.

Aunque ambos grupos presentan patrones similares en llamadas y mensajes, el consumo de datos móviles y la estructura tarifaria producen diferencias relevantes en la facturación. Los usuarios de Ultimate generan mayores ingresos promedio y muestran un comportamiento más estable, mientras que los usuarios de Surf presentan una mayor variabilidad debido a los cargos adicionales por exceder los límites incluidos.

Las pruebas estadísticas confirmaron que la diferencia observada en los ingresos no es producto del azar, por lo que existe evidencia suficiente para concluir que **Ultimate es el plan que genera mayores ingresos para Megaline**.

Desde una perspectiva de negocio, los resultados sugieren que la compañía podría obtener mejores resultados financieros promoviendo el plan Ultimate dentro de sus estrategias comerciales y campañas publicitarias.
