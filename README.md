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

  ![image](https://github.com/user-attachments/assets/f822a3f0-2731-40e3-b297-38fe838e9673)

  <div align="initial">

- **_Arquitectura técnica de operación:_**
  
  La **_EmpresaX_** cuenta con sistemas propios para el manejo y control de la operación de los CEDI, e instaló adicionalmente un sistema de manejo de bodegas **_(WMS)_** para 3 de ellos, los cuales funcionan bajo esquemas técnicos híbridos ( OnPremise y Cloud ).

  Como parte del proceso de gestión y monitoreo de dicha operación, se  implementaron una serie de indicadores **_(KPI)_** para la toma oportuna de decisiones, basándose en la información consolidada **_( periódica / en línea )_** de las transacciones y registros de actividad:

  <div align="center">

  ![image](https://github.com/user-attachments/assets/2f8ab92f-609e-4aaa-b84a-aef068179b61)

  <div align="initial">

- **_KPI Operativos / Productividad:_**
  
  Los principales indicadores contemplados en el **_Dashboard Operativo_** abarcan el seguimiento de los procesos logísticos de **_pedidos, picking, despachos_**, organización de pallets/contenedores, rutas, áreas y el control de la productividad de los operarios que laboran en los diferentes CEDI.

  A continuación, una muestra referencial de algunos de ellos:

  - **_Cajas por actividad_**

  <div align="center">

  ![image](https://github.com/user-attachments/assets/4dfd5f26-58cd-4596-bcf1-c2ae5a546531)

  <div align="initial">

  - **_Cajas por Areas_**
  
  <div align="center">

  ![image](https://github.com/user-attachments/assets/59bc0642-d3d1-48cc-a002-4332951e8328)

  <div align="initial">

  - **_Cajas por Contenedor_**

  <div align="center">

  ![image](https://github.com/user-attachments/assets/821a295c-bcf9-474d-9510-0a9b081c36bc)

  <div align="initial">

  - **_Productividad Picking_**
  
  <div align="center">

  ![image](https://github.com/user-attachments/assets/2524c516-fdce-4499-af4e-ad3918c33ca4)

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

# **2. Configuración**

# **3. Análisis exploratorio de datos (EDA)**

## 3.1 - Fuentes de datos

- **_Consideraciones generales:_**

  1. A partir de los scripts utilizados para la generación del Dashboard Operativo (KPI), se obtuvieron varios archivos planos con la **_consolidación del proceso de pedidos, picking y despachos_** de un CEDI en particular, dentro de un rango de días.

  1. Las observaciones generadas contienen la información **_detallada_** del proceso logístico de todas las tiendas bajo la cobertura geográfica del CEDI respectivo, con el fin de tener muestras representativas del proceso.
  
  1. Para la escogencia del período de tiempo, se consideraron en lo posible, las actividades recurrentes y ocasionales dentro de la operación del CEDI: **_durante la semana, fines de semana y fechas especiales_** ( día de la madre, por ejemplo ).

  1. Se pretende realizar el análisis teniendo en cuenta las observaciones más adecuadas dentro de las posibles generadas.  

- **_Observaciones disponibles:_**

  - **_Formato de archivos:_** WMS_Consolidado \_ [ FechaFinal ] \_ [ FechaInicial ] \_ [ NroDías ] . csv

  - **_Información adicional:_** Cantidad de días y registros generados en cada caso

<div align="center">

| Nro | Archivo | Días | Registros |
|:---:|---|:---:|---:|
| 1 | WMS_Consolidado_20221109_20221103_07d.csv |  7 |   188,497 |
| 2 | WMS_Consolidado_20230102_20221231_05d.csv |  5 |   186,963 |
| 3 | WMS_Consolidado_20230423_20230418_07d.csv |  7 |   226,025 |
| 4 | WMS_Consolidado_20230427_20230413_15d.csv | 15 |   525,206 |
| 5 | WMS_Consolidado_20230514_20230418_27d.csv | 27 |   957,931 |
| 6 | WMS_Consolidado_20230517_20230510_08d.csv |  8 |   308,635 |
| 7 | WMS_Consolidado_20230531_20230418_44d.csv | 44 | 1,562,109 |

<div align="initial">

- **_Campos de información detallada:_**

<div align="center">

| Nro | Columna | Descripción Columna |
|:---:|---|---|
|  1 | ALMACE                 | Código del CEDI                                                                           |
|  2 | CEDI                   | Nombre del CEDI                                                                           |
|  3 | COD_CLIENTE            | Código del cliente (tienda)                                                               |
|  4 | NOMBRE                 | Nombre largo de la tienda, incluyendo ciudad de ubicación                                 |
|  5 | NOM_CORTO              | Nombre corto de la tienda                                                                 |
|  6 | FECHA_SERVICIO         | Fecha en la que se habilita el servicio en tiendas ( inventario físico )                  |
|  7 | FECHA_TRANSMISION      | Fecha en la que se genera la transmisión de información para procesamiento                |
|  8 | FECHA_ALTA             | Fecha en la que se da el alta para servicio ( luego de inactivación temporal )            |
|  9 | FECHA_PROCESAMIENTO    | Fecha en la que se realiza el procesamiento de información                                |
| 10 | FECHA_ACTIVACION       | Fecha de activacion del inventario en tiendas                                             |
| 11 | RUTA                   | Código de la ruta de transporte ( despachos )                                             |
| 12 | DESC_RUTA              | Nombre de la ruta de transporte ( Ruta1 ... Ruta12, Sin Asignación )                      |
| 13 | PEDIDO_INLOG           | Número del pedido dentro del sistema WMS                                                  |
| 14 | AREA                   | Código del área o familia de productos                                                    |
| 15 | DESC_AREA              | Descripción del área o familia de productos ( Cuadrante 1, Alimentos, Aseo,               |
|    |                        | Extradimensionados, Refrigerados, Congelados, Fruver Seco, Fruver Frío, Extraordinarios ) |
| 16 | PEDIDO_SAP             | Número del pedido dentro del sistema ERP (SAP)                                            |
| 17 | LIN_PEDIDO             | Línea del pedido del Sistema ERP (SAP)                                                    |
| 18 | ARTICULO               | Código del artículo                                                                       |
| 19 | NOMBRE_ARTICULO        | Nombre del artículo                                                                       |
| 20 | CANTI_PEDIDA           | Cantidad de artículos solicitados por tienda dentro del pedido                            |
| 21 | SITUACION_PEDIDO       | Situación del pedido: Pedidos (PE,PR,AC) / Picking (CU,TE,ET) / Despachos (EX)            |
| 22 | UNI_CAJ_PEDIDO         | Cantidad de unidades por caja de pedido                                                   |
| 23 | UNIDAD_DISPLAY_PEDIDO  | Cantidad de unidades para pedido                                                          |
| 24 | CANTIDAD_RECOGIDA      | Cantidad de artículos recogidos para picking                                              |
| 25 | UNI_CAJ_SERVIDA        | Cantidad de unidades por caja de picking                                                  |
| 26 | UNIDAD_DISPLAY_SERVIDA | Cantidad de unidades para picking                                                         |
| 27 | CANTIDAD_CARGADA       | Cantidad de artículos cargados para despacho                                              |
| 28 | UNI_CAJ_ACTUAL         | Cantidad de unidades por caja de despacho                                                 |
| 29 | UNIDAD_DISPLAY_ACTUAL  | Cantidad de unidades para despacho                                                        |
| 30 | MATRICULA_CAMION       | Matrícula del vehículo que realizará el despacho, dentro de la ruta planeada              |

<div align="initial">

---
**<font color='red'>Notas de revisión</font>**

Teniendo en cuenta la cantidad de registros y columnas, es necesario realizar algunas pruebas **_preliminares_** enfocadas en lo siguiente:
- **_Carga de archivos_**, para la ejecución de los modelos de análisis y predicción
- **_Tamaño de archivos_**, para optimización de recursos de memoria y espacio
- **_Número de columnas_**, para verificación de redundancia de información y reducción de variables
- **_Número de registros_**, para la selección adecuada del rango de observaciones
- **_Generación de gráficas_**, de acuerdo con las columnas involucradas
- **_Procesamiento_**, para la obtención de los resultados
- **_Privacidad de información_**, para protección de datos sensibles o confidenciales presentes en las observaciones

---

## 3.2 - Ingeniería de datos

- **_Revisión preliminar de fuentes de datos:_**

  - Se identificaron varios campos que pueden ser **_eliminados_**, ya que no aportan información **_relevante_** para el análisis.
  
  - Se identificaron algunos campos **_redundantes_** que representan la misma unidad de información: **_código/descripción_**. En este caso se pueden dejar los códigos respectivos excluyendo sus descripciones.

  - Se identificaron algunos campos que contienen **_información confidencial_**, y pueden ser **_modificados/eliminados_** para su tratamiento de forma **_anónima_**.

  - Se identificaron algunos campos utilizados para el **_cálculo de datos adicionales_**, y pueden ser **_eliminados_** reemplazándolos por los **_valores finales calculados_**.
  
  - Se determinó que la **_mejor alternativa de observaciones_** corresponde al archivo generado **_#7 (WMS_Consolidado_20230531_20230418_44d.csv)_**, dado que contiene información representativa de la **_operación recurrente y ocasional_** del CEDI, de acuerdo con la estrategia planteada inicialmente.

  - Se determinó/comprobó que al utilizar el archivo escogido, se presentan **_varios inconvenientes_** ( carga, tamaño, procesamiento, graficación ), y por ende, es necesario **_replantear su generación_** para su adecuado manejo.

  - Para la regeneración de la misma información, se podrán considerar como mecanismos alternativos, el **_agrupamiento de valores por día y pivotes de columnas_**, con el fin de reducir la cantidad de registros a obtener.

  <div align="center">

  ![image](https://github.com/user-attachments/assets/f7913f9f-ba7d-4327-9647-abf4513c6caf)

  <div align="initial">

- **_Relación de campos eliminados:_**

<div align="center">

| Nro | Columna | Descripción Columna |
|:---:|---|---|
|  1 | ALMACE                 | Código del CEDI                                                                |
|  2 | NOMBRE                 | Nombre largo de la tienda, incluyendo ciudad de ubicación                      |
|  3 | NOM_CORTO              | Nombre corto de la tienda                                                      |
|  4 | FECHA_SERVICIO         | Fecha en la que se habilita el servicio en tiendas ( inventario físico )       |
|  5 | FECHA_TRANSMISION      | Fecha en la que se genera la transmisión de información para procesamiento     |
|  6 | FECHA_ALTA             | Fecha en la que se da el alta para servicio ( luego de inactivación temporal ) |
|  7 | FECHA_PROCESAMIENTO    | Fecha en la que se realiza el procesamiento de información                     |
|  8 | FECHA_ACTIVACION       | Fecha de activacion del inventario en tiendas                                  |
|  9 | RUTA                   | Código de la ruta de transporte ( despachos )                                  |
| 10 | DESC_RUTA              | Nombre de la ruta de transporte ( Ruta1 ... Ruta12, Sin Asignación )           |
| 11 | AREA                   | Código del área o familia de productos                                         |
| 12 | PEDIDO_SAP             | Número del pedido dentro del sistema ERP (SAP)                                 |
| 13 | LIN_PEDIDO             | Línea del pedido del Sistema ERP (SAP)                                         |
| 14 | NOMBRE_ARTICULO        | Nombre del artículo                                                            |
| 15 | CANTI_PEDIDA           | Cantidad de artículos solicitados por tienda dentro del pedido                 |
| 16 | UNI_CAJ_PEDIDO         | Cantidad de unidades por caja de pedido                                        |
| 17 | UNIDAD_DISPLAY_PEDIDO  | Cantidad de unidades para pedido                                               |
| 18 | CANTIDAD_RECOGIDA      | Cantidad de artículos recogidos para picking                                   |
| 19 | UNI_CAJ_SERVIDA        | Cantidad de unidades por caja de picking                                       |
| 20 | UNIDAD_DISPLAY_SERVIDA | Cantidad de unidades para picking                                              |
| 21 | CANTIDAD_CARGADA       | Cantidad de artículos cargados para despacho                                   |
| 22 | UNI_CAJ_ACTUAL         | Cantidad de unidades por caja de despacho                                      |
| 23 | UNIDAD_DISPLAY_ACTUAL  | Cantidad de unidades para despacho                                             |
| 24 | MATRICULA_CAMION       | Matrícula del vehículo que realizará el despacho, dentro de la ruta planeada   |

<div align="initial">

- **_Relación de campos filtrados:_**

<div align="center">

| Nro | Columna | Descripción Columna |
|:---:|---|---|
|  1 | CEDI             | Nombre del CEDI                                                                           |
|  2 | COD_CLIENTE      | Código del cliente (tienda)                                                               |
|  3 | PEDIDO_INLOG     | Número del pedido dentro del sistema WMS                                                  |
|  4 | DESC_AREA        | Descripción del área o familia de productos ( Cuadrante 1, Alimentos, Aseo,               |
|    |                  | Extradimensionados, Refrigerados, Congelados, Fruver Seco, Fruver Frío, Extraordinarios ) |
|  5 | ARTICULO         | Código del artículo                                                                       |
|  6 | SITUACION_PEDIDO | Situación del pedido: Pedidos (PE,PR,AC) / Picking (CU,TE,ET) / Despachos (EX)            |

<div align="initial">

- **_Relación de campos calculados:_**

<div align="center">

| Nro | Columna | Descripción Columna |
|:---:|---|---|
|  1 | FECHA_PEDIDO  | Fecha en la que se realizó el pedido                                                   |
|  2 | CAJAS_PED     | Cantidad de cajas solicitadas en el pedido de cada tienda                              |
|  3 | FECHA_PICKING | Fecha en la que se realizó el picking                                                  |
|  4 | CAJAS_PICK    | Cantidad de cajas manejadas dentro del alistamiento del picking                        |
|  5 | FECHA_CARGA   | Fecha en la que se realizó el despacho                                                 |
|  6 | CAJAS_DESP    | Cantidad de cajas manejadas en el despacho, dentro de las rutas de carga programadas   |
|  7 | NO_ATENDIDO   | Cantidad de cajas no atendidas ( diferencia entre cajas de pedido y cajas de picking ) |

<div align="initial">

- **_Observaciones regeneradas (métodos optimizados):_**

  - **_Formato de archivos:_** WMS_Consolidado \_ [ FechaFinal ] \_ [ FechaInicial ] \_ [ NroDías ] . csv

  - **_Información adicional:_** Cantidad de días y registros generados en cada caso

<div align="center">

| Nro | Archivo | Días | Registros |
|:---:|---|:---:|---:|
| 1 | WMS_Consolidado_20230531_20230418_44d_Group.csv | 44 | 142,474 |
| 2 | WMS_Consolidado_20230531_20230418_44d_Pivot.csv | 44 |  57,826 |

<div align="initial">

- **_Relación de campos generados - Método 1 ( agrupamiento valores por día ):_**

<div align="center">

| Nro | Columna | Descripción Columna |
|:---:|---|---|
|  1 | PROCESO          | Tipo de proceso logístico manejado ( PEDIDOS, PICKING, DESPACHO )                       |
|  2 | FECHA_OPERATIVA  | Fecha operativa del proceso logístico ( FECHA_PEDIDO, FECHA_PICKING, FECHA_CARGA )      |
|  3 | CEDI             | Nombre del CEDI  ( CEDI_1, CEDI_2, CEDI_3 )                                             |
|  4 | TIENDA           | Código del cliente (tienda)                                                             |
|  5 | AREA             | Descripción del área o familia de productos                                             |
|  6 | SITUACION_PEDIDO | Situación del pedido: Pedidos (PE,PR,AC) / Picking (CU,TE,ET) / Despachos (EX)          |
|  7 | PEDIDOS          | Cantidad de pedidos distintos por agrupamiento                                          |
|  8 | ARTICULOS        | Cantidad de artículos distintos por agrupamiento                                        |
|  9 | CAJAS            | Sumatoria de cajas por proceso logístico agrupado ( CAJAS_PED, CAJAS_PICK, CAJAS_DESP ) |
| 10 | NO_ATENDIDO      | Sumatoria de cajas no atendidas por agrupamiento                                        |

<div align="initial">

- **_Relación de campos generados - Método 2 ( pivotes de columnas ):_**

<div align="center">

| Nro | Columna | Descripción Columna |
|:---:|---|---|
|  1 | FECHA_OPERATIVA  | Fecha operativa del proceso logístico ( FECHA_PEDIDO, FECHA_PICKING, FECHA_CARGA ) |
|  2 | CEDI             | Nombre del CEDI  ( CEDI_1, CEDI_2, CEDI_3 )                                        |
|  3 | TIENDA           | Código del cliente (tienda)                                                        |
|  4 | AREA             | Descripción del área o familia de productos                                        |
|  5 | SITUACION_PEDIDO | Situación del pedido: Pedidos (PE,PR,AC) / Picking (CU,TE,ET) / Despachos (EX)     |
|  6 | PED_PEDIDOS      | Proceso PEDIDOS - Cantidad de pedidos distintos por agrupamiento                   |
|  7 | PED_ARTICULOS    | Proceso PEDIDOS - Cantidad de artículos distintos por agrupamiento                 |
|  8 | PED_CAJAS        | Proceso PEDIDOS - Sumatoria de cajas por proceso logístico agrupado                |
|  9 | PED_NOATENDID    | Proceso PEDIDOS - Sumatoria de cajas no atendidas por agrupamiento                 |
| 10 | PICK_PEDIDOS     | Proceso PICKING - Cantidad de pedidos distintos por agrupamiento                   |
| 11 | PICK_ARTICULOS   | Proceso PICKING - Cantidad de artículos distintos por agrupamiento                 |
| 12 | PICK_CAJAS       | Proceso PICKING - Sumatoria de cajas por proceso logístico agrupado                |
| 13 | PICK_NOATENDID   | Proceso PICKING - Sumatoria de cajas no atendidas por agrupamiento                 |
| 14 | DESP_PEDIDOS     | Proceso DESPACHO - Cantidad de pedidos distintos por agrupamiento                  |
| 15 | DESP_ARTICULOS   | Proceso DESPACHO - Cantidad de artículos distintos por agrupamiento                |
| 16 | DESP_CAJAS       | Proceso DESPACHO - Sumatoria de cajas por proceso logístico agrupado               |
| 17 | DESP_NOATENDID   | Proceso DESPACHO - Sumatoria de cajas no atendidas por agrupamiento                |

<div align="initial">
