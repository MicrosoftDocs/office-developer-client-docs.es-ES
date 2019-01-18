---
title: Proveedores necesarios para la creación de formas de datos
TOCTitle: Required providers for data shaping
ms:assetid: eb8933fb-d533-3ea7-e045-35c1ca585765
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250194(v=office.15)
ms:contentKeyID: 48548488
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ffb45599c01121204fe036cfdf60f17865388cd4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706677"
---
# <a name="required-providers-for-data-shaping"></a><span data-ttu-id="f2506-102">Proveedores necesarios para la creación de formas de datos</span><span class="sxs-lookup"><span data-stu-id="f2506-102">Required providers for data shaping</span></span>

<span data-ttu-id="f2506-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f2506-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f2506-p101">La forma de datos requiere normalmente dos proveedores. El proveedor de servicios, [Servicio de forma de datos para OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), proporciona la funcionalidad de la forma de datos y el proveedor de datos, como el proveedor OLE DB para SQL Server, proporciona filas de datos para rellenar el objeto [Recordset](recordset-object-ado.md) con forma.</span><span class="sxs-lookup"><span data-stu-id="f2506-p101">Data shaping typically requires two providers. The service provider, [Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), supplies the data shaping functionality, and a data provider, such as the OLE DB Provider for SQL Server, supplies rows of data to populate the shaped [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="f2506-106">Se puede especificar el nombre del proveedor de servicios (MSDataShape) como valor de la propiedad [Provider](connection-object-ado.md) del objeto [Connection](provider-property-ado.md) o la palabra clave de la cadena de conexión "Provider=MSDataShape;".</span><span class="sxs-lookup"><span data-stu-id="f2506-106">The name of the service provider (MSDataShape) can be specified as the value of the [Connection](connection-object-ado.md) object [Provider](provider-property-ado.md) property or the connection string keyword "Provider=MSDataShape;".</span></span>

<span data-ttu-id="f2506-107">Se puede especificar el nombre del proveedor de datos como el valor de la propiedad dinámica de **Proveedor de datos** , que se agrega a la colección [Properties](properties-collection-ado.md) del objeto **Connection** por el servicio de forma de datos para OLE DB, o la palabra clave de cadena de conexión "\* *Proveedor de datos = \*\*\* proveedor*".</span><span class="sxs-lookup"><span data-stu-id="f2506-107">The name of the data provider can be specified as the value of the **Data Provider** dynamic property, which is added to the **Connection** object [Properties](properties-collection-ado.md) collection by the Data Shaping Service for OLE DB, or the connection string keyword "\**Data Provider=\*\*\*provider*".</span></span>

<span data-ttu-id="f2506-p102">No se requiere ningún proveedor de datos si no se rellena el objeto **Recordset** (por ejemplo, como en un objeto **Recordset** donde las columnas se crean con la palabra clave NEW). En ese caso, se debe especificar "**Data Provider=** none;".</span><span class="sxs-lookup"><span data-stu-id="f2506-p102">No data provider is required if the **Recordset** is not populated (for example, as in a fabricated **Recordset** where columns are created with the NEW keyword). In that case, specify "**Data Provider=** none;".</span></span>

## <a name="example"></a><span data-ttu-id="f2506-110">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f2506-110">Example</span></span>

```vb 
 
Dim cnn As New ADODB.Connection 
cnn.Provider = "MSDataShape" 
cnn.Open "Data Provider=SQLOLEDB;Integrated Security=SSPI;Database=Northwind" 
```

