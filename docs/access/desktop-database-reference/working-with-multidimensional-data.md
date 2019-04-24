---
title: Trabajo con datos multidimensionales
TOCTitle: Working with multidimensional data
ms:assetid: a0c9ac73-04da-cfdd-8787-15c8a53ff819
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249740(v=office.15)
ms:contentKeyID: 48546717
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 67b22219fdbbec8bf518b7be0fabd9a6adfbcf7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306044"
---
# <a name="working-with-multidimensional-data"></a>Trabajo con datos multidimensionales

**Se aplica a:** Access 2013, Office 2013

Un *conjunto de celdas* es el resultado de una consulta de datos multidimensionales. Consta de una colección de ejes, que no suele tener más de cuatro ejes (normalmente, dos o tres). Un *eje* es una colección de miembros de una o varias dimensiones que se utiliza para localizar o filtrar valores específicos de un cubo.

Una *posición* es un punto a lo largo de un eje. En un eje que consta de una sola dimensión, estas posiciones son un subconjunto de los miembros de una dimensión. Si un eje consta de varias dimensiones, cada posición es una entidad compuesta, que tiene *n* partes donde *n* es el número de dimensiones orientadas a lo largo del eje. Cada parte de la posición es un miembro de una dimensión integrante.

Por ejemplo, si las dimensiones Zona geográfica y Producto de un cubo que contiene datos de ventas están orientadas a lo largo del eje x de un conjunto de celdas, una posición a lo largo de este eje puede contener los miembros "EE.UU." y "Equipos". En este ejemplo, para determinar una posición a lo largo del eje x es necesario que los miembros de cada dimensión estén orientados a lo largo del eje.

Una *celda* es un objeto situado en la intersección de las coordenadas de ejes. Cada celda tiene varios segmentos de información asociados, incluidos los propios datos, una cadena con formato (la forma en que se muestran los datos de la celda) y el valor ordinal de la celda. Cada celda es un valor ordinal único en el conjunto de celdas. El valor ordinal de la primera celda en el conjunto de celdas es cero, mientras que la celda situada en el extremo izquierdo de la segunda fila de un conjunto de celdas con ocho columnas tendría el valor ordinal de ocho.

Por ejemplo, un cubo tiene las seis dimensiones siguientes (observe que este esquema de cubo presenta ligeras diferencias con respecto al ejemplo incluido en [Descripción general de esquemas y datos multidimensionales](overview-of-multidimensional-schemas-and-data.md)):

- Vendedor
- Zona geográfica (jerarquía natural): Continentes, Países, Estados, etc.
- Trimestres: Trimestres, Meses, Días
- Años
- Medidas: Ventas, CambioPorcentual, VentasPresupuestadas
- Productos

> [!NOTE]
> Los valores de celda del ejemplo pueden considerarse pares ordenados de ordinales de posiciones de eje, donde el primer dígito representa la posición en el eje x y el segundo dígito, la posición en el eje y.

Las características de este conjunto de celdas son las siguientes:

- Dimensiones de eje: Trimestres, Vendedor, Zona geográfica

- Dimensiones de filtro: Medidas, Años, Productos

- Dos ejes: COLUMNA (x o Eje 0) y FILA (y o Eje 1)

- Eje x: dos dimensiones anidadas, Vendedor y Zona geográfica

- Eje y: dimensión Trimestres

El eje x tiene dos dimensiones anidadas, Vendedor y Zona geográfica. De Zona geográfica se seleccionan cuatro miembros: Seattle, Boston, USA-South y Japan. De Vendedor se seleccionan dos miembros: Valentine y Nash. Esto produce un total de ocho posiciones en este eje (8 = 4\*2).

Cada coordenada se representa como una posición con dos miembros: uno de la dimensión Vendedor y otro de la dimensión Zona geográfica:

```vb 
 
(Valentine, Seattle), (Valentine, Boston), (Valentine, USA_North), 
(Valentine, Japan), (Nash, Seattle), (Nash, Boston), (Nash, USA_North), 
(Nash, Japan) 
```

El eje y sólo tiene una dimensión, que contiene las ocho posiciones siguientes:

```vb 
 
Jan, Feb, Mar, Qtr2, Qtr3, Oct, Nov, Dec 
```

Los conjuntos de celdas, celdas, ejes y posiciones se representan en ADO MD mediante los objetos correspondientes: [Cellset](cellset-object-ado-md.md), [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md) y [Position](position-object-ado-md.md).

