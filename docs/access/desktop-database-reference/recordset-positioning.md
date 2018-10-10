---
title: Colocación de un conjunto de registros
TOCTitle: Recordset Positioning
ms:assetid: 1b8b08d5-a11c-ec6e-201c-1405171a1264
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248955(v=office.15)
ms:contentKeyID: 48543546
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 10586c711b9931c1cac93401111f4d477ca8a987
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486445"
---
# <a name="recordset-positioning"></a><span data-ttu-id="20052-102">Colocación de un conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="20052-102">Recordset Positioning</span></span>


<span data-ttu-id="20052-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="20052-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="20052-p101">Use la propiedad **AbsolutePosition** para desplazarse a un registro basándose en su posición ordinal en el objeto **Recordset**, o bien, para especificar la posición ordinal del registro actual. El proveedor debe admitir la funcionalidad adecuada para que esta propiedad esté disponible.</span><span class="sxs-lookup"><span data-stu-id="20052-p101">Use the **AbsolutePosition** property to move to a record, based on its ordinal position in the **Recordset** object, or to determine the ordinal position of the current record. The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="20052-p102">**AbsolutePosition** es de base uno y es igual a 1 cuando el registro activo es el primero del **conjunto de registros**. Como se indicó previamente, el número total de registros del objeto **Recordset** se puede obtener a partir de la propiedad **RecordCount**.</span><span class="sxs-lookup"><span data-stu-id="20052-p102">**AbsolutePosition** is 1-based and equals 1 when the current record is the first record in the **Recordset**. As mentioned previously, you can obtain the total number of records in the **Recordset** object from the **RecordCount** property.</span></span>

<span data-ttu-id="20052-p103">Cuando se establece la propiedad **AbsolutePosition**, incluso aunque sea en un registro en la caché actual, ADO vuelve a cargar la caché con un nuevo grupo de registros empezando por el registro que se haya especificado. La propiedad **CacheSize** determina el tamaño de este grupo.</span><span class="sxs-lookup"><span data-stu-id="20052-p103">When you set the **AbsolutePosition** property, even if it is to a record in the current cache, ADO reloads the cache with a new group of records starting with the record you specified. The **CacheSize** property determines the size of this group.</span></span>


> [!NOTE]
> <P><span data-ttu-id="20052-p104">[!NOTA] No es aconsejable usar la propiedad <STRONG>AbsolutePosition</STRONG> como número de registro suplente. La posición de un registro determinado cambia cuando se elimina un registro anterior. Además, no se tiene la certeza de que un registro dado tenga el mismo valor de <STRONG>AbsolutePosition</STRONG> si se vuelve a consultar y a abrir el objeto <STRONG>Recordset</STRONG>. Los marcadores son el método recomendado para retener cierta posición y volver a ella, y son la única manera de establecer un posicionamiento a través de todos los tipos de objetos <STRONG>Recordset</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="20052-p104">You should not use the <STRONG>AbsolutePosition</STRONG> property as a surrogate record number. The position of a given record changes when you delete a preceding record. There also is no assurance that a given record will have the same <STRONG>AbsolutePosition</STRONG> if the <STRONG>Recordset</STRONG> object is requeried or reopened. Bookmarks are the recommended way of retaining and returning to a given position and are the only way of positioning across all types of <STRONG>Recordset</STRONG> objects.</span></span></P>


