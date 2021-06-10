---
title: Sección de UserList del archivo de personalización
TOCTitle: Customization File UserList section
ms:assetid: b60ba3b0-37d4-bb59-d3cd-2ab44d178b8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249873(v=office.15)
ms:contentKeyID: 48547263
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ecaf77765051a202925449d0221f0a68a2a06622
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295159"
---
# <a name="customization-file-userlist-section"></a>Sección de UserList del archivo de personalización


**Se aplica a:** Access 2013, Office 2013

La sección **Userlist** forma parte de la sección **Connect** con el mismo parámetro *identifier* de la sección.

Esta sección puede contener *una* entrada de acceso de usuario , que  especifica los derechos de acceso para el usuario especificado y invalida la entrada de acceso predeterminada *en* la sección **de conexión** correspondiente.

## <a name="syntax"></a>Sintaxis

Una entrada de acceso de usuario tiene el siguiente formato:

*userName***=* accessRights***

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parte</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>userName</em></p></td>
<td><p><em>Nombre de usuario</em> de la persona que utiliza esta conexión. Para configurar nombres de usuario válidos, utilice el cuadro de diálogo <strong>Administrador de servicios</strong> de IIS.</p></td>
</tr>
<tr class="even">
<td><p><strong><em>accessRights</em></strong></p></td>
<td><p>Uno de los siguientes derechos de acceso:<br />
</p>
<ul>
<li><p><strong>NoAccess</strong> el usuario no puede obtener acceso al origen de datos.</p></li>
<li><p><strong>ReadOnly</strong> el usuario puede leer el origen de datos.</p></li>
<li><p><strong>ReadWrite</strong> el usuario puede leer o escribir en el origen de datos.</p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

