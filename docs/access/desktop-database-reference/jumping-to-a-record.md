---
title: Salto a un registro
TOCTitle: Jumping to a record
ms:assetid: 27177bbe-066c-aeb0-6dfd-45d8c2a87487
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249033(v=office.15)
ms:contentKeyID: 48543829
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 08d8a3d7b3d6012867a91aa306f45872bfebb2e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290789"
---
# <a name="jumping-to-a-record"></a><span data-ttu-id="a8af6-102">Salto a un registro</span><span class="sxs-lookup"><span data-stu-id="a8af6-102">Jumping to a record</span></span>


<span data-ttu-id="a8af6-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a8af6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a8af6-104">El método [Move](move-method-ado.md) permite avanzar o retroceder un número determinado de registros en el **conjunto de registros** utilizando la sintaxis siguiente:</span><span class="sxs-lookup"><span data-stu-id="a8af6-104">The [Move](move-method-ado.md) method allows you to move forward or backward in the **Recordset** a specified number of records by using the following syntax:</span></span>

```vb 
 
oRs.Move NumRecords, Start
```

<span data-ttu-id="a8af6-105">El método **Move** se admite en todos los objetos **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="a8af6-105">The **Move** method is supported on all **Recordset** objects.</span></span>

<span data-ttu-id="a8af6-p101">Si el argumento *NumRecords* es mayor que cero, la posición de registro activo avanza (hacia el final del **conjunto de registros**). Si *NumRecords* es menor que cero, la posición de registro activo retrocede (hacia el principio del **conjunto de registros**).</span><span class="sxs-lookup"><span data-stu-id="a8af6-p101">If the *NumRecords* argument is greater than zero, the current record position moves forward (toward the end of the **Recordset**). If *NumRecords* is less than zero, the current record position moves backward (toward the beginning of the **Recordset**).</span></span>

<span data-ttu-id="a8af6-p102">Si la llamada a **Move** moviese la posición del registro activo a un punto anterior al primer registro, ADO establecería el registro activo en la posición anterior al primer registro del **conjunto de registros** (**BOF** es **True**). Si se intenta retroceder cuando la propiedad **BOF** ya es **True**, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="a8af6-p102">If the **Move** call would move the current record position to a point before the first record, ADO sets the current record to the position before the first record in the **Recordset** (**BOF** is **True**). An attempt to move backward when the **BOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="a8af6-p103">Si la llamada a **Move** moviese la posición del registro activo a un punto posterior al último registro, ADO establecería el registro activo en la posición posterior al último registro del **conjunto de registros** (**EOF** es **True**). Si se intenta avanzar cuando la propiedad **EOF** ya es **True**, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="a8af6-p103">If the **Move** call would move the current record position to a point after the last record, ADO sets the current record to the position after the last record in the **Recordset** (**EOF** is **True**). An attempt to move forward when the **EOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="a8af6-112">Si se llama al método **Move** desde un objeto **Recordset** vacío, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="a8af6-112">Calling the **Move** method from an empty **Recordset** object generates an error.</span></span>

<span data-ttu-id="a8af6-p104">Si se pasa un marcador en el argumento *Start*, el desplazamiento se realiza respecto al registro con este marcador, suponiendo que el objeto **Recordset** admite marcadores. Un marcador se obtiene usando la propiedad [Bookmark](bookmark-property-ado.md). Si no se especifica, el desplazamiento se realiza respecto al registro activo.</span><span class="sxs-lookup"><span data-stu-id="a8af6-p104">If you pass a bookmark in the *Start* argument, the move is relative to the record with this bookmark, assuming the **Recordset** object supports bookmarks. A bookmark is obtained by using the [Bookmark](bookmark-property-ado.md) property. If not specified, the move is relative to the current record.</span></span>

<span data-ttu-id="a8af6-p105">Si se utiliza la propiedad **CacheSize** para almacenar localmente en caché registros del proveedor, el paso de un argumento *NumRecords* que mueve la posición del registro activo fuera del grupo actual de registros almacenados en caché provoca que ADO recupere un nuevo grupo de registros, a partir del registro de destino. La propiedad **CacheSize** determina el tamaño del grupo recién recuperado y el registro de destino es el primer registro recuperado.</span><span class="sxs-lookup"><span data-stu-id="a8af6-p105">If you are using the **CacheSize** property to locally cache records from the provider, passing a *NumRecords* argument that moves the current record position outside the current group of cached records forces ADO to retrieve a new group of records, starting from the destination record. The **CacheSize** property determines the size of the newly retrieved group, and the destination record is the first record retrieved.</span></span>

