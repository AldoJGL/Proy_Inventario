# Proy_Inventario

## Descripción del proyecto
Este proyecto consiste en un sistema básico de control de inventarios desarrollado en Microsoft Excel, utilizando tablas estructuradas, fórmulas y tablas dinámicas para el análisis de entradas, salidas y stock de productos tecnológicos.

El proyecto simula un escenario real de gestión de inventarios, común en áreas de operaciones, logística, análisis de datos y sistemas de información, aplicando buenas prácticas en el manejo y análisis de datos.

---

## Objetivos del proyecto
- Registrar un catálogo de productos tecnológicos  
- Controlar entradas (compras) y salidas (ventas)  
- Analizar los movimientos de inventario  
- Calcular y visualizar el stock actual  
- Identificar productos con bajo nivel de inventario  

---

## Estructura del proyecto
El archivo de Excel está compuesto por tres hojas principales:

### Productos
Catálogo maestro de productos tecnológicos.

Columnas:
- Código del producto  
- Descripción  
- Precio unitario  
- Stock inicial  

![Hoja Productos](imagenes/CapProd1.png)

---

### Entradas
Registro histórico de compras o ingresos al inventario.

Columnas:
- Fecha  
- Código del producto  
- Cantidad  

![Hoja Entradas](imagenes/CapEntr1.png)

---

### Salidas
Registro histórico de ventas o egresos del inventario.

Columnas:
- Fecha  
- Código del producto  
- Cantidad  

![Hoja Salidas](imagenes/CapSal1.png)

---

## Proceso de desarrollo

### Conversión a tablas de Excel
Los rangos de datos de cada hoja fueron convertidos en Tablas oficiales de Excel para permitir la actualización automática de fórmulas, mejorar la organización de los datos y facilitar su análisis.

![Tabla Productos convertida](imagenes/CapProd2.png)

---

### Creación de la hoja maestra "Inventario"
Se creó una hoja adicional denominada Inventario, en la cual se consolidan los datos provenientes de las demás hojas.

Pasos realizados:
1. Se copiaron los códigos de producto desde la hoja Productos.
2. Se utilizó la función BUSCARV para obtener automáticamente la descripción y el stock inicial.
3. Se empleó la función SUMAR.SI.CONJUNTO para calcular el total de entradas y salidas por producto.

![Inventario inicial](imagenes/CapInv1.png) 

4. Se calculó el stock actual mediante la fórmula: Stock Actual = Stock Inicial + Entradas − Salidas
5. Se creó una columna Estado utilizando la función: =SI(StockActual<=10,"Pedir Stock","En Stock")
6. Se aplicó formato condicional para resaltar visualmente los productos con bajo inventario.
 
![Inventario final](imagenes/CapInv2.png)

---

## Herramientas utilizadas
- Microsoft Excel  
- Tablas estructuradas  
- Funciones: BUSCARV, SUMAR.SI.CONJUNTO, SI  
- Formato condicional

## Autor
Aldo Gonzalez
