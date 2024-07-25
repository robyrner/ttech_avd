# WMS Retail

# **1. Caso de negocio**

## 1.1 - Descripción

Optimización del manejo de bodegas (WMS) en una Central de Distribución (CEDI) de la **_EmpresaX_**, perteneciente al sector Retail.

## 1.2 - Definición del problema

La **_EmpresaX_** se enfrenta a desafíos en la gestión de su cadena de suministro debido a fluctuaciones en la demanda, errores en la predicción de inventario y falta de coordinación entre las diferentes bodegas.

## 1.3 - Objetivos

- Mejorar la eficiencia en el manejo de bodegas en la central de distribución de la **_EmpresaX_**, optimizando el inventario y sus procesos logísticos.

- Reducción de costos en el manejo del inventario.

- Implementar modelos predictivos que permitan tomar decisiones más informadas y mejorar la eficiencia operativa en toda la cadena de suministro.

## 1.4 - Solución propuesta

- **_Análisis de datos:_** Se utilizarán datos históricos de inventario y movimientos de productos para identificar patrones de demanda, estacionalidad y tendencias.

- **_Modelamiento predictivo:_** Se desarrollarán modelos predictivos utilizando técnicas como series temporales para predecir la demanda futura de productos.

- **_Optimización de inventarios:_** Se utilizarán técnicas de optimización para determinar los niveles óptimos de inventario en cada bodega, minimizando los costos de almacenamiento y maximizando el cumplimiento de pedidos.

- **_Dashboard interactivo:_** Se creará un dashboard interactivo para visualizar métricas clave de rendimiento, como el nivel de inventario, la precisión de las predicciones y el cumplimiento de pedidos.

## 1.5 - Resultados esperados

- **_Reducción de costos:_** Se espera reducir los costos asociados con el exceso de inventario y los errores en la predicción de la demanda.

- **_Mejora en el servicio al cliente:_** Se espera mejorar la disponibilidad de productos y reducir los tiempos de entrega, lo que se traducirá en una mejor experiencia para el cliente.

- **_Eficiencia operativa:_** Se espera aumentar la eficiencia en los procesos logísticos, reduciendo los tiempos de manipulación y optimizando el uso de los recursos.

## 1.6 - Contexto

- **_Operación logística:_**
  
  La **_EmpresaX_** cuenta con varios Centros de Distribución **_(CEDI)_** operando en el país, que atienden procesos logísticos para las diferentes **_tiendas_** según la cercanía de cobertura geográfica.

  Los CEDI manejan la recepción de mercancías/productos del ecosistema de proveedores según la planeación de compras establecida en este sentido, y su ingreso correspondiente a las **_bodegas permanentes o en tránsito_**, para su posterior distribución y reparto.

  Dicha organización y gestión de almacenamiento se basa principalmente en los grupos de productos/familias (**_áreas_**), los métodos de conservación/preservación de vida útil, y el grado de ocupación/disponibilidad de bodegaje:

  - Cuadrante 1 (tránsito a despacho)
  - Alimentos
  - Aseo
  - Extradimensionados
  - Refrigerados
  - Congelados
  - Fruver Seco
  - Fruver Frío
  - Extraordinarios

  Los principales **_procesos de negocio_** de la cadena de valor que afectan el **_inventario_**, están relacionados con el manejo de pedidos, picking y despachos de los productos hacia las tiendas y entre CEDI (ingresos, retiros, reaprovisionamientos, calidad, traslados, bajas, entre otros).

  <div align="center">

  ![An image](https://drive.google.com/uc?id=1lQp0OpgtmyET3Cphjtds0M4b8N7rolP5)

  <div align="initial">

- **_Arquitectura técnica de operación:_**
  
  La **_EmpresaX_** cuenta con sistemas propios para el manejo y control de la operación de los CEDI, e instaló adicionalmente un sistema de manejo de bodegas **_(WMS)_** para 3 de ellos, los cuales funcionan bajo esquemas técnicos híbridos ( OnPremise y Cloud ).

  Como parte del proceso de gestión y monitoreo de dicha operación, se  implementaron una serie de indicadores **_(KPI)_** para la toma oportuna de decisiones, basándose en la información consolidada **_( periódica / en línea )_** de las transacciones y registros de actividad:

  <div align="center">

  ![An image](https://drive.google.com/uc?id=1hBEhwCATBOxE0xohjrR7w4rtDQOkuKhK)

  <div align="initial">

- **_KPI Operativos / Productividad:_**
  
  Los principales indicadores contemplados en el **_Dashboard Operativo_** abarcan el seguimiento de los procesos logísticos de **_pedidos, picking, despachos_**, organización de pallets/contenedores, rutas, áreas y el control de la productividad de los operarios que laboran en los diferentes CEDI.

  A continuación, una muestra referencial de algunos de ellos:

  - **_Cajas por actividad_**

  <div align="center">

  ![An image](https://drive.google.com/uc?id=1hB31ZcAnFGIBrKVigCej1Vc4s7d8Uev4)

  <div align="initial">

  - **_Cajas por Areas_**
  
  <div align="center">

  ![An image](https://drive.google.com/uc?id=1h-V6HCtPQAfNe5rAAOo7sjZYRVNJNHCi)

  <div align="initial">

  - **_Cajas por Contenedor_**

  <div align="center">

  ![An image](https://drive.google.com/uc?id=1gydqp1O05oOt1Bht2Qm-b-tRqTkS5drk)

  <div align="initial">

  - **_Productividad Picking_**
  
  <div align="center">

  ![An image](https://drive.google.com/uc?id=1gsAOviGdhRgjycWRTKO3cG6req2A6eXP)

  <div align="initial">

  ---
**<font color='red'>Notas de revisión</font>**

Es necesario identificar oportunidades de mejora en la **_gestión de la demanda_**:
- Manejo del inventario
- Stocks mínimos
- Planeación de despachos
- Predicciones más acertadas de pedidos
- Organización del bodegaje respectivo

---
