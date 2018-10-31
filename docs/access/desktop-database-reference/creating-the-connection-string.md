---
title: Crear la cadena de conexión
TOCTitle: Creating the Connection String
ms:assetid: 0d34b1c6-bf2e-1299-9778-573ccd2da1c7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248853(v=office.15)
ms:contentKeyID: 48543214
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6d4c869d6021c807e27fb7970ef6ea91f91bd4de
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860458"
---
# <a name="creating-the-connection-string"></a><span data-ttu-id="0303d-102">Crear la cadena de conexión</span><span class="sxs-lookup"><span data-stu-id="0303d-102">Creating the Connection String</span></span>


<span data-ttu-id="0303d-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0303d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0303d-p101">ADO admite directamente cinco argumentos en una cadena de conexión. ADO pasa otros argumentos al proveedor que se menciona en el argumento *Provider* sin ningún procesamiento.</span><span class="sxs-lookup"><span data-stu-id="0303d-p101">ADO directly supports five arguments in a connection string. Other arguments are passed to the provider that is named in the *Provider* argument without any processing by ADO.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0303d-106">Argumento</span><span class="sxs-lookup"><span data-stu-id="0303d-106">Argument</span></span></p></th>
<th><p><span data-ttu-id="0303d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="0303d-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0303d-108"><em>Provider</em></span><span class="sxs-lookup"><span data-stu-id="0303d-108"><em>Provider</em></span></span></p></td>
<td><p><span data-ttu-id="0303d-109">Especifica el nombre del proveedor que se va a usar en la conexión.</span><span class="sxs-lookup"><span data-stu-id="0303d-109">Specifies the name of a provider to use for the connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0303d-110"><em>Nombre del archivo</em></span><span class="sxs-lookup"><span data-stu-id="0303d-110"><em>File Name</em></span></span></p></td>
<td><p><span data-ttu-id="0303d-111">Especifica el nombre de un archivo específico del proveedor (por ejemplo, un objeto de origen de datos almacenado de manera persistente) que contiene información de conexión predefinida.</span><span class="sxs-lookup"><span data-stu-id="0303d-111">Specifies the name of a provider-specific file (for example, a persisted data source object) containing preset connection information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0303d-112"><em>URL</em></span><span class="sxs-lookup"><span data-stu-id="0303d-112"><em>URL</em></span></span></p></td>
<td><p><span data-ttu-id="0303d-113">Especifica la cadena de conexión como una dirección URL absoluta que identifica un recurso, como un archivo o un directorio.</span><span class="sxs-lookup"><span data-stu-id="0303d-113">Specifies the connection string as an absolute URL identifying a resource, such as a file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0303d-114"><em>Remote Provider</em></span><span class="sxs-lookup"><span data-stu-id="0303d-114"><em>Remote Provider</em></span></span></p></td>
<td><p><span data-ttu-id="0303d-p102">Especifica el nombre del proveedor que se va a usar cuando se abre una conexión de cliente (sólo con el Servicio de datos remotos, RDS).</span><span class="sxs-lookup"><span data-stu-id="0303d-p102">Specifies the name of a provider to use when opening a client-side connection. (Remote Data Service only.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0303d-117"><em>Remote Server</em></span><span class="sxs-lookup"><span data-stu-id="0303d-117"><em>Remote Server</em></span></span></p></td>
<td><p><span data-ttu-id="0303d-p103">Especifica el nombre de la ruta de acceso del servidor que se utilizará al abrir una conexión de cliente (sólo Servicio de datos remoto).</span><span class="sxs-lookup"><span data-stu-id="0303d-p103">Specifies the path name of the server to use when opening a client-side connection. (Remote Data Service only.)</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="0303d-p104">En los ejemplos siguientes y en toda la Guía del programador de ADO, se utiliza el identificador de usuario "MyId" con la contraseña "123aBc" para autenticación en el servidor. Debe sustituir estos valores con credenciales de inicio de sesión válidas para su servidor. Sustituya también el nombre de su servidor por "MySqlServer".</span><span class="sxs-lookup"><span data-stu-id="0303d-p104">In the following examples and throughout the ADO Programmer's Guide, the user id "MyId" with a password of "123aBc" is used to authenticate against the server. You should substitute these values with valid login credentials for your server. Also, substitute the name of your server for "MySqlServer".</span></span>

<span data-ttu-id="0303d-123">La aplicación HelloData del capítulo 1 utilizó la cadena de conexión siguiente:</span><span class="sxs-lookup"><span data-stu-id="0303d-123">The HelloData application in Chapter 1 used the following connection string:</span></span>

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
```

<span data-ttu-id="0303d-124">El único parámetro de ADO que se proporcionó en esta cadena de conexión fue "Provider=SQLOLEDB ", que indicó el proveedor de Microsoft OLE DB para SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0303d-124">The only ADO parameter supplied in this connection string was "Provider=SQLOLEDB", which indicated the Microsoft OLE DB Provider for SQL Server.</span></span> <span data-ttu-id="0303d-125">Para determinar otros parámetros válidos que se pueden pasar en la cadena de conexión, se puede consultar la documentación de cada proveedor.</span><span class="sxs-lookup"><span data-stu-id="0303d-125">Other valid parameters that can be passed in the connection string can be determined by referring to individual providers' documentation.</span></span> <span data-ttu-id="0303d-126">Según el proveedor OLE DB para la documentación de SQL Server, puede sustituir "Server" para el parámetro *Data Source* y "Database" por el parámetro *Initial Catalog* .</span><span class="sxs-lookup"><span data-stu-id="0303d-126">According to the OLE DB Provider for SQL Server documentation, you can substitute "Server" for the *Data Source* parameter and "Database" for the *Initial Catalog* parameter.</span></span> <span data-ttu-id="0303d-127">Por tanto, la cadena de conexión siguiente generaría resultados idénticos a la primera:</span><span class="sxs-lookup"><span data-stu-id="0303d-127">Thus, the following connection string would produce results identical to the first:</span></span>

```vb 
 
m_sConnStr = "Provider='SQLOLEDB';Server='MySqlServer';" & _ 
 "Database='Northwind';Integrated Security='SSPI';" 
```

<span data-ttu-id="0303d-128">Para abrir la conexión, simplemente pase la cadena de conexión como primer argumento en el método **Open** del objeto **Connection**:</span><span class="sxs-lookup"><span data-stu-id="0303d-128">To open the connection, simply pass the connection string as the first argument in the **Connection** object **Open** method:</span></span>

```vb 
 
objConn.Open m_sConnStr 
```

<span data-ttu-id="0303d-p106">También es posible proporcionar una gran parte de esta información estableciendo propiedades del objeto **Connection** antes de abrir la conexión. Por ejemplo, se podría lograr el mismo efecto que con la cadena de conexión anterior utilizando el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="0303d-p106">It is also possible to supply much of this information by setting properties of the **Connection** object before opening the connection. For example, you could achieve the same effect as the connection string above by using the following code:</span></span>

```vb 
 
With objConn 
 .Provider = "SQLOLEDB" 
 .DefaultDatabase = "Northwind" 
 .Properties("Data Source") = "MySqlServer" 
 .Properties("Integrated Security") = "SSPI" 
 .Open 
End With 
```

