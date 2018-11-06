---
title: OLE DB Provider for Internet Publishing
TOCTitle: Microsoft OLE DB Provider for Internet Publishing
ms:assetid: 5d1e8db5-dabb-0914-e11e-e2eac72bfa77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249327(v=office.15)
ms:contentKeyID: 48545100
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c6f1c7c65d0ac1dd2a6d3ea132a31955f175bc7f
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997486"
---
# <a name="microsoft-ole-db-provider-for-internet-publishing"></a>OLE DB Provider for Internet Publishing

**Se aplica a**: Access 2013, Office 2013

Microsoft OLE DB Provider for Internet Publishing permite que ADO obtenga acceso a recursos proporcionados por Microsoft FrontPage o Microsoft Internet Information Server. Los recursos incluyen archivos Web de código fuente como archivos HTML o carpetas Web de Windows 2000.

## <a name="connection-string-parameters"></a>Parámetros de cadena de conexión

Para conectar con este proveedor, establezca el argumento *Provider* de la propiedad [ConnectionString](connectionstring-property-ado.md) en:

```vb 
 
MSDAIPP.DSO 
```

Este valor también puede establecerse o leerse mediante la propiedad [Provider](provider-property-ado.md).

## <a name="typical-connection-string"></a>Cadena de conexión típica

Una típica cadena de conexión de este proveedor es:

```vb 
 
"Provider=MSDAIPP.DSO;Data Source=ResourceURL;User ID=userName;Password=userPassword;" 
```

\-o -

```vb 
 
"URL=ResourceURL;User ID=userName;Password=userPassword;" 
```

La cadena consta de estas palabras clave:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Palabra clave</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Provider</strong></p></td>
<td><p>Especifica el Proveedor OLE DB para Publicación en Internet.</p></td>
</tr>
<tr class="even">
<td><p><strong>Data Source</strong> o <strong>URL</strong></p></td>
<td><p>Especifica la dirección URL de un archivo o directorio publicado en una carpeta web.</p></td>
</tr>
<tr class="odd">
<td><p><strong>User ID</strong></p></td>
<td><p>Especifica el nombre de usuario.</p></td>
</tr>
<tr class="even">
<td><p><strong>Password</strong></p></td>
<td><p>Especifica la contraseña de usuario.</p></td>
</tr>
</tbody>
</table>


Si se establece el valor de *ResourceURL* desde la "URL=" de la cadena de conexión en un valor no válido, el Proveedor para Publicación en Internet muestra de forma predeterminada un cuadro de diálogo para solicitar un valor válido. Se trata de un comportamiento no deseado de un componente del nivel intermedio de una aplicación, dado que detiene la ejecución del programa hasta que se borra el cuadro de diálogo y parece que el cliente esté bloqueado debido a que no ha recibido una respuesta del componente.

> [!NOTE]
> Si MSDAIPP. DSO se especifica explícitamente como el valor del proveedor, ya sea con la palabra clave la cadena de conexión de *proveedor* o la propiedad **Provider** , no se puede usar "dirección URL =" en la cadena de conexión. Si se hace así, se producirá un error. En lugar de esto, especifique la dirección URL como se muestra en el tema [Utilizar ADO con OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md).

