---
title: Utilizar marcadores (referencia de escritorio de la base de datos de Access)
TOCTitle: Using Bookmarks
ms:assetid: fe6333ef-c9d9-1e84-2252-d27edc676e97
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250306(v=office.15)
ms:contentKeyID: 48548935
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9c362e87f3e962586c2bd821bd6facb35966a77f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886840"
---
# <a name="using-bookmarks"></a><span data-ttu-id="0f77a-102">Uso de marcadores</span><span class="sxs-lookup"><span data-stu-id="0f77a-102">Using Bookmarks</span></span>


<span data-ttu-id="0f77a-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0f77a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0f77a-p101">A menudo, es útil volver directamente a un registro específico después de haberse movido por el **conjunto de registros** sin tener que desplazarse por cada registro y comparar valores. Por ejemplo, si se intenta buscar un registro mediante el método **Find** pero la búsqueda no devuelve ningún registro, se le lleva automáticamente a cualquier extremo del **conjunto de registros**. Si su proveedor los admite, se pueden utilizar marcadores para marcar la ubicación propia antes de utilizar el método **Find**, para poder regresar a esa ubicación. Un marcador es un valor de tipo **Variant** que identifica un registro de un **conjunto de registros** de forma exclusiva.</span><span class="sxs-lookup"><span data-stu-id="0f77a-p101">It is often useful to return directly to a specific record after having moved around in the **Recordset** without having to scroll through every record and compare values. For example, if you attempt to search for a record using the **Find** method but the search returns no records, you are automatically placed at either end of the **Recordset**. If your provider supports them, bookmarks can be used to mark your place before using the **Find** method so you can return to your location. A bookmark is a **Variant** type value that uniquely identifies a record in a **Recordset** object.</span></span>

<span data-ttu-id="0f77a-p102">También se puede usar una matriz de marcadores variant con el método **Filter** del **conjunto de registros** para aplicar un filtro a un conjunto de registros seleccionados. Para obtener detalles acerca de esta técnica, vea Filtrar los resultados en el tema [Trabajar con objetos Recordset](working-with-recordsets.md), más adelante en este capítulo.</span><span class="sxs-lookup"><span data-stu-id="0f77a-p102">You can also use a variant array of bookmarks with the **Recordset** **Filter** method to filter on a selected set of records. For details about this technique, see Filtering the Results in the topic, [Working with Recordsets](working-with-recordsets.md), later in this chapter.</span></span>

<span data-ttu-id="0f77a-p103">Se puede utilizar la propiedad **Bookmark** para obtener un marcador para un registro, o establecer el registro activo de un objeto **Recordset** en el registro identificado por un marcador válido. El código siguiente utiliza la propiedad **Bookmark** para establecer un marcador y, posteriormente, volver al registro del marcador después de moverse por otros registros. Para determinar si un **conjunto de registros** admite marcadores, use el método **Supports**.</span><span class="sxs-lookup"><span data-stu-id="0f77a-p103">You can use the **Bookmark** property to get a bookmark for a record, or set the current record in a **Recordset** object to the record identified by a valid bookmark. The following code uses the **Bookmark** property to set a bookmark and then return to the bookmarked record after moving on to other records. To determine if your **Recordset** supports bookmarks, use the **Supports** method.</span></span>

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

<span data-ttu-id="0f77a-113">El método [Supports](supports-method-ado.md) se describe posteriormente con más detalle.</span><span class="sxs-lookup"><span data-stu-id="0f77a-113">The [Supports](supports-method-ado.md) method is covered in more detail later.</span></span>

<span data-ttu-id="0f77a-p104">Excepto en el caso de **conjuntos de registros** clonados, los marcadores son únicos para el **conjunto de registros** en el que se crearon, incluso si se utiliza el mismo comando. Esto significa que no se puede utilizar un **marcador** obtenido de un **conjunto de registros** para moverse al mismo registro en un segundo **conjunto de registros** abierto con el mismo comando.</span><span class="sxs-lookup"><span data-stu-id="0f77a-p104">Except for the case of cloned **Recordsets**, bookmarks are unique to the **Recordset** in which they were created, even if the same command is used. This means that you cannot use a **Bookmark** obtained from one **Recordset** to move to the same record in a second **Recordset** opened with the same command.</span></span>

