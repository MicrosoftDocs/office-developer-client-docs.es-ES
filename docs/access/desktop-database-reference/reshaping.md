---
title: Forma (referencia de escritorio de la base de datos de Access)
TOCTitle: Reshaping
ms:assetid: 89c6a0d6-3bf4-36ae-26ec-d4e60f920490
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249605(v=office.15)
ms:contentKeyID: 48546174
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c820e82669789d7c3806cc1fd38a2eb6844b722e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711906"
---
# <a name="reshaping"></a>Cambio de forma

**Se aplica a**: Access 2013, Office 2013

A un objeto **Recordset** creado mediante una cláusula de un comando Shape se le puede asignar un nombre de *alias* (normalmente con la palabra clave AS). Se puede usar un comando totalmente diferente para hacer referencia al alias de un objeto **Recordset** con forma. Es decir, se puede volver a utilizar, o *crear con nuevas formas*, un objeto **Recordset** al que se aplicó forma anteriormente, en un nuevo comando Shape. Para admitir esta característica, ADO proporciona una propiedad [Reshape Name](reshape-name-property-dynamic-ado.md).

Las nuevas formas cumplen dos funciones principales. La primera es asociar un objeto **Recordset** existente a un nuevo objeto **Recordset** principal.

## <a name="example"></a>Ejemplo

```vb 
 
. . . 
rs1.Open "SHAPE {select * from Customers} " & _ 
 "APPEND ({select * from Orders} AS chapOrders " & _ 
 "RELATE CustomerID to CustomerID)", cn 
 
rs2.Open "SHAPE {select * from Employees} " & _ 
 "APPEND (chapOrders RELATE EmployeeID to EmployeeID)", cn 
. . . 
```

La segunda función consiste en habilitar el acceso no estructurado en capítulos en los objetos **Recordset** secundarios existentes, mediante la sintaxis `"SHAPE <recordset reshape name>"`.

> [!NOTE]
> [!NOTA] No se pueden anexar columnas a un objeto **Recordset** existente, crear nuevas formas para un objeto **Recordset** parametrizado o los objetos **Recordset** de cualquier cláusula COMPUTE intermedia, ni realizar operaciones de agregado en cualquier objeto **Recordset** descendiente del objeto **Recordset** que se está creando con nuevas formas. El **conjunto de registros** que se va a cambiar la forma y la nueva forma de comando deben utilizar ambos el mismo ** objeto[Connection](connection-object-ado.md) .


