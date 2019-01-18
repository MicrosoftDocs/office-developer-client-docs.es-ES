---
title: Cell (objeto, ADO MD)
TOCTitle: Cell object (ADO MD)
ms:assetid: b9d00b71-1f40-5bd1-4b89-fbdb59c552ba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249892(v=office.15)
ms:contentKeyID: 48547356
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7bb2a479789a8c5bd1825b6cb04e602e0b829dfb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/18/2019
ms.locfileid: "28725990"
---
# <a name="cell-object-ado-md"></a>Cell (objeto, ADO MD)


**Se aplica a**: Access 2013, Office 2013

Representa los datos de la intersección de coordenadas de ejes contenidos en un conjunto de celdas.

## <a name="remarks"></a>Comentarios

El objeto **Cell** lo devuelve la propiedad [Item](item-property-ado-md-cellset.md) de un objeto [Cellset](cellset-object-ado-md.md).

Con las colecciones y las propiedades de un objeto **Cell**, puede hacer lo siguiente:

- Devolver los datos de la **celda** con la propiedad [Value](value-property-ado-md.md).

- Devolver la cadena que representa la presentación con formato de la propiedad **Value** con la propiedad [FormattedValue](formattedvalue-property-ado-md.md).

- Devolver el valor ordinal de la **celda** incluida en el **conjunto de celdas** con la propiedad [Ordinal](ordinal-property-ado-md-cell.md).

- Determinar la posición de la **celda** incluida en el objeto [CubeDef](cubedef-object-ado-md.md) con la colección [Positions](positions-collection-ado-md.md).

- Recuperar otra información sobre la **celda** con la colección [Properties](properties-collection-ado.md) de ADO estándar.

La colección **Properties** contiene propiedades proporcionadas por el proveedor. En la tabla siguiente se incluyen las propiedades que pueden estar disponibles. La lista de propiedades reales puede variar en función de la implementación del proveedor. Vea la documentación del proveedor para obtener una lista más completa de las propiedades disponibles.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>BackColor</p></td>
<td><p>Color de fondo utilizado al mostrar la celda.</p></td>
</tr>
<tr class="even">
<td><p>FontFlags</p></td>
<td><p>Máscara de bits que incluye los efectos de la fuente.</p></td>
</tr>
<tr class="odd">
<td><p>FontName</p></td>
<td><p>Fuente utilizada para mostrar el valor de la celda.</p></td>
</tr>
<tr class="even">
<td><p>FontSize</p></td>
<td><p>Tamaño de fuente utilizado para mostrar el valor de la celda.</p></td>
</tr>
<tr class="odd">
<td><p>ForeColor</p></td>
<td><p>Color de primer plano utilizado al mostrar la celda.</p></td>
</tr>
<tr class="even">
<td><p>FormatString</p></td>
<td><p>Valor de la cadena con formato.</p></td>
</tr>
</tbody>
</table>

