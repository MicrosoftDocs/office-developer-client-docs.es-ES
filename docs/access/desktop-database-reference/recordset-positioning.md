---
title: Posicionamiento de conjunto de registros
TOCTitle: Recordset positioning
ms:assetid: 1b8b08d5-a11c-ec6e-201c-1405171a1264
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248955(v=office.15)
ms:contentKeyID: 48543546
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bf4c442ecd7cbce740df69d60b5ec3e1e405a412
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997857"
---
# <a name="recordset-positioning"></a><span data-ttu-id="89e15-102">Posicionamiento de conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="89e15-102">Recordset positioning</span></span>

<span data-ttu-id="89e15-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="89e15-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="89e15-p101">Use la propiedad **AbsolutePosition** para desplazarse a un registro basándose en su posición ordinal en el objeto **Recordset**, o bien, para especificar la posición ordinal del registro actual. El proveedor debe admitir la funcionalidad adecuada para que esta propiedad esté disponible.</span><span class="sxs-lookup"><span data-stu-id="89e15-p101">Use the **AbsolutePosition** property to move to a record, based on its ordinal position in the **Recordset** object, or to determine the ordinal position of the current record. The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="89e15-p102">**AbsolutePosition** es de base uno y es igual a 1 cuando el registro activo es el primero del **conjunto de registros**. Como se indicó previamente, el número total de registros del objeto **Recordset** se puede obtener a partir de la propiedad **RecordCount**.</span><span class="sxs-lookup"><span data-stu-id="89e15-p102">**AbsolutePosition** is 1-based and equals 1 when the current record is the first record in the **Recordset**. As mentioned previously, you can obtain the total number of records in the **Recordset** object from the **RecordCount** property.</span></span>

<span data-ttu-id="89e15-p103">Cuando se establece la propiedad **AbsolutePosition**, incluso aunque sea en un registro en la caché actual, ADO vuelve a cargar la caché con un nuevo grupo de registros empezando por el registro que se haya especificado. La propiedad **CacheSize** determina el tamaño de este grupo.</span><span class="sxs-lookup"><span data-stu-id="89e15-p103">When you set the **AbsolutePosition** property, even if it is to a record in the current cache, ADO reloads the cache with a new group of records starting with the record you specified. The **CacheSize** property determines the size of this group.</span></span>

> [!NOTE]
> <span data-ttu-id="89e15-p104">[!NOTA] No es aconsejable usar la propiedad **AbsolutePosition** como número de registro suplente. La posición de un registro determinado cambia cuando se elimina un registro anterior. Además, no se tiene la certeza de que un registro dado tenga el mismo valor de **AbsolutePosition** si se vuelve a consultar y a abrir el objeto **Recordset**. Los marcadores son el método recomendado para retener cierta posición y volver a ella, y son la única manera de establecer un posicionamiento a través de todos los tipos de objetos **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="89e15-p104">You should not use the **AbsolutePosition** property as a surrogate record number. The position of a given record changes when you delete a preceding record. There also is no assurance that a given record will have the same **AbsolutePosition** if the **Recordset** object is requeried or reopened. Bookmarks are the recommended way of retaining and returning to a given position and are the only way of positioning across all types of **Recordset** objects.</span></span>


