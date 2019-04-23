---
title: Persistencia de los conjuntos de registros filtrados y jerárquicos
TOCTitle: Persisting filtered and hierarchical Recordsets
ms:assetid: 3648a997-dac7-d8a3-3cca-a6827f26a4f0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249120(v=office.15)
ms:contentKeyID: 48544162
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1332d4348c993f94d8b2ee61280b8b35c02324c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287590"
---
# <a name="persisting-filtered-and-hierarchical-recordsets"></a><span data-ttu-id="e2ce7-102">Persistencia de los conjuntos de registros filtrados y jerárquicos</span><span class="sxs-lookup"><span data-stu-id="e2ce7-102">Persisting filtered and hierarchical Recordsets</span></span>


<span data-ttu-id="e2ce7-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e2ce7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e2ce7-p101">Si la propiedad [Filter](filter-property-ado.md) está activada para el **conjunto de registros**, solo se guardarán las filas para las que se tenga acceso con el filtro. Si el **conjunto de registros** es jerárquico, se guardará el **conjunto de registros** secundario y sus elementos secundarios, incluido el **conjunto de registros** principal. Si se llama al método **Save** de un **conjunto de registros** secundario, se guarda el secundario y todos sus secundarios, pero el principal, no. Para obtener más información acerca de los **conjuntos de registros** jerárquicos, vea el [Capítulo 9: Forma de datos](chapter-9-data-shaping.md).</span><span class="sxs-lookup"><span data-stu-id="e2ce7-p101">If the [Filter](filter-property-ado.md) property is in effect for the **Recordset**, only the rows accessible under the filter are saved. If the **Recordset** is hierarchical, the current child **Recordset** and its children are saved, including the parent **Recordset**. If the **Save** method of a child **Recordset** is called, the child and all its children are saved, but the parent is not. For more information about hierarchical **Recordsets**, see [Chapter 9: Data Shaping](chapter-9-data-shaping.md).</span></span>


> [!NOTE]
> <span data-ttu-id="e2ce7-p102">[!NOTA] Existen algunas limitaciones para guardar **conjuntos de registros** jerárquicos (formas de datos) en formato XML. Para obtener más información, vea [Conjuntos de registros jerárquicos en XML](hierarchical-recordsets-in-xml.md).</span><span class="sxs-lookup"><span data-stu-id="e2ce7-p102">Some limitations apply when saving hierarchical **Recordsets** (data shapes) in XML format. For more information, see [Hierarchical Recordsets in XML](hierarchical-recordsets-in-xml.md).</span></span>


