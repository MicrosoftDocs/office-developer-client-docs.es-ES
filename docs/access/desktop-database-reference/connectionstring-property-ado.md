---
title: ConnectionString (propiedad, ADO)
TOCTitle: ConnectionString property (ADO)
ms:assetid: c67a7daf-258f-d99d-6475-a4aa98d1e99d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249968(v=office.15)
ms:contentKeyID: 48547627
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3612652f3473c0794dbfe9be60f84ea2e3fee252
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712732"
---
# <a name="connectionstring-property-ado"></a><span data-ttu-id="a153c-102">ConnectionString (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="a153c-102">ConnectionString property (ADO)</span></span>


<span data-ttu-id="a153c-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a153c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a153c-104">Indica la información utilizada para establecer una conexión con un origen de datos.</span><span class="sxs-lookup"><span data-stu-id="a153c-104">Indicates the information used to establish a connection to a data source.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="a153c-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="a153c-105">Settings and return values</span></span>

<span data-ttu-id="a153c-106">Establece o devuelve un valor de tipo **String**.</span><span class="sxs-lookup"><span data-stu-id="a153c-106">Sets or returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a153c-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a153c-107">Remarks</span></span>

<span data-ttu-id="a153c-108">Utilice la propiedad **ConnectionString** para especificar un origen de datos pasando una cadena de conexión detallada que contiene una serie de instrucciones de *argumento* *= valor* separadas por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="a153c-108">Use the **ConnectionString** property to specify a data source by passing a detailed connection string containing a series of *argument* *= value* statements separated by semicolons.</span></span>

<span data-ttu-id="a153c-p101">ADO admite cinco argumentos para la propiedad **ConnectionString**; todos los demás argumentos pasan directamente al proveedor sin que ADO los procese. Los argumentos admitidos por ADO son:</span><span class="sxs-lookup"><span data-stu-id="a153c-p101">ADO supports five arguments for the **ConnectionString** property; any other arguments pass directly to the provider without any processing by ADO. The arguments ADO supports are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a153c-111">Argumento</span><span class="sxs-lookup"><span data-stu-id="a153c-111">Argument</span></span></p></th>
<th><p><span data-ttu-id="a153c-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="a153c-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a153c-113"><em>Provider=</em></span><span class="sxs-lookup"><span data-stu-id="a153c-113"><em>Provider=</em></span></span></p></td>
<td><p><span data-ttu-id="a153c-114">Especifica el nombre del proveedor que se va a usar en la conexión.</span><span class="sxs-lookup"><span data-stu-id="a153c-114">Specifies the name of a provider to use for the connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a153c-115"><em>Nombre de archivo =</em></span><span class="sxs-lookup"><span data-stu-id="a153c-115"><em>File Name=</em></span></span></p></td>
<td><p><span data-ttu-id="a153c-116">Especifica el nombre de un archivo específico del proveedor (por ejemplo, un objeto de origen de datos almacenado de manera persistente) que contiene información de conexión predefinida.</span><span class="sxs-lookup"><span data-stu-id="a153c-116">Specifies the name of a provider-specific file (for example, a persisted data source object) containing preset connection information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a153c-117"><em>Proveedor remoto =</em></span><span class="sxs-lookup"><span data-stu-id="a153c-117"><em>Remote Provider=</em></span></span></p></td>
<td><p><span data-ttu-id="a153c-p102">Especifica el nombre del proveedor que se va a usar cuando se abre una conexión de cliente (sólo con el Servicio de datos remotos, RDS).</span><span class="sxs-lookup"><span data-stu-id="a153c-p102">Specifies the name of a provider to use when opening a client-side connection. (Remote Data Service only.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a153c-120"><em>Servidor remoto =</em></span><span class="sxs-lookup"><span data-stu-id="a153c-120"><em>Remote Server=</em></span></span></p></td>
<td><p><span data-ttu-id="a153c-p103">Especifica el nombre de la ruta de acceso del servidor que se utilizará al abrir una conexión de cliente. (Sólo con el Servicio de datos remotos, RDS.)</span><span class="sxs-lookup"><span data-stu-id="a153c-p103">Specifies the path name of the server to use when opening a client-side connection. (Remote Data Service only.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a153c-123"><em>URL=</em></span><span class="sxs-lookup"><span data-stu-id="a153c-123"><em>URL=</em></span></span></p></td>
<td><p><span data-ttu-id="a153c-124">Especifica la cadena de conexión como una dirección URL absoluta que identifica un recurso, como un archivo o un directorio.</span><span class="sxs-lookup"><span data-stu-id="a153c-124">Specifies the connection string as an absolute URL identifying a resource, such as a file or directory.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a153c-125">Después de que se establezca el valor de la propiedad **ConnectionString** y se abra el objeto [Connection](connection-object-ado.md), puede que el proveedor modifique el contenido de la propiedad, por ejemplo, mediante la asignación de los nombres de argumento definidos por ADO a sus propios equivalentes.</span><span class="sxs-lookup"><span data-stu-id="a153c-125">After you set the **ConnectionString** property and open the [Connection](connection-object-ado.md) object, the provider may alter the contents of the property, for example, by mapping the ADO-defined argument names to their provider equivalents.</span></span>

<span data-ttu-id="a153c-126">La propiedad **ConnectionString** hereda automáticamente el valor utilizado para el argumento *ConnectionString* del método [Open](open-method-ado-connection.md) , por lo que se puede reemplazar la actual propiedad **ConnectionString** durante la llamada al método **Open** .</span><span class="sxs-lookup"><span data-stu-id="a153c-126">The **ConnectionString** property automatically inherits the value used for the *ConnectionString* argument of the [Open](open-method-ado-connection.md) method, so you can override the current **ConnectionString** property during the **Open** method call.</span></span>

<span data-ttu-id="a153c-127">Debido a que el argumento de *Nombre de archivo* hace que ADO cargue el proveedor asociado, no se puede pasar el *proveedor* y el *Nombre de archivo* de argumentos.</span><span class="sxs-lookup"><span data-stu-id="a153c-127">Because the *File Name* argument causes ADO to load the associated provider, you cannot pass both the *Provider* and *File Name* arguments.</span></span>

<span data-ttu-id="a153c-128">La propiedad **ConnectionString** es de lectura y escritura cuando está cerrada la conexión, y es de sólo lectura cuando la conexión está abierta.</span><span class="sxs-lookup"><span data-stu-id="a153c-128">The **ConnectionString** property is read/write when the connection is closed and read-only when it is open.</span></span>

<span data-ttu-id="a153c-p104">Se omiten los duplicados de un argumento en la propiedad **ConnectionString**. Se utiliza la última instancia de los argumentos.</span><span class="sxs-lookup"><span data-stu-id="a153c-p104">Duplicates of an argument in the **ConnectionString** property are ignored. The last instance of any argument is used.</span></span>

<span data-ttu-id="a153c-131">**Uso de servicio de datos remotos** Cuando se utiliza en un objeto **Connection** de cliente, la propiedad **ConnectionString** puede incluir sólo los parámetros *Remote Provider* y *Remote Server* .</span><span class="sxs-lookup"><span data-stu-id="a153c-131">**Remote Data Service Usage**When used on a client-side **Connection** object, the **ConnectionString** property can include only the *Remote Provider* and *Remote Server* parameters.</span></span>

