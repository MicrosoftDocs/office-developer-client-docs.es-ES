---
title: Miembros del parámetro (DAO)
TOCTitle: Parameter Members
ms:assetid: 38e19de8-5318-6077-13b1-10653069aaeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192517(v=office.15)
ms:contentKeyID: 48544228
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25eae70d88307331c44983c4e7cbbcce3fe9d309
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288115"
---
# <a name="parameter-members-dao"></a>Miembros del parámetro (DAO)

**Se aplica a:** Access 2013, Office 2013

Un objeto Parameter representa un valor suministrado a una consulta. El parámetro está asociado con un objeto QueryDef creado a partir de una consulta de parámetros.

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
<td><p><strong><a href="parameter-direction-property-dao.md">Direction</a></strong></p></td>
<td><p><strong>NOTA</strong>: las áreas de trabajo de ODBCDirect no se admiten en Microsoft Access 2013. Use ADO si desea obtener acceso a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</p>
<p>Establece o devuelve un valor que indica si un objeto <strong><a href="parameter-object-dao.md">Parameter</a></strong> representa un parámetro de entrada, un parámetro de salida, ambos o el valor devuelto del procedimiento (sólo áreas de trabajo de ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="parameter-name-property-dao.md">Name</a></strong></p></td>
<td><p>Devuelve el nombre del objeto especificado. Sólo lectura de la <strong>cadena</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="parameter-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>Devuelve la colección <strong><a href="properties-collection-dao.md">Properties</a></strong> de un objeto especificado. Sólo lectura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="parameter-type-property-dao.md">Tipo</a></strong></p></td>
<td><p>Establece o devuelve un valor que indica el tipo operativo o el tipo de datos de un objeto. <strong>Integer</strong> de lectura y escritura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="parameter-value-property-dao.md">Valor</a></strong></p></td>
<td><p>Establece o devuelve el valor de un objeto. <strong>Variant</strong> de lectura y escritura.</p></td>
</tr>
</tbody>
</table>

