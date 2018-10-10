---
title: Children (propiedad, ADO MD)
TOCTitle: Children Property (ADO MD)
ms:assetid: 66eff203-68e5-a36d-eb2f-2e9faa80deb6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249400(v=office.15)
ms:contentKeyID: 48545352
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e126b203e2282f96070f1f3eb14a9b926c04f432
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483906"
---
# <a name="children-property-ado-md"></a><span data-ttu-id="f8b6d-102">Children (propiedad, ADO MD)</span><span class="sxs-lookup"><span data-stu-id="f8b6d-102">Children Property (ADO MD)</span></span>


<span data-ttu-id="f8b6d-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f8b6d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f8b6d-104">Devuelve una colección [Members](members-collection-ado-md.md) para la que el [elemento](member-object-ado-md.md) activo es el principal en la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="f8b6d-104">Returns a [Members](members-collection-ado-md.md) collection for which the current [Member](member-object-ado-md.md) is the parent in the hierarchy.</span></span>

## <a name="return-values"></a><span data-ttu-id="f8b6d-105">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="f8b6d-105">Return Values</span></span>

<span data-ttu-id="f8b6d-106">Devuelve una colección **Members** y es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="f8b6d-106">Returns a **Members** collection and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8b6d-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f8b6d-107">Remarks</span></span>

<span data-ttu-id="f8b6d-p101">La propiedad **Children** contiene una colección **Members** para la que el **elemento** activo es el principal de la jerarquía. Los objetos **Member** del nivel de hoja no tienen elementos secundarios en la colección **Members**. Esta propiedad solo es compatible con objetos **Member** pertenecientes a un objeto [Level](level-object-ado-md.md). Si se hace referencia a esta propiedad desde objetos **Member** pertenecientes a un objeto [Position](position-object-ado-md.md), se produce un error.</span><span class="sxs-lookup"><span data-stu-id="f8b6d-p101">The **Children** property contains a **Members** collection for which the current **Member** is the hierarchical parent. Leaf level **Member** objects have no child members in the **Members** collection. This property is only supported on **Member** objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

