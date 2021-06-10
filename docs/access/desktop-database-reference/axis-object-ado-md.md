---
title: Objeto Axis (ADO MD)
TOCTitle: Axis object (ADO MD)
ms:assetid: a4332b69-8900-08f1-a4e2-9395d005ed42
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249763(v=office.15)
ms:contentKeyID: 48546807
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 23fdb0d9ba636ae58fa19b42d5a8a47cb01d4ab2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296902"
---
# <a name="axis-object-ado-md"></a>Objeto Axis (ADO MD)


**Se aplica a:** Access 2013, Office 2013

Representa un eje de posición o de filtro de un conjunto de celdas, que contiene elementos seleccionados de una o más dimensiones.

## <a name="remarks"></a>Comentarios

Un objeto **Axis** puede estar incluido en una colección [Axes](axes-collection-ado-md.md) o ser devuelvo por la propiedad [FilterAxis](filteraxis-property-ado-md.md) de un objeto [Cellset](cellset-object-ado-md.md).

Con las colecciones y las propiedades de un objeto **Axis**, puede hacer lo siguiente:

- Identificar el **eje** con la propiedad [Name](name-property-ado-md.md).

- Recorrer en iteración cada posición a lo largo de un **eje** mediante la colección [Positions](positions-collection-ado-md.md).

- Obtener el número de dimensiones del **eje** con la propiedad [DimensionCount](dimensioncount-property-ado-md.md).

- Obtener atributos específicos de proveedor del **eje** con la colección [Properties](properties-collection-ado.md) de ADO estándar.

