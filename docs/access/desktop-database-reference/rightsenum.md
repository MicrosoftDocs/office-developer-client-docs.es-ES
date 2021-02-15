---
title: RightsEnum (referencia de base de datos de escritorio de Access)
TOCTitle: RightsEnum
ms:assetid: 7647b9d5-5271-fdcf-489d-5a8beb931ca5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249485(v=office.15)
ms:contentKeyID: 48545693
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3c7bf2f88632265cda7537215f2ea3c68507f16f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306492"
---
# <a name="rightsenum"></a>RightsEnum

**Se aplica a:** Access 2013, Office 2013

Especifica los derechos o los permisos para un grupo o un usuario en un objeto.

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
<td><p><strong>adRightCreate</strong></p></td>
<td><p>16384<br />
( &amp; H4000)</p></td>
<td><p>El usuario o el grupo tiene permiso para crear objetos nuevos de este tipo.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightDelete</strong></p></td>
<td><p>65536<br />
( &amp; H10000)</p></td>
<td><p>El usuario o el grupo tienen permiso para eliminar datos de un objeto.
Para objetos tal como <strong>Tables</strong>, el usuario tiene permiso para eliminar valores de datos de los registros.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightDrop</strong></p></td>
<td><p>256<br />
( &amp; H100)</p></td>
<td><p>El usuario o el grupo tiene permiso para quitar objetos del catálogo.
Por ejemplo, <strong>Tables</strong> se puede eliminar mediante un comando SQL DROP TABLE.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightExclusive</strong></p></td>
<td><p>512<br />
( &amp; H200)</p></td>
<td><p>El usuario o el grupo tiene permiso de acceso exclusivo al objeto.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightExecute</strong></p></td>
<td><p>536870912<br />
( &amp; H20000000)</p></td>
<td><p>El usuario o el grupo tiene permiso para ejecutar el objeto.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightFull</strong></p></td>
<td><p>268435456<br />
( &amp; H10000000)</p></td>
<td><p>El usuario o el grupo tiene todos los permisos en el objeto.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightInsert</strong></p></td>
<td><p>32768<br />
( &amp; H8000)</p></td>
<td><p>El usuario o el grupo tiene permiso para insertar el objeto.
Para objetos tales como <strong>Tables</strong>, el usuario tiene permiso para insertar datos en la tabla.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightMaximumAllowed</strong></p></td>
<td><p>33554432 ( &amp; H2000000)</p></td>
<td><p>El usuario o el grupo tiene el número máximo de permisos que concede el proveedor. Los permisos específicos dependen del proveedor.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightNone</strong></p></td>
<td><p>0</p></td>
<td><p>El usuario o el grupo no tiene ningún permiso para el objeto.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightRead</strong></p></td>
<td><p>-2147483648<br />
( &amp; H80000000)</p></td>
<td><p>El usuario o el grupo tiene permiso para leer el objeto.
Para objetos tales como <a href="table-object-adox.md">Tables</a>, el usuario tiene permiso para leer los datos de la tabla.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightReadDesign</strong></p></td>
<td><p>1024<br />
( &amp; H400)</p></td>
<td><p>El usuario o el grupo tiene permiso para leer el diseño para el objeto.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightReadPermissions</strong></p></td>
<td><p>131072<br />
( &amp; H20000)</p></td>
<td><p>El usuario o el grupo puede ver, pero no cambiar, los permisos específicos para un objeto del catálogo.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightReference</strong></p></td>
<td><p>8192<br />
( &amp; H2000)</p></td>
<td><p>El usuario o el grupo tiene permiso para hacer referencia al objeto.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightUpdate</strong></p></td>
<td><p>1073741824<br />
( &amp; H40000000)</p></td>
<td><p>El usuario o el grupo tiene permiso para actualizar el objeto.
Para objetos tales como <strong>Tables</strong>, el usuario tiene permiso para actualizar los datos de la tabla.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightWithGrant</strong></p></td>
<td><p>4096<br />
( &amp; H1000)</p></td>
<td><p>El usuario o el grupo tiene permiso para conceder permisos para el objeto.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightWriteDesign</strong></p></td>
<td><p>2048<br />
( &amp; H800)</p></td>
<td><p>El usuario o el grupo tiene permiso para modificar el diseño para el objeto.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightWriteOwner</strong></p></td>
<td><p>524288<br />
( &amp; H80000)</p></td>
<td><p>El usuario o el grupo tiene permiso para modificar el propietario del objeto.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightWritePermissions</strong></p></td>
<td><p>262144<br />
( &amp; H40000)</p></td>
<td><p>El usuario o el grupo puede modificar los permisos específicos para un objeto del catálogo.</p></td>
</tr>
</tbody>
</table>

