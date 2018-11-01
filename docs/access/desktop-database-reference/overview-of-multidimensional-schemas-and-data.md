---
title: Descripción general de esquemas y datos multidimensionales
TOCTitle: Overview of Multidimensional Schemas and Data
ms:assetid: a963e993-b7bf-eeb4-ecd5-d6fe43cf4bb5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249784(v=office.15)
ms:contentKeyID: 48546923
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 376d80bc79af772cfd09b6f5b8759321ed4431ee
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887171"
---
# <a name="overview-of-multidimensional-schemas-and-data"></a>Descripción general de esquemas y datos multidimensionales


**Se aplica a**: Access 2013, Office 2013

## <a name="understanding-multidimensional-schemas"></a>Esquemas multidimensionales

El objeto de metadatos central en ADO MD es el *cubo*, que consiste en un conjunto estructurado de dimensiones, jerarquías, niveles y miembros relacionados.

Una *dimensión* es una categoría independiente de datos de la base de datos multidimensional, derivado de las entidades empresariales. Una dimensión suele contener elementos que se utilizan como criterios de consulta para las mediciones de la base de datos.

Una *jerarquía* es una ruta de acceso de agregación de una dimensión. Una dimensión puede tener varios niveles de detalle, con relaciones principal-secundario. Una jerarquía define cómo están relacionados estos niveles.

Un *nivel* es un paso de agregación de una jerarquía. En las dimensiones con varias capas de información, cada capa es un nivel.

Un *miembro* es un elemento de datos en una dimensión. Normalmente, se utilizan miembros para crear un título o describir una medida de la base de datos.

Los cubos se representan mediante objetos [CubeDef](cubedef-object-ado-md.md) en ADO MD. Las dimensiones, jerarquías, niveles y miembros se representan también mediante sus objetos ADO MD correspondientes: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md) y [Member](member-object-ado-md.md).

## <a name="dimensions"></a>Dimensiones

Las dimensiones de un cubo dependen de las entidades del negocio y de los tipos de datos que se van a diseñar en la base de datos. Normalmente, cada dimensión es un punto de entrada o mecanismo independiente para la selección de datos.

Por ejemplo, un cubo que contiene datos de ventas tiene las cinco dimensiones siguientes: Vendedor, Zona geográfica, Fecha, Productos y Medidas. La dimensión Medidas contiene datos de ventas reales, mientras que las otras dimensiones representan formas de clasificar y agrupar los valores de datos de ventas.

La dimensión Zona geográfica tiene el siguiente conjunto de miembros:

```text
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a>Jerarquías

Las jerarquías definen el modo en que los niveles de una dimensión se pueden "condensar" o agrupar. Una dimensión puede tener varias jerarquías.

## <a name="levels"></a>Niveles

En el ejemplo de la dimensión Zona geográfica mostrado en la ilustración anterior, cada cuadro representa un nivel de la jerarquía.

Cada nivel tiene el siguiente conjunto de miembros:

  - El mundo = {All}


  - Continentes = {North America, Europe}


  - Países = {Canada, USA, UK, Germany}


  - Regiones = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}


  - Ciudades = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}


## <a name="members"></a>Miembros

Los miembros en el nivel de hoja de una jerarquía no tienen miembros secundarios y los miembros en el nivel raíz no tienen miembros principales. Todos los demás miembros tienen al menos un miembro principal y un miembro secundario. Por ejemplo, un recorrido transversal parcial del árbol jerárquico de la dimensión Zona geográfica da lugar a las siguientes relaciones principal-secundario:

  - {All} (elemento principal de) {Europa, Norteamérica}

  - {North America} (elemento principal de) {Canada, USA}

  - {EE.} (elemento principal de) {USA-NE, USA-NW, USA-SE, USA-SW}

  - {USA-NW} (elemento principal de) {Boise, Seattle}

Los miembros se pueden consolidar en una o varias jerarquías para cada dimensión.

Este ejemplo ilustra también otra característica: algunos miembros del nivel Semana de la jerarquía Año-Semana no aparecen en ningún nivel de la jerarquía Año-Trimestre. Por tanto, una jerarquía no incluye necesariamente todos los miembros de una dimensión.

## <a name="understanding-multidimensional-schemas"></a>Esquemas multidimensionales

El objeto de metadatos central en ADO MD es el *cubo*, que consiste en un conjunto estructurado de dimensiones, jerarquías, niveles y miembros relacionados.

Una *dimensión* es una categoría independiente de datos de la base de datos multidimensional, derivado de las entidades empresariales. Una dimensión suele contener elementos que se utilizan como criterios de consulta para las mediciones de la base de datos.

Una *jerarquía* es una ruta de acceso de agregación de una dimensión. Una dimensión puede tener varios niveles de detalle, con relaciones principal-secundario. Una jerarquía define cómo están relacionados estos niveles.

Un *nivel* es un paso de agregación de una jerarquía. En las dimensiones con varias capas de información, cada capa es un nivel.

Un *miembro* es un elemento de datos en una dimensión. Normalmente, se utilizan miembros para crear un título o describir una medida de la base de datos.

Los cubos se representan mediante objetos [CubeDef](cubedef-object-ado-md.md) en ADO MD. Las dimensiones, jerarquías, niveles y miembros se representan también mediante sus objetos ADO MD correspondientes: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md) y [Member](member-object-ado-md.md).

## <a name="dimensions"></a>Dimensiones

Las dimensiones de un cubo dependen de las entidades del negocio y de los tipos de datos que se van a diseñar en la base de datos. Normalmente, cada dimensión es un punto de entrada o mecanismo independiente para la selección de datos.

Por ejemplo, un cubo que contiene datos de ventas tiene las cinco dimensiones siguientes: Vendedor, Zona geográfica, Fecha, Productos y Medidas. La dimensión Medidas contiene datos de ventas reales, mientras que las otras dimensiones representan formas de clasificar y agrupar los valores de datos de ventas.

La dimensión Zona geográfica tiene el siguiente conjunto de miembros:

```text 
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a>Jerarquías

Las jerarquías definen el modo en que los niveles de una dimensión se pueden "condensar" o agrupar. Una dimensión puede tener varias jerarquías.

## <a name="levels"></a>Niveles

En el ejemplo de la dimensión Zona geográfica mostrado en la ilustración anterior, cada cuadro representa un nivel de la jerarquía.

Cada nivel tiene el siguiente conjunto de miembros:

- El mundo = {All}


- Continentes = {North America, Europe}


- Países = {Canada, USA, UK, Germany}


- Regiones = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}


- Ciudades = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}


## <a name="members"></a>Miembros

Los miembros en el nivel de hoja de una jerarquía no tienen miembros secundarios y los miembros en el nivel raíz no tienen miembros principales. Todos los demás miembros tienen al menos un miembro principal y un miembro secundario. Por ejemplo, un recorrido transversal parcial del árbol jerárquico de la dimensión Zona geográfica da lugar a las siguientes relaciones principal-secundario:

- {All} (elemento principal de) {Europa, Norteamérica}

- {North America} (elemento principal de) {Canada, USA}

- {EE.} (elemento principal de) {USA-NE, USA-NW, USA-SE, USA-SW}

- {USA-NW} (elemento principal de) {Boise, Seattle}

Los miembros se pueden consolidar en una o varias jerarquías para cada dimensión.

Este ejemplo ilustra también otra característica: algunos miembros del nivel Semana de la jerarquía Año-Semana no aparecen en ningún nivel de la jerarquía Año-Trimestre. Por tanto, una jerarquía no incluye necesariamente todos los miembros de una dimensión.

