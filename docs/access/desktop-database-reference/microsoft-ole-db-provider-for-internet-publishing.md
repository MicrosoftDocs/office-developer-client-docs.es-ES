---
title: OLE DB Provider for Internet Publishing
TOCTitle: Microsoft OLE DB Provider for Internet Publishing
ms:assetid: 5d1e8db5-dabb-0914-e11e-e2eac72bfa77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249327(v=office.15)
ms:contentKeyID: 48545100
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7221c6bd0a6e8576237fdf4cbfcabe70620f6af8
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603997"
---
# <a name="microsoft-ole-db-provider-for-internet-publishing"></a>OLE DB Provider for Internet Publishing

**Se aplica a**: Access 2013 | Office 2013

Microsoft OLE DB Provider for Internet Publishing permite que ADO obtenga acceso a recursos proporcionados por Microsoft FrontPage o Microsoft Internet Information Server. Los recursos incluyen archivos Web de código fuente como archivos HTML o carpetas Web de Windows 2000.

## <a name="connection-string-parameters"></a>Parámetros de la cadena de conexión

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
<<<<<<< HEAD
<td><p>Especifica la dirección URL de un archivo o directorio publicado en una carpeta Web.</p></td>
=======
<td><p>Especifica la dirección URL de un archivo o directorio publicado en una carpeta web.</p></td>
>>>>>>>patrón
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
> <P>Si MSDAIPP. DSO se especifica explícitamente como el valor del proveedor, ya sea con la palabra clave la cadena de conexión de <EM>proveedor</EM> o la propiedad <STRONG>Provider</STRONG> , no se puede usar "dirección URL =" en la cadena de conexión. Si se hace así, se producirá un error. En lugar de esto, especifique la dirección URL como se muestra en el tema <A href="the-ole-db-provider-for-internet-publishing.md">Utilizar ADO con OLE DB Provider for Internet Publishing</A>.</P>


