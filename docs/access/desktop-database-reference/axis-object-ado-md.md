---
title: Axis (objeto) (ADO MD)
TOCTitle: Axis Object (ADO MD)
ms:assetid: a4332b69-8900-08f1-a4e2-9395d005ed42
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249763(v=office.15)
ms:contentKeyID: 48546807
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 76fe2e0aa90397b32d95172318f3657741e1b1ec
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875024"
---
# <a name="axis-object-ado-md"></a>Axis (objeto) (ADO MD)


**Se aplica a**: Access 2013, Office 2013

Representa un eje de posición o de filtro de un conjunto de celdas, que contiene elementos seleccionados de una o más dimensiones.

## <a name="remarks"></a>Comentarios

Un objeto **Axis** puede estar incluido en una colección [Axes](axes-collection-ado-md.md) o ser devuelvo por la propiedad [FilterAxis](filteraxis-property-ado-md.md) de un objeto [Cellset](cellset-object-ado-md.md).

Con las colecciones y las propiedades de un objeto **Axis**, puede hacer lo siguiente:

  - Identificar el **eje** con la propiedad [Name](name-property-ado-md.md).

  - Recorrer en iteración cada posición a lo largo de un **eje** mediante la colección [Positions](positions-collection-ado-md.md).

  - Obtener el número de dimensiones del **eje** con la propiedad [DimensionCount](dimensioncount-property-ado-md.md).

  - Obtener atributos específicos de proveedor del **eje** con la colección [Properties](properties-collection-ado.md) de ADO estándar.

