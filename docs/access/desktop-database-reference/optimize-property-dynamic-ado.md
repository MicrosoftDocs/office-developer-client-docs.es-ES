---
title: Propiedad dinámica Optimize (ADO)
TOCTitle: Optimize dynamic property (ADO)
ms:assetid: 2253b052-2d8a-f6f0-f8b8-f56e79d243de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249001(v=office.15)
ms:contentKeyID: 48543705
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 11bb7872514a828fdd97fb404f5366c35ff9a883
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288255"
---
# <a name="optimize-dynamic-property-ado"></a>Propiedad dinámica Optimize (ADO)


**Se aplica a:** Access 2013, Office 2013

Especifica si se debe crear un índice en un campo.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo **Boolean** que indica si se debe crear un índice.

## <a name="remarks"></a>Comentarios

Un índice puede mejorar el rendimiento de operaciones que buscan u ordenan valores de un objeto [Recordset](recordset-object-ado.md). El índice es interno a ADO: no es posible obtener acceso a él de forma explícita ni usarlo en la aplicación.

Para crear un índice en un campo, establezca la propiedad **Optimize** en **True**. Para eliminar el índice, establezca esta propiedad en **False**.

**Optimize** es una propiedad dinámica que se anexa a la colección [Properties](field-object-ado.md) del objeto [Field](properties-collection-ado.md) cuando la propiedad [CursorLocation](cursorlocation-property-ado.md) está establecida en **adUseClient**.

**Uso**

```vb
    Dim rs As New Recordset
    Dim fld As Field
    rs.CursorLocation = adUseClient      'Enable index creation
    rs.Fields.Append "Field1", adChar, 35, adFldIsNullable
    rs.Open
    Set fld = rs.Fields(0)
    fld.Properties("Optimize") = True    'Create an index
    fld.Properties("Optimize") = False   'Delete an index
```
