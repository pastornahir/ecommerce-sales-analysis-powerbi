
# 🛒 Análisis de eCommerce: Comportamiento del Usuario y Rendimiento Comercial

Este proyecto consiste en un análisis integral de los datos históricos de un eCommerce (período 2023-2025), orientado a identificar patrones de compra, niveles de actividad de clientes y el rendimiento de productos para optimizar la toma de decisiones estratégicas.

## 📊 Dashboard Interactivo
![Vista del Dashboard 1](./Dashboard_eCommerce_PowerBI%20(1).png)
![Vista del Dashboard 2](./Dashboard_eCommerce_PowerBI%20(2).png)
![Vista del Dashboard 3](./Dashboard_eCommerce_PowerBI%20(3).png)

> 📁 **[DESCARGAR INFORME COMPLETO EN PDF](./Proyecto_eCommerce_PastorNahir.pdf)** > *Consulta la documentación detallada con el proceso de limpieza, modelado y recomendaciones de negocio.*

---

## 🛠️ Stack Tecnológico
* **Power BI / Power Query:** Limpieza, normalización y modelado de datos.
* **DAX:** Implementación de medidas avanzadas e inteligencia temporal.
* **Excel:** Fuente de datos original.

---

## ⚙️ Proceso de Ingeniería de Datos (ETL)

La transformación se realizó en **Power Query**, priorizando la integridad del modelo:
* **Normalización Geográfica:** Conversión de códigos postales a formato Texto para evitar pérdida de ceros a la izquierda.
* **Saneamiento de Catálogo:** Eliminación de categorías con celdas vacías para asegurar la consistencia del análisis.
* **Optimización de Modelo:** Eliminación de columnas ambiguas (como `MetodoPagoID` en Órdenes) para simplificar la relación entre Ventas y Pagos vía `OrdenID`.
* **Inteligencia Temporal:** Creación de una **Tabla Calendario** personalizada para análisis comparativos por año, trimestre y mes.

---

## 🧠 Modelado y DAX
Se implementó un **Modelo Entidad-Relación** eficiente, centralizando todas las fórmulas en una tabla de medidas organizada.



* **Ventas Reales:** `SUMX(DetalleOrden, Cantidad * PrecioUnitario * (1 - Descuento))` - Cálculo neto considerando descuentos aplicados.
* **Ticket Promedio:** `DIVIDE([Ventas], [Órdenes generadas])` - Gasto medio por pedido.
* **Tasa de Actividad:** Porcentaje de usuarios que realizaron compras sobre el total registrado.
* **Métricas Dinámicas:** Uso de parámetros para alternar visualizaciones entre Ingresos y Unidades Vendidas.

---

## 📈 Hallazgos Clave y Conclusiones
* **Contraste Financiero:** Mientras las ventas crecieron un **24.18%**, el monto efectivamente cobrado disminuyó un **24.56%**, detectando un quiebre crítico a partir de marzo 2025.
* **Comportamiento del Usuario:** Se observó un retroceso del **46.60%** en usuarios activos desde febrero 2025, lo que sugiere la necesidad de nuevas estrategias de retención.
* **Preferencias de Pago:** La tarjeta de crédito concentra el **27.05%** del volumen transaccional.
* **Liderazgo Regional:** Chubut se posicionó como la provincia con mayor volumen de unidades vendidas en el período analizado.

---

## 👥 Perfil del Proyecto
* **Autor:** Nahir Anael Pastor 
* **Nivel:** Proyecto final de Data Analytics 2025 - CoderHouse
* **Alcance:** Limpieza, integración, análisis exploratorio y visualización.
