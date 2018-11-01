---
title: InheritTypeEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: InheritTypeEnum
ms:assetid: aa505c66-5871-10a8-35a7-cb30bb5dc21a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249787(v=office.15)
ms:contentKeyID: 48546944
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: df631319abc1eba06d7ac804b6d8dbdaf5fc9b18
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888057"
---
# <a name="inherittypeenum"></a>InheritTypeEnum

**Se aplica a**: Access 2013, Office 2013

Especifica cómo heredan permisos establecidos con [SetPermissions](setpermissions-method-adox.md) los objetos.

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Valor</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adInheritBoth</strong></p></td>
<td><p>3</p></td>
<td><p>Los objetos y otros contenedores contenidos en el objeto principal heredan la entrada.</p></td>
</tr>
<tr class="even">
<td><p><strong>adInheritContainers</strong></p></td>
<td><p>2</p></td>
<td><p>Otros contenedores que están contenidos en el objeto principal heredan la entrada.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adInheritNone</strong></p></td>
<td><p>0</p></td>
<td><p>Valor predeterminado.

No se produce ninguna herencia.</p></td>
</tr>
<tr class="even">
<td><p><strong>adInheritNoPropagate</strong></p></td>
<td><p>4</p></td>
<td><p>Las marcas <strong>adInheritObjects</strong> y <strong>adInheritContainers</strong> no se propagan a una entrada heredada.</p></td>
</tr>
<tr class="odd">
<td><p><strong>marcas adInheritObjects</strong></p></td>
<td><p>1</p></td>
<td><p>Los objetos que nos son contenedores y están incluidos en el contenedor heredan los permisos.</p></td>
</tr>
</tbody>
</table>

