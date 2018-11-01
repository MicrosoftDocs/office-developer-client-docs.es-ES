---
title: Crear la cadena de conexión
TOCTitle: Creating the Connection String
ms:assetid: 0d34b1c6-bf2e-1299-9778-573ccd2da1c7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248853(v=office.15)
ms:contentKeyID: 48543214
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bd4bafd29195e2ff9898973351cd7d13262c3cec
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869683"
---
# <a name="creating-the-connection-string"></a>Crear la cadena de conexión


**Se aplica a**: Access 2013, Office 2013

ADO admite directamente cinco argumentos en una cadena de conexión. ADO pasa otros argumentos al proveedor que se menciona en el argumento *Provider* sin ningún procesamiento.

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
<td><p><em>Provider</em></p></td>
<td><p>Especifica el nombre del proveedor que se va a usar en la conexión.</p></td>
</tr>
<tr class="even">
<td><p><em>Nombre del archivo</em></p></td>
<td><p>Especifica el nombre de un archivo específico del proveedor (por ejemplo, un objeto de origen de datos almacenado de manera persistente) que contiene información de conexión predefinida.</p></td>
</tr>
<tr class="odd">
<td><p><em>URL</em></p></td>
<td><p>Especifica la cadena de conexión como una dirección URL absoluta que identifica un recurso, como un archivo o un directorio.</p></td>
</tr>
<tr class="even">
<td><p><em>Remote Provider</em></p></td>
<td><p>Especifica el nombre del proveedor que se va a usar cuando se abre una conexión de cliente (sólo con el Servicio de datos remotos, RDS).</p></td>
</tr>
<tr class="odd">
<td><p><em>Remote Server</em></p></td>
<td><p>Especifica el nombre de la ruta de acceso del servidor que se utilizará al abrir una conexión de cliente (sólo Servicio de datos remoto).</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> En los ejemplos siguientes y en toda la Guía del programador de ADO, se utiliza el identificador de usuario "MyId" con la contraseña "123aBc" para autenticación en el servidor. Debe sustituir estos valores con credenciales de inicio de sesión válidas para su servidor. Sustituya también el nombre de su servidor por "MySqlServer".

La aplicación HelloData del capítulo 1 utilizó la cadena de conexión siguiente:

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
```

El único parámetro de ADO que se proporcionó en esta cadena de conexión fue "Provider=SQLOLEDB ", que indicó el proveedor de Microsoft OLE DB para SQL Server. Para determinar otros parámetros válidos que se pueden pasar en la cadena de conexión, se puede consultar la documentación de cada proveedor. Según el proveedor OLE DB para la documentación de SQL Server, puede sustituir "Server" para el parámetro *Data Source* y "Database" por el parámetro *Initial Catalog* . Por tanto, la cadena de conexión siguiente generaría resultados idénticos a la primera:

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Server='MySqlServer';" & _ 
 "Database='Northwind';Integrated Security='SSPI';" 
```

Para abrir la conexión, simplemente pase la cadena de conexión como primer argumento en el método **Open** del objeto **Connection**:

```vb 
 
objConn.Open m_sConnStr 
```

También es posible proporcionar una gran parte de esta información estableciendo propiedades del objeto **Connection** antes de abrir la conexión. Por ejemplo, se podría lograr el mismo efecto que con la cadena de conexión anterior utilizando el código siguiente:

```vb 
 
With objConn 
 .Provider = "SQLOLEDB" 
 .DefaultDatabase = "Northwind" 
 .Properties("Data Source") = "MySqlServer" 
 .Properties("Integrated Security") = "SSPI" 
 .Open 
End With 
```

