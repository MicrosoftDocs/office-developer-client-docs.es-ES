---
title: Servicio de forma de datos de Microsoft para OLE DB (proveedor de servicios ADO)
TOCTitle: Microsoft Data Shaping Service for OLE DB (ADO Service Provider)
ms:assetid: 6e6e5f39-6f43-7c7b-5812-796096d1d31b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249436(v=office.15)
ms:contentKeyID: 48545511
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5065b966608f8d6a3ef1cb05be890b9a1f147dc8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288963"
---
# <a name="microsoft-data-shaping-service-for-ole-db-ado-service-provider"></a>Servicio de forma de datos de Microsoft para OLE DB (proveedor de servicios ADO)


**Se aplica a:** Access 2013, Office 2013

El proveedor de servicios del Servicio de forma de datos de Microsoft para OLE DB admite la construcción de objetos [Recordset](recordset-object-ado.md) jerárquicos (con forma) desde un proveedor de datos.

## <a name="provider-keyword"></a>Palabra clave del proveedor

Para llamar al Servicio de forma de datos para OLE DB, especifique la siguiente palabra clave y el siguiente valor en la cadena de conexión.

```vb 
 
"Provider=MSDataShape" 
```

## <a name="dynamic-properties"></a>Propiedades dinámicas

Cuando se llama a este proveedor de servicios, se agregan las siguientes propiedades dinámicas a la colección [Properties](connection-object-ado.md) del objeto [Connection](properties-collection-ado.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre de la propiedad dinámica</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Unique Reshape Names</strong></p></td>
<td><p>Indica si se permiten los objetos <strong>Recordset</strong> con valores duplicados para sus propiedades <strong>Reshape Name</strong>. Si esta propiedad dinámica es <strong>True</strong> y se crea un nuevo objeto <strong>Recordset</strong> con el mismo nombre de cambio de forma especificado por el usuario que un objeto <strong>Recordset</strong> existente, el nombre de cambio de forma del nuevo objeto <strong>Recordset</strong> se modifica para hacerlo exclusivo. Si esta propiedad es <strong>False</strong> y se crea un nuevo objeto <strong>Recordset</strong> con el mismo nombre de cambio de forma especificado por el usuario que el objeto <strong>Recordset</strong> existente, ambos objetos <strong>Recordset</strong> tendrán el mismo nombre de cambio de forma. Por lo tanto, no será posible cambiar la forma de ninguno de los objetos <strong>Recordset</strong> mientras existan ambos. El valor predeterminado de la propiedad es <strong>False</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Data Provider</strong></p></td>
<td><p>Indica el nombre del proveedor que suministrará las filas a las que se les va a aplicar forma. Este valor puede ser NONE si no se va a utilizar un proveedor para suministrar filas.</p></td>
</tr>
</tbody>
</table>


También es posible establecer propiedades dinámicas que se pueden escribir si se especifican sus nombres como palabras clave en la cadena de conexión. Por ejemplo, en Microsoft Visual Basic, establezca la propiedad dinámica **Data Provider** en "MSDASQL" al especificar:

```vb 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MSDataShape;Data Provider=MSDASQL" 
```

También es posible establecer o recuperar una propiedad dinámica al especificar su nombre como índice de la propiedad [Properties](properties-collection-ado.md). Por ejemplo, obtenga e imprima el valor actual de la propiedad dinámica **Data Provider** y, a continuación, establezca un nuevo valor como éste:

```vb 
 
Debug.Print cn.Properties("Data Provider") 
cn.Properties("Data Provider") = "MSDASQL" 
```

Para obtener más información acerca de la forma de datos, vea [Forma de datos](data-shaping.md).

