---
title: Crear conjuntos de registros jerárquicos
TOCTitle: Fabricating hierarchical Recordsets
ms:assetid: 0a6e41ba-015e-c07e-8876-1e744256b876
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248836(v=office.15)
ms:contentKeyID: 48543153
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 302ca12b96317cdb203b2091c2b2da916188175a
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943965"
---
# <a name="fabricating-hierarchical-recordsets"></a><span data-ttu-id="54b84-102">Crear conjuntos de registros jerárquicos</span><span class="sxs-lookup"><span data-stu-id="54b84-102">Fabricating hierarchical Recordsets</span></span>


<span data-ttu-id="54b84-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="54b84-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="54b84-104">En el ejemplo siguiente se muestra cómo crear un objeto Recordset jerárquico sin origen de datos subyacente mediante la gramática de forma de datos para definir las columnas de los objetos **Recordset** primarios y secundarios.</span><span class="sxs-lookup"><span data-stu-id="54b84-104">The following example shows how to fabricate a hierarchical Recordset without an underlying data source by using the data shaping grammar to define columns for parent, child, and grandchild **Recordsets**.</span></span>

<span data-ttu-id="54b84-p101">Para crear un objeto **Recordset** jerárquico, debe especificar el Servicio de forma de datos de Microsoft para OLE DB (MSDataShape) y puede especificar el valor NONE para el proveedor de datos en el parámetro de la cadena de conexión del método [Open](connection-object-ado.md) del objeto [Connection](open-method-ado-connection.md). Para obtener más información, vea [Proveedores necesarios para la forma de datos](required-providers-for-data-shaping.md).</span><span class="sxs-lookup"><span data-stu-id="54b84-p101">To fabricate a hierarchical **Recordset**, you must specify the Microsoft Data Shaping Service for OLE DB (MSDataShape), and you may specify a Data Provider value of NONE in the connection string parameter of the [Connection](connection-object-ado.md) object's [Open](open-method-ado-connection.md) method. For more information, see [Required Providers for Data Shaping](required-providers-for-data-shaping.md).</span></span>

```vb
    Dim cn As New ADODB.Connection
    Dim rsCustomers As New ADODB.Recordset
    
    cn.Open "Provider=MSDataShape;Data Provider=NONE;"
     
    strShape = _
    "SHAPE APPEND NEW adInteger AS CustID," & _
                " NEW adChar(25) AS FirstName," & _
                " NEW adChar(25) AS LastName," & _
                " NEW adChar(12) AS SSN," & _
                " NEW adChar(50) AS Address," & _
             " ((SHAPE APPEND NEW adChar(80) AS VIN_NO," & _
                            " NEW adInteger AS CustID," & _
                            " NEW adChar(20) AS BodyColor, " & _
                         " ((SHAPE APPEND NEW adChar(80) AS VIN_NO," & _
                                        " NEW adChar(20) AS Make, " & _
                                        " NEW adChar(20) AS Model," & _
                                        " NEW adChar(4) AS Year) " & _
                            " AS VINS RELATE VIN_NO TO VIN_NO))" & _
                " AS Vehicles RELATE CustID TO CustID) "
     
    rsCustomers.Open strShape, cn, adOpenStatic, adLockOptimistic, -1
```

<span data-ttu-id="54b84-107">Una vez creado el **objeto Recordset** , puede ser rellena, manipular o almacenar en un archivo.</span><span class="sxs-lookup"><span data-stu-id="54b84-107">After the **Recordset** has been fabricated, it can be populated, manipulated, or persisted to a file.</span></span>

