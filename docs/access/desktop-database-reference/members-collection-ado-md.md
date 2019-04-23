---
title: Members (colección) (ADO MD)
TOCTitle: Members collection (ADO MD)
ms:assetid: 1389c554-e4f1-107d-22c6-7fe851d53d23
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248910(v=office.15)
ms:contentKeyID: 48543371
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: adc8ed771bcba6a4b6532b33b27980f8aab695c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289245"
---
# <a name="members-collection-ado-md"></a>Members (colección) (ADO MD)


**Se aplica a:** Access 2013, Office 2013

Contiene los objetos [Member](member-object-ado-md.md) de un nivel o una posición a lo largo de un eje.

## <a name="remarks"></a>Comentarios

La colección **Members** sirve para albergar los siguientes tipos de miembros:

  - Los miembros que componen un nivel de un cubo. Estos miembros se incluyen en la colección **Members** de un objeto [Level](level-object-ado-md.md). Por ejemplo, en el ejemplo de [Descripción general de esquemas y datos multidimensionales](overview-of-multidimensional-schemas-and-data.md), los cuatro miembros del nivel Countries son Canada, USA, UK y Germany.

  - Los miembros secundarios de un miembro específico en una jerarquía. Estos miembros los devuelve la propiedad [Children](children-property-ado-md.md) del objeto principal **Member**. Por ejemplo, en ese mismo ejemplo, los dos miembros secundarios del miembro Canada son Canada-East y Canada-West.

  - Los miembros que definen una posición específica a lo largo de un eje de un [conjunto de celdas](cellset-object-ado-md.md). En el conjunto de celdas del ejemplo de [Trabajar con datos multidimensionales](working-with-multidimensional-data.md), los dos miembros de la primera posición en el eje x son Valentine y Seattle. Estos miembros están incluidos en la colección **Members** de un objeto [Position](position-object-ado-md.md).

**Members** es una colección de ADO estándar. Con las propiedades y los métodos de una colección, puede realizar las siguientes operaciones:

  - Obtener el número de objetos de la colección con la propiedad [Count](count-property-ado.md).

  - Devolver un objeto de la colección con la propiedad [Item](item-property-ado.md) predeterminada.

  - Actualizar los objetos de la colección del proveedor con el método [Refresh](refresh-method-ado.md).

