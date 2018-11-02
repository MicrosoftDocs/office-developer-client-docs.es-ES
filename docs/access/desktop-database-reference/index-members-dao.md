---
title: Miembros de índice (DAO)
TOCTitle: Index Members
ms:assetid: e261c5fa-ca7d-0d63-1c29-48e9231b39d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835712(v=office.15)
ms:contentKeyID: 48548290
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: df4400752545be2d91cda978b41b32523d28f079
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927385"
---
# <a name="index-members-dao"></a>Miembros de índice (DAO)


**Se aplica a**: Access 2013, Office 2013

El objeto Index especifica el orden de los registros a los que se tiene acceso desde las tablas de la base de datos y si se aceptan o no los registros duplicados, lo que proporciona un acceso a los datos eficaz. Para bases de datos externas, los objetos Index describen los índices establecidos para tablas externas (sólo áreas de trabajo de Microsoft Access).

## <a name="methods"></a>Métodos

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
<td><p><strong><a href="index-createfield-method-dao.md">CreateField</a></strong></p></td>
<td><p>Crea un nuevo objeto <strong><a href="field-object-dao.md">Field</a></strong> (sólo áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Crea un nuevo objeto <strong><a href="property-object-dao.md">Property</a></strong> definido por el usuario (sólo áreas de trabajo de Microsoft Access).</p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a>Propiedades

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
<td><p><strong><a href="index-clustered-property-dao.md">Clustered</a></strong></p></td>
<td><p>Establece o devuelve un valor que indica si un objeto <strong>Index</strong> representa un índice agrupado para una tabla (sólo áreas de trabajo de Microsoft Access). <strong>Boolean</strong> de lectura y escritura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-distinctcount-property-dao.md">DistinctCount</a></strong></p></td>
<td><p>Devuelve un valor que indica el número de valores únicos del objeto <strong><a href="index-object-dao.md">Index</a></strong> que se incluyen en la tabla asociada (sólo áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-fields-property-dao.md">Fields</a></strong></p></td>
<td><p>Devuelve una colección <strong>Fields</strong> que representa a todos los objetos <strong>Field</strong> almacenados para el objeto especificado. Lectura y escritura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-foreign-property-dao.md">Foreign</a></strong></p></td>
<td><p>Devuelve un valor que indica si un objeto <strong><a href="index-object-dao.md">Index</a></strong> representa una clave externa en una tabla (solo en áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-ignorenulls-property-dao.md">IgnoreNulls</a></strong></p></td>
<td><p>Establece o devuelve un valor que indica si los registros con valores Null en sus campos de índice tienen entradas de índice (sólo para áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-name-property-dao.md">Name</a></strong></p></td>
<td><p>Devuelve o establece el nombre del objeto especificado. <strong>String</strong> de lectura y escritura si el objeto no se anexó a una colección. <strong>String</strong> de solo lectura si el objeto se anexó a una colección.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-primary-property-dao.md">Primary</a></strong></p></td>
<td><p>Establece o devuelve un valor que indica si un objeto <strong><a href="index-object-dao.md">Index</a></strong> representa un índice de clave principal en una tabla (sólo para áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-properties-property-dao.md">Propiedades</a></strong></p></td>
<td><p>Devuelve la colección <strong><a href="properties-collection-dao.md">Properties</a></strong> de un objeto especificado. solo lectura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="index-required-property-dao.md">Obligatorio</a></strong></p></td>
<td><p>Establece o devuelve un valor que indica si un objeto <strong><a href="field-object-dao.md">Field</a></strong> requiere un valor no Null.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="index-unique-property-dao.md">Unique</a></strong></p></td>
<td><p>Establece o devuelve un valor que indica si un objeto <strong><a href="index-object-dao.md">Index</a></strong> representa un índice (clave) único para una tabla (únicamente áreas de trabajo de Microsoft Access).</p></td>
</tr>
</tbody>
</table>

