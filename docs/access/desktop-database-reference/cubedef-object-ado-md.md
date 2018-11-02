---
title: CubeDef (objeto, ADO MD)
TOCTitle: CubeDef object (ADO MD)
ms:assetid: 199235b7-3d98-f655-27bc-94f66e994e06
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248941(v=office.15)
ms:contentKeyID: 48543502
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9f48b3ea16e45b3bde12ed9f8584c3218f955eba
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922394"
---
# <a name="cubedef-object-ado-md"></a>CubeDef (objeto, ADO MD)


**Se aplica a**: Access 2013, Office 2013

Representa un cubo de un esquema multidimensional, que contiene un conjunto de dimensiones relacionadas.

## <a name="remarks"></a>Comentarios

Con las colecciones y las propiedades de un objeto **CubeDef**, puede hacer lo siguiente:

  - Identificar el objeto **CubeDef** con la propiedad [Name](name-property-ado-md.md).

  - Devolver una cadena que describa el cubo con la propiedad [Description](description-property-ado-md.md).

  - Devolver las dimensiones que conforman el cubo con la colección [Dimensions](dimensions-collection-ado-md.md).

  - Obtener información adicional sobre el objeto **CubeDef** con la colección [Properties](properties-collection-ado.md) de ADO estándar.

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
<td><p>NombreCatálogo</p></td>
<td><p>Nombre del catálogo al que pertenece el cubo.</p></td>
</tr>
<tr class="even">
<td><p>CreatedOn</p></td>
<td><p>Fecha y hora de creación del cubo.</p></td>
</tr>
<tr class="odd">
<td><p>CubeGUID</p></td>
<td><p>GUID del cubo.</p></td>
</tr>
<tr class="even">
<td><p>Nombre de cubo</p></td>
<td><p>Nombre del cubo.</p></td>
</tr>
<tr class="odd">
<td><p>CubeType</p></td>
<td><p>Tipo del cubo.</p></td>
</tr>
<tr class="even">
<td><p>DataUpdatedBy</p></td>
<td><p>Id. de usuario de la persona que actualizó por última vez los datos.</p></td>
</tr>
<tr class="odd">
<td><p>Description</p></td>
<td><p>Descripción del cubo.</p></td>
</tr>
<tr class="even">
<td><p>LastSchemaUpdate</p></td>
<td><p>Fecha y hora de la última actualización del esquema.</p></td>
</tr>
<tr class="odd">
<td><p>SchemaName</p></td>
<td><p>Nombre del esquema al que pertenece el cubo.</p></td>
</tr>
<tr class="even">
<td><p>SchemaUpdatedBy</p></td>
<td><p>Id. de usuario de la persona que actualizó por última vez el esquema.</p></td>
</tr>
</tbody>
</table>

