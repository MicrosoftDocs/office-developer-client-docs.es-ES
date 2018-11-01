---
title: Servicio de forma de datos de Microsoft para OLE DB (proveedor de servicios ADO)
TOCTitle: Microsoft Data Shaping Service for OLE DB (ADO Service Provider)
ms:assetid: 6e6e5f39-6f43-7c7b-5812-796096d1d31b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249436(v=office.15)
ms:contentKeyID: 48545511
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9f18ae0a218adb65d453c3f54eb7af43af68097c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870726"
---
# <a name="microsoft-data-shaping-service-for-ole-db-ado-service-provider"></a><span data-ttu-id="d303f-102">Servicio de forma de datos de Microsoft para OLE DB (proveedor de servicios ADO)</span><span class="sxs-lookup"><span data-stu-id="d303f-102">Microsoft Data Shaping Service for OLE DB (ADO Service Provider)</span></span>


<span data-ttu-id="d303f-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d303f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d303f-104">El proveedor de servicios del Servicio de forma de datos de Microsoft para OLE DB admite la construcción de objetos [Recordset](recordset-object-ado.md) jerárquicos (con forma) desde un proveedor de datos.</span><span class="sxs-lookup"><span data-stu-id="d303f-104">The Microsoft Data Shaping Service for OLE DB service provider supports the construction of hierarchical (shaped) [Recordset](recordset-object-ado.md) objects from a data provider.</span></span>

## <a name="provider-keyword"></a><span data-ttu-id="d303f-105">Palabra clave del proveedor</span><span class="sxs-lookup"><span data-stu-id="d303f-105">Provider Keyword</span></span>

<span data-ttu-id="d303f-106">Para llamar al Servicio de forma de datos para OLE DB, especifique la siguiente palabra clave y el siguiente valor en la cadena de conexión.</span><span class="sxs-lookup"><span data-stu-id="d303f-106">To invoke the Data Shaping Service for OLE DB, specify the following keyword and value in the connection string.</span></span>

```vb 
 
"Provider=MSDataShape" 
```

## <a name="dynamic-properties"></a><span data-ttu-id="d303f-107">Propiedades dinámicas</span><span class="sxs-lookup"><span data-stu-id="d303f-107">Dynamic Properties</span></span>

<span data-ttu-id="d303f-108">Cuando se llama a este proveedor de servicios, se agregan las siguientes propiedades dinámicas a la colección [Properties](connection-object-ado.md) del objeto [Connection](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d303f-108">When this service provider is invoked, the following dynamic properties are added to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d303f-109">Nombre de la propiedad dinámica</span><span class="sxs-lookup"><span data-stu-id="d303f-109">Dynamic Property Name</span></span></p></th>
<th><p><span data-ttu-id="d303f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d303f-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d303f-111"><strong>Unique Reshape Names</strong></span><span class="sxs-lookup"><span data-stu-id="d303f-111"><strong>Unique Reshape Names</strong></span></span></p></td>
<td><p><span data-ttu-id="d303f-112">Indica si se permiten los objetos <strong>Recordset</strong> con valores duplicados para sus propiedades <strong>Reshape Name</strong> .</span><span class="sxs-lookup"><span data-stu-id="d303f-112">Indicates whether <strong>Recordset</strong> objects with duplicate values for their <strong>Reshape Name</strong> properties are allowed.</span></span> <span data-ttu-id="d303f-113">Si esta propiedad dinámica es <strong>True</strong> y se crea un nuevo <strong>objeto Recordset</strong> con el mismo especificada por el usuario cambiar la forma de nombre como un <strong>conjunto de registros</strong>de existentes, a continuación, el nuevo <strong>conjunto de registros de</strong> nombre del objeto reshape se modifica para que sea único.</span><span class="sxs-lookup"><span data-stu-id="d303f-113">If this dynamic property is <strong>True</strong> and a new <strong>Recordset</strong> is created with the same user-specified reshape name as an existing <strong>Recordset</strong>, then the new <strong>Recordset</strong> object's reshape name is modified to make it unique.</span></span> <span data-ttu-id="d303f-114">Si esta propiedad es <strong>False</strong> y se crea un nuevo <strong>objeto Recordset</strong> con el mismo especificada por el usuario cambiar la forma de nombre como <strong>objeto Recordset</strong>existente, ambos objetos <strong>Recordset</strong> tendrá el mismo nombre cambiar la forma.</span><span class="sxs-lookup"><span data-stu-id="d303f-114">If this property is <strong>False</strong> and a new <strong>Recordset</strong> is created with the same user-specified reshape name as the existing <strong>Recordset</strong>, both <strong>Recordset</strong> objects will have the same reshape name.</span></span> <span data-ttu-id="d303f-115">Por lo tanto, puede cambiarse ni <strong>Recordset</strong> mientras existan ambos conjuntos de registros.</span><span class="sxs-lookup"><span data-stu-id="d303f-115">Therefore, neither <strong>Recordset</strong> can be reshaped as long as both recordsets exist.</span></span> <span data-ttu-id="d303f-116">El valor predeterminado de la propiedad es <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="d303f-116">The default value of the property is <strong>False</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d303f-117"><strong>Data Provider</strong></span><span class="sxs-lookup"><span data-stu-id="d303f-117"><strong>Data Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="d303f-p102">Indica el nombre del proveedor que suministrará las filas a las que se les va a aplicar forma. Este valor puede ser NONE si no se va a utilizar un proveedor para suministrar filas.</span><span class="sxs-lookup"><span data-stu-id="d303f-p102">Indicates the name of the provider that will supply rows to be shaped. This value may be NONE if a provider will not be used to supply rows.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d303f-p103">También es posible establecer propiedades dinámicas que se pueden escribir si se especifican sus nombres como palabras clave en la cadena de conexión. Por ejemplo, en Microsoft Visual Basic, establezca la propiedad dinámica **Data Provider** en "MSDASQL" al especificar:</span><span class="sxs-lookup"><span data-stu-id="d303f-p103">You may also set writable dynamic properties by specifying their names as keywords in the connection string. For example, in Microsoft Visual Basic, set the **Data Provider** dynamic property to "MSDASQL" by specifying:</span></span>

```vb 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MSDataShape;Data Provider=MSDASQL" 
```

<span data-ttu-id="d303f-p104">También es posible establecer o recuperar una propiedad dinámica al especificar su nombre como índice de la propiedad [Properties](properties-collection-ado.md). Por ejemplo, obtenga e imprima el valor actual de la propiedad dinámica **Data Provider** y, a continuación, establezca un nuevo valor como éste:</span><span class="sxs-lookup"><span data-stu-id="d303f-p104">You may also set or retrieve a dynamic property by specifying its name as the index to the [Properties](properties-collection-ado.md) property. For example, get and print the current value of the **Data Provider** dynamic property, then set a new value, like this:</span></span>

```vb 
 
Debug.Print cn.Properties("Data Provider") 
cn.Properties("Data Provider") = "MSDASQL" 
```

<span data-ttu-id="d303f-124">Para obtener más información acerca de la forma de datos, vea [Forma de datos](data-shaping.md).</span><span class="sxs-lookup"><span data-stu-id="d303f-124">For more information about data shaping, see [Data Shaping](data-shaping.md).</span></span>

