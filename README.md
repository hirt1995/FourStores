## 📈 Análisis de Rendimiento de Tiendas y Recomendaciones Estratégicas (2020-2023)

### 📝 Resumen del Notebook

Este *notebook* realiza un análisis en profundidad de los datos de ventas de cuatro tiendas distintas (`Tienda 1` a `Tienda 4`) para evaluar su rendimiento, identificar tendencias clave y proporcionar recomendaciones estratégicas a las partes interesadas. El objetivo principal es determinar qué tienda, si acaso, debe ser considerada para el cierre, basándose en diversas métricas financieras y operacionales.

### 📊 Conjunto de Datos Utilizado
El análisis utiliza datos de transacciones de ventas de cuatro archivos CSV separados (`tienda_1.csv`, `tienda_2.csv`, `tienda_3.csv`, `tienda_4.csv`), los cuales se consolidan en un único *Pandas DataFrame*. Este conjunto de datos exhaustivo incluye información detallada como:
- **Product (Producto):** Nombre del artículo vendido.
- **Categoría del Producto:** Categoría a la que pertenece el producto.
- **Precio:** Precio del producto.
- **Costo de envío:** Costo del envío.
- **Fecha de Compra:** Fecha en que se realizó la compra.
- **Vendedor:** Nombre del vendedor.
- **Lugar de Compra:** Ciudad donde se realizó la compra.
- **Calificación:** Puntuación del cliente para la transacción.
- **Método de pago:** Método de pago utilizado.
- **Cantidad de cuotas:** Número de cuotas del pago.
- **lat/lon:** Coordenadas geográficas de la ubicación de la compra.
- **Tienda:** Identificador de la tienda donde ocurrió la venta.

### 🚀 Resumen del Proceso Analítico
El *notebook* sigue un enfoque analítico estructurado:
1. **Importación y Preparación de Datos:** Carga de datos de las cuatro tiendas, fusión y realización de conversiones iniciales de tipos de datos (p. ej., convertir 'Fecha de Compra' a objetos `datetime`).
2. **Análisis Exploratorio de Datos (EDA):** Inspección inicial de la estructura del conjunto de datos, estadísticas básicas, valores únicos y una revisión exhaustiva de valores faltantes o duplicados para garantizar la calidad de los datos.
3. **Análisis de Facturación:** Evaluación del volumen de ventas, ingresos totales (precio + costo de envío) tanto en COP como en USD, y análisis de las preferencias de pago de los clientes en todas las tiendas.
4. **Ventas por Categoría:** Análisis del número de artículos vendidos y los ingresos totales generados por cada categoría de producto para cada tienda, incluyendo visualizaciones.
5. **Rendimiento de Producto/Categoría:** Identificación de las categorías de productos y productos individuales con mayores y menores ingresos para cada tienda, basándose en los ingresos totales.
6. **Evaluación del Rendimiento de la Tienda:** Evaluación de la calificación promedio de los clientes para cada tienda.
7. **Análisis Geográfico:** Examen del volumen de compras por ciudad y visualización de la distribución geográfica de las categorías de productos más vendidos en Colombia para cada tienda.
8. **Análisis del Costo de Envío:** Cálculo del costo de envío promedio por tienda.
9. **Análisis del Rendimiento del Vendedor:** Evaluación detallada del rendimiento individual de los vendedores basándose en el volumen de ventas, las calificaciones promedio y el porcentaje de calificaciones altas/bajas, identificando a los vendedores y tiendas con mejor y peor rendimiento para cada uno.
10. **Análisis de Ingresos de Series de Tiempo:** Visualización de las tendencias de ingresos mensuales para cada tienda a lo largo de varios años (2020-2023) para comprender los patrones estacionales y el rendimiento a largo plazo.
11. **Recomendaciones:** Basado en el análisis exhaustivo, proporcionar una conclusión final sobre el rendimiento de la tienda y recomendaciones accionables para Mr. Joao, incluyendo sugerencias para mejorar la recopilación de datos.

---

## 📊 Conclusiones Clave del Rendimiento de Tiendas

### 1. Volumen de Ventas e Ingresos Totales

| Métrica | Tienda 1 | Tienda 4 | Comentario General |
| :--- | :--- | :--- | :--- |
| Volumen de Artículos | 2,359 | 2,358 | Muy similar entre las 4 tiendas.|
| Ingresos Totales (USD) | **297,769 USD** | **268,661 USD** | Tienda 1 lidera; Tienda 4 es la de menor ingreso.|

Tienda 2 y 3 están por encima de los ingresos de Tienda 4.

### 2. Tendencias de Ingresos Históricos (2020-2023)

La métrica más crítica es la **tendencia descendente de la Tienda 4**.

* **Periodo 2020-2021:** Tienda 4 alcanzó picos máximos de **40 Millones COP/mes**.
* **Periodo 2022-2023:** Tienda 4 **no logra superar la barrera de los 30 Millones COP/mes**, mientras que las demás tiendas mantienen o superan consistentemente este umbral.

### 3. Rendimiento de Categorías y Métodos de Pago

* **Métodos de Pago Preferidos:** **Tarjeta de crédito** y **Nequi** son los más utilizados en todas las tiendas.
* **Categorías Más Rentables:** **Electrónicos** y **Electrodomésticos** generan las mayores ganancias, a pesar de que 'Muebles' tiene un alto volumen de ventas con un margen de ganancia inferior.
* **Categorías de Baja Rentabilidad:** **Artículos para el hogar** y **Libros** son las menos vendidas y menos rentables (no superan los $4,000 USD/mes).
* **Distribución Geográfica:** Los productos más rentables se distribuyen de manera uniforme en **Medellín, Bogotá y Cali**.

### 4. Calificación y Rendimiento del Personal

* **Calificación de Tiendas:** El promedio de satisfacción del cliente es similar en todas las tiendas, con **4.0**.
* **Rendimiento de Vendedores:** Se identificó a **Izabela de León** como la vendedora con el mayor volumen de ventas, pero con la **peor calificación y rendimiento** en comparación con sus compañeros, lo que indica un problema de calidad que requiere atención.

---

## 🔍 Análisis Detallado de Rendimiento de Tiendas y Estrategia Operativa (2020-2023)

Este análisis amplía las conclusiones clave sobre el desempeño financiero, la eficiencia operativa y las tendencias históricas de las cuatro tiendas, ofreciendo una base más sólida para la toma de decisiones estratégicas.

---

### 1. 💰 Desempeño Financiero y de Volumen

#### 1.1. Volumen de Ventas e Ingresos Totales
Las tiendas muestran una notable **homogeneidad en la capacidad de mover inventario**, con un volumen de artículos vendidos que apenas varía entre ellas.

* **Volumen de Artículos:** 2,359 artículos en promedio. La Tienda 4 (2,358) no difiere significativamente en volumen de transacciones.
* **Disparidad de Ingresos:** A pesar del volumen similar, existe una brecha de ingresos notable:
    * **Tienda 1 (Líder):** $297,769 USD en ingresos totales.
    * **Tienda 4 (Rezago):** $268,661 USD en ingresos totales.

> **Implicación:** La Tienda 4 está vendiendo la misma cantidad de artículos, pero su cesta promedio o la mezcla de productos vendidos es menos valiosa que la de sus competidores, lo que ya sugiere problemas de mezcla de inventario o precios.

#### 1.2. Rentabilidad por Categoría y Estrategia de Inventario

El análisis de categorías revela una **clara necesidad de optimización de inventario**:

| Categoría de Producto | Estrategia de Venta | Recomendación de Estrategia |
| :--- | :--- | :--- |
| **Electrónicos y Electrodomésticos** | Alto Margen de Ganancia | **Foco Prioritario:** Maximizar el inventario y la estrategia de *marketing* en estas categorías. |
| **Muebles** | Alto Volumen, Bajo Margen | **Revisión de Margen:** Evaluar costos de adquisición, almacenamiento y logística. El alto volumen no justifica la baja rentabilidad. |
| **Artículos para el hogar y Libros** | Bajo Volumen y Baja Ganancia | **Descontinuación/Reducción:** Considerar eliminar estas líneas en las tiendas que no superan los $4,000 USD/mes, liberando espacio y recursos. |

---

### 2. 📉 Crisis de la Tienda 4: Tendencia Histórica

El principal riesgo para la empresa se centra en la sosteniblidad de la Tienda 4, como lo demuestra el análisis de series de tiempo.

* **Estabilidad General (2020-2023):** Tienda 1, Tienda 2 y Tienda 3 han demostrado **resiliencia**, manteniendo o superando consistentemente el umbral de **30 Millones COP/mes**.
* **Declive de la Tienda 4:** La tienda tuvo buenos rendimientos en 2020-2021 (picos de 40 Millones COP/mes), pero a partir de 2022 y en los registros de 2023, ha **fallado consistentemente en alcanzar los 30 Millones COP/mes**.

> **Conclusión Financiera:** La Tienda 4 ya no opera al nivel de sus pares y está en una trayectoria de declive sostenido. Su volumen de ventas ya no se traduce en ingresos competitivos.

---

### 3. 👥 Rendimiento Operacional y de Personal

#### 3.1. Calidad de Servicio y Capacitación
* **Calificación General:** El promedio de **4.0** es aceptable, pero indica que existe margen de mejora en la satisfacción del cliente.
* **El Problema Izabela de León:** El caso de esta vendedora ilustra una desconexión entre la eficiencia en la venta y la calidad del servicio. Su alto volumen de ventas con la **peor calificación promedio** sugiere:
    * **Necesidad de Intervención:** Urgente capacitación enfocada en servicio al cliente.
    * **Riesgo de Marca:** Su bajo rendimiento puede estar dañando la reputación de la marca a pesar de generar altos ingresos.

#### 3.2. Geografía y Costos de Envío
* **Estrategia Geográfica:** Los puntos calientes de venta (**Medellín, Bogotá y Cali**) son consistentes para los productos más rentables, lo que sugiere que la distribución actual de las tiendas es adecuada.
* **Costo de Envío:** El costo promedio de **$6 USD** es uniforme, eliminándolo como un factor de diferenciación o problema logístico entre las tiendas.

---

### 🎯 Conclusión Final y Recomendaciones
Es fundamental complementar el análisis con datos de costos para calcular la verdadera **Utilidad Neta**.

#### Conclusiones Clave

1.  **Recomendación de Cierre (Tienda 4):** Dada su persistente tendencia a la baja en ventas y su inferior rentabilidad en 2022-2023, se recomienda el **cierre potencial** de la Tienda 4.
2.  **Reevaluación de Stock:** Se debe considerar **replantear la venta** de 'Artículos para el hogar' y 'Libros' en todas las tiendas debido a su baja rentabilidad.
3.  **Acción de Personal:** Es crucial **revisar el desempeño y capacitación** del personal, especialmente de vendedores de alto volumen con bajas calificaciones (ej. Izabela de León).
4.   **Registro de Costos Operacionales:** Implementar un sistema de contabilidad por centro de costo para capturar gastos como **mantenimiento, nómina y gastos fijos** de cada tienda. Esto permitirá calcular la:

    **Utilidad Neta = Ingresos Totales Costo de Bienes Vendidos - Gastos Operativos**

#### 📝Recomendaciones para Mejoras en el Registro de Datos

Para una toma de decisiones más precisa en el futuro, se requiere la implementación de las siguientes mejoras en la captura de datos:

1.  **Diferenciación de Canales de Venta:** Es vital registrar **'En Persona' vs. 'Online'** para cada transacción. Esta información permitirá:
    * **Optimizar Logística:** Tomar decisiones sobre dónde ubicar inventario o centros de distribución para reducir los $6 USD de costo de envío promedio.
    * **Entender al Cliente:** Adaptar promociones y la experiencia de compra a la preferencia de cada canal.
2.  **Rastrear Costos Operacionales:** Implementar un sistema para registrar **gastos operativos** (mantenimiento, nómina, etc.) por tienda. Esto es esencial para calcular una **verdadera utilidad neta** y el rendimiento real de cada sucursal.
