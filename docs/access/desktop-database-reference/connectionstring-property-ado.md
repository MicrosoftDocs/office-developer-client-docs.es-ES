---
title: Propiedad ConnectionString (ADO)
TOCTitle: ConnectionString property (ADO)
ms:assetid: c67a7daf-258f-d99d-6475-a4aa98d1e99d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249968(v=office.15)
ms:contentKeyID: 48547627
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3612652f3473c0794dbfe9be60f84ea2e3fee252
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295712"
---
# <a name="connectionstring-property-ado"></a>Propiedad ConnectionString (ADO)


**Se aplica a:** Access 2013, Office 2013

Indica la información utilizada para establecer una conexión con un origen de datos.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo **String**.

## <a name="remarks"></a>Comentarios

Utilice la **propiedad ConnectionString** para especificar un origen de datos pasando  una cadena de conexión detallada que contenga una serie de argumento *=* instrucciones de valor separadas por punto y coma.

ADO admite cinco argumentos para la propiedad **ConnectionString**; todos los demás argumentos pasan directamente al proveedor sin que ADO los procese. Los argumentos admitidos por ADO son:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Provider=</em></p></td>
<td><p>Especifica el nombre del proveedor que se va a usar en la conexión.</p></td>
</tr>
<tr class="even">
<td><p><em>File Name=</em></p></td>
<td><p>Especifica el nombre de un archivo específico del proveedor (por ejemplo, un objeto de origen de datos almacenado de manera persistente) que contiene información de conexión predefinida.</p></td>
</tr>
<tr class="odd">
<td><p><em>Remote Provider=</em></p></td>
<td><p>Especifica el nombre de un proveedor que se debe usar al abrir una conexión del lado cliente. (Sólo con el Servicio de datos remotos, RDS.)</p></td>
</tr>
<tr class="even">
<td><p><em>Remote Server=</em></p></td>
<td><p>Especifica el nombre de la ruta de acceso del servidor que se utilizará al abrir una conexión de cliente. (Sólo con el Servicio de datos remotos, RDS.)</p></td>
</tr>
<tr class="odd">
<td><p><em>URL=</em></p></td>
<td><p>Especifica la cadena de conexión como una dirección URL absoluta que identifica un recurso, como un archivo o un directorio.</p></td>
</tr>
</tbody>
</table>


Después de que se establezca el valor de la propiedad **ConnectionString** y se abra el objeto [Connection](connection-object-ado.md), puede que el proveedor modifique el contenido de la propiedad, por ejemplo, mediante la asignación de los nombres de argumento definidos por ADO a sus propios equivalentes.

La propiedad **ConnectionString** hereda automáticamente el valor usado para el argumento *ConnectionString* del método [Open](open-method-ado-connection.md), por lo que se puede invalidar la actual propiedad **ConnectionString** durante la llamada al método **Open**.

Dado que el argumento *File Name* hace que ADO cargue el proveedor asociado, no se puede pasar tanto el argumento *Provider* como el argumento *File Name*.

La propiedad **ConnectionString** es de lectura y escritura cuando está cerrada la conexión, y es de sólo lectura cuando la conexión está abierta.

Se omiten los duplicados de un argumento en la propiedad **ConnectionString**. Se utiliza la última instancia de los argumentos.

**Uso del servicio de datos remotos** Cuando se usa en un objeto **Connection** del lado cliente, la propiedad **ConnectionString** solo puede incluir los parámetros *proveedor* remoto y *servidor* remoto.

