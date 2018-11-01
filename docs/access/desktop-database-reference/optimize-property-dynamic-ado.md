---
title: dinámica Optimize (propiedad, ADO)
TOCTitle: Optimize Property--Dynamic (ADO)
ms:assetid: 2253b052-2d8a-f6f0-f8b8-f56e79d243de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249001(v=office.15)
ms:contentKeyID: 48543705
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 62af17d9590b2fad39d61639a32de536f0438193
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883235"
---
# <a name="optimize-property--dynamic-ado"></a>dinámica Optimize (propiedad, ADO)


**Se aplica a**: Access 2013, Office 2013

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
