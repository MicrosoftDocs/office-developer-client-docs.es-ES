---
title: DriverPromptEnum Enumeration (DAO)
TOCTitle: DriverPromptEnum Enumeration
ms:assetid: 8dda5e9f-a58f-a62d-eb49-5966d4a1e086
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197361(v=office.15)
ms:contentKeyID: 48546266
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c20542c89537f16f20c9d3e30cbc14ce115bf4d6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486719"
---
# <a name="driverpromptenum-enumeration-dao"></a>DriverPromptEnum Enumeration (DAO)


**Se aplica a**: Access 2013 | Office 2013

Especifica si se ha de preguntar al usuario para establecer una conexión y cuándo.

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
<td><p>dbDriverComplete</p></td>
<td><p>0</p></td>
<td><p>Si la cadena de conexión proporcionada incluye la palabra clave DSN, el administrador de controladores utiliza la cadena que se proporciona al establecer conexión; en caso contrario, se comporta al igual que cuando se especifica <strong>dbDriverPrompt</strong>.</p></td>
</tr>
<tr class="even">
<td><p>dbDriverCompleteRequired</p></td>
<td><p>3</p></td>
<td><p>(Valor predeterminado) Se comporta como <strong>dbDriverComplete</strong>, con la excepción de que el controlador deshabilita los controles correspondientes a la información no necesaria para realizar la conexión.</p></td>
</tr>
<tr class="odd">
<td><p>dbDriverNoPrompt</p></td>
<td><p>1</p></td>
<td><p>El administrador de controladores utiliza la cadena de conexión proporcionada al establecer conexión. Si no se proporciona información suficiente, se devuelve un error interceptable.</p></td>
</tr>
<tr class="even">
<td><p>dbDriverPrompt</p></td>
<td><p>2</p></td>
<td><p>El administrador de controladores muestra el cuadro de diálogo <strong>Orígenes de datos ODBC</strong>. La cadena de conexión utilizada para establecer la conexión se crea a partir del nombre del origen de datos (DSN) seleccionado y cumplimentado por el usuario a través de los cuadros de diálogo.</p></td>
</tr>
</tbody>
</table>

