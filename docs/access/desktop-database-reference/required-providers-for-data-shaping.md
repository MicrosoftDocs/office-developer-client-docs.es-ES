---
title: Proveedores necesarios para la forma de datos
TOCTitle: Required providers for data shaping
ms:assetid: eb8933fb-d533-3ea7-e045-35c1ca585765
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250194(v=office.15)
ms:contentKeyID: 48548488
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fd4460b96cf222a9c6e4f7a8ea66ed22c0f2ff10
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947640"
---
# <a name="required-providers-for-data-shaping"></a>Proveedores necesarios para la forma de datos

**Se aplica a**: Access 2013, Office 2013

La forma de datos requiere normalmente dos proveedores. El proveedor de servicios, [Servicio de forma de datos para OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), proporciona la funcionalidad de la forma de datos y el proveedor de datos, como el proveedor OLE DB para SQL Server, proporciona filas de datos para rellenar el objeto [Recordset](recordset-object-ado.md) con forma.

Se puede especificar el nombre del proveedor de servicios (MSDataShape) como valor de la propiedad [Provider](connection-object-ado.md) del objeto [Connection](provider-property-ado.md) o la palabra clave de la cadena de conexión "Provider=MSDataShape;".

Se puede especificar el nombre del proveedor de datos como el valor de la propiedad dinámica de **Proveedor de datos** , que se agrega a la colección [Properties](properties-collection-ado.md) del objeto **Connection** por el servicio de forma de datos para OLE DB, o la palabra clave de cadena de conexión "* *Proveedor de datos = *** proveedor*".

No se requiere ningún proveedor de datos si no se rellena el objeto **Recordset** (por ejemplo, como en un objeto **Recordset** donde las columnas se crean con la palabra clave NEW). En ese caso, se debe especificar "**Data Provider=** none;".

## <a name="example"></a>Ejemplo

```vb 
 
Dim cnn As New ADODB.Connection 
cnn.Provider = "MSDataShape" 
cnn.Open "Data Provider=SQLOLEDB;Integrated Security=SSPI;Database=Northwind" 
```

