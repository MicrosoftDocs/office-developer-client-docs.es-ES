---
title: Colección Axes (ADO MD)
TOCTitle: Axes collection (ADO MD)
ms:assetid: 7c719197-45f1-a5b9-665d-25cb693b1eb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249520(v=office.15)
ms:contentKeyID: 48545836
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8183b0bad1dcbaba33088dffcf21959f5b9fd993
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296937"
---
# <a name="axes-collection-ado-md"></a>Colección Axes (ADO MD)


**Se aplica a:** Access 2013, Office 2013

Contiene los objetos [Axis](axis-object-ado-md.md) que definen un conjunto de celdas.

## <a name="remarks"></a>Comentarios

Un objeto [Cellset](cellset-object-ado-md.md) contiene una colección **Axes**. Una vez abierta la colección **Cellset**, esta colección contendrá al menos un objeto **Axis**. Vea el tema relativo al objeto [Axis](axis-object-ado-md.md) para obtener una explicación más detallada de cómo usar objetos **Axis**.


> [!NOTE]
> [!NOTA] El eje de filtro de un **conjunto de celdas** no está incluido en la colección **Axes**. Vea el tema relativo a la propiedad [FilterAxis](filteraxis-property-ado-md.md) para obtener más información.



**Axes** es una colección de ADO estándar. Con las propiedades y los métodos de una colección, puede realizar las siguientes operaciones:

- Obtener el número de objetos de la colección con la propiedad [Count](count-property-ado.md).

- Devolver un objeto de la colección con la propiedad [Item](item-property-ado.md) predeterminada.

- Actualizar los objetos de la colección del proveedor con el método [Refresh](refresh-method-ado.md).

