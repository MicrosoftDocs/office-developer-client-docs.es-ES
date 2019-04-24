---
title: Crear la cadena de conexión
TOCTitle: Creating the connection string
ms:assetid: 0d34b1c6-bf2e-1299-9778-573ccd2da1c7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248853(v=office.15)
ms:contentKeyID: 48543214
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f43207edec0c0acb58c66318e5dc7668a28ea595
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295330"
---
# <a name="creating-the-connection-string"></a>Crear la cadena de conexión

**Se aplica a:** Access 2013, Office 2013

ADO admite directamente cinco argumentos en una cadena de conexión. ADO pasa otros argumentos al proveedor que se menciona en el argumento *Provider* sin ningún procesamiento.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Provider</em></p></td>
<td><p>Especifica el nombre del proveedor que se va a usar en la conexión.</p></td>
</tr>
<tr class="even">
<td><p><em>File Name</em></p></td>
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
<td><p>Especifica el nombre de la ruta de acceso del servidor que se utilizará al abrir una conexión de cliente. (Sólo con el Servicio de datos remotos, RDS.)</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> En los ejemplos siguientes y en toda la guía del programador de ADO, se utiliza el identificador de usuario "MyId" con la contraseña "123aBc" para autenticarse en el servidor. Debe sustituir estos valores con credenciales de inicio de sesión válidas para su servidor. Sustituya también el nombre de su servidor por "MySqlServer".

La aplicación HelloData del capítulo 1 utilizó la cadena de conexión siguiente:

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
```

El único parámetro de ADO que se proporcionó en esta cadena de conexión fue "Provider=SQLOLEDB ", que indicó el proveedor de Microsoft OLE DB para SQL Server. Para determinar otros parámetros válidos que se pueden pasar en la cadena de conexión, se puede consultar la documentación de cada proveedor. Según la documentación de OLE DB Provider para SQL Server, se puede sustituir "Server" por el parámetro *Data Source* y "Database" por el parámetro *Initial Catalog*. Por tanto, la cadena de conexión siguiente generaría resultados idénticos a la primera:

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

