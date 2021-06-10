---
title: Enumeración PermissionEnum (DAO)
TOCTitle: PermissionEnum Enumeration
ms:assetid: dcce9940-f8a7-e915-1b69-05c341bea8cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835373(v=office.15)
ms:contentKeyID: 48548147
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8d4f6741bd6203dbdeffb364650b5e3550ea8b1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287713"
---
# <a name="permissionenum-enumeration-dao"></a>Enumeración PermissionEnum (DAO)


**Se aplica a:** Access 2013, Office 2013

Se utiliza con la propiedad **Permissions** para especificar el tipo de permisos.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Valor</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbSecCreate</p></td>
<td><p>1</p></td>
<td><p>El usuario puede crear documentos nuevos (no es válido para objetos Document).</p></td>
</tr>
<tr class="even">
<td><p>dbSecDBAdmin</p></td>
<td><p>8 </p></td>
<td><p>El usuario puede replicar una base de datos y cambiar su contraseña (no es válido para objetos Document).</p></td>
</tr>
<tr class="odd">
<td><p>dbSecDBCreate</p></td>
<td><p>1</p></td>
<td><p>El usuario puede crear nuevas bases de datos. Esta opción sólo es válida en el contenedor de bases de datos en el archivo de información del grupo de trabajo (Systen.mdw). Esta constante no es válida para objetos Document.</p></td>
</tr>
<tr class="even">
<td><p>dbSecDBExclusive</p></td>
<td><p>4 </p></td>
<td><p>El usuario tiene acceso exclusivo a la base de datos.</p></td>
</tr>
<tr class="odd">
<td><p>dbSecDBOpen</p></td>
<td><p>2</p></td>
<td><p>El usuario puede abrir la base de datos.</p></td>
</tr>
<tr class="even">
<td><p>dbSecDelete</p></td>
<td><p>65536</p></td>
<td><p>El usuario puede eliminar el objeto.</p></td>
</tr>
<tr class="odd">
<td><p>dbSecDeleteData</p></td>
<td><p>128</p></td>
<td><p>El usuario puede eliminar registros.</p></td>
</tr>
<tr class="even">
<td><p>dbSecFullAccess</p></td>
<td><p>1048575</p></td>
<td><p>El usuario tiene acceso total al objeto.</p></td>
</tr>
<tr class="odd">
<td><p>dbSecInsertData</p></td>
<td><p>32</p></td>
<td><p>El usuario puede agregar registros.</p></td>
</tr>
<tr class="even">
<td><p>dbSecNoAccess</p></td>
<td><p>0</p></td>
<td><p>El usuario no tiene acceso al objeto (no es válido para objetos Document).</p></td>
</tr>
<tr class="odd">
<td><p>dbSecReadDef</p></td>
<td><p>4 </p></td>
<td><p>El usuario puede leer la definición de tabla, incluida la información de índice y de columnas.</p></td>
</tr>
<tr class="even">
<td><p>dbSecReadSec</p></td>
<td><p>131072</p></td>
<td><p>El usuario puede leer la información relacionada con la seguridad del objeto.</p></td>
</tr>
<tr class="odd">
<td><p>dbSecReplaceData</p></td>
<td><p>64</p></td>
<td><p>El usuario puede modificar registros.</p></td>
</tr>
<tr class="even">
<td><p>dbSecRetrieveData</p></td>
<td><p>20</p></td>
<td><p>El usuario puede recuperar datos del objeto Document.</p></td>
</tr>
<tr class="odd">
<td><p>dbSecWriteDef</p></td>
<td><p>65548</p></td>
<td><p>El usuario puede modificar o eliminar la definición de tabla, incluida la información de índice y de columnas.</p></td>
</tr>
<tr class="even">
<td><p>dbSecWriteOwner</p></td>
<td><p>524288</p></td>
<td><p>El usuario puede cambiar el valor de la propiedad Owner.</p></td>
</tr>
<tr class="odd">
<td><p>dbSecWriteSec</p></td>
<td><p>262144</p></td>
<td><p>El usuario puede alterar los permisos de acceso.</p></td>
</tr>
</tbody>
</table>

