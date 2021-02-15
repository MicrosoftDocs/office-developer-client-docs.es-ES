---
title: Fabricación de conjuntos de registros jerárquicos
TOCTitle: Fabricating hierarchical Recordsets
ms:assetid: 0a6e41ba-015e-c07e-8876-1e744256b876
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248836(v=office.15)
ms:contentKeyID: 48543153
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f644f25a04c5573a93aa106884473fed6b45440e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293206"
---
# <a name="fabricating-hierarchical-recordsets"></a>Fabricación de conjuntos de registros jerárquicos


**Se aplica a:** Access 2013, Office 2013

En el ejemplo siguiente se muestra cómo crear un objeto Recordset jerárquico sin origen de datos subyacente mediante la gramática de forma de datos para definir las columnas de los objetos **Recordset** primarios y secundarios.

Para crear un objeto **Recordset** jerárquico, debe especificar el Servicio de forma de datos de Microsoft para OLE DB (MSDataShape) y puede especificar el valor NONE para el proveedor de datos en el parámetro de la cadena de conexión del método [Open](connection-object-ado.md) del objeto [Connection](open-method-ado-connection.md). Para obtener más información, vea [Proveedores necesarios para la forma de datos](required-providers-for-data-shaping.md).

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

Una vez **que se** ha diseñado el conjunto de registros, se puede rellenar, manipular o conservar en un archivo.

