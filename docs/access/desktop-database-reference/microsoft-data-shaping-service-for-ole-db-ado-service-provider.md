---
title: Servicio de forma de datos de Microsoft para OLE DB (proveedor de servicios ADO)
TOCTitle: Microsoft Data Shaping Service for OLE DB (ADO Service Provider)
ms:assetid: 6e6e5f39-6f43-7c7b-5812-796096d1d31b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249436(v=office.15)
ms:contentKeyID: 48545511
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5065b966608f8d6a3ef1cb05be890b9a1f147dc8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288963"
---
# <a name="microsoft-data-shaping-service-for-ole-db-ado-service-provider"></a><span data-ttu-id="a9966-102">Servicio de forma de datos de Microsoft para OLE DB (proveedor de servicios ADO)</span><span class="sxs-lookup"><span data-stu-id="a9966-102">Microsoft Data Shaping Service for OLE DB (ADO Service Provider)</span></span>


<span data-ttu-id="a9966-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a9966-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a9966-104">El proveedor de servicios del Servicio de forma de datos de Microsoft para OLE DB admite la construcción de objetos [Recordset](recordset-object-ado.md) jerárquicos (con forma) desde un proveedor de datos.</span><span class="sxs-lookup"><span data-stu-id="a9966-104">The Microsoft Data Shaping Service for OLE DB service provider supports the construction of hierarchical (shaped) [Recordset](recordset-object-ado.md) objects from a data provider.</span></span>

## <a name="provider-keyword"></a><span data-ttu-id="a9966-105">Palabra clave del proveedor</span><span class="sxs-lookup"><span data-stu-id="a9966-105">Provider Keyword</span></span>

<span data-ttu-id="a9966-106">Para llamar al Servicio de forma de datos para OLE DB, especifique la siguiente palabra clave y el siguiente valor en la cadena de conexión.</span><span class="sxs-lookup"><span data-stu-id="a9966-106">To invoke the Data Shaping Service for OLE DB, specify the following keyword and value in the connection string.</span></span>

```vb 
 
"Provider=MSDataShape" 
```

## <a name="dynamic-properties"></a><span data-ttu-id="a9966-107">Propiedades dinámicas</span><span class="sxs-lookup"><span data-stu-id="a9966-107">Dynamic Properties</span></span>

<span data-ttu-id="a9966-108">Cuando se llama a este proveedor de servicios, se agregan las siguientes propiedades dinámicas a la colección [Properties](connection-object-ado.md) del objeto [Connection](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a9966-108">When this service provider is invoked, the following dynamic properties are added to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a9966-109">Nombre de la propiedad dinámica</span><span class="sxs-lookup"><span data-stu-id="a9966-109">Dynamic Property Name</span></span></p></th>
<th><p><span data-ttu-id="a9966-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9966-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9966-111"><strong>Unique Reshape Names</strong></span><span class="sxs-lookup"><span data-stu-id="a9966-111"><strong>Unique Reshape Names</strong></span></span></p></td>
<td><p><span data-ttu-id="a9966-112">Indica si se permiten los objetos <strong>Recordset</strong> con valores duplicados para sus propiedades <strong>Reshape Name</strong>.</span><span class="sxs-lookup"><span data-stu-id="a9966-112">Indicates whether <strong>Recordset</strong> objects with duplicate values for their <strong>Reshape Name</strong> properties are allowed.</span></span> <span data-ttu-id="a9966-113">Si esta propiedad dinámica es <strong>True</strong> y se crea un nuevo objeto <strong>Recordset</strong> con el mismo nombre de cambio de forma especificado por el usuario que un objeto <strong>Recordset</strong> existente, el nombre de cambio de forma del nuevo objeto <strong>Recordset</strong> se modifica para hacerlo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="a9966-113">If this dynamic property is <strong>True</strong> and a new <strong>Recordset</strong> is created with the same user-specified reshape name as an existing <strong>Recordset</strong>, then the new <strong>Recordset</strong> object's reshape name is modified to make it unique.</span></span> <span data-ttu-id="a9966-114">Si esta propiedad es <strong>False</strong> y se crea un nuevo objeto <strong>Recordset</strong> con el mismo nombre de cambio de forma especificado por el usuario que el objeto <strong>Recordset</strong> existente, ambos objetos <strong>Recordset</strong> tendrán el mismo nombre de cambio de forma.</span><span class="sxs-lookup"><span data-stu-id="a9966-114">If this property is <strong>False</strong> and a new <strong>Recordset</strong> is created with the same user-specified reshape name as the existing <strong>Recordset</strong>, both <strong>Recordset</strong> objects will have the same reshape name.</span></span> <span data-ttu-id="a9966-115">Por lo tanto, no será posible cambiar la forma de ninguno de los objetos <strong>Recordset</strong> mientras existan ambos.</span><span class="sxs-lookup"><span data-stu-id="a9966-115">Therefore, neither <strong>Recordset</strong> can be reshaped as long as both recordsets exist.</span></span> <span data-ttu-id="a9966-116">El valor predeterminado de la propiedad es <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="a9966-116">The default value of the property is <strong>False</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9966-117"><strong>Data Provider</strong></span><span class="sxs-lookup"><span data-stu-id="a9966-117"><strong>Data Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="a9966-p102">Indica el nombre del proveedor que suministrará las filas a las que se les va a aplicar forma. Este valor puede ser NONE si no se va a utilizar un proveedor para suministrar filas.</span><span class="sxs-lookup"><span data-stu-id="a9966-p102">Indicates the name of the provider that will supply rows to be shaped. This value may be NONE if a provider will not be used to supply rows.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a9966-p103">También es posible establecer propiedades dinámicas que se pueden escribir si se especifican sus nombres como palabras clave en la cadena de conexión. Por ejemplo, en Microsoft Visual Basic, establezca la propiedad dinámica **Data Provider** en "MSDASQL" al especificar:</span><span class="sxs-lookup"><span data-stu-id="a9966-p103">You may also set writable dynamic properties by specifying their names as keywords in the connection string. For example, in Microsoft Visual Basic, set the **Data Provider** dynamic property to "MSDASQL" by specifying:</span></span>

```vb 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MSDataShape;Data Provider=MSDASQL" 
```

<span data-ttu-id="a9966-p104">También es posible establecer o recuperar una propiedad dinámica al especificar su nombre como índice de la propiedad [Properties](properties-collection-ado.md). Por ejemplo, obtenga e imprima el valor actual de la propiedad dinámica **Data Provider** y, a continuación, establezca un nuevo valor como éste:</span><span class="sxs-lookup"><span data-stu-id="a9966-p104">You may also set or retrieve a dynamic property by specifying its name as the index to the [Properties](properties-collection-ado.md) property. For example, get and print the current value of the **Data Provider** dynamic property, then set a new value, like this:</span></span>

```vb 
 
Debug.Print cn.Properties("Data Provider") 
cn.Properties("Data Provider") = "MSDASQL" 
```

<span data-ttu-id="a9966-124">Para obtener más información acerca de la forma de datos, vea [Forma de datos](data-shaping.md).</span><span class="sxs-lookup"><span data-stu-id="a9966-124">For more information about data shaping, see [Data Shaping](data-shaping.md).</span></span>

