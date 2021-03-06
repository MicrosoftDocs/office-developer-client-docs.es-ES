---
title: Sección de Connect del archivo de personalización
TOCTitle: Customization File Connect section
ms:assetid: 037abfb4-798d-4b09-6133-356969aee95c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248802(v=office.15)
ms:contentKeyID: 48542985
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8652aa2c028350aab79cdf101cba189026b9a5ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295145"
---
# <a name="customization-file-connect-section"></a>Sección de Connect del archivo de personalización

**Se aplica a:** Access 2013, Office 2013

El comportamiento predeterminado del controlador es denegar todas las conexiones. La sección **Connect** especifica las excepciones de ese comportamiento. Por ejemplo, si todas las secciones **Connect** están ausentes o vacías, no se podrá establecer ninguna conexión de manera predeterminada.

La sección **Connect** puede contener:

- Una entrada de acceso predeterminada que especifica las operaciones de lectura y escritura predeterminadas que se permiten en esta conexión.Si no hay ninguna entrada de acceso predeterminada en la sección, se omitirá la sección.

- Una nueva cadena de conexión que reemplaza la cadena de conexión del cliente.

## <a name="syntax"></a>Sintaxis

Una entrada de acceso predeterminada tiene el siguiente formato:

`Access=accessRight`

Una cadena de conexión de reemplazo tiene el siguiente formato:

`Connect=connectionString`

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
<td><p><strong>Connect</strong></p></td>
<td><p>Cadena literal que indica que se trata de una entrada de cadena de conexión.</p></td>
</tr>
<tr class="even">
<td><p><strong><em>connectionString</em></strong></p></td>
<td><p>Cadena que va a reemplazar toda la cadena de conexión del cliente.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Access</strong></p></td>
<td><p>Cadena literal que indica que se trata de una entrada de acceso.</p></td>
</tr>
<tr class="even">
<td><p><strong><em>accessRight</em></strong></p></td>
<td><p>Uno de los siguientes derechos de acceso:</p>
<p></p>
<ul>
<li><p><strong>NoAccess</strong> el usuario no puede obtener acceso al origen de datos.</p></li>
<li><p><strong>ReadOnly</strong> el usuario puede leer el origen de datos.</p></li>
<li><p><strong>ReadWrite</strong> el usuario puede leer o escribir en el origen de datos.</p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


Si desea permitir cualquier conexión (en efecto, deshabilitar el comportamiento predeterminado  del controlador), establezca la entrada de  acceso de la sección predeterminada de conexión en y elimine o comente cualquier otra sección de identificador *de* conexión.

