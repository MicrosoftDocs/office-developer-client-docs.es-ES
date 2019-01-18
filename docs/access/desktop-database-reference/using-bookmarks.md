---
title: Utilizar marcadores (referencia de escritorio de la base de datos de Access)
TOCTitle: Using Bookmarks
ms:assetid: fe6333ef-c9d9-1e84-2252-d27edc676e97
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250306(v=office.15)
ms:contentKeyID: 48548935
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 469d8a0cc9b644fe434770d51c21d8210c8038d0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706327"
---
# <a name="using-bookmarks"></a>Uso de marcadores


**Se aplica a**: Access 2013, Office 2013

A menudo, es útil volver directamente a un registro específico después de haberse movido por el **conjunto de registros** sin tener que desplazarse por cada registro y comparar valores. Por ejemplo, si se intenta buscar un registro mediante el método **Find** pero la búsqueda no devuelve ningún registro, se le lleva automáticamente a cualquier extremo del **conjunto de registros**. Si su proveedor los admite, se pueden utilizar marcadores para marcar la ubicación propia antes de utilizar el método **Find**, para poder regresar a esa ubicación. Un marcador es un valor de tipo **Variant** que identifica un registro de un **conjunto de registros** de forma exclusiva.

También se puede usar una matriz de marcadores variant con el método **Filter** del **conjunto de registros** para aplicar un filtro a un conjunto de registros seleccionados. Para obtener detalles acerca de esta técnica, vea Filtrar los resultados en el tema [Trabajar con objetos Recordset](working-with-recordsets.md), más adelante en este capítulo.

Se puede utilizar la propiedad **Bookmark** para obtener un marcador para un registro, o establecer el registro activo de un objeto **Recordset** en el registro identificado por un marcador válido. El código siguiente utiliza la propiedad **Bookmark** para establecer un marcador y, posteriormente, volver al registro del marcador después de moverse por otros registros. Para determinar si un **conjunto de registros** admite marcadores, use el método **Supports**.

```vb 
 
'BeginBookmarkEg 
 Dim varBookmark As Variant 
 Dim blnCanBkmrk As Boolean 
 
 objRs.Open strSQL, strConnStr, adOpenStatic, adLockOptimistic, adCmdText 
 
 If objRs.RecordCount > 4 Then 
 objRs.Move 4 ' move to the fifth record 
 blnCanBkmrk = objRs.Supports(adBookmark) 
 If blnCanBkmrk = True Then 
 varBookmark = objRs.Bookmark ' record the bookmark 
 objRs.MoveLast ' move to a different record 
 objRs.Bookmark = varBookmark ' return to the bookmarked (sixth) record 
 End If 
 End If 
'EndBookmarkEg 
```

El método [Supports](supports-method-ado.md) se describe posteriormente con más detalle.

Excepto en el caso de **conjuntos de registros** clonados, los marcadores son únicos para el **conjunto de registros** en el que se crearon, incluso si se utiliza el mismo comando. Esto significa que no se puede utilizar un **marcador** obtenido de un **conjunto de registros** para moverse al mismo registro en un segundo **conjunto de registros** abierto con el mismo comando.

