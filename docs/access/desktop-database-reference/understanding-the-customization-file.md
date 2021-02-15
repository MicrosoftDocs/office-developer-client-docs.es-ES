---
title: Introducción al archivo de personalización
TOCTitle: Understanding the Customization File
ms:assetid: 98fd5ec1-d5bd-cdd2-5eb5-9a1682fbed79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249686(v=office.15)
ms:contentKeyID: 48546507
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b977fc4273068ac52efe8960761a9e28a6234e2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314073"
---
# <a name="understanding-the-customization-file"></a>Introducción al archivo de personalización


**Se aplica a:** Access 2013, Office 2013

Cada encabezado de sección del archivo de personalización consta de corchetes ( **\[\]** ) que contienen un tipo y parámetro. Los cuatro tipos de sección vienen indicados por las cadenas literales **connect**, **sql**, **userlist** o **logs**. El parámetro es la cadena literal, el valor predeterminado, un identificador especificado por el usuario o nada.

Por lo tanto, cada sección viene marcada con uno de los encabezados siguientes:

```text 
 
[ connect   default     ]
[ connect   identifier  ]
[ sql       default     ]
[ sql       identifier  ]
[ userlist  identifier  ]
[ logs                  ]
```

Los encabezados de sección constan de los siguientes elementos.

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
<td><p><strong>connect</strong></p></td>
<td><p>Cadena literal que modifica una cadena de conexión.</p></td>
</tr>
<tr class="even">
<td><p><strong>sql</strong></p></td>
<td><p>Cadena literal que modifica una cadena de comandos.</p></td>
</tr>
<tr class="odd">
<td><p><strong>userlist</strong></p></td>
<td><p>Cadena literal que modifica los derechos de acceso de un usuario específico.</p></td>
</tr>
<tr class="even">
<td><p><strong>logs</strong></p></td>
<td><p>Cadena literal que especifica un archivo de registro donde se registran los errores operativos.</p></td>
</tr>
<tr class="odd">
<td><p><strong>default</strong></p></td>
<td><p>Cadena literal que se utiliza si no se ha especificado o no se encuentra ningún identificador.</p></td>
</tr>
<tr class="even">
<td><p><em>identificador</em></p></td>
<td><p>Cadena que corresponde a una cadena en la cadena de <strong>conexión</strong> o de <strong>comandos</strong>.</p>
<p></p>
<ul>
<li><p>Utilice esta sección si el encabezado de sección contiene <strong>connect</strong> y se encuentra la cadena de identificador en la cadena de conexión.</p></li>
<li><p>Utilice esta sección si el encabezado de sección contiene <strong>sql</strong> y se encuentra la cadena de identificador en la cadena de comandos.</p></li>
<li><p>Utilice esta sección si el encabezado de sección contiene <strong>userlist</strong> y la cadena de identificador coincide con un identificador de la sección <strong>connect</strong>.</p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


**DataFactory** llama al controlador, pasando parámetros de cliente. El controlador busca cadenas completas en los parámetros de cliente que coincidan con los identificadores en los correspondientes encabezados de sección. Si se encuentra una coincidencia, se aplica el contenido de esa sección al parámetro de cliente.

Se utiliza una sección concreta en las circunstancias siguientes:

  - Se **usa** una sección connect si la parte del valor de la palabra clave de cadena de conexión del cliente, "**Data Source=***value",* coincide con un identificador **de** sección connect *.*

  - Se utiliza una sección **sql** si la cadena de comandos del cliente contiene una cadena que coincide con un identificador de la sección **sql**.

  - Se utiliza una sección **connect** o **sql** con un parámetro predeterminado si no hay ningún identificador coincidente.

  - Se utiliza una sección **userlist** si el identificador de la sección **userlist** coincide con un identificador de la sección **connect**. Si hay una coincidencia, se aplica el contenido de la sección **userlist** a la conexión que rige la sección **connect**.

  - Si la cadena en una cadena de conexión o de comandos no coincide con ningún identificador del encabezado de sección **connect** o **sql**, y si no hay ningún encabezado de sección **connect** o **sql** con un parámetro predeterminado, se utilizará la cadena de cliente sin modificación alguna.

  - Se utiliza la sección **logs** cada vez que se encuentra operativo el objeto **DataFactory**.

