---
title: ActionEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: ActionEnum
ms:assetid: 225024c1-9088-b532-2a23-04c1aaaaa892
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248998(v=office.15)
ms:contentKeyID: 48543704
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: af0e5fd734c03b88990383b99815d6e35f2c1290
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483771"
---
# <a name="actionenum"></a>ActionEnum


**Se aplica a**: Access 2013 | Office 2013

Especifica el tipo de acción que se debe realizar cuando se llama a [SetPermissions](setpermissions-method-adox.md).

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
<td><p><strong>adAccessDeny</strong></p></td>
<td><p>3</p></td>
<td><p>Se denegarán los permisos especificados al grupo o al usuario.</p></td>
</tr>
<tr class="even">
<td><p><strong>adAccessGrant</strong></p></td>
<td><p>1</p></td>
<td><p>El grupo o el usuario tendrá al menos los permisos solicitados.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adAccessRevoke</strong></p></td>
<td><p>4</p></td>
<td><p>Se revocará todo derecho de acceso explícito que tenga el grupo o el usuario.</p></td>
</tr>
<tr class="even">
<td><p><strong>adAccessSet</strong></p></td>
<td><p>2</p></td>
<td><p>El grupo o el usuario tendrá exactamente los permisos solicitados.</p></td>
</tr>
</tbody>
</table>

