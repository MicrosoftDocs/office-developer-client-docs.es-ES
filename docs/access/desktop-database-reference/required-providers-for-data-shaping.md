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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306660"
---
# <a name="required-providers-for-data-shaping"></a>Proveedores necesarios para la creación de formas de datos

**Se aplica a:** Access 2013, Office 2013

La forma de datos requiere normalmente dos proveedores. El proveedor de servicios, [Servicio de forma de datos para OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), proporciona la funcionalidad de la forma de datos y el proveedor de datos, como el proveedor OLE DB para SQL Server, proporciona filas de datos para rellenar el objeto [Recordset](recordset-object-ado.md) con forma.

Se puede especificar el nombre del proveedor de servicios (MSDataShape) como valor de la propiedad [Provider](connection-object-ado.md) del objeto [Connection](provider-property-ado.md) o la palabra clave de la cadena de conexión "Provider=MSDataShape;".

El nombre del proveedor de datos se puede  especificar como el valor de la [](properties-collection-ado.md) propiedad dinámica Proveedor de datos, que se agrega a la colección Propiedades del objeto **Connection** mediante el Servicio de forma de datos para OLE DB o la palabra clave de cadena de conexión "**Proveedor de datos=***proveedor".*

No se requiere ningún proveedor de datos si no se rellena el objeto **Recordset** (por ejemplo, como en un objeto **Recordset** donde las columnas se crean con la palabra clave NEW). En ese caso, se debe especificar "**Data Provider=** none;".

## <a name="example"></a>Ejemplo

```vb 
 
Dim cnn As New ADODB.Connection 
cnn.Provider = "MSDataShape" 
cnn.Open "Data Provider=SQLOLEDB;Integrated Security=SSPI;Database=Northwind" 
```

