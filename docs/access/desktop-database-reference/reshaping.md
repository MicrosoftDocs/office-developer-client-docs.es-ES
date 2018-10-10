---
title: Forma (referencia de escritorio de la base de datos de Access)
TOCTitle: Reshaping
ms:assetid: 89c6a0d6-3bf4-36ae-26ec-d4e60f920490
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249605(v=office.15)
ms:contentKeyID: 48546174
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be9e0f8e017e91152ed876b933e0c0c01a7f355e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486820"
---
# <a name="reshaping"></a>Nuevas formas


**Se aplica a**: Access 2013 | Office 2013

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
> <P>[!NOTA] No se pueden anexar columnas a un objeto <STRONG>Recordset</STRONG> existente, crear nuevas formas para un objeto <STRONG>Recordset</STRONG> parametrizado o los objetos <STRONG>Recordset</STRONG> de cualquier cláusula COMPUTE intermedia, ni realizar operaciones de agregado en cualquier objeto <STRONG>Recordset</STRONG> descendiente del objeto <STRONG>Recordset</STRONG> que se está creando con nuevas formas. Este objeto <STRONG>Recordset</STRONG> y el nuevo comando Shape deben usar ambos el mismo objeto <A href="connection-object-ado.md">Connection</A>.</P>


