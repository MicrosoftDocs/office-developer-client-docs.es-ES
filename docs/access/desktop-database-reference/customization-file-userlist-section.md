---
title: Sección UserList del archivo de personalización
TOCTitle: Customization File UserList Section
ms:assetid: b60ba3b0-37d4-bb59-d3cd-2ab44d178b8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249873(v=office.15)
ms:contentKeyID: 48547263
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a4aa7604edc887e97cbdfbea9b75e6f46ad55f35
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880771"
---
# <a name="customization-file-userlist-section"></a>Sección UserList del archivo de personalización


**Se aplica a**: Access 2013, Office 2013

La sección **userlist** pertenece a la sección **connect** con el mismo parámetro *identifier* de sección.

En esta sección puede contener una *entrada de acceso de usuario*, que especifica los derechos de acceso para el usuario especificado y reemplaza la *entrada de acceso* de *predeterminada* en la correspondiente sección **connect** .

## <a name="syntax"></a>Sintaxis

Una entrada de acceso de usuario tiene el siguiente formato:

*userName *** =* accessRights ***

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
<td><p>Uno de los siguientes derechos de acceso:
<br />
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

