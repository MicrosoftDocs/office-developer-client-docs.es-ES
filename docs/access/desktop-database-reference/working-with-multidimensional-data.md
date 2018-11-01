---
title: Trabajar con datos multidimensionales
TOCTitle: Working with Multidimensional Data
ms:assetid: a0c9ac73-04da-cfdd-8787-15c8a53ff819
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249740(v=office.15)
ms:contentKeyID: 48546717
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7aba6eda9abc84c6f34442f828fe802c4b016653
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871993"
---
# <a name="working-with-multidimensional-data"></a>Trabajar con datos multidimensionales


**Se aplica a**: Access 2013, Office 2013

Un *conjunto de celdas* es el resultado de una consulta de datos multidimensionales. Consta de una colección de ejes, que no suele tener más de cuatro ejes (normalmente, dos o tres). Un *eje* es una colección de miembros de una o más dimensiones, que se utiliza para localizar o filtrar valores específicos de un cubo.

Una *posición* es un punto a lo largo de un eje. En un eje que consta de una sola dimensión, estas posiciones son un subconjunto de los miembros de una dimensión. Si un eje consta de varias dimensiones, cada posición es una entidad compuesta, que consta de los elementos de *n* donde *n* es el número de dimensiones orientadas a lo largo del eje. Cada parte de la posición es un miembro de una dimensión integrante.

Por ejemplo, si las dimensiones Zona geográfica y Producto de un cubo que contiene datos de ventas están orientadas a lo largo del eje x de un conjunto de celdas, una posición a lo largo de este eje puede contener los miembros "EE.UU." y "Equipos". En este ejemplo, para determinar una posición a lo largo del eje x es necesario que los miembros de cada dimensión estén orientados a lo largo del eje.

Una *celda* es un objeto situado en la intersección de coordenadas de ejes. Cada celda tiene varios segmentos de información asociados, incluidos los propios datos, una cadena con formato (la forma en que se muestran los datos de la celda) y el valor ordinal de la celda. Cada celda es un valor ordinal único en el conjunto de celdas. El valor ordinal de la primera celda en el conjunto de celdas es cero, mientras que la celda situada en el extremo izquierdo de la segunda fila de un conjunto de celdas con ocho columnas tendría el valor ordinal de ocho.

Por ejemplo, un cubo tiene las seis dimensiones siguientes (observe que este esquema de cubo presenta ligeras diferencias con respecto al ejemplo incluido en [Descripción general de esquemas y datos multidimensionales](overview-of-multidimensional-schemas-and-data.md)):

  - Vendedor

  - Zona geográfica (jerarquía natural): Continentes, Países, Estados, etc.

  - Trimestres: Trimestres, Meses, Días

  - Años

  - Medidas: Ventas, CambioPorcentual, VentasPresupuestadas

  - Productos


> [!NOTE]
> <P>[!NOTA] Los valores de celda del ejemplo pueden considerarse pares ordenados de ordinales de posiciones de eje, donde el primer dígito representa la posición en el eje x y el segundo dígito, la posición en el eje y.</P>



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

