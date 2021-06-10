---
title: Objeto Cellset (ADO MD)
TOCTitle: Cellset object (ADO MD)
ms:assetid: 28d4b3b9-f907-9ec0-00e1-9666c887cdf0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249047(v=office.15)
ms:contentKeyID: 48543869
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c8cb75ad7277386cfe81b2edcffa234498318444
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296517"
---
# <a name="cellset-object-ado-md"></a>Objeto Cellset (ADO MD)

**Se aplica a:** Access 2013, Office 2013

Representa los resultados de una consulta multidimensional. Es un conjunto de celdas seleccionadas de cubos u otro conjuntos de celdas.

## <a name="remarks"></a>Comentarios

Los datos incluidos en un **conjunto de celdas** se recuperan mediante acceso directo en forma de matriz. Puede "profundizar" hasta un miembro específico para obtener datos sobre ese miembro. Por ejemplo, el código siguiente devuelve el título del primer miembro de la primera posición en el primer eje de un conjunto de celdas denominado cst:

`cst.Axes(0).Positions(0).Members(0).Caption`

No hay ninguna indicación de la celda actual dentro de un conjunto de celdas, pero la propiedad [Item](item-property-ado-md-cellset.md) recupera un objeto [Cell](cell-object-ado-md.md) específico del conjunto de celdas. Los argumentos de la propiedad **Item** determinan la celda que se recupera. Puede especificar el valor ordinal único de una celda. Puede también recuperar celdas utilizando sus números de posición a lo largo de cada eje del conjunto de celdas. Para obtener más información sobre cómo recuperar celdas, vea el tema relativo a la propiedad [Item](item-property-ado-md-cellset.md).

Con las colecciones, los métodos y las propiedades de un objeto **Cellset**, puede hacer lo siguiente:

  - Asociar una conexión abierta a un objeto **Cellset** estableciendo su propiedad [ActiveConnection](activeconnection-property-ado-md.md).

  - Ejecutar y recuperar los resultados de una consulta multidimensional con el método [Open](open-method-ado-md.md).

  - Recuperar una **celda** del **conjunto de celdas** con la propiedad [Item](item-property-ado-md-cellset.md).

  - Devolver los objetos [Axis](axis-object-ado-md.md) que define el **conjunto de celdas** con la colección [Axes](axes-collection-ado-md.md).

  - Recuperar información sobre las dimensiones utilizadas para filtrar los datos del **conjunto de celdas** con la propiedad [FilterAxis](filteraxis-property-ado-md.md).

  - Devolver o especificar la consulta utilizada para definir el **conjunto de celdas** con la propiedad [Source](source-property-ado-md.md).

  - Devolver el estado actual del **conjunto de celdas** (abierto, cerrado, en ejecución o en conexión) con la propiedad [State](state-property-ado-md.md).

  - Cerrar un **conjunto de celdas** abierto con el método [Close](close-method-ado-md.md).

  - Obtener información específica del proveedor sobre el **conjunto de celdas** con la colección [Properties](properties-collection-ado.md) de ADO estándar.

